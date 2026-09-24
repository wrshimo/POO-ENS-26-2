# Capítulo 00: Introdução e Fundamentos

## 1. Contextualização do Problema

Imagine a **"TechParts Ltda."**, uma pequena revendedora de componentes eletrônicos. Atualmente, o controle de estoque é feito em cadernos e planilhas soltas. O gerente frequentemente enfrenta problemas como:
*   Vender produtos que já acabaram no armazém.
*   Não saber o valor total investido em mercadorias.
*   Dificuldade em rastrear quando e por qual preço um item foi comprado ou vendido.

**Proposta de Solução:**
Desenvolver uma aplicação desktop chamada **StockControl**, que centralize o cadastro de produtos, automatize a atualização do estoque através de registros de entrada e saída, e forneça um painel visual com indicadores de desempenho.

## 2. Tecnologias Envolvidas

Para construir esta aplicação, utilizaremos um conjunto de tecnologias padrão da indústria Java:

| Tecnologia | Função | Exemplo Prático |
| :--- | :--- | :--- |
| **Java SE** | Linguagem base e lógica de negócio. | `if (estoque < 0) { ... }` |
| **Swing** | Criação da interface gráfica (GUI). | `JButton btn = new JButton("Salvar");` |
| **MariaDB** | Banco de dados relacional para persistência. | `CREATE TABLE produto (...);` |
| **JDBC** | Ponte de comunicação entre Java e Banco. | `Connection conn = DriverManager.getConnection(...);` |
| **Maven** | Gerenciamento de dependências e build. | Adicionar o driver do MariaDB no `pom.xml`. |
| **Lombok** | Redução de código repetitivo (getters/setters). | `@Data` gera automaticamente os métodos de acesso. |

## 3. Conceitos Básicos de Swing

O Swing é um toolkit para criar interfaces gráficas. Os componentes mais usados neste projeto serão:

*   **JFrame:** A janela principal da aplicação.
*   **JPanel:** Um container para organizar outros componentes.
*   **JTable:** Tabela para exibir listas de dados (como a lista de produtos).
*   **JTextField:** Campo de texto para entrada de dados.
*   **JOptionPane:** Janelas pop-up para mensagens de sucesso ou erro.

## 4. Estrutura do Projeto no VS Code

Utilizaremos o **Apache Maven** para gerenciar o projeto. A estrutura de pastas seguirá o padrão:

```text
stock-control/
├── pom.xml
└── src/
    ├── main/
    │   ├── java/
    │   │   └── com/techparts/
    │   │       ├── model/      (Entidades/Beans)
    │   │       ├── dao/        (Acesso ao Banco)
    │   │       └── view/       (Telas Swing)
    │   └── resources/
    └── test/