# Sistema de Cadastro e Notificação de Eventos

## Introdução

Este projeto consiste em um sistema desenvolvido em Java que permite o cadastro de usuários e eventos, além de possibilitar a inscrição dos usuários nos eventos de seu interesse. O sistema é desenvolvido seguindo o paradigma de programação orientada a objetos e é estruturado em um projeto organizado em um repositório Git.

## Estrutura do Projeto

O projeto é dividido em várias classes, cada uma responsável por uma funcionalidade específica. Aqui está uma visão geral da estrutura:

- `Main`: Classe principal que contém o método `main` e serve como ponto de entrada para o programa.
- `Usuario`: Classe que representa um usuário do sistema, contendo atributos como nome, endereço e telefone.
- `Evento`: Classe que representa um evento, com atributos como nome, endereço, categoria, horário e descrição.
- `GerenciadorEventos`: Classe responsável por gerenciar os eventos cadastrados, permitindo adicionar, remover, buscar e salvar eventos em um arquivo.
- `GerenciadorUsuarios`: Classe responsável por gerenciar os usuários cadastrados, permitindo adicionar, remover e buscar usuários.
- `InterfaceUsuario`: Classe que implementa a interface de usuário por meio de menus em console.

### Padrões e Boas Práticas

Durante o desenvolvimento do sistema, foram seguidas algumas boas práticas e padrões de codificação, como:

- 🗂️ **Organização em Pacotes**: O código está organizado em pacotes separados por funcionalidades, tornando-o mais modular e fácil de manter.
- 🔄 **Padrão MVC**: O sistema segue parcialmente o padrão Modelo-Visão-Controlador (MVC), separando as responsabilidades em diferentes classes.
- 💡 **Encapsulamento**: Os atributos das classes são privados e acessados por meio de métodos getters e setters, garantindo o encapsulamento dos dados.
- 📝 **Javadoc**: O código é documentado utilizando comentários Javadoc, facilitando a compreensão e manutenção do sistema.

## Funcionalidades

O sistema possui as seguintes funcionalidades principais:

### Cadastro de Usuários

- 👤 Os usuários podem se cadastrar fornecendo informações como nome, endereço e telefone.
- 🔍 É possível buscar usuários cadastrados pelo nome ou por um identificador único.
- 🗑️ Os usuários podem ser removidos do sistema.

### Cadastro de Eventos

- 📅 Eventos podem ser cadastrados com informações como nome, endereço, categoria, horário e descrição.
- 🔢 Cada evento recebe um identificador único.
- 🔍 É possível buscar eventos cadastrados por nome, categoria ou identificador.
- 🗑️ Os eventos podem ser removidos do sistema.

### Inscrição em Eventos

- 🖋️ Os usuários podem se inscrever em eventos de seu interesse.
- 🗓️ O sistema ordena os eventos mais próximos com base no horário.
- 🔔 Notifica os usuários sobre eventos que estão ocorrendo no momento.
- 📝 Os usuários podem visualizar os eventos em que estão inscritos.
- ❌ É possível cancelar a inscrição em um evento.

### Persistência de Dados

- 💾 Os dados dos eventos cadastrados são persistidos em um arquivo de texto chamado `events.data`.
- ⬆️ Ao iniciar o programa, os eventos são carregados a partir deste arquivo.

## Utilização

Para executar o sistema, siga estas etapas:

1. Clone o repositório ou baixe os arquivos do projeto.
2. Importe o projeto em sua IDE Java preferida (como Eclipse, IntelliJ ou NetBeans).
3. Execute a classe `Main` para iniciar o programa.
4. Siga as instruções exibidas no console para interagir com o sistema e utilizar suas funcionalidades.

## Exemplos

Aqui estão alguns exemplos de como utilizar o sistema:

### Cadastro de Usuário

```java
Scanner scanner = new Scanner(System.in);
System.out.print("Digite o nome do usuário: ");
String nome = scanner.nextLine();
System.out.print("Digite o endereço do usuário: ");
String endereco = scanner.nextLine();
System.out.print("Digite o telefone do usuário: ");
String telefone = scanner.nextLine();

Usuario novoUsuario = new Usuario(nome, endereco, telefone);
gerenciadorUsuarios.adicionarUsuario(novoUsuario);
