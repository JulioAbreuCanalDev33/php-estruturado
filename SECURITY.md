# Política de Segurança

## 🛡️ Relatório de Vulnerabilidades

Se você descobrir uma vulnerabilidade de segurança, **não a divulgue publicamente**. 

### Como Reportar:

1. **Email**: Envie um relatório detalhado para o mantenedor do projeto
2. **GitHub Security Advisory**: Use a função de Security Advisory do GitHub
3. **Não publique** em issues públicas ou pull requests

### O que incluir no relatório:

- Descrição clara da vulnerabilidade
- Passos para reproduzir o problema
- Impacto potencial
- Sugestões de correção (se houver)

---

## 🔐 Práticas de Segurança

### Autenticação & Autorização
- Todas as senhas devem ser hash com `bcrypt` ou `Argon2`
- Implementar verificação de permissões em todas as ações sensíveis
- Usar sessões seguras com expiração

### Validação de Entrada
- Validar e sanitizar TODOS os dados de entrada do usuário
- Usar prepared statements para consultas ao banco de dados
- Implementar rate limiting para endpoints públicos

### Gerenciamento de Secrets
- **NUNCA** commitar `.env` ou arquivos com credenciais
- Usar GitHub Secrets para variáveis sensíveis
- Rotacionar credentials regularmente

### Dependências
- Manter dependências atualizadas
- Revisar alertas do Dependabot
- Usar `composer.lock` para versões fixas em produção

### Criptografia
- Usar HTTPS em produção (obrigatório)
- Criptografar dados sensíveis em repouso
- Usar algoritmos modernos (não use MD5, SHA1)

### Logs & Monitoramento
- Não logar dados sensíveis (senhas, tokens, PII)
- Manter logs por pelo menos 30 dias
- Monitorar tentativas de acesso suspeitas

---

## 🚀 Resposta a Incidentes

1. Confirmar e validar a vulnerabilidade
2. Criar um branch de correção (não em main)
3. Implementar o fix e testes
4. Fazer code review antes do merge
5. Liberar atualização de segurança
6. Comunicar aos usuários (se necessário)

---

## 📋 Checklist de Segurança

- [ ] Código revisado por pelo menos 2 pessoas
- [ ] Testes de segurança implementados
- [ ] Sem hardcoded secrets ou credenciais
- [ ] Dependências atualizadas
- [ ] HTTPS configurado (produção)
- [ ] Rate limiting implementado
- [ ] Validação de entrada completa
- [ ] Prepared statements em uso
- [ ] Logging seguro configurado

---

## 📚 Recursos

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [PHP Security Best Practices](https://www.php.net/manual/en/security.php)
- [GitHub Security Documentation](https://docs.github.com/en/code-security)

---

**Última atualização**: 2026-06-29
