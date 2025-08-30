# ☕ Tomcat 11 (Jakarta EE 11 + JDK 24) – Status Técnico

## ⚙️ Configuração atual
- **Tomcat 11** instalado no **Windows Server 2022**.  
- Executando com **Java JDK 24**, configurado via variável `JAVA_HOME`.  
- Instalado como **serviço do Windows**, iniciando automaticamente com o sistema.  
- Conectado ao **IIS (ARR + URL Rewrite)** como proxy reverso para `/app` e `/api`.  
- Estrutura pronta para aplicações **JSP/Servlets** e integração com **APIs REST**.  

## 📊 Observações
- Porta **8080** interna, acessível apenas via proxy reverso do IIS.  
- Logs organizados em `logs\catalina.out` e `logs\localhost_access_log`.  
- Configuração de **Server Shutdown Port** desativada por segurança.  
- Testes confirmados com páginas **JSP** e integração básica funcionando.  
- Integração validada com PHP/IIS no mesmo servidor (ambiente híbrido).  

## 🚀 Próximos passos
- Configurar **SSL/TLS** direto no Tomcat (apenas se necessário, já há proxy HTTPS via IIS).  
- Monitorar consumo de memória/heap (`-Xms`, `-Xmx`) e ajustar conforme carga.  
- Avaliar integração com **MariaDB** usando `JDBC Connector`.  
- Testar deploy de aplicação **Jakarta EE completa** (WAR) para validar recursos avançados.  
