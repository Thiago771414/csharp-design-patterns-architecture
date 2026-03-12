# C# Design Patterns Architecture (OOP Case Study)

![Language](https://img.shields.io/badge/language-C%23-blue)
![Framework](https://img.shields.io/badge/.NET-OOP-green)
![Architecture](https://img.shields.io/badge/Architecture-Design%20Patterns-purple)
![Patterns](https://img.shields.io/badge/Patterns-Strategy%20%7C%20State%20%7C%20Builder%20%7C%20Observer-orange)
![Project Type](https://img.shields.io/badge/Project%20Type-Software%20Architecture%20Case%20Study-yellow)

---

# Overview

This repository demonstrates the implementation of several **classic software design patterns using C# and object-oriented programming principles**.

The project simulates a **financial system that calculates taxes, discounts, invoice generation, and order state transitions** while applying widely adopted enterprise design patterns.

The goal of this project is to show how design patterns improve:

- code extensibility
- maintainability
- separation of concerns
- system architecture

---

# Design Patterns Implemented

## Strategy Pattern

Used for tax calculation strategies.

Example classes:

Imposto
ICMS
ISS
IKCV
ICPP


This pattern allows dynamic selection of tax algorithms at runtime.

---

## Chain of Responsibility

Used to apply discount rules sequentially.

Classes:

Desconto
DescontoPorCincoItens
DescontoPorMaisDeQuinhentosReais
SemDesconto


Each rule decides whether to apply the discount or delegate to the next rule.

---

## State Pattern

Controls budget lifecycle states.

EmAprovacao
Aprovado
Reprovado
Finalizado


This prevents invalid state transitions in the system.

---

## Builder Pattern

Used to construct complex objects such as invoices.
NotaFiscalBuilder

This simplifies the creation of objects with multiple parameters.

---

## Observer Pattern

Executed after invoice generation.

AcaoAposGerarNota
EnviadorDeEmail
EnviadorDeSms


Multiple actions can react to the same event.

---

## Template Method Pattern

Used to define reusable algorithm structures for tax calculation.
TemplateDeImpostoCondicional

---

# Architecture

The architecture demonstrates how enterprise systems combine multiple patterns.
```text
Application
│
├── Budget (Orcamento)
│ ├── State Pattern
│ └── Discount Chain
│
├── Tax Calculation
│ └── Strategy Pattern
│
├── Invoice Generation
│ └── Builder Pattern
│
└── Post Processing
└── Observer Pattern
```

This layered design keeps business logic modular and extensible.

---

# Folder Structure
```text
CursoDesignPatterns
│
├── Program.cs
│
├── Orcamento.cs
├── EstadoDeUmOrcamento.cs
│
├── Strategy
│ ├── Imposto.cs
│ ├── ICMS.cs
│ ├── ISS.cs
│ ├── IKCV.cs
│ └── ICPP.cs
│
├── ChainOfResponsibility
│ ├── Desconto.cs
│ ├── DescontoPorCincoItens.cs
│ ├── DescontoPorMaisDeQuinhentosReais.cs
│ └── SemDesconto.cs
│
├── Builder
│ └── NotaFiscalBuilder.cs
│
├── Observer
│ ├── AcaoAposGerarNota.cs
│ ├── EnviadorDeEmail.cs
│ └── EnviadorDeSms.cs
│
└── State
├── EmAprovacao.cs
├── Aprovado.cs
├── Reprovado.cs
└── Finalizado.cs
```

---

# How to Run

### 1 Clone repository
```bash
git clone
```

### 2 Open project

Open the solution file:
```bash
CursoDesignPatterns.sln
```

Using:

- Visual Studio
- Rider
- VS Code with C# extension

---

### 3 Run the application
```bash
dotnet run
```

or run from Visual Studio.

---

# Example Execution Flow

1️⃣ Create a budget (`Orcamento`)

2️⃣ Apply discount chain

3️⃣ Calculate taxes using strategy pattern

4️⃣ Build invoice using builder pattern

5️⃣ Trigger observers (email + SMS)

---

# Learning Outcomes

This project demonstrates how to apply **classic design patterns in real business logic**.

Concepts covered:

- Object-Oriented Architecture
- SOLID principles
- Behavioral patterns
- Creational patterns
- Enterprise code organization

---

# Technologies

- C#
- .NET
- Object-Oriented Programming
- Software Design Patterns

---

# Author

Thiago Reis Lima
https://www.linkedin.com/in/thiago-lima-2a5896166
