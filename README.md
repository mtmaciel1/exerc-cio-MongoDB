# Relatório: MongoDB vs Postgres (JSONB)

## Missão 1: Setup
Utilizei Docker Compose para subir os bancos. 
- MongoDB na porta 27017
- Postgres na porta 5432

## Missão 2: Inserção
Inseri um JSON de 15 níveis em ambos os bancos. 
No MongoDB a inserção foi nativa. No Postgres, utilizei o tipo `JSONB`.

## Missão 3: Consulta no 15º Nível
- **MongoDB:** Usei Dot Notation (`n1.n2...`). Tempo: X ms.
- **Postgres:** Usei o operador `#>`. Tempo: 0.004s.

### Conclusão
O MongoDB se mostrou mais intuitivo para lidar com dados muito aninhados, 
enquanto o Postgres exige uma sintaxe mais rigorosa para navegar no JSON.
