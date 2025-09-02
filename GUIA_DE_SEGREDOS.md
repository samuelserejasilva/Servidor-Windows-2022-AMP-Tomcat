# Guia de Segredos (não versionar)

Guarde fora do Git:
- Certificados `.pfx` + senhas
- Usuários/senhas de DB (PostgreSQL/MariaDB)
- Chaves privadas DKIM
- Credenciais SMTP, API keys

Sugerido:
- **Windows Credential Manager** / **GPO** para serviços no Windows
- **KeePass** (arquivo `.kdbx` com backup offline)
- **Repositório privado** separado só para *templates* (`.env.example`, `application.properties.example`)

