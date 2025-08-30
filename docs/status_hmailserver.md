# 📬 hMailServer 5.6.8 – Status Técnico

## ⚙️ Configuração atual
- Servidor ativo e integrado com **SSL/TLS** válido.  
- **Filtros globais** criados para tratamento de mensagens críticas (SPF/DMARC, Receita, Prefeitura, etc.).  
- **Anti-spam** configurado com:
  - DNS Blacklists (Spamhaus, Barracuda, Sorbs, etc.).  
  - SURBL ativo.  
  - Greylisting habilitado.  
- **Anti-vírus** integrado com ClamAV (ver status no relatório específico).  
- **Scripts customizados** ativos (`EventHandlers.vbs`) com suporte a:
  - `blacklist.txt` → bloqueio imediato de domínios recorrentes.  
  - `whitelist.txt` → proteção contra falsos positivos.  
- **Thresholds configurados**:
  - Marcar como spam = score ≥ 5.  
  - Deletar spam = score ≥ 8.  
- **Logs** ativados para SMTP/IMAP/DEBUG (auxiliando na auditoria).  

## 📊 Observações
- Filtros + script + listas auxiliaram em **~90% de redução de spam** efetivo.  
- Não há alertas críticos no momento; sistema estável.  
- Scripts e listas de bloqueio/whitelist são revisados periodicamente.  

## 🚀 Próximos passos
- Revisar pontualmente falsos positivos em filtros mais agressivos.  
- Expandir integrações com RBLs adicionais, caso necessário.  
- Criar **dashboard consolidado de métricas** (spam bloqueado x entregue) para relatórios gerenciais.  
