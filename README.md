<div align="center">

<img src="aln.png" alt="Dev A.L.N" height="72"/>

# TOME Produção

### Diário · R-022 · Folha OF — chão de fábrica  
**TOME S/A · Usinagem**

[![APK](https://img.shields.io/badge/Download-Tome__Producao.apk-00C853?style=for-the-badge&logo=android&logoColor=white)](./Tome_Producao.apk)
[![Líder](https://img.shields.io/badge/Irmão-APK--LIDER-2979FF?style=for-the-badge&logo=github)](https://github.com/ALN2025/APK-LIDER)

`com.tome.producao` · offline · tablet da usinagem

</div>

---

<br/>

# 🔀 FLUXO — SÓ O LÍDER ENVIA AO PCP

> **Operador** manda Diário e R-022 ao **Líder** (pode a qualquer hora).  
> **Ninguém do chão envia direto ao PCP** — isso é só no APK Líder.

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
    "tertiaryColor": "#B71C1C",
    "fontSize": "16px"
  }
}}%%
flowchart LR
  OP[👷 Operador<br/>APK Produção] -->|"Diário + R-022<br/>XLS/PDF"| LID[📱 Líder]
  LID -->|"🟢 Enviar PCP<br/>SÓ O LÍDER"| PCP[(🏭 PCP)]
  LID -->|"🔵 Qualidade"| Q[(✅ Qualidade)]
  OP -.->|"❌ NÃO"| PCP
```

<br/>

```mermaid
%%{init: {
  "theme": "dark",
  "themeVariables": {
    "primaryColor": "#0D47A1",
    "primaryTextColor": "#fff",
    "primaryBorderColor": "#4FC3F7",
    "lineColor": "#4FC3F7",
    "fontSize": "15px"
  }
}}%%
flowchart TB
  subgraph PRODUCAO["📱 APK PRODUÇÃO"]
    U[Usinar] --> R[R-022 → envia ao Líder]
    U --> D[Diário → envia ao Líder]
    U --> F[Folha OF]
  end
  subgraph LIDER["📱 APK LÍDER"]
    I[Importar] --> PCP_BTN[🟢 Enviar PCP — SÓ O LÍDER]
    I --> QUAL[🔵 Enviar Qualidade]
  end
  R --> I
  D --> I
  F -.-> I
  PCP_BTN ==> PCP[(🏭 PCP)]
  QUAL ==> QUALIDADE[(✅ Qualidade)]
```

<br/>

| Quem | Pode fazer | Destino |
|------|------------|---------|
| **Operador** | Enviar Diário + R-022 | → **Líder** |
| **Operador** | ❌ Enviar ao PCP | — |
| **Líder** | **Enviar PCP** | → **PCP** |
| **Líder** | Enviar Qualidade | → **Qualidade** |

---

## Turno

1. Login + OF + ID tambor  
2. **R-022** peça a peça → envie ao Líder quando quiser  
3. **Legendas** se parar  
4. Fim → **Diário** → Líder  
5. **Bater ponto** limpa Diário+R-022 · OF fica  

---

### [`Tome_Producao.apk`](./Tome_Producao.apk)

<div align="center">
<img src="aln.png" alt="Dev A.L.N" height="56"/>
### Desenvolvido por **Dev A.L.N** · TOME S/A · 2026
</div>
