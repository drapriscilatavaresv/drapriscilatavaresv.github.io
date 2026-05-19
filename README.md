# Dra. Priscila Tavares — Site Oficial

Site institucional com blog, desenvolvido com Jekyll e hospedado no GitHub Pages.

## Como publicar no GitHub Pages

### 1. Criar repositório no GitHub
1. Acesse [github.com](https://github.com) e faça login
2. Clique em **New repository**
3. Nome sugerido: `dra-priscila-tavares` (ou `SEU-USUARIO.github.io` para URL mais curta)
4. Deixe **público**
5. Clique em **Create repository**

### 2. Configurar o `_config.yml`
Antes de subir os arquivos, edite `_config.yml` e atualize:
```yaml
url: "https://SEU-USUARIO.github.io"
baseurl: "/dra-priscila-tavares"  # ou "" se o repo se chamar SEU-USUARIO.github.io
```

### 3. Subir os arquivos
```bash
cd priscila-tavares-site
git init
git add .
git commit -m "Lançamento do site"
git remote add origin https://github.com/SEU-USUARIO/dra-priscila-tavares.git
git push -u origin main
```

### 4. Ativar o GitHub Pages
1. No repositório, clique em **Settings**
2. No menu lateral, clique em **Pages**
3. Em **Source**, selecione `Deploy from a branch`
4. Selecione a branch `main` e a pasta `/ (root)`
5. Clique em **Save**

O site ficará disponível em alguns minutos em:
`https://SEU-USUARIO.github.io/dra-priscila-tavares/`

## Como rodar localmente

```bash
gem install bundler
bundle install
bundle exec jekyll serve
```
Acesse: `http://localhost:4000`

## Como adicionar um novo post no blog

1. Crie um arquivo em `_posts/` com o formato: `AAAA-MM-DD-titulo-do-post.md`
2. Adicione o cabeçalho (front matter):

```yaml
---
layout: post
title: "Título do artigo"
date: 2025-06-01
category: "Suplementação"
icon: "🌿"
reading_time: 5
excerpt: "Resumo breve do artigo que aparece na listagem do blog."
---

Conteúdo do artigo em Markdown...
```

3. Salve e faça push para o GitHub — o site atualiza automaticamente.

## Estrutura de arquivos

```
├── _config.yml          # Configurações do Jekyll
├── _layouts/            # Templates HTML
├── _posts/              # Posts do blog
├── assets/
│   ├── css/style.css    # Estilos do site
│   ├── js/main.js       # JavaScript
│   └── images/          # Fotos e logo
├── index.html           # Página inicial
├── sobre.html           # Sobre a Dra. Priscila
├── servicos.html        # Como posso ajudar
├── blog/index.html      # Listagem do blog
└── agendamento.html     # Agendamento
```
