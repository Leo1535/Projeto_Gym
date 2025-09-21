Nome do Aplicativo: GymLog
Integrantes do Grupo
Leonardo Antonio da Silva
Gabriel Gaioti 
Otavio Augusto 


1. Problema a Ser Resolvido
Frequentadores de academia, especialmente iniciantes e intermediários, muitas vezes dependem de fichas de treino em papel ou anotações desorganizadas no celular. Isto torna difícil acompanhar o progresso, lembrar as cargas corretas para cada exercício e visualizar a rotina do dia, o que pode levar à desmotivação e a treinos menos eficientes.

2. Solução Proposta
O nosso aplicativo, o GymLog, funciona como uma ficha de treino digital e inteligente. Ele permite que o usuário cadastre os seus treinos (ex: Treino A, B, C) e os exercícios correspondentes, incluindo informações como séries, repetições e a última carga utilizada. Ao chegar na academia, o usuário pode simplesmente abrir a app, selecionar o treino do dia e seguir a lista de exercícios, atualizando as cargas conforme progride.

3. Justificativa Pessoal
Como praticantes de musculação, sentimos na pele a dificuldade de gerir a nossa evolução. Ter um aplicativo simples para registar e consultar informações de carga e repetições diretamente no celular tornaria os nossos treinos mais produtivos e ajudar-nos-ia a visualizar claramente o nosso progresso, servindo como uma grande fonte de motivação.

4. DER dos Dados (Diagrama Entidade-Relacionamento)
A estrutura de dados da API será baseada em duas entidades principais: usuarios e exercicios, com uma relação de "um para muitos".

Tabela: usuarios
| Coluna | Tipo | Descrição |
| :--- | :--- | :--- |
| id | INT (PRIMARY KEY) | Identificador único do usuário |
| nome | VARCHAR | Nome do usuário |
| email | VARCHAR | E-mail de login |
| senha | VARCHAR | Senha (criptografada) |

Tabela: exercicios
| Coluna | Tipo | Descrição |
| :--- | :--- | :--- |
| id | INT (PRIMARY KEY) | Identificador único do exercício |
| nome | VARCHAR | Nome do exercício (Ex: Supino Reto) |
| carga | DECIMAL | Carga utilizada em kg (Ex: 25.5) |
| series | INT | Número de séries (Ex: 4) |
| repeticoes | VARCHAR | Repetições (Ex: "10-12") |
| letra_treino | CHAR(1) | Agrupador do treino (Ex: 'A', 'B', 'C') |
| usuario_id | INT (FOREIGN KEY) | Liga o exercício ao id da tabela usuarios |