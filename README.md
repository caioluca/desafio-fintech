# Desafio Fintech

This is dash board where users can analyse a list of transactions.

[Figma Layout](https://www.figma.com/file/i0diXnZ5d6FSCKiQjgdtzf/Untitled?type=design&t=7kmLfKgWKRn914ii-1)

[Layout Reference](<https://www.figma.com/file/ojNagH7l12m5HS62ChmFw7/Dashboard-Finance-Bank-Fintech-(Community)?type=design&t=7kmLfKgWKRn914ii-1>)

Techs used:

- [Next.js](https://nextjs.org/)
- [Reactjs - Context api for state management](https://react.dev/reference/react/useContext)
- [Styled-components for styling](https://styled-components.com/)
- [Prisma as ORM](https://www.prisma.io/)
- [SQLite as the database](https://sqlite.org/index.html)
- [Next.js - Api Routes for API](https://nextjs.org/docs/pages/building-your-application/routing/api-routes)
- [Iron-Session for authorization](https://github.com/vvo/iron-session)

## Running locally

So you can run this project locally in your machine you have two options:

#### Standard

clone the project, then:

```bash
cd desafio-fintech

npm i

npm run dev
```

or, if you prefer Yarn:

```bash
yarn

yarn dev
```

#### Docker

clone the project, then:

```bash
cd desafio-fintech

docker compose up # if you are using docker compose plugin
# or
docker-compose up # if you are using standalone docker compose
```

After that all you need is to open your web browser and run:
[http://localhost:3000](http://localhost:3000) and thats it.

## Formato do arquivo de entrada

| Campo    | Início | Fim | Tamanho | Descrição                      |
| -------- | ------ | --- | ------- | ------------------------------ |
| Tipo     | 1      | 1   | 1       | Tipo da transação              |
| Data     | 2      | 26  | 25      | Data - ISO Date + GMT          |
| Produto  | 27     | 56  | 30      | Descrição do produto           |
| Valor    | 57     | 66  | 10      | Valor da transação em centavos |
| Vendedor | 67     | 86  | 20      | Nome do vendedor               |

### Tipos de transação

Esses são os valores possíveis para o campo Tipo:

| Tipo | Descrição         | Natureza | Sinal |
| ---- | ----------------- | -------- | ----- |
| 1    | Venda produtor    | Entrada  | +     |
| 2    | Venda afiliado    | Entrada  | +     |
| 3    | Comissão paga     | Saída    | -     |
| 4    | Comissão recebida | Entrada  | +     |

# Obs

This used to be a job application test, thats why it doesnt have a commit history.
