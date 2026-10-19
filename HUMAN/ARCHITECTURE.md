# ERI — Arquitectura y límites

**Estado:** diseño inicial, no implementación del motor.

```mermaid
flowchart LR
 A[RAW Excel S0] --> B[Captura S1 OOXML]
 A --> C[Recálculo copia S2 Excel]
 B --> D[DB forense]
 C --> D
 D --> E[Grafo de fórmulas]
 E --> F[Interpretación semántica]
 F --> G[Motor ERI]
 G --> H[Salida S3]
 C --> I{Comparación}
 H --> I
 I --> J[Evidencia / diferencias]
```

El oráculo Excel nativo opera en Windows; extracción y modelado pueden operar en Windows o WSL2. No confundir `openpyxl` con evaluador de fórmulas. Las Skills transversales norman conducta, las internas todavía están por crear.
