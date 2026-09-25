# 💊 Análisis Lean 3MU · Arredondo Soluciones

> 📦 Proyecto de mejora Lean para la logística e inventario de medicamentos: pasar de **comprar por intuición** a **comprar por consumo** con un sistema pull nivelado.

![Estado](https://img.shields.io/badge/estado-en%20progreso-yellow) ![Metodología](https://img.shields.io/badge/metodología-Lean%20%7C%20PDCA-blue) ![Tablero](https://img.shields.io/badge/tablero-Kanban-green)

---

## 📖 Descripción

Este repositorio documenta el análisis Lean de la operación de compras y almacén de **Arredondo Soluciones**, una distribuidora de medicamentos. Con datos de **800 órdenes de compra** y **1,500 pedidos de venta** (1-ene a 31-jul-2026), identificamos los desperdicios con el enfoque **3MU (Muda, Mura, Muri)** y proponemos un plan de implementación por fases.

## 🚨 El problema en números

| 📊 Indicador | Valor |
|---|---|
| 🛒 Lo comprado que realmente se vendió | **55%** (meta ≥ 95%) |
| 📦 Inventario excedente | **400,925 unidades ≈ $11.9 M MXN** |
| ⏳ Semanas de venta cubiertas por el exceso | **≈ 25 semanas** (sano: 2–4) |
| 💸 Flujo neto del periodo | **−$5.36 M MXN** |
| 🏷️ Sobrecosto por no comprar al mejor proveedor | **$335,337 MXN** |
| 🌊 Efecto látigo semanal (varianza compras ÷ ventas) | **5.3×** |
| 🔗 Correlación semanal compras–ventas | **0.19** |
| 🚚 Día pico de recepción vs promedio | **3.2×** |

## 🔍 Diagnóstico 3MU

- 🌀 **MURA (causa raíz):** las compras no siguen al consumo real. Se compra en lotes grandes, a tres proveedores y en fechas irregulares.
- 🏋️ **MURI (consecuencia operativa):** picos de recepción de hasta 3 veces la carga normal y un almacén que crece cada semana.
- 🗑️ **MUDA (consecuencia económica):** sobrecompra, inventario excedente, riesgo de caducidad y flujo de caja negativo.

> 💡 **Conclusión:** rematar el inventario no basta. Hay que eliminar la Mura con un **sistema pull nivelado** para que la Muri y la Muda no se repitan.

## 🛠️ Herramientas Lean propuestas

| Tipo | Herramienta | Ataca |
|---|---|---|
| 🧰 Física | Kanban de dos contenedores (two-bin) por medicamento | Muda · Mura |
| 🧰 Física | Racks FEFO + etiquetas de caducidad por color 🟢🟡🔴 | Muda |
| 🧰 Física | 5S y control visual (máximos y mínimos en rack) | Muri · Muda |
| 🧰 Física | Tablero Heijunka de compras y ventanas de recepción | Mura · Muri |
| 💻 Software | ERP/WMS con reglas mín./máx. y lotes (p. ej. Odoo) | Muda · Mura |
| 💻 Software | Tablero de indicadores (Power BI / Excel) | Las tres |

## 🗂️ Tableros Kanban

Este proyecto usa **GitHub Projects** con dos vistas, separadas por etiqueta:

### 🏗️ 1. Implementación (`implementacion`)
Cada tarjeta es una acción del plan de mejora.

`📥 Backlog` → `📝 Por hacer` → `🔨 En progreso (WIP 3)` → `🔎 En validación` → `✅ Hecho`

### 🔄 2. Reabastecimiento (`reabasto`)
Cada tarjeta es un medicamento y simula el sistema pull.

`⛔ Sobre el máximo` → `🟢 Entre ROP y máximo` → `🔔 Punto de reorden` → `📨 Pedido colocado` → `🚚 En tránsito` → `🏬 Recibido FEFO`

## 🏁 Milestones (plan PDCA)

| Milestone | Semanas | Entregable |
|---|---|---|
| 🧯 Fase 0 · Contener | 1–2 | Inventario real validado y lista de producto en riesgo |
| 🧹 Fase 1 · Estabilizar | 2–6 | Almacén con 5S, FEFO y control visual |
| 🔄 Fase 2 · Jalar (pull) | 4–10 | Kanban operando en los 8 medicamentos |
| ⚖️ Fase 3 · Nivelar | 8–14 | Calendario Heijunka y acuerdos con proveedores |
| 📈 Fase 4 · Controlar | Continuo | Tablero de KPIs y registro de Kaizen |

## 🎯 Indicadores de control

| KPI | 3MU | Línea base | Meta |
|---|---|---|---|
| % de lo comprado que se vendió | Muda | 55% | 95% |
| Semanas de cobertura de inventario | Muda | 24.7 | 3.0 |
| Efecto látigo semanal | Mura | 5.3 | 1.5 |
| Correlación semanal compras–ventas | Mura | 0.19 | 0.70 |
| Recepción diaria pico ÷ promedio | Muri | 3.2 | 1.5 |
| Proveedores activos por medicamento | Muri | 3 | 2 |

## 📁 Estructura del repositorio

```
📂 /
├── 📄 README.md
├── 📊 Analisis_Lean_3MU_Inventario.xlsx   ← análisis completo (Resumen, Muda, Mura, Muri, Kanban)
├── 📂 docs/                               ← reportes, presentaciones y minutas
└── 📂 evidencias/                         ← fotos antes/después, conteos, 5S
```

## 🤝 Cómo colaborar

1. 🎫 Cada tarea es un **issue** con su etiqueta de 3MU: `muda` 🗑️ `mura` 🌀 `muri` 🏋️
2. 🏁 Asigna el issue al **milestone** de su fase.
3. 👤 Indica **responsable** y **fecha límite** en el proyecto.
4. ✅ Al cerrar un issue, comenta el valor del KPI **antes y después**.
5. 🗓️ Revisamos el tablero en la **junta semanal de 15 minutos**.

## 👥 Equipo

| Integrante | Rol |
|---|---|
| _Nombre_ | _Rol_ |
| _Nombre_ | _Rol_ |

## 📚 Referencias

- 📘 Lean Enterprise Institute · *Lean Lexicon* (Heijunka, Kanban, EPEI)
- 📗 Art Smalley · *Creating Level Pull*
- 📙 Rother & Shook · *Observar para crear valor*
- 🌐 Kanban Tool · *¿Qué es Heijunka?*

---

⭐ _Proyecto académico de Análisis Lean · 2026_
