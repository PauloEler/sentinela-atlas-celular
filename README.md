# SENTINELA — Atlas da Vida Celular

PWA educativo do NEO LAB para explorar célula saudável, DNA, proteção celular e transformação cancerígena em animações didáticas.

**Versão:** v0.9. Validação em Android real e migração de uma instalação v0.8 pendentes.

**Destino público:** https://pauloeler.github.io/sentinela-atlas-celular/ (GitHub Pages, branch `main`, pasta raiz).

## Escopo público
Somente arquivos educativos do aplicativo (`index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `LEIA_ME.txt`). Não incluir registros privados, dados médicos, pesquisas internas, credenciais ou backups.

## Limitações
As animações são esquemáticas e não constituem modelos biomédicos validados, diagnóstico ou orientação terapêutica.

## Execução local
Execute `python -m http.server 8779 --bind 127.0.0.1` nesta pasta e abra http://127.0.0.1:8779/.

## Atualização e funcionamento offline
O service worker armazena o aplicativo para uso offline após a primeira carga online bem-sucedida. Cada versão deve usar uma nova chave de cache. A atualização aguarda o fechamento das janelas da versão anterior; reabra o aplicativo conectado para concluir o ciclo. Apenas caches antigos com prefixo `sentinela-modular-` são removidos.

## Validação e manutenção
- Conferir módulos 01 a 04 em telas pequenas, toque e teclado.
- No Android, instalar por HTTPS, fechar e reabrir offline.
- Validar atualização da v0.8 para v0.9 fechando todas as janelas antigas.
- Após cada publicação, conferir o build do GitHub Pages e os recursos no endereço público.

Não adicionar dados privados ao repositório. O `.gitignore` é uma proteção auxiliar e não substitui a revisão dos arquivos antes de cada commit.
