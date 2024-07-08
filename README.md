# API de Histórico do IPCA 

Esta API permite a consulta de dados do Índice Nacional de Preços ao Consumidor Amplo (IPCA) dos anos de 2015 a 2023. A API fornece endpoints para obter a lista completa de dados, dados filtrados por ano, por ID específico e um cálculo ajustado do IPCA entre dois períodos.

## Tecnologias Utilizadas

- Node.js
- Express.js
- Javascript

## Endpoints

1. Obter Lista Completa de Dados

```markdown
> GET /historicoIPCA 
```
Retorna a lista completa de dados do IPCA.

2. Obter Dados por Ano

```markdown
> GET /historicoIPCA?ano=<ANO>
```
Retorna os dados do IPCA filtrados pelo ano especificado (2015 a 2023).

3. Obter Dados por ID

```markdown
> GET /historicoIPCA/:idIPCA
```
Retorna os dados do IPCA com o ID especificado.

4. Calcular IPCA Ajustado

```markdown
> GET /historicoIPCA/calculo?valor=<VALOR>&mesInicial=<MES_INICIAL>&anoInicial=<ANO_INICIAL>&mesFinal=<MES_FINAL>&anoFinal=<ANO_FINAL>
```
Retorna o valor reajustado do IPCA para o período especificado.

## Tratamento de Erros

A API possui tratamento de erros para:

- Valores de entrada inválidos.
- Anos fora do intervalo de 2015 a 2023.
- Meses fora do intervalo de 1 a 12.
- Parâmetros faltando ou incorretos.

## Como Executar

1. Clone o repositório:
```markdown
> git clone <URL_DO_REPOSITORIO>
```

2. Instale as dependências:
```markdown
> npm install
```

3. Execute o servidor:
```markdown
> node index.js
```
