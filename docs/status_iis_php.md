# 🌐 Status Técnico – IIS + PHP (FastCGI)

**Última atualização:** 29/08/2025  
**Responsável:** Samuel Cereja  
**Servidor:** Windows Server 2022 Datacenter  

---

## 🔧 Configuração do IIS
- IIS 10 instalado e ativo ✅
- ARR + URL Rewrite habilitados ✅
- Sites configurados:
  - Portal Auditoria (páginas AMP + proxy para Tomcat)
  - Webmail (Roundcube em `/webmail`) ✅
- Regras de URL Rewrite:
  - Proxy IIS → Tomcat (`/app/*` e `/api/*`) ✅
  - Bypass `/webmail` ✅
  - Redirect **www → não-www** ✅
- HTTPS habilitado em todos os bindings (SSL/TLS válido via Win-ACME) ✅

---

## 🔧 Configuração do PHP
- Versão instalada: **PHP 8.4 (x64)** ✅
- Modo de execução: **CGI/FastCGI** (`C:\php\php-cgi.exe`) ✅
- Configuração FastCGI no IIS:
  - `PHPRC = C:\php\`
  - `PHP_FCGI_MAX_REQUESTS = 10000`
- `php.ini` revisado com:
  - Extensões ativas: `mbstring`, `imap`, `openssl`, `intl`, `pdo_mysql`, `mysqli`, `fileinfo`, `curl`, `zip` ✅
  - Diretivas de segurança: `expose_php=Off`, `display_errors=Off`, `log_errors=On` ✅
  - Sessões seguras: `session.cookie_secure=1`, `session.cookie_httponly=1` ✅
  - Upload configurado: `upload_max_filesize=20M`, `post_max_size=25M` ✅
- `phpinfo()` validado — carregando `php.ini` correto ✅

---

## 🔒 Segurança
- Certificados SSL/TLS aplicados no IIS ✅
- HSTS configurado (`Strict-Transport-Security`) ✅
- Cabeçalhos adicionais:
  - `X-Content-Type-Options: nosniff`
  - `Referrer-Policy: no-referrer-when-downgrade`
- Directory browsing desabilitado ✅

---

## 📊 Observações
- PHP está rodando de forma estável no IIS com Roundcube.  
- Logs de erro em `C:\inetpub\logs\php\php_errors.log`.  
- Próximos passos: monitorar consumo de memória e validar desempenho em produção com AMP + Roundcube.
