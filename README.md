[readmi (1).txt](https://github.com/user-attachments/files/20906123/readmi.1.txt)

Olá Professor,

Estou enviando um resumo sobre o projeto da Barbearia do David, que desenvolvemos. Ele é uma aplicação web que ajuda a gerenciar agendamentos, planos de serviço e os dados dos clientes da barbearia.

## Como o Projeto Foi Feito (Tecnologias):

**Na parte da frente (o que a gente vê no navegador - Frontend):**
*   Usamos **React** com **TypeScript** para fazer a interface. É tipo um JavaScript mais organizado, que ajuda a evitar erros.
*   Para montar tudo rapidinho, usamos o **Vite**.
*   O visual foi feito com **Tailwind CSS** (para estilizar sem complicação) e **Radix UI** 
*   Para lidar com os dados que vêm do servidor, usamos **React Query** e para os formulários, o **React Hook Form**.

**Na parte de Backend:**
*   O servidor foi construído com **Node.js** e o **Express**, que é um framework para criar APIs (que são as "pontes" de comunicação entre o frontend e o backend).
*   Aqui também usamos **TypeScript** para deixar o código mais seguro e fácil de mexer.

**Banco de dados:**
*   A gente usou o **Drizzle ORM**, que é uma ferramenta que nos ajuda a conversar com o banco de dados usando TypeScript, sem precisar escrever muito código SQL na mão.
*   O banco de dados mesmo é o **Neon Database**, que é um tipo de **PostgreSQL** que funciona na nuvem. Ele é bom porque se adapta sozinho ao tanto de gente que está usando o site.

**Como a Pessoa Entra no Sistema:**
*   Para o login e segurança, usamos o **Passport.js**.

## Estrutura do Projeto:

O projeto está dividido assim:
*   `client/`: É onde está todo o código da parte que o usuário vê (o site mesmo).
*   `server/`: É onde está o código que faz o site funcionar por trás (a lógica, a comunicação com o banco de dados).
*   `shared/`: Tem coisas que o frontend e o backend usam juntos, tipo as regras de como os dados são organizados.
*   `dist/`: É a pasta onde o site "pronto" fica depois de ser construído.

## Como Rodar o Projeto:

1.  Primeiro, precisa ter o Node.js e o npm  instalados.
2.  Abre o terminal, vai na pasta do projeto e digita `npm install` pra instalar as coisas que o projeto precisa.
3.  Para o banco de dados, a gente usa o Neon Database. Precisa de um arquivo `.env` com as informações de acesso (tem um exemplo no repositório). Depois, roda `npm run db:push` pra arrumar o banco de dados.
4.  Pra montar o site pra produção, digita `npm run build`.
5.  Pra rodar o site no seu computador (modo de desenvolvimento), usa `npm run dev`. Se for pra rodar como se estivesse no ar (produção), é `npm start`.

## Sobre o Problema de Hospedagem no Netlify:

Quando tentei colocar o site no Netlify, deu um erro de "Page not found". Descobri que o Netlify precisava saber onde estavam os arquivos "prontos" do site. A solução foi configurar o "Publish directory" para `dist/public` lá nas configurações do Netlify. Além disso, se as rotas do site não funcionarem direito depois de recarregar a página, a gente precisa criar um arquivo chamado `_redirects` na pasta `public` com o texto `/*    /index.html   200`. Isso faz com que o Netlify sempre mostre a página principal e o React cuide do resto das rotas.

Espero que ajude a entender o projeto!

Atenciosamente,
Davi Monteiro
