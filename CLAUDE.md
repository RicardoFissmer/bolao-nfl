# Bolão NFL

App de bolão da NFL em Flutter (web + Android). É um trabalho acadêmico: o objetivo
principal é **aplicar na prática um Plano de Gerenciamento de Configuração (GCS) com
DevOps**, baseado no documento `Plano_GCS_DevOps_ONGConectaR.pdf` (o "ONGConecta" do
PDF é fictício; o bolão é o projeto real onde o plano é aplicado).

O autor (Ricardo) está aprendendo. Ao trabalhar aqui, **explique cada passo em
português**, ligando a decisão à seção do plano quando fizer sentido.

## Stack e decisões

- **Flutter** (versão fixada em `3.47.2` no CI, igual à máquina local). Plataformas: `web` e `android`.
- **Backend previsto:** Supabase (ainda não integrado).
- **Web:** publicação prevista no GitHub Pages. **Mobile:** APK/Android.
- **Repositório:** github.com/RicardoFissmer/bolao-nfl (público, para usar recursos gratuitos).
- Orçamento zero: só ferramentas gratuitas (GitHub Actions, Dependabot etc.).

## Fluxo de trabalho (GitHub Flow, seção 3.3 do plano)

- `main` sempre pronta para produção. Mudanças entram por branch curta + Pull Request.
- Branches: `feature/<issue>-descricao`, `fix/...`, `hotfix/...`, `release/x.y` (opcional).
- Commits no padrão **Conventional Commits**: `feat:`, `fix:`, `chore:`, `ci:`, `docs:`, `test:`.
  Esses prefixos serão usados depois para gerar versão SemVer e release notes automaticamente.
- O merge na `main` só deve acontecer com o CI verde.

## Comandos

```bash
flutter pub get
flutter analyze
dart format --output=none --set-exit-if-changed .
flutter test
flutter run -d chrome
flutter build web
```

O CI (`.github/workflows/ci.yml`) roda exatamente essas checagens. Se passam localmente,
devem passar no GitHub.

## Etapas

1. ✅ Projeto Flutter criado e enviado ao GitHub.
2. ⏳ CI com GitHub Actions + Dependabot + proteção da `main`.
3. CD: deploy automático da web (staging) e build do APK.
4. Releases: tag SemVer automática e release notes a partir dos commits.
5. Funcionalidades do bolão (times, jogos, palpites, ranking).
