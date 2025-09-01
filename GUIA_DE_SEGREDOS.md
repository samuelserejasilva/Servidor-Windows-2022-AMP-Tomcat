# Guia de Gestão de Segredos

Este documento descreve como armazenar e tratar credenciais, certificados e outros dados sensíveis usados neste projeto.

## Boas práticas

- Nunca versionar segredos diretamente (senhas, chaves privadas, certificados). Veja [SECURITY.md](SECURITY.md) para uma lista dos itens que devem permanecer fora do Git.
- Utilize variáveis de ambiente ou arquivos de configuração fora do repositório para guardar credenciais.
- Prefira gerenciadores seguros como Windows Credential Manager, Azure Key Vault, AWS Secrets Manager ou KeePass para armazenar senhas.
- Forneça apenas arquivos modelo (`.env.example`, `application.properties.example`) sem credenciais reais.
- Limite o acesso a segredos em produção e realize rotação periódica.
- Revise commits com scanners de segredos (por exemplo, `git-secrets`, `trufflehog`).
- Em caso de vazamento, revogue e gere novas chaves imediatamente seguindo as políticas descritas em [SECURITY.md](SECURITY.md).

## Referências

- [SECURITY.md](SECURITY.md) – itens não versionados e recomendações de armazenamento.
