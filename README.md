# Dra. Priscila Tavares — Site Oficial

Site estático hospedado no **GitHub Pages** (sem Jekyll — servido diretamente pelo `.nojekyll`).

## Como publicar no GitHub Pages

### 1. Criar o repositório no GitHub
1. Acesse [github.com](https://github.com) com o usuário **drapriscilatavaresv**
2. Clique em **New repository**
3. Nome do repositório: `drapriscilatavaresv.github.io`
   - Com esse nome, o site ficará em: `https://drapriscilatavaresv.github.io/`
4. Deixe **público**
5. Clique em **Create repository**

### 2. Subir os arquivos
Abra o Terminal, navegue até a pasta do site e execute:

```bash
cd ~/Downloads/priscila-tavares-site
git init
git add .
git commit -m "Lançamento do site da Dra. Priscila Tavares"
git branch -M main
git remote add origin https://github.com/drapriscilatavaresv/drapriscilatavaresv.github.io.git
git push -u origin main
```

### 3. Ativar o GitHub Pages
1. No repositório, clique em **Settings**
2. No menu lateral, clique em **Pages**
3. Em **Source**, selecione `Deploy from a branch`
4. Selecione a branch `main` e a pasta `/ (root)`
5. Clique em **Save**

O site ficará disponível em alguns minutos em:
**https://drapriscilatavaresv.github.io/**

> Não é necessário `_config.yml` — o arquivo `.nojekyll` instrui o GitHub Pages a servir os arquivos HTML diretamente, sem processamento Jekyll.

## Como adicionar um novo post no blog

1. Copie um dos arquivos em `blog/` (ex: `blog/vitamina-d.html`)
2. Renomeie para `blog/nome-do-artigo.html`
3. Edite o conteúdo HTML dentro de `<div class="artigo-corpo">`
4. Adicione o link para o novo artigo em `blog.html` e na seção de preview em `index.html`
5. Faça push para o GitHub — o site atualiza automaticamente

## Estrutura de arquivos

```
priscila-tavares-site/
├── .nojekyll               ← diz ao GitHub Pages para não usar Jekyll
├── index.html              ← Página inicial
├── sobre.html              ← Sobre a Dra. Priscila
├── servicos.html           ← Como posso ajudar
├── blog.html               ← Listagem do blog
├── agendamento.html        ← Agendamento e contato
├── blog/
│   ├── vitamina-d.html     ← Artigo: Vitamina D
│   ├── magnesio.html       ← Artigo: Magnésio
│   └── ferro.html          ← Artigo: Ferro e ferritina
└── assets/
    ├── css/style.css        ← Todos os estilos
    └── images/
        ├── logo.png         ← Logo da Dra. Priscila
        ├── foto-hero.jpg    ← Foto da hero (blusa rosa)
        └── foto-sobre.png   ← Foto da seção Sobre (blusa vinho)
```
