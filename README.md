<div align="center">

<img src="aln.png" alt="Dev A.L.N" height="72"/>

# TOME Produção

### Diário · R-022 · Folha OF — chão de fábrica  
**TOME S/A · Usinagem**

[![APK](https://img.shields.io/badge/Download-Tome__Producao.apk-00C853?style=for-the-badge&logo=android&logoColor=white)](./Tome_Producao.apk)
[![Líder](https://img.shields.io/badge/Irmão-APK--LIDER-2979FF?style=for-the-badge&logo=github)](https://github.com/ALN2025/APK-LIDER)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)

`com.tome.producao` · offline · tablet da usinagem

</div>

---

## O que este APK faz

App do **operador**. Lança produção no turno e **envia arquivos ao líder**.  
**Não envia ao PCP** — isso é só no [APK Líder](https://github.com/ALN2025/APK-LIDER).

| Aba | Durante o dia | No fim |
|-----|---------------|--------|
| **R-022** | Mede peça a peça | XLS + PDF → **líder** |
| **Legendas** | Paradas De/Até (refeição, limpeza…) | Entram no Diário |
| **Diário** | — | Qtd **exata** boas + sucata → **líder** |
| **Ordem** | Folha OF no celular | Salva / envia ao **líder** quando quiser |

---

## Fluxo completo

```mermaid
flowchart TB
  subgraph chao [APK Produção — você está aqui]
    A[Login + hora início]
    B[OF + ID: TAMBOR 534]
    C[Usinar]
    D[R-022 medir]
    E[Legendas parada]
    F[Diário qtd exata]
    G[Folha OF no celular]
    H[Bater ponto]
    A --> B --> C
    C --> D
    C --> E
    D --> F
    E --> F
    C --> G
    F --> H
  end

  subgraph lider [APK Líder]
    I[Importa XLS/PDF]
    J[Enviar PCP]
    K[Enviar Qualidade]
  end

  F -->|Bluetooth / arquivo| I
  D -->|Bluetooth / arquivo| I
  G -.->|quando salvar| I
  I --> J
  I --> K
  J --> PCP[PCP]
  K --> QUAL[Qualidade]
```

```
 OPERADOR                         LÍDER
 ────────                         ─────
 salva Diário  ──────XLS/PDF───►  importar ──► Enviar PCP ──────► PCP
 salva R-022   ──────XLS/PDF───►  importar ──► Enviar Qualidade ► Qualidade
 Folha OF      ──────XLS/PDF───►  (opcional) ─► Qualidade
 Bater ponto   → limpa Diário+R-022 | Folha OF PERMANECE
```

---

## Bater ponto

- Apaga **Diário** e **R-022** do turno  
- **Folha OF permanece** no celular (mesma OF)  
- Fecha o app  

---

## Download

### [`Tome_Producao.apk`](./Tome_Producao.apk)

1. Desinstale a versão antiga  
2. Instale o APK  
3. Nome + Setor → máquina + **ID da peça** + ordem de usinagem  

---

## Stack

| | |
|---|---|
| UI | Flutter / Dart 3 · Material |
| Banco | SQLite (`sqflite`) |
| Excel | `excel` (.xlsx) |
| PDF | `pdf` + Noto Sans |
| Envio | `share_plus` · Bluetooth / arquivo |
| Flavor | `producao` |

---

<div align="center">

<br/>

<img src="aln.png" alt="Dev A.L.N" height="56"/>

### Desenvolvido por **Dev A.L.N**

[github.com/ALN2025](https://github.com/ALN2025) · TOME S/A · 2026

</div>
