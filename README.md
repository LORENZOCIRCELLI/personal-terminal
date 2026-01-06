# Personal-Terminal

## 📌 Descrição

**Personal-Terminal** é um projeto desenvolvido em **C** com o objetivo de simular um **terminal de comandos**, inspirado em shells reais como `cmd`, `bash` e `powershell`.  
Internamente, o sistema utiliza uma **árvore virtual** para representar um sistema de arquivos próprio, totalmente desacoplado do sistema operacional.

O foco do projeto é educacional, explorando estruturas de dados, ponteiros e arquitetura de software em baixo nível.

---

## 🎯 Objetivos do Projeto

- Simular comandos básicos de um terminal real (`cd`, `mkdir`, criação de arquivos, etc.)
- Implementar uma árvore hierárquica para representar diretórios e arquivos
- Separar claramente:
  - parsing de comandos
  - execução de comandos
  - estrutura de dados
- Aprofundar o estudo da linguagem C
- Servir como base para estudos de sistemas de arquivos e shells

---

## 🧠 Conceitos Trabalhados

- Árvores n-árias
- Alocação dinâmica de memória
- Manipulação de strings em C
- Uso de `enum` para comandos
- Separação entre interface (`.h`) e implementação (`.c`)
- Arquitetura em camadas
- Sistema de arquivos virtual
- Design modular e escalável

---

## 💡 Ideia Central

O funcionamento do terminal é dividido em camadas bem definidas:

1. O usuário digita um comando
2. O parser interpreta a entrada
3. O comando é identificado
4. A ação correspondente é executada
5. A árvore virtual gerencia todo o estado do sistema

A árvore **não conhece comandos**, e os comandos **não conhecem a implementação interna da árvore**, garantindo baixo acoplamento e organização do código.

---

## 📁 Sistema de Arquivos Virtual

Cada diretório ou arquivo é representado por um nó da árvore, contendo informações como:

- nome
- tipo (diretório ou arquivo)
- ponteiro para o nó pai
- lista dinâmica de filhos

Essa abordagem permite simular navegação e organização de arquivos de forma semelhante a um filesystem real.

---

## 💾 Persistência (Planejada)

O projeto foi pensado para suportar persistência no futuro, por exemplo:

- Serialização da árvore virtual em arquivo
- Reconstrução da árvore a partir de um diretório sandbox real

Essas funcionalidades podem ser adicionadas sem alterar a lógica central da árvore.

---

## 🚀 Motivação

Este projeto surgiu como uma forma de praticar estruturas de dados e arquitetura de software em C de maneira mais próxima de aplicações reais, como shells e sistemas de arquivos, indo além de exemplos acadêmicos simples.

---

## ⚠️ Observações

- Projeto com fins educacionais
- Não executa comandos reais do sistema operacional
- Não altera arquivos fora do escopo do projeto
- Foco em aprendizado, clareza e organização do código

---

## 📚 Tecnologias

- Linguagem C (C99)
- Biblioteca padrão da linguagem C
- Estruturas de dados dinâmicas

---

## 🧪 Status do Projeto

🚧 Em desenvolvimento
