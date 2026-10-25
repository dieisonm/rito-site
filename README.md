# rito-site

Site institucional da RITO Sistemas (https://ritosistemas.com). Só o código do site; documentação, operação, segredos e materiais ficam na pasta RITO do OneDrive (backup) e arquivos grandes no Google Drive.

Separado do repositório `dieisonm/RITO` em 2026-10-25 a partir do commit `8be21bf`. O histórico anterior do site continua lá.

## Build e deploy

- Build local: `./scripts/build_dist.sh` gera `dist/`.
- Deploy: push na `main` alterando `site/**` dispara o GitHub Actions, que publica a branch `hostinger`; a Hostinger faz o Git Deployment dessa branch para `/public_html`.
- Conferir: `python3 scripts/verify_live_site.py` e `https://ritosistemas.com/deploy-info.json` com a mesma `asset_version` de `dist/deploy-info.json`.
- Nunca publicar por upload direto.
