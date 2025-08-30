# 🔐 Win-ACME (Let's Encrypt) – Status Técnico

## ⚙️ Configuração atual
- Ferramenta: **Win-ACME v2.x** instalada no Windows Server 2022 ✅  
- Certificados emitidos para:
  - `portalauditoria.com.br`
  - `www.portalauditoria.com.br`
  - `mail.portalauditoria.com.br` ✅  
- Validação realizada via **HTTP-01** em IIS (`.well-known/acme-challenge`).  
- Certificados gerados como **exportáveis (.pfx)**.  
- Renovação automática configurada pelo **Agendador de Tarefas do Windows**.  

## 📊 Observações
- Certificados aplicados com sucesso no:
  - **IIS (HTTPS bindings)**  
  - **hMailServer (SMTP/IMAP/POP)**  
- Testes externos confirmam:
  - **SSL Labs** → nota A+  
  - Navegadores → cadeias confiáveis ✅  
- Última emissão: **11/08/2025**  
- Próxima renovação prevista: **09/11/2025**  

