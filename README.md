# GranaXP

Aplicação Node.js/Express com interface React servida pelo próprio servidor e banco SQLite.

## Executar localmente

Requer Node.js 20 ou 22.

Defina estas variáveis de ambiente antes de iniciar:
- `ADMIN_PASSWORD`: senha forte para o painel administrativo.
- `JWT_SECRET`: segredo aleatório para sessões de usuários.
- `ADMIN_JWT_SECRET`: outro segredo aleatório, diferente do anterior.
- `DB_PATH` (opcional): caminho do arquivo SQLite.

Depois execute `npm install` e `npm start`.

## Hospedagem

O `render.yaml` prepara o serviço para Render com disco persistente. O serviço com disco persistente pode ter custo; confira preços e condições atuais antes de criar o serviço. Configure `ADMIN_PASSWORD` como segredo no painel do Render. Nunca publique `.env`, senhas ou arquivos de banco de dados no GitHub.

O projeto usa SQLite e precisa de armazenamento persistente para preservar os dados. Não é recomendável implantá-lo como uma função serverless sem adaptar a camada de dados.
