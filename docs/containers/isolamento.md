# Isolamento no Docker

O Docker utiliza tecnologias do kernel do Linux para criar ambientes isolados onde aplicações podem ser executadas de forma segura e independente. Esse isolamento é essencial para garantir que os containers não interfiram uns nos outros nem no sistema host.

---

## Tecnologias de Isolamento

### **1. Control Groups (cgroups)**

Os _Control Groups_ (cgroups) permitem gerenciar e limitar os recursos de hardware utilizados por processos no sistema operacional.

#### O que fazem:

- Controlam o uso de **CPU, memória, disco e rede** de cada container.
- Evitam que um container consuma todos os recursos do host, garantindo a estabilidade do sistema.
- Permitem definir políticas de alocação de recursos.

#### Exemplo:

Um container pode ser configurado para usar no máximo 512 MB de RAM ou uma porcentagem específica da CPU.

---

### **2. Namespaces**

Os _namespaces_ criam um ambiente isolado para cada container, garantindo que ele enxergue apenas os recursos que pertencem a ele.

#### Tipos de Namespaces Utilizados:

- **PID (Process IDs):** Isola os processos para que cada container veja apenas os seus próprios.
- **NET (Networking):** Cria interfaces de rede exclusivas para cada container.
- **MNT (Mount):** Isola o sistema de arquivos, garantindo que cada container tenha sua própria visão do sistema.
- **IPC (Interprocess Communication):** Isola a comunicação entre processos.
- **UTS (Unix Timesharing System):** Permite que cada container tenha seu próprio hostname.
- **USER:** Isola identificadores de usuários, permitindo que o container tenha usuários diferentes do host.

#### Exemplo:

Um container pode ter processos com IDs iguais aos do host, mas esses IDs não colidem devido ao isolamento do namespace de PID.

---

### **3. Unshare**

O comando `unshare` é usado para desassociar um processo de determinados namespaces, criando um ambiente isolado manualmente.

#### Como funciona:

- Permite criar um novo namespace para um processo específico sem afetar os demais.
- É útil para testar o comportamento de isolamento diretamente, sem usar o Docker.

#### Exemplo:

```powershell
unshare --net --pid bash
```
