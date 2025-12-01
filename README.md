# Arquivos do Servidor Nardoto

Estes arquivos devem ser hospedados em `https://nardoto.com.br/`

## Como Funciona

1. **Edite os arquivos aqui** (Cursor, VSCode, qualquer editor)
2. **Suba pro servidor** (via Git deploy, FTP, ou hosting)
3. **O navegador busca automaticamente** as atualizacoes

---

## Arquivos

### browser-news.json
Novidades que aparecem no painel lateral da pagina inicial.

**Campos:**
- `tag`: Categoria (Novo, Dica, Update, Tutorial, etc)
- `date`: Data no formato "DD Mes AAAA"
- `title`: Titulo da novidade
- `desc`: Descricao curta
- `url`: Link opcional (null se nao tiver)

**Quando atualizar:** Sempre que quiser comunicar algo aos usuarios.

---

### browser-version.json
Controla atualizacoes do navegador.

**Campos:**
- `version`: Versao atual (ex: "2.0", "2.1")
- `downloadUrl`: URL do instalador .exe
- `releaseNotes`: Descricao da atualizacao

**Quando atualizar:** Quando compilar nova versao do instalador.

**Fluxo:**
1. Compile novo instalador com versao X.X
2. Suba o .exe para o servidor
3. Atualize este JSON com a nova versao e URL
4. O updater dos usuarios vai baixar automaticamente

---

### extensions-version.json
Controla atualizacoes das extensoes individuais.

**Campos por extensao:**
- `name`: Nome da pasta da extensao (EXATO)
- `version`: Versao no manifest.json da extensao
- `downloadUrl`: URL do .zip da extensao

**Quando atualizar:** Quando modificar alguma extensao.

**Fluxo:**
1. Modifique a extensao e atualize o version no manifest.json
2. Compacte a pasta da extensao em .zip
3. Suba o .zip para o servidor
4. Atualize este JSON com a nova versao

---

## Deploy no Servidor

### Opcao 1: Firebase Hosting (Recomendado)
Se voce usa Firebase para o Nardoto Labs:

```bash
# Na pasta do projeto Firebase
firebase deploy --only hosting
```

### Opcao 2: Git + Deploy Automatico
Configure GitHub Actions ou similar para deploy automatico.

### Opcao 3: Upload Manual
Suba os arquivos via FTP/painel do hosting para:
- nardoto.com.br/browser-news.json
- nardoto.com.br/browser-version.json
- nardoto.com.br/extensions-version.json
- nardoto.com.br/downloads/ (instaladores)
- nardoto.com.br/extensions/ (zips das extensoes)

---

## Dicas

- Sempre teste os JSONs em https://jsonlint.com antes de subir
- Mantenha backup das versoes anteriores
- O updater roda a cada 6 horas automaticamente
