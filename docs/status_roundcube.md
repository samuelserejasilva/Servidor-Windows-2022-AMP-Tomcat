# 📧 Status Técnico – Roundcube 1.7 (Webmail em IIS/PHP)

**Última atualização:** 29/08/2025  
**Responsável:** Samuel Cereja  
**Servidor:** Windows Server 2022 Datacenter  

---

## 🔧 Configuração do Roundcube
- Versão instalada: **Roundcube 1.7 beta** ✅  
- Local de instalação: `C:\inetpub\wwwroot\webmail` ✅  
- Executando via **IIS 10 + PHP 8.4 (FastCGI)** ✅  
- Configuração `config.inc.php`:  
  - Banco de dados: MariaDB (`roundcubemail`) ✅  
  - Autenticação IMAP/SMTP: `mail.portalauditoria.com.br` ✅  
- Diretório de logs: `C:\inetpub\wwwroot\webmail\logs` ✅  

---

## 🔧 Integração com IIS
- Binding HTTPS configurado em `mail.portalauditoria.com.br` ✅  
- `web.config` customizado para:
  - Permitir `.json` ✅  
  - Bloquear directory browsing ✅  
  - Adicionar headers de segurança ✅  
- Rewrite rules: `/webmail` bypass no ARR para não redirecionar para Tomcat ✅  

---

## 🔒 Segurança
- Conexões forçadas em **SSL/TLS** (IMAP 993 / SMTP 465) ✅  
- Cabeçalhos de segurança ativos (`X-Frame-Options`, `X-Content-Type-Options`) ✅  
- Autenticação SPA desativada (não necessária) ✅  
- Logs monitorados para falhas de login ✅  

---

## 📊 Observações
- Roundcube funcionando em produção como cliente IMAP/SMTP.  
- Testado com contas: `contabil@portalauditoria.com.br` e `luciane@portalauditoria.com.br`.  
- Próximos passos:
  - Ajustar plugins úteis (password change, managesieve).  
  - Validar envio/recebimento com logs SMTP/IMAP ativos.  
