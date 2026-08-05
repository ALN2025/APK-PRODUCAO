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

<br/>

# 🔀 FLUXOGRAMA DO SISTEMA

> **Operador envia Diário e R-022 ao LÍDER (pode a qualquer hora).**  
> **Só o Líder envia ao PCP.**

<br/>

```mermaid
%%{init: {
  "theme": "dark",
  "themeVariables": {
    "primaryColor": "#0D47A1",
    "primaryTextColor": "#fff",
    "primaryBorderColor": "#4FC3F7",
    "lineColor": "#4FC3F7",
    "secondaryColor": "#1B5E20",
    "tertiaryColor": "#E65100",
    "fontSize": "16px"
  }
}}%%
flowchart TB
  subgraph PRODUCAO["📱 APK PRODUÇÃO — chão de fábrica"]
    direction TB
    L[👤 Login + hora início]
    OF[📋 OF + ID: TAMBOR nº peça]
    U[⚙️ Usinar]
    R[📐 R-022 — medir e enviar ao Líder]
    P[⏸️ Legendas — parada De / Até]
    D[📓 Diário — qtd boas + sucata]
    F[📄 Folha OF — fica no celular]
    BP[🚪 Bater ponto]
    L --> OF --> U
    U --> R
    U --> P
    U --> F
    R --> D
    P --> D
    D --> BP
  end

  subgraph LIDER["📱 APK LÍDER"]
    direction TB
    I[📥 Importar XLS / PDF]
    PCP_BTN[🟢 Enviar PCP — SÓ O LÍDER]
    QUAL_BTN[🔵 Enviar Qualidade]
    I --> PCP_BTN
    I --> QUAL_BTN
  end

  D -->|"XLS + PDF"| I
  R -->|"XLS + PDF — ok enviar"| I
  F -.->|"quando salvar"| I
  PCP_BTN ==> PCP[(🏭 PCP)]
  QUAL_BTN ==> QUAL[(✅ Qualidade)]
```

<br/>

| Quem | Faz | Destino |
|------|-----|---------|
| **Produção** | Diário + **R-022** (ok) | → **Líder** |
| **Líder** | **Enviar PCP** | → **PCP** (só o líder) |
| **Líder** | Enviar Qualidade | → **Qualidade** |

---

## Turno no tablet

1. Entra → hora + **ID: TAMBOR 534** + OF  
2. Usina → **R-022** a cada peça → **pode enviar ao Líder**  
3. Parou → **Legendas**: De agora, Até depois  
4. Fim → **Diário** qtd exata → envia ao líder  
5. **Folha OF** fica no celular  
6. **Bater ponto** limpa Diário+R-022 · OF permanece  

---

## Download

### [`Tome_Producao.apk`](./Tome_Producao.apk)

---

<div align="center">

<img src="aln.png" alt="Dev A.L.N" height="56"/>

### Desenvolvido por **Dev A.L.N**

[github.com/ALN2025](https://github.com/ALN2025) · TOME S/A · 2026

</div>
