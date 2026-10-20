# Bolão NFL

[![CI](https://github.com/RicardoFissmer/bolao-nfl/actions/workflows/ci.yml/badge.svg)](https://github.com/RicardoFissmer/bolao-nfl/actions/workflows/ci.yml)

App de bolão da NFL feito em Flutter, para web e Android.

O projeto também serve para aplicar na prática um **Plano de Gerenciamento de
Configuração (GCS) com DevOps**: versionamento com GitHub Flow, integração contínua,
entrega contínua e releases versionadas.

## Como rodar

Pré-requisito: [Flutter](https://docs.flutter.dev/get-started/install) 3.47.2.

```bash
flutter pub get
flutter run -d chrome
```

## Como contribuir

1. Crie uma branch a partir da `main`: `feature/<descricao>` ou `fix/<descricao>`.
2. Faça commits no padrão [Conventional Commits](https://www.conventionalcommits.org/pt-br/):
   `feat: ...`, `fix: ...`, `docs: ...`, `chore: ...`, `ci: ...`.
3. Antes de enviar, rode as mesmas checagens do CI:

   ```bash
   dart format .
   flutter analyze
   flutter test
   ```

4. Abra um Pull Request para a `main`. O título do PR também segue o Conventional
   Commits, porque vira a mensagem do commit no merge (squash).
5. O merge só é liberado com o CI verde.

A `main` é protegida: não aceita push direto nem force push.
