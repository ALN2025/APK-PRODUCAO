# TOME Produção

**Sistema offline de Diário de Bordo, R-022 e Folha de Ordem de Fabricação**  
TOME S/A — Usinagem

[![Android](https://img.shields.io/badge/Android-APK-3DDC84?logo=android&logoColor=white)](./Tome_Producao.apk)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?logo=flutter&logoColor=white)](https://flutter.dev)

| | |
|---|---|
| **APK** | [`Tome_Producao.apk`](./Tome_Producao.apk) |
| **Pacote** | `com.tome.producao` |
| **Irmão** | [APK-LIDER](https://github.com/ALN2025/APK-LIDER) |

---

## Fluxo (importante)

```
Operador (este APK)
   └─ salva XLS/PDF e envia ao LÍDER
         │
         ▼
APK Líder
   ├─ Diário importado  → gera e ENVIA ao PCP
   └─ R-022 / Folha OF  → gera e ENVIA à Qualidade
```

**Só o APK Líder envia ao PCP.** O operador nunca manda direto.

---

## Turno no chão

1. Entra → hora + OF + **ID: TAMBOR 534**  
2. Usina → R-022 peça a peça  
3. Paradas → Legendas (De/Até)  
4. Fim → Diário qtd exata → XLS/PDF **ao líder**  
5. Folha OF → salva no celular / envia ao líder quando quiser  
6. Bater ponto → limpa Diário+R-022; **Folha OF permanece**

---

## Stack

Flutter · SQLite · excel · pdf · share_plus · flavor `producao`

---

## Assinatura

<p align="center"><img src="aln.png" alt="Dev A.L.N" height="48"/></p>
<p align="center"><b>Dev A.L.N</b> · TOME S/A · 2026</p>
