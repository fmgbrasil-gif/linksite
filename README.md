# Portal de Atalhos — FMG

Site estático com caixas de departamentos contendo atalhos para os sistemas da empresa.

Não precisa de servidor nem instalação: é um único arquivo `index.html` que funciona aberto direto no navegador.

## Como usar

1. Baixe o arquivo `index.html` (ou clone este repositório).
2. Dê dois cliques em `index.html` — ele abre no navegador.
3. Opcional: hospede no GitHub Pages, em uma intranet ou em qualquer pasta compartilhada da rede.

## Como adicionar/editar departamentos e links

Abra o `index.html` em um editor de texto (Bloco de Notas, VS Code...) e procure a lista `DEPARTAMENTOS` no início do `<script>`. Cada departamento segue este formato:

```js
{
  nome:  "Nome do departamento",
  icone: "📁",              // qualquer emoji
  cor:   "#3b6fd4",         // cor do cabeçalho da caixa
  links: [
    { nome: "Nome do atalho", url: "https://exemplo.com" },
    { nome: "Outro atalho",   url: "https://exemplo.com/sistema" },
  ]
},
```

Todos os atalhos abrem em nova aba.

## Funcionalidades

- 🔍 Busca que filtra atalhos e departamentos em tempo real
- 🌙 Tema claro/escuro automático (segue o sistema)
- 📱 Layout responsivo (funciona em celular e desktop)
