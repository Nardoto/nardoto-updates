====================================================
ARQUIVOS PARA SUBIR NO SERVIDOR - NARDOTO BROWSER
====================================================

ESTRUTURA DE PASTAS NO SEU SERVIDOR (nardoto.com.br):

/
├── browser-version.json      <- Subir na raiz
├── browser-news.json         <- Subir na raiz
├── extensions-version.json   <- Subir na raiz
├── downloads/
│   └── NardotoBrowser_Setup.exe   <- Instalador do navegador
└── extensions/
    ├── whisk-automator.zip
    ├── veo3-automator.zip
    ├── veo3-downloader.zip
    ├── suno-automator.zip
    ├── suno-downloader.zip
    ├── capcut-script-sender.zip
    ├── midjourney-automator.zip
    ├── google-tts-automator.zip
    ├── google-labs-downloader.zip
    ├── auto-folder.zip
    ├── gold-optimizer.zip
    ├── youtube-link-helper.zip
    ├── nardoto-newtab.zip
    ├── nardoto-theme.zip
    ├── nardoto-productivity.zip
    └── nardoto-adblocker.zip

====================================================
COMO ATUALIZAR:
====================================================

1. ATUALIZAR O NAVEGADOR:
   - Compile o novo instalador
   - Suba para /downloads/NardotoBrowser_Setup.exe
   - Edite browser-version.json e aumente a versao
   - O updater vai baixar automaticamente

2. ATUALIZAR UMA EXTENSAO:
   - Compacte a pasta da extensao em .zip
   - Suba para /extensions/nome-extensao.zip
   - Edite extensions-version.json e aumente a versao
   - O updater vai baixar automaticamente

3. ADICIONAR NOVIDADES/NOTICIAS:
   - Edite browser-news.json
   - Adicione um novo item no array "news"
   - As novidades aparecem na pagina inicial

====================================================
COMO CRIAR OS ARQUIVOS ZIP DAS EXTENSOES:
====================================================

Para cada extensao em C:\NardotoTest\NardotoBrowser\Extensions\:

1. Selecione TODOS os arquivos dentro da pasta da extensao
2. Clique direito > Enviar para > Pasta compactada
3. Renomeie para nome-extensao.zip
4. Suba para o servidor em /extensions/

IMPORTANTE: O ZIP deve conter os arquivos na raiz,
NAO uma pasta com o nome da extensao dentro!

Estrutura CORRETA do ZIP:
whisk-automator.zip
├── manifest.json
├── src/
└── assets/

Estrutura ERRADA do ZIP:
whisk-automator.zip
└── whisk-automator/
    ├── manifest.json
    └── ...

====================================================
