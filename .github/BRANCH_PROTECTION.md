# Branch Protection Configuration

## 🔒 Protected Branches: `main` e `develop`

Este documento descreve as políticas de proteção de branch configuradas no repositório.

### Requisitos de Merge para `main`

✅ **Habilitados:**

1. **Require pull request reviews before merging**
   - Número mínimo de aprovações: 1
   - Dismiss stale pull request approvals when new commits are pushed
   - Require review from Code Owners: ✓

2. **Require status checks to pass before merging**
   - Require branches to be up to date before merging: ✓
   - Security Checks: ✓
   - PHP Lint: ✓

3. **Require conversation resolution before merging**: ✓

4. **Require signed commits**: ✓

5. **Require linear history**: ✓

### Requisitos de Merge para `develop`

✅ **Habilitados:**

1. **Require pull request reviews before merging**
   - Número mínimo de aprovações: 1

2. **Require status checks to pass before merging**
   - Security Checks: ✓
   - PHP Lint: ✓

### Dismiss Rules

- Stale pull request approvals serão automaticamente removidas quando novos commits forem enviados
- Code Owners devem fornecer aprovação em mudanças sensíveis

### Quien Pode Fazer Merge

- Apenas o proprietário do repositório ou usuários com permissão `admin`

---

## 🚀 Como Configurar Manualmente (se necessário)

Para habilitar branch protection manualmente:

1. Vá para **Settings** → **Branches**
2. Clique em **Add rule** ou selecione o branch
3. Configure conforme as políticas acima
4. Salve as mudanças

## 📋 Checklist de Merge

Antes de fazer merge para `main`:

- [ ] Código revisado por pelo menos 1 pessoa
- [ ] Todos os testes passando (Security Checks + PHP Lint)
- [ ] Nenhuma conversa pendente
- [ ] Branch atualizado com main
- [ ] Commits assinados (signed commits)
- [ ] Descrição clara do PR

---

**Última atualização**: 2026-06-29
