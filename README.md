# n8n-gitops

Репозиторий для хранения и автодеплоя воркфлоу n8n из GitHub в n8n-сервер.

## Как это работает
- Я правлю JSON-файлы воркфлоу в папке `workflows/` (в Cursor).
- Делаю **Commit → Push** в ветку `main`.
- GitHub Action `.github/workflows/deploy-to-n8n.yml` автоматически создаёт/обновляет воркфлоу в n8n через API.
- История версий хранится в Git — можно откатываться к любому коммиту.

## Требования
- Доступный n8n по адресу: `https://anyvier.ru`
- Включён API key (Settings → API) — **X-N8N-API-KEY**
- В репозитории добавлены секреты (Settings → Secrets → Actions):
  - `N8N_URL` = `https://anyvier.ru`
  - `N8N_API_KEY` = `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJiNzJhNjQxYi00MzM5LTQzMmYtOWI1MC1iNmI3NmFmOGQ1NTYiLCJpc3MiOiJuOG4iLCJhdWQiOiJwdWJsaWMtYXBpIiwiaWF0IjoxNzYwNDUxNTE4fQ.E05b96on9UEFicPVS3h35-78BcvXodi9Kh8hMdSYCD4`

## Структура
