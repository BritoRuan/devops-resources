# Containers e Máquinas Virtuais

## O que é um Container?

Um container é um ambiente isolado que permite executar aplicações de maneira independente, mas compartilhando o mesmo sistema host. Ele pode ser comparado a um contêiner de navio, que contém tudo o que é necessário para transportar uma carga de forma eficiente e segura.

### Características dos Containers:

- **Ambiente Isolado:** Garante que a aplicação não interfira em outras rodando no mesmo host.
- **Compartilha o Host:** Apesar de ser isolado, o container utiliza recursos do sistema operacional do host.
- **Completo para Aplicações:** Contém todos os elementos necessários para rodar a aplicação, como bibliotecas e dependências.
- **Baseado em Linux Containers (LXC):** Usa tecnologias como namespaces e cgroups para criar ambientes leves e isolados.

---

## Máquinas Virtuais (VMs)

As máquinas virtuais oferecem outro nível de virtualização, permitindo executar múltiplos sistemas operacionais em um único host físico.

### Características das Máquinas Virtuais:

- **SO Próprio:** Cada VM possui seu próprio sistema operacional, independente do sistema do host.
- **Tudo na Mesma Máquina:** Compartilham o hardware físico do host, mas são isoladas umas das outras.

---

## Docker

O Docker é uma plataforma que simplifica o uso de containers, tornando-os mais acessíveis e fáceis de gerenciar.

### Características do Docker:

- **História:** Surgiu há cerca de 15 anos como uma interface para lidar com containers de maneira eficiente.
- **Baseado no Kernel Linux:** Usa o kernel para criar e gerenciar containers de forma leve e eficaz.
- **Baseado em Imagens:** As aplicações são empacotadas em imagens que contêm tudo o que é necessário para sua execução, garantindo consistência.
- **Ciclo de Entrega Facilitado:** Simplifica o desenvolvimento, a integração e a entrega contínua (CI/CD).
- **Leve e Portátil:** Containers são mais rápidos e usam menos recursos comparados às VMs.

---

### Comparação: Containers x Máquinas Virtuais

| **Aspecto**             | **Containers**                      | **Máquinas Virtuais**            |
| ----------------------- | ----------------------------------- | -------------------------------- |
| **Sistema Operacional** | Compartilha o kernel do host        | Cada VM tem seu próprio SO       |
| **Isolamento**          | Isolamento por cgroups e namespaces | Isolamento completo (hypervisor) |
| **Desempenho**          | Leve e rápido                       | Mais pesado, depende do SO       |
| **Portabilidade**       | Altamente portátil                  | Limitada devido ao tamanho       |

Com Docker, o uso de containers tornou-se uma prática padrão na entrega de software moderno, permitindo maior eficiência e escalabilidade.
