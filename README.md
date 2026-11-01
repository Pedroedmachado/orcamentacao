# Funilar Orçamentos

Orçamentos, vistorias e sinistros: dados do carro e do cliente, mapa de avarias, fotos, orçamento (troca, reparo, pintura, R&I, mão de obra por hora ou por peça), catálogo, consulta FIPE, busca no Mercado Livre e PDF.

Faz parte da família **Funilar**: o Funilar completo (repositório `robervall-app`) junta tudo;
este sistema traz só a sua parte e funciona sozinho, com os próprios dados.
Android, iPhone, Windows e Linux (Flutter). Funciona offline; os dados ficam no aparelho.

## Baixar
Cada push na `main` compila no GitHub Actions e publica em **Releases**:
`Orcamentacao-android.apk`, `Orcamentacao-windows-x64.zip`, `Orcamentacao-linux-x64.tar.gz`
(iPhone: `[ios]` na mensagem do commit gera `Orcamentacao-ios-sem-assinatura.ipa`).

No Windows, para instalar ou atualizar pelo PowerShell:
```powershell
irm https://raw.githubusercontent.com/Pedroedmachado/orcamentacao/main/tool/atualizar-orcamentacao.ps1 | iex
```
Dentro do app: **Ajustes › Atualizações**.

## Backup entre os sistemas
O backup (.zip) de qualquer sistema Funilar pode ser restaurado em outro —
por exemplo, levar os cadastros para o Funilar completo.

## Compilar na sua máquina
```bash
bash tool/prepare_platforms.sh   # gera android/, ios/, linux/, windows/
flutter pub get
flutter test
flutter run
```

## Código
Este repositório é gerado a partir do Funilar completo
(`bash tool/gerar_modulos.sh orcamentacao <pasta>` no `robervall-app`), por isso as correções
feitas lá chegam aqui na próxima geração.
