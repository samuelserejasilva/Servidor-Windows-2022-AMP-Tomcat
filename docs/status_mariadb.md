# 🗄️ Status Técnico – MariaDB 11.8 + Integração PHP

**Última atualização:** 29/08/2025  
**Responsável:** Samuel Cereja  
**Servidor:** Windows Server 2022 Datacenter  

---

## 🔧 Configuração do MariaDB
- Versão instalada: **MariaDB 11.8** ✅  
- Serviço ativo: `MariaDB` no Windows Services ✅  
- Porta padrão: **3306** ✅  
- Usuário root protegido com senha forte ✅  
- Usuários dedicados criados para:
  - **Roundcube** (base: `roundcubemail`)  
  - **hMailServer** (base: `hmailserver`)  
- Charset padrão: `utf8mb4` ✅  

---

## 🔧 Integração PHP
- Extensões ativas no `php.ini`:  
  - `mysqli` ✅  
  - `pdo_mysql` ✅  
- Teste de conexão com `phpinfo()` validado ✅  
- Roundcube acessando corretamente a base `roundcubemail` ✅  
- hMailServer integrado com banco `hmailserver` ✅  

---

## 🔒 Segurança
- Conexões externas desabilitadas (acesso local apenas) ✅  
- Usuários do DB restritos a permissões mínimas (principle of least privilege) ✅  
- Backups manuais configurados em `C:\Backups\MariaDB` ✅  
- Logs ativos: `C:\Program Files\MariaDB 11.8\data\hostname.err` ✅  

---

## 📊 Observações
- MariaDB estável e integrado ao PHP via FastCGI.  
- Bancos em uso:
  - `roundcubemail` → autenticação e sessões do Roundcube.  
  - `hmailserver` → contas, domínios e regras de e-mail.  
- Próximos passos:
  - Automatizar backup com script agendado.  
  - Avaliar replicação para redundância futura.
