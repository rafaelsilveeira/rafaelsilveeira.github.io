---
applyTo: "**/.git/**"
description: "Geração de mensagens de commit em português brasileiro"
---

# Commit Message Guidelines

## Core Rules
- Generate commit messages in Brazilian Portuguese (pt-BR)
- Use imperative mood verbs (adiciona, corrige, remove, atualiza)
- Analyze ONLY staged files (after `git add`)
- Keep total message under 300 characters
- Title maximum 72 characters
- Body maximum 4 bullets, each 50-60 characters

## Message Format
```
type(scope): brief description in pt-BR

- Technical detail 1 (max 60 chars)
- Technical detail 2 (max 60 chars)
- Impact or context (max 60 chars)
```

## Change Types
- `feat:` - New functionality or feature
- `fix:` - Bug correction
- `refactor:` - Code refactoring (no functional change)
- `docs:` - Documentation
- `style:` - Formatting, linting (no functional change)
- `test:` - Tests
- `chore:` - Maintenance, build, dependencies

## Scopes
- `gamification` - Gamification system
- `ui` - Interface and components
- `api` - Integrations and services
- `auth` - Authentication
- `types` - TypeScript typings
- `config` - Configurations

## Examples

### Feature
```
feat(gamification): adiciona sistema de conquistas diárias

- Implementa hook useDailyStreak para tracking
- Adiciona componente DailyStreakCard
- Integra com API de gamificação existente
```

### Bug Fix
```
fix(ui): corrige overflow em cards de ranking

- Ajusta largura máxima para mobile
- Remove padding excessivo em telas pequenas
- Mantém responsividade em todos os breakpoints
```

### Refactor
```
refactor(api): simplifica hooks de gamificação

- Remove duplicação em useGamificationQuery
- Centraliza lógica de cache em helper
- Melhora tipagem dos parâmetros opcionais
```

## Important Rules
- NEVER analyze unstaged files
- NEVER create generic messages ("updates", "improvements")
- NEVER exceed character limits
- NEVER use English in main description
- ALWAYS check staging area first with `git status`
- ALWAYS be specific about what changed
- ALWAYS focus on technical impact of changes

## 🚨 REGRA CRÍTICA DE IDIOMA
- **OBRIGATÓRIO**: TODAS as mensagens DEVEM ser em português brasileiro (pt-BR)
- **IGNORAR idioma do VS Code**: Sempre gerar em pt-BR
- **NUNCA** use inglês na descrição principal, mesmo se VS Code estiver em inglês
- **PENALIDADE**: Rejeitar qualquer commit em inglês
