# 🛠️ Modelos Declarativo e Imperativo

Quando se trata de gerenciar infraestrutura ou realizar tarefas automatizadas, podemos optar por dois modelos principais: **Declarativo** e **Imperativo**. Abaixo, explicamos cada um deles com exemplos simples.

---

## 🌟 Modelo Declarativo (O que precisa fazer)

No modelo declarativo, você especifica o estado final que deseja alcançar, e o sistema se encarrega de realizar as ações necessárias para atingir esse estado.

### 🎯 Características

- Define o **estado desejado**.
- Engloba todos os recursos do fluxo.
- Mantém o **histórico de estados anteriores**.
- Facilita possíveis deleções futuras.

### 📝 Exemplo: Organizando uma sala

- **Objetivo**: "Quero que a sala tenha 5 cadeiras, uma mesa central e um sofá."
- **Como funciona**: Você descreve o que deseja, e alguém organiza a sala exatamente como foi solicitado, independentemente do estado atual.

### 💻 Em código (YAML)

```yaml
resources:
  - name: database
    type: postgres
    version: 13
  - name: webserver
    type: nginx
    version: 1.21
```

## 🌟 Modelo Imperativo (Foca no como fazer)

No modelo imperativo, você fornece instruções detalhadas sobre como atingir o estado desejado, geralmente passo a passo.

### 🎯 Características

- Define os comandos para criar o recurso.
- Geralmente exige execução em ordem, caso haja interdependências.
  -Em alguns casos, é possível manter o histórico do que foi feito.

### 📝 Exemplo: Organizando uma sala

- **Objetivo**: "Pegue 5 cadeiras, coloque ao redor da mesa, depois traga o sofá e posicione no canto esquerdo."
- **Como funciona**: Você descreve cada ação necessária para organizar a sala.

### 💻 Em código (Comandos Shell)

```bash
# Criar banco de dados

create-database --type postgres --version 13

# Configurar servidor web

install-webserver --type nginx --version 1.21
```

Você precisa executar os comandos na ordem correta, e a responsabilidade de gerenciar dependências e ajustes é sua.

## 🤔 Conclusão

O **modelo declarativo** é ideal para gerenciar infraestrutura em larga escala devido à sua facilidade de manutenção e automação. Já o **modelo imperativo** oferece maior controle granular, sendo útil em cenários específicos que demandam intervenções detalhadas.
