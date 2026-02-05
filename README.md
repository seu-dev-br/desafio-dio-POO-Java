# Desafio DIO - Programação Orientada a Objetos

## 📋 Sobre o Projeto

Este projeto é um desafio da Digital Innovation One (DIO) que implementa um sistema de gerenciamento de Bootcamps utilizando os conceitos de Programação Orientada a Objetos (POO) em Java.

## 🎯 Objetivo

Criar um sistema que permita:
- Cadastrar bootcamps com cursos e mentorias
- Inscrever desenvolvedores em bootcamps
- Acompanhar o progresso dos desenvolvedores
- Calcular o XP (experiência) acumulado

## 🏗️ Estrutura do Projeto

```
src/br/com/dio/desafio/dominio/
├── Conteudo.java       # Classe abstrata base para conteúdos
├── Curso.java          # Representa um curso
├── Mentoria.java       # Representa uma mentoria
├── Bootcamp.java       # Representa um bootcamp
├── Dev.java            # Representa um desenvolvedor
└── Main.java           # Classe principal com exemplos
```

## 💡 Conceitos de POO Utilizados

- **Abstração**: Classe abstrata `Conteudo` define estrutura base
- **Encapsulamento**: Atributos privados com getters e setters
- **Herança**: `Curso` e `Mentoria` herdam de `Conteudo`
- **Polimorfismo**: Método `calcularXp()` implementado de forma diferente em cada classe

## 🚀 Como Executar

1. Clone o repositório
2. Compile os arquivos Java:
```bash
javac src/br/com/dio/desafio/dominio/*.java
```
3. Execute a classe Main:
```bash
java br.com.dio.desafio.dominio.Main
```

## 📊 Funcionalidades

### Bootcamp
- Nome e descrição
- Data inicial e final (45 dias de duração)
- Lista de conteúdos (cursos e mentorias)
- Lista de devs inscritos

### Desenvolvedor (Dev)
- Nome
- Conteúdos inscritos
- Conteúdos concluídos
- Cálculo de XP total

### Curso
- Título e descrição
- Carga horária
- XP = XP_PADRÃO * carga horária

### Mentoria
- Título e descrição
- Data
- XP = XP_PADRÃO + 20

## 🎓 Exemplo de Uso

```java
// Criar cursos
Curso curso1 = new Curso();
curso1.setTitulo("curso java");
curso1.setCargaHoraria(8);

// Criar bootcamp
Bootcamp bootcamp = new Bootcamp();
bootcamp.setNome("Bootcamp Java Developer");
bootcamp.getConteudos().add(curso1);

// Inscrever desenvolvedor
Dev dev = new Dev();
dev.setNome("Camila");
dev.inscreverBootcamp(bootcamp);

// Progredir nos conteúdos
dev.progredir();
System.out.println("XP: " + dev.calcularTotalXp());
```

## 🛠️ Tecnologias

- Java 8+
- Collections (Set, LinkedHashSet)
- Java Time API (LocalDate)
- Optional

## 👨‍💻 Autor

Projeto desenvolvido como parte do desafio de Programação Orientada a Objetos da Digital Innovation One.

---

⭐ Se este projeto foi útil para você, considere dar uma estrela!
