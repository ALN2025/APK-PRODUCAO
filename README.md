# TOME Produção

APK do **chão de fábrica** (tablet/celular compartilhado da usinagem) — TOME S/A.

Repositório: [ALN2025/APK-PRODUCAO](https://github.com/ALN2025/APK-PRODUCAO)

APK irmão (líder): [ALN2025/APK-LIDER](https://github.com/ALN2025/APK-LIDER)

---

## Download

Arquivo de instalação:

**[Tome_Producao.apk](./Tome_Producao.apk)**

Pacote: `com.tome.producao`

---

## Para que serve

Substitui o papel no turno:

| Aba | Destino |
|-----|---------|
| **Diário** | Produção / paradas / sucata → **PCP** |
| **R-022** | Cotas críticas do dia → **Qualidade** (planilha diária) |
| **Ordem** | Folha OF (Focco) que fica com o desenho até o fim → **Qualidade** (envio **separado** do R-022) |
| **Legendas** | Consultar significado dos códigos |

Cada documento gera **PDF + Excel** e envia ao líder por Bluetooth / arquivo (**sem WhatsApp** no chão).

---

## Instalação (Android)

1. Desinstale a versão antiga (se houver).
2. Ative **Fontes desconhecidas** / instalar apps desconhecidos.
3. Abra o `Tome_Producao.apk` e instale.
4. Login: **Nome + Setor** → preencha máquina, código da peça e **ordem de usinagem (OF)**.

Arquivos salvos em geral em `Download/Tome` e na pasta do app.

---

## Fluxo resumido

```
Cadastro OF
   ├─ Diário  → PDF/XLS → PCP
   ├─ R-022   → PDF/XLS → Qualidade (dia)
   └─ Folha OF → PDF/XLS → Qualidade (fim da OF — separado)
```

- **Bater ponto** no Diário: salva, abre envio e **fecha o app**.
- Folha OF **não** precisa ir todo dia; acompanha a peça/desenho.

---

## Compilar (desenvolvimento)

```bash
cd tome_producao
flutter pub get
flutter build apk --release --flavor producao --dart-define=FLAVOR=producao
```

Saída: `build/app/outputs/flutter-apk/app-producao-release.apk`

---

## Créditos

TOME S/A · 2026
