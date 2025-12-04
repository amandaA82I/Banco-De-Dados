# 🗄️ Modelagem: Sistema de Transportes e Frotas

> Repositório contendo o esquema relacional para gestão de trânsito, bilhetagem e locação de veículos.

## 📋 Visão Geral do Schema

Este modelo de dados foi desenvolvido para resolver o problema de *logística de transporte multimodal*. A estrutura normalizada garante integridade referencial entre usuários, veículos e a execução dos serviços (viagens ou aluguéis).

## 🔍 Análise das Estruturas

### 1. Núcleo de Operação (Veiculo, Tipo_Veiculo)
A tabela veiculo é centralizada e polimórfica, atendendo tanto a veículos de transporte de massa quanto individuais.
*   Atributos chave: codigo_autenticacao, status (Disponível/Em uso), nivel_autonomia.

### 2. Módulo de Rotas (Rota, Parada, Parada_Rota)
Implementação de relacionamento *N:M* entre Rotas e Paradas.
*   A entidade associativa parada_rota define a *ordem* das paradas e a distancia_proxima_parada, permitindo cálculos de roteirização.

### 3. Transacional (Passagem, Aluguel, Pagamento)
*   *Aluguel:* Lógica de Check-in/Check-out (id_parada_retirada e id_parada_devolucao).
*   *Viagem/Passagem:* Lógica de transporte coletivo, onde uma viagem ocorre em uma rota específica e o usuário adquire uma passagem.

## 🚀 Como implementar

1. Clone o repositório.
2. Execute o script DDL (Data Definition Language) no seu SGBD preferido (MySQL/PostgreSQL).
3. Popule com os dados de teste (DML).

## 🛠️ Tech Stack
*   *Design:* Modelo Lógico e Conceitual.
*   *Ferramenta:* brModelo.
*   *Linguagem:* SQL (ANSI).

---
