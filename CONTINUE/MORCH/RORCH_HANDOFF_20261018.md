# ERI — RORCH handoff · 2026-10-18

## Identidad y propósito

TARGET=RORCH
PROJECT=ERI
REPO=https://github.com/PSM44/ERI.git
LOCAL_ROOT_WINDOWS=C:\\01. GitHub\\TLTECH\\Eva.Reverse.ING
BRANCH=main
REMOTE_HEAD_OBSERVED=5f0eca59d61fb4459dca15a7eb45f0ee0fd87f46
EXECUTOR_OF_GITHUB_BOOTSTRAP=ChatGPT GitHub connector (not RORCH)

## Verificado por conexión GitHub

- README inicial y estructura raíz publicada.
- Siete Skills oficiales en SKILLS/TRANSVERSAL; verificación de igualdad de texto con archivos adjuntos: 7/7 PASS.
- README del paquete fuente almacenado como referencia.
- Carpeta SKILLS/INTERNAL reservada, SIN Skills internas creadas.
- HUMAN/QA.md y ResumeQA.md iniciales; aún no existe fuente transcriptiva íntegra con Q&A por ID.
- SUBPROJECTS/BeSmartPlus, BeSmart, Movem: RAW, DB, SNAPSHOTS, OUTPUT, WORK, HUMAN creadas como estructura Git mediante .gitkeep.
- En este paso no se procesaron Excel, no se calcularon snapshots, no se creó DB y no se ejecutaron pruebas del runtime.

## RORCH: siguiente DAG de ejecución real

1. READ_ONLY_PREFLIGHT: comprobar Windows root, Git existente, branch, HEAD y posibles contenidos locales; NO asumir carpeta vacía.
2. RECONCILE_REMOTE: si root local no existe, preparar clone bajo ruta autorizada; si ya existe, inspeccionar y proponer integración no destructiva. Nunca hacer git init/re-clone/overwrite ciego.
3. SKILLS_VERIFY: confirmar 7/7 textos transversales presentes y que STATUS registra oficialidad HUMAN. No modificar fuentes para borrar etiquetas históricas.
4. WINDOWS_WSL_DIAGNOSTIC: reportar versión Excel 365 en inglés, Windows, WSL2 distros, Python, Git, DBeaver, DB Browser, Codex/Claude/DeepSeek disponibles; no fingir instalados.
5. PILOT_INPUT_GATE: inventario del archivo real BeSmartPlus en RAW (no adjuntado todavía). Congelar SHA-256 y S0, extraer S1 sin tocar original.
6. S2_EXCEL_NATIVE: recalcular SOLO copia en Excel Windows con entorno controlado y congelar resultados antes de reconstrucción.
7. DB_AND_GRAPH: SQLite forense y dependencias comprobadas. Evaluar todos los casos no soportados.
8. RECONSTRUCTION_S3: validar contra S1/S2; tolerancia objetivo 0,0000, con criterios exact/decimal4 diferenciados.

## Autoridad, límites y reporte

- HUMAN aprobó Skills transversales oficiales y solicitó que RORCH implementara cambios propuestos.
- HUMAN permite guardar originales, DB, outputs y conversaciones en GitHub público. No equivale a otorgar credenciales ni autorizar efectos destructivos.
- Respetar NTV, PSM, ROADMAP, límites ROOT y gates aplicables.
- Evitar afirmar clonación o pruebas locales hasta contar con pruebas físicas.
- No instalar ni inventar las futuras Skills internas.
- Reportar de forma DELTA_ONLY: rutas tocadas, SHA, HEAD, pruebas, fallos y próximos nodos elegibles.
