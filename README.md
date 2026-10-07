# 🤖 ChatGPT Clone

Aplicação web inspirada no **ChatGPT**, desenvolvida com **Next.js**, **TypeScript**, **Tailwind CSS** e a **OpenAI API**.

O projeto simula uma experiência de conversa com inteligência artificial, permitindo criar novos chats, enviar mensagens de forma assíncrona e acompanhar o processamento da resposta em tempo real, incluindo um estado de carregamento enquanto a IA está processando a solicitação.

Além da conversação, o sistema possui gerenciamento do histórico de chats, permitindo **editar e excluir conversas**.

---

## ✨ Funcionalidades

* 💬 Criar novas conversas
* 🤖 Conversar com a IA através da OpenAI API
* ⚡ Comunicação assíncrona entre usuário e IA
* ⏳ Indicador de processamento enquanto a IA está gerando a resposta
* 📝 Editar o histórico das conversas
* 🗑️ Excluir conversas
* 📚 Visualizar o histórico de chats
* 📱 Interface responsiva
* 🎨 Interface inspirada na experiência do ChatGPT
* 🚀 Aplicação construída com Next.js
* 🎨 Estilização utilizando Tailwind CSS

---

## 🛠️ Tecnologias

### Frontend

* [Next.js](https://nextjs.org/)
* [React](https://react.dev/)
* TypeScript
* Tailwind CSS

### Inteligência Artificial

* OpenAI API

### Gerenciamento

* Node.js
* npm / pnpm

---

## 🧠 Como funciona

O fluxo principal da aplicação funciona de forma semelhante ao ChatGPT:

```text
Usuário
   │
   │ Envia uma pergunta
   ▼
Next.js
   │
   │ Requisição para OpenAI API
   ▼
OpenAI
   │
   │ Processamento da pergunta
   ▼
Next.js
   │
   │ Retorna a resposta
   ▼
Interface
   │
   ▼
Usuário
```

Enquanto a solicitação está sendo processada, a aplicação apresenta um estado de carregamento, indicando que a IA está trabalhando na resposta.

---

## 📋 Pré-requisitos

Antes de começar, você precisa ter instalado:

* **Node.js** `20+`
* **npm**, **pnpm** ou **yarn**
* Uma conta na OpenAI
* Uma **API Key da OpenAI**

---

## 🚀 Instalação

### 1. Clone o repositório

```bash
git clone https://github.com/luan-junior/chatgpt-clone/
```

Entre no diretório:

```bash
cd SEU_REPOSITORIO
```

---

### 2. Instale as dependências

Utilizando npm:

```bash
npm install
```

Ou utilizando pnpm:

```bash
pnpm install
```

Ou yarn:

```bash
yarn
```

---

## 🔐 Configuração da OpenAI API

Crie um arquivo `.env.example` na raiz do projeto:

```env
OPENAI_API_KEY=sua_api_key_aqui
```

Substitua `sua_api_key_aqui` pela sua chave da OpenAI.

> ⚠️ **Importante:** nunca envie sua API Key para o GitHub ou qualquer outro repositório público.

Certifique-se de que o arquivo `.env.example` esteja incluído no `.gitignore`:

```gitignore
.env.example
.env
```

---

## ▶️ Executando o projeto

Para iniciar o ambiente de desenvolvimento:

### npm

```bash
npm run dev
```

### pnpm

```bash
pnpm dev
```

### yarn

```bash
yarn dev
```

Depois, acesse:

```text
http://localhost:3000
```

---

## 📦 Build para produção

Para gerar a versão de produção:

```bash
npm run build
```

Depois de realizar o build:

```bash
npm run start
```

Utilizando pnpm:

```bash
pnpm build
pnpm start
```

## 💬 Gerenciamento das conversas

Cada conversa possui seu próprio histórico de mensagens.

O usuário pode:

```text
┌───────────────────────────────┐
│          Novo Chat             │
├───────────────────────────────┤
│ Chat sobre React               │
│ Projeto Next.js                │
│ Estudos de Node.js             │
│ OpenAI API                     │
├───────────────────────────────┤
│          Histórico             │
└───────────────────────────────┘
```

Também é possível editar e excluir conversas existentes.

---

## ⏳ Processamento assíncrono

A aplicação não bloqueia a interface enquanto aguarda a resposta da IA.

Ao enviar uma mensagem, o usuário recebe um feedback visual indicando que a solicitação está sendo processada.

Exemplo:

```text
Você:
Como funciona o React Server Components?

         ↓

🤖 Pensando...

         ↓

Assistente:
React Server Components permitem...
```

Esse comportamento proporciona uma experiência mais próxima da utilização de aplicações modernas de IA, como o ChatGPT.

---

## 🎨 Interface

A interface foi construída utilizando **Tailwind CSS**, permitindo criar uma UI responsiva e consistente através de classes utilitárias.

O objetivo é reproduzir os principais conceitos de UX encontrados em aplicações de chat com IA:

* Sidebar com histórico
* Área principal de conversa
* Campo de entrada de mensagens
* Indicador de processamento
* Mensagens diferenciadas entre usuário e assistente
* Ações para gerenciamento das conversas

---

## 🔑 Variáveis de ambiente

| Variável         | Descrição                                         |
| ---------------- | ------------------------------------------------- |
| `OPENAI_API_KEY` | Chave utilizada para comunicação com a OpenAI API |

Exemplo:

```env
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxx
```

---

## 🔒 Segurança

A API Key da OpenAI deve ser utilizada exclusivamente no servidor.

Não exponha a chave diretamente no código do frontend ou em variáveis públicas como:

```env
NEXT_PUBLIC_OPENAI_API_KEY
```

A comunicação com a OpenAI deve ser realizada através de uma rota/API server-side do Next.js.

---

## 📌 Possíveis melhorias

Algumas funcionalidades que podem ser adicionadas futuramente:

* [ ] Streaming das respostas da IA
* [ ] Autenticação de usuários
* [ ] Persistência das conversas em banco de dados
* [ ] Markdown nas respostas
* [ ] Syntax highlighting para código
* [ ] Upload de arquivos
* [ ] Upload e análise de imagens
* [ ] Seleção de diferentes modelos da OpenAI
* [ ] Regeneração de respostas
* [ ] Copiar resposta
* [ ] Dark/Light mode
* [ ] Busca no histórico
* [ ] Deploy em produção

---

## 🎯 Objetivo do projeto

Este projeto foi desenvolvido com o objetivo de explorar a construção de uma aplicação moderna baseada em **IA generativa**, utilizando a OpenAI API integrada a uma aplicação **Next.js**.

Além da integração com inteligência artificial, o projeto aborda conceitos importantes de desenvolvimento frontend, como:

* Comunicação assíncrona
* Gerenciamento de estado
* Componentização
* API Routes
* Experiência do usuário
* Estados de loading
* Responsividade
* Integração com APIs externas
* Organização e arquitetura de aplicações Next.js

---

## 👨‍💻 Autor

**Luan Junior**

Desenvolvedor Full Stack com experiência em **React, Next.js, Node.js e TypeScript**.

---

## ⭐ Contribuição

Contribuições são bem-vindas!

1. Faça um fork do projeto
2. Crie uma branch para sua alteração

```bash
git checkout -b feature/minha-feature
```

3. Faça o commit:

```bash
git commit -m "feat: adiciona minha feature"
```

4. Envie para o repositório:

```bash
git push origin feature/minha-feature
```

5. Abra um Pull Request.

---

## 📄 Licença

Este projeto está disponível sob a licença definida neste repositório.
