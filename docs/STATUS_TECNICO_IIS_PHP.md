# 🌐 IIS + PHP 8.4 – Status Técnico

## ⚙️ Configuração atual
- **IIS (Internet Information Services)** rodando no **Windows Server 2022**.  
- Configuração integrada com:
  - **FastCGI** (`C:\php\php-cgi.exe`) para execução do PHP.  
  - Variáveis de ambiente:  
    - `PHPRC = C:\php\`  
    - `PHP_FCGI_MAX_REQUESTS = 10000`  
- **PHP 8.4** instalado e validado com `phpinfo()`.  
- Diretório configurado com permissões adequadas para **IIS_IUSRS**.  
- **SSL/TLS** habilitado via certificados Let's Encrypt (Win-ACME).  

## 📊 Observações
- **php.ini** revisado e otimizado:
  - Segurança: `expose_php = Off`, `display_errors = Off`, `log_errors = On`.  
  - Performance: `memory_limit = 256M`, `opcache` habilitado.  
  - Uploads: `upload_max_filesize = 20M`, `post_max_size = 25M`.  
  - Sessões protegidas com `cookie_secure = 1`, `cookie_httponly = 1`, `cookie_samesite = Lax`.  
- Extensões críticas para Roundcube habilitadas: `mbstring`, `imap`, `openssl`, `intl`, `pdo_mysql`, `mysqli`, `fileinfo`, `curl`, `zip`.  
- Logs de erros direcionados para `C:\inetpub\logs\php\php_errors.log`.  
- **Configuração validada** com Roundcube Webmail e aplicações em produção.  

## 🚀 Próximos passos
- Monitorar uso de **opcache** em produção para ajustes finos.  
- Avaliar ativação de **brotli/gzip** no IIS para compressão de conteúdo.  
- Testar cenários de carga maior (stress test no PHP-FastCGI).  
