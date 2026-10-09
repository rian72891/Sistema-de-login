# Atividade_Login

Sistema de autenticação em HTML, CSS e JavaScript puros, com três telas: **cadastro**, **login** e **painel**. O projeto se chama **Tech System** e roda direto no navegador, sem back-end.

Versão publicada: https://jonathas32.github.io/Atividade_Login/

## Telas

| Arquivo | O que faz |
|---|---|
| `cadastro.html` | Cria a conta (nome, e-mail, usuário, senha e confirmação) e redireciona para o login. |
| `login.html` | Valida usuário e senha e redireciona para o painel. |
| `index.html` | Painel com mensagem de boas-vindas, as áreas do sistema e o botão **Sair**. |

## Fluxo de navegação

```
cadastro.html  ->  login.html  ->  index.html
      ^                |               |
      +--- Cadastre-se-+               |
                       <------ Sair ---+
```

- No login, o link **Cadastre-se** leva ao cadastro.
- No cadastro, o link **Entrar** leva ao login.
- No painel, o botão **Sair** volta ao login.

## Como funciona

**Cadastro.** Antes de salvar, o formulário valida:

1. nome com pelo menos 3 caracteres;
2. e-mail com `@` e `.`;
3. usuário sem espaços;
4. senha com pelo menos 6 caracteres;
5. senha e confirmação iguais.

Se algo estiver errado, o campo fica com borda vermelha e uma mensagem explica o problema. Se tudo estiver certo, o usuário e a senha são salvos no `localStorage` do navegador (chaves `usuarioCadastrado` e `senhaCadastrada`).

**Login.** Compara o que foi digitado com os dados salvos no cadastro. Se baterem, abre o painel; se não, mostra "Usuário ou senha incorretos."

**Painel.** Mostra o nome do usuário cadastrado no canto superior direito.

## Como executar

1. Baixe ou clone o repositório.
2. Abra `cadastro.html` no navegador (duplo clique).
3. Crie uma conta, entre pelo login e acesse o painel.

Não é preciso instalar nada. Para publicar no GitHub Pages, envie os arquivos para o repositório e ative o Pages nas configurações.

## Estrutura

```
Atividade_Login/
├── cadastro.html
├── login.html
├── index.html
└── README.md
```

Cada página tem o CSS e o JavaScript no próprio arquivo.

## Visual

- Layout dividido em duas partes nas telas de login e cadastro, com painel de marca à esquerda e formulário à direita.
- Responsivo: no celular, o painel de marca some e o formulário ocupa a tela.
- Botão para mostrar ou ocultar a senha.
- Fonte [Manrope](https://fonts.google.com/specimen/Manrope) via Google Fonts, com fontes do sistema como alternativa.

## Limitações

Este é um projeto de estudo. Para uso real, faltaria:

- **Back-end e banco de dados.** Os dados ficam só no navegador de quem cadastrou, e a senha é salva em texto puro.
- **Um único usuário.** Cada novo cadastro substitui o anterior.
- **Proteção do painel.** Quem abrir `index.html` diretamente consegue ver a tela sem fazer login.
- **Recuperação de senha.** O link "Esqueci minha senha" ainda não leva a nenhuma página.

## Tecnologias

HTML5, CSS3 e JavaScript (ES6).
