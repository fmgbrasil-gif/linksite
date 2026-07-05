# Portal de Atalhos — Departamentos

Site estático com caixas de departamentos contendo atalhos para **sites** e **caminhos locais/de rede** (pastas do Windows, servidor de arquivos etc.).

Não precisa de servidor nem instalação: é um único arquivo `index.html` que funciona aberto direto no navegador.

## Como usar

1. Baixe o arquivo `index.html` (ou clone este repositório).
2. Dê dois cliques em `index.html` — ele abre no navegador.
3. Opcional: hospede em uma intranet, no GitHub Pages ou em qualquer pasta compartilhada da rede.

## Como adicionar/editar departamentos e links

Abra o `index.html` em um editor de texto (Bloco de Notas, VS Code...) e procure a lista `DEPARTAMENTOS` no início do `<script>`. Cada departamento segue este formato:

```js
{
  nome:  "Nome do departamento",
  icone: "📁",              // qualquer emoji
  cor:   "#3b6fd4",         // cor do cabeçalho da caixa
  links: [
    // Atalho de site (abre em nova aba):
    { nome: "Nome do atalho", url: "https://exemplo.com" },

    // Atalho de pasta local ou de rede (mostra botão "Copiar"):
    { nome: "Pasta do setor", caminho: "\\\\servidor\\Setor\\Pasta" },
    { nome: "Pasta no C:",    caminho: "C:\\Users\\Publico\\Documentos" },
  ]
},
```

> **Atenção:** em caminhos, cada barra invertida `\` precisa ser escrita em dobro (`\\`). Então `\\servidor\RH` vira `"\\\\servidor\\RH"`.

## Sobre os caminhos locais

Por segurança, os navegadores bloqueiam que uma página aberta pela internet (`http/https`) abra links `file://` diretamente. Por isso:

- Cada atalho de caminho local tem um botão **Copiar** — basta colar no Explorer de Arquivos (`Windows + E`, colar na barra de endereço e Enter).
- Se o `index.html` for aberto **localmente** (duplo clique no arquivo), alguns navegadores permitem abrir os links `file://` direto.
- Em intranets corporativas, é possível liberar links `file://` por política de grupo (GPO) no Edge/Chrome, se a TI desejar.

## Funcionalidades

- 🔍 Busca que filtra atalhos e departamentos em tempo real
- 🌙 Tema claro/escuro automático (segue o sistema)
- 📱 Layout responsivo (funciona em celular e desktop)
- 📋 Botão "Copiar" com confirmação visual para caminhos locais
