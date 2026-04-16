# SAFEGUARD INDUSTRIAL
## Plataforma de Inteligencia de Riesgo Industrial
### PLAN DE NEGOCIOS — Versión 2.1 | Abril 2026

> **La tesis en una línea:** SafeGuard es la primera capa de datos de cumplimiento industrial de Argentina. Quien construya ese dataset primero, lo posee para siempre.

---

## 1. RESUMEN EJECUTIVO

SafeGuard Industrial es una plataforma B2B que digitaliza, certifica y monetiza el cumplimiento normativo de instalaciones industriales (PCI + gas natural) en Argentina.

El modelo tiene **tres vectores de valor** que se refuerzan entre sí:

| Vector | Canal | Producto | Revenue |
|---|---|---|---|
| **Riesgo** | Aseguradoras | SaaS de gestión + dashboard | USD 3-5/póliza/mes |
| **Compliance** | Empresas | Certificación + IoT opcional | USD 200-800/año + hardware |
| **Data** | Reaseguradoras | Informes de riesgo industrial LATAM | USD 30-150K/contrato |

**El insight que cambia todo:** Las aseguradoras hoy tarифican riesgos industriales con datos insuficientes — prima estándar para todos. Con SafeGuard, obtienen historial de cumplimiento verificable por empresa y pueden diferenciar tarifas: menor prima para quien demuestra bajo riesgo, mayor para quien no. SafeGuard crea demanda desde arriba (la aseguradora diferencia su producto) y desde abajo (la empresa quiere calificar para mejor tarifa), simultáneamente.

### Proyección Financiera

| Métrica | Año 1 | Año 2 | Año 3 | Año 4 |
|---|---|---|---|---|
| Aseguradoras activas | 2 | 5 | 9 | 16 |
| Pólizas en plataforma | 6.000 | 22.000 | 55.000 | 130.000 |
| Revenue total (base) | USD 420K | USD 1.35M | USD 3.4M | USD 8.1M |
| Revenue total (conservador) | USD 280K | USD 720K | USD 1.8M | USD 4.2M |
| Margen bruto | 76% | 79% | 82% | 83% |

*Ver Sección 4.3 para detalle de escenarios.*

---

## 2. EL PROBLEMA

### 2.1 El Laberinto Normativo (Empresas)

Las PyMEs industriales argentinas operan bajo un sistema de normas fragmentado e inaccesible: NAG-200/201 para gas natural, IRAM 3501-3546 para PCI, NFPA adaptadas. El 70%+ tiene algún grado de incumplimiento **sin saberlo** — no por negligencia, sino porque la complejidad supera su capacidad operativa.

Las consecuencias son tres:
- No pueden demostrar cumplimiento cuando lo necesitan (siniestro, auditoría, habilitación)
- Sus sistemas se degradan silenciosamente sin alertas
- Pagan la prima estándar de su rubro porque no tienen forma de acreditar que son un riesgo mejor que el promedio

### 2.2 El Ciclo de Dolor (Aseguradoras)

Las aseguradoras industriales suscriben riesgos a ciegas y pagan las consecuencias:

```
Suscripción → Inspección puntual (foto del momento, USD 200-500)
     ↓
Vigencia → CERO visibilidad del estado real del riesgo
     ↓
Siniestro → El perito descubre incumplimientos que existían desde el día 1
     ↓
Dilema: Pagar (pérdida evitable) o Rechazar (Art. 56 Ley 17.418 = juicio)
```

**Art. 56 Ley 17.418:** La aseguradora tiene 30 días para pronunciarse ante un siniestro. Si no responde: aceptación tácita. Resultado: juicio + costas + daño reputacional.

Sin evidencia digital, ni pagar ni rechazar es gratis.

| KPI | Situación Actual | Con SafeGuard |
|---|---|---|
| Loss Ratio industrial | 60-70% | Objetivo: reducir 3-8 puntos |
| Inspección pre-suscripción | USD 200-500, puntual | Monitoreo continuo incluido |
| Evidencia ante rechazo | Declaración jurada | Registro inmutable con firma técnica |
| Tarificación | Prima estándar por rubro | Diferenciada por riesgo real |
| Diferenciación comercial | Póliza commodity | "Póliza con certificación SafeGuard" |

### 2.3 El Problema Ignorado (Reaseguradoras)

Munich Re, Swiss Re, SCOR y Hannover Re definen los precios del mercado asegurador industrial en toda Latinoamérica. Lo hacen con modelos que no incluyen data de cumplimiento normativo local — porque esa data no existe.

Consecuencia: sobrestiman el riesgo en mercados emergentes, cobran primas más altas de lo necesario, y pierden oportunidad de crecer en segmentos donde el riesgo real es mejor de lo que sus modelos predicen.

**SafeGuard puede construir el primer dataset estructurado de riesgo industrial argentino y vendérselo.**

---

## 3. LA SOLUCIÓN

### 3.1 MVP — Lo que se construye primero

Antes de hablar de la plataforma completa, hay que definir qué se construye en las **primeras 6 semanas** para poder ejecutar el primer piloto. Todo lo demás viene después.

**MVP (Semanas 1-6):**

| Componente | Descripción | Tecnología |
|---|---|---|
| App mobile de inspección | Checklist offline-first para NAG-200, IRAM 3543 y extintores. Firma digital del técnico, foto geotaggeada | React Native o Flutter |
| Dashboard web básico | Vista de cartera para la aseguradora: estado por empresa (verde/amarillo/rojo), alertas activas | React / .NET backend |
| PDF de certificado | Generación automática de certificado de cumplimiento con timestamp y firma | PDFsharp o equivalente |
| Motor normativo (v1) | Las 3 normas más comunes codificadas como reglas. Sin IoT, sin marketplace | Reglas configurables en backend |

**Lo que NO es el MVP:** IoT, marketplace de instaladores, integración con sistemas core de la aseguradora, data products para reaseguradoras, scoring predictivo. Todo eso es Fase 2 en adelante.

### 3.2 Dos Tracks de Producto (Fase 2+)

**Track A — SaaS (Despliegue rápido, sin hardware)**
La aseguradora paga. Las empresas adoptan digitalmente. Cero fricción de instalación.

- Inventario digital de activos PCI y redes de gas
- Checklist de inspección mobile (offline-first)
- Motor normativo configurable (NAG/IRAM/NFPA como reglas versionadas)
- Certificado de cumplimiento con timestamp
- Dashboard de cartera para la aseguradora

**Track B — SaaS + IoT (Despliegue profundo, con sensores)**
Agrega monitoreo continuo real, habilitando tarificación diferenciada automatizada.

| Sensor | Norma | Evento detectado | Costo estimado |
|---|---|---|---|
| Presión en red PCI | IRAM 3543 | Caída de presión = sistema inoperativo | USD 80-120 |
| Detector de gas (metano) | NAG-200 | Fuga activa | USD 60-100 |
| QR/NFC en extintores | IRAM 3517 | Vencimiento, falta de revisión | USD 5-15/unidad |
| Temperatura en tableros | IRAM | Sobrecarga térmica | USD 40-80 |

Costo típico de instalación completa: USD 400-800 por empresa.

**¿Cuándo ofrecer Track B?** En empresas con prima > USD 3.000/año, o cuando la aseguradora quiere activar tarificación diferenciada con base en datos de sensores.

### 3.3 El Motor Normativo: el IP Central

El corazón técnico de SafeGuard es un **motor de reglas configurable**:

- Cada norma (NAG-200, IRAM 3501, NFPA 13) se modela como reglas **versionadas**
- Las reglas se actualizan cuando cambia la normativa — sin reescribir la app
- Nuevas jurisdicciones (Chile, Colombia) = nuevo **módulo normativo**, no nuevo producto
- Cada empresa se evalúa contra el conjunto de normas aplicable a su actividad

**Por qué importa:** Convierte el conocimiento de Adrián en **IP de la empresa**, no en dependencia personal. Extensible, licenciable, auditable.

### 3.4 El Sello SafeGuard: el Activo de Marca

Certificación visible de cumplimiento activo. Las empresas con estatus activo reciben:

- Badge digital verificable (QR con historial)
- Listado en directorio público SafeGuard
- Elegibilidad para tarificación diferenciada de aseguradoras partner

Si el Sello se instala como estándar de mercado, la demanda se vuelve pull — las empresas lo piden a sus aseguradoras para calificar para mejores tarifas.

---

## 4. MODELO DE NEGOCIO

### 4.1 El Mecanismo Central: Tarificación Diferenciada por Riesgo Real

El modelo no se basa en un "descuento automático desde el día 1" — ese mecanismo requiere historial actuarial y en Argentina está regulado por la SSN. El mecanismo real, y más sostenible, es la **tarificación diferenciada basada en riesgo real**:

```
Empresa usa SafeGuard → 12 meses de historial de cumplimiento verificable
→ La aseguradora puede demostrar ante la SSN que ese riesgo es menor al promedio
→ Tarificación diferenciada: menor prima para quienes cumplen, mayor para quienes no
→ La empresa tiene incentivo activo para mantener el cumplimiento y calificar
→ La aseguradora diferencia su producto: "Póliza con tarificación inteligente SafeGuard"
```

**Los números para la empresa (a partir del segundo año):**

| Concepto | Valor |
|---|---|
| Prima industrial promedio | USD 5.000/año |
| Reducción por tarificación diferenciada (estimado conservador: 8%) | USD 400/año |
| Costo Track A (SaaS, absorbido por aseguradora) | USD 0 directo |
| Costo Track B (sensores + instalación, amortizado Año 2+) | USD 200/año |
| **Beneficio neto para la empresa (Año 2+)** | **USD 200-400** |

**Por qué esto es más robusto que un "descuento del 15%":** La tarificación diferenciada tiene base actuarial (se apoya en el historial de SafeGuard), es regulatoriamente válida, y se fortalece con el tiempo a medida que se acumula data. No es una promesa de marketing — es un mecanismo que se construye junto con la aseguradora.

### 4.2 Cinco Fuentes de Ingreso

| Fuente | Canal | Modelo | Precio |
|---|---|---|---|
| **Setup Fee** | Aseguradora | Por implementación e integración (ver lógica abajo) | USD 30-90K |
| **Recurrente SaaS** | Aseguradora | Por póliza activa en plataforma, mensual | USD 3-5/póliza/mes |
| **Hardware** | Empresa (vía instaladores) | Venta o leasing de sensores | USD 400-800 CapEx o USD 30-50/mes |
| **Certificaciones** | Empresa directa | Sello SafeGuard anual verificable | USD 200-600/año |
| **Data Products** | Reaseguradoras | Informes de riesgo, API de scoring | USD 30-150K/contrato |

**Lógica de pricing del Setup Fee:**

| Tamaño de la aseguradora | Pólizas industriales | Setup Fee |
|---|---|---|
| Pequeña | < 2.000 | USD 30-40K |
| Mediana | 2.000-8.000 | USD 50-65K |
| Grande | 8.000+ | USD 70-90K |

El Setup Fee cubre: integración con sistemas core (pólizas, siniestros), configuración del motor normativo para los ramos de la aseguradora, onboarding del equipo, y soporte durante los primeros 60 días.

**Mecanismo de pricing en moneda local:**
Los contratos con aseguradoras argentinas se firman en **pesos ajustados por CVS (Coeficiente de Variación Salarial) con revisión semestral**, con referencia al equivalente en USD al tipo de cambio oficial. Esto protege el revenue real de SafeGuard ante la inflación sin requerir que la aseguradora pague en divisas.

### 4.3 Proyecciones Financieras — Dos Escenarios

**Escenario Base** (2 aseguradoras en Año 1, crecimiento sostenido, IoT desde Año 2):

| Fuente | Año 1 | Año 2 | Año 3 | Año 4 |
|---|---|---|---|---|
| Setup Fees | USD 120K | USD 150K | USD 200K | USD 260K |
| Recurrente SaaS | USD 252K | USD 924K | USD 2.31M | USD 5.46M |
| Hardware (venta/leasing) | USD 30K | USD 150K | USD 500K | USD 1.1M |
| Certificaciones directas | USD 18K | USD 60K | USD 200K | USD 450K |
| Data Products (reaseguradoras) | — | USD 65K | USD 190K | USD 830K |
| **REVENUE TOTAL** | **USD 420K** | **USD 1.35M** | **USD 3.4M** | **USD 8.1M** |
| Margen Bruto | 76% | 79% | 82% | 83% |

**Escenario Conservador** (ciclo de ventas más lento, 1 aseguradora efectiva Año 1, sin IoT hasta Año 3):

| Fuente | Año 1 | Año 2 | Año 3 | Año 4 |
|---|---|---|---|---|
| Setup Fees | USD 60K | USD 80K | USD 120K | USD 180K |
| Recurrente SaaS | USD 180K | USD 500K | USD 1.2M | USD 2.8M |
| Hardware + Certificaciones | USD 10K | USD 60K | USD 250K | USD 700K |
| Data Products | — | — | USD 130K | USD 520K |
| **REVENUE TOTAL** | **USD 280K** | **USD 640K** | **USD 1.7M** | **USD 4.2M** |
| Margen Bruto | 72% | 76% | 80% | 82% |

*Supuesto IoT escenario base: Track B en 15% de instalaciones Año 2, 25% Año 3, 35% Año 4.*

### 4.4 Unit Economics

**LTV por aseguradora (Año 3+, cartera de 5.000 pólizas):**

| Componente | Año 1 | Año 2+ (anual) |
|---|---|---|
| Setup Fee | USD 57K (promedio) | — |
| Recurrente (USD 3.8 × 5.000 × 12) | USD 228K | USD 228K |
| Certificaciones + Hardware indirecto | USD 30K | USD 60K |
| **Total por aseguradora** | **USD 315K** | **USD 288K** |
| **LTV a 5 años** | | **~USD 1.5M** |

**CAC por aseguradora:**
- Ciclo de ventas: 4-7 meses, 2 personas
- Esfuerzo estimado: USD 15-25K
- **LTV/CAC: ~65x**

---

## 5. ANÁLISIS DE MERCADO

### 5.1 TAM / SAM / SOM

**TAM — Canal Aseguradoras Argentina**
- 124 aseguradoras patrimoniales/mixtas (SSN, 2024)
- Estimado: ~300.000 pólizas industriales activas en Argentina
- Precio objetivo: USD 4/póliza/mes
- **TAM: ~USD 14.4M ARR**

**TAM — Canal Reaseguradoras LATAM**
- 5 grandes reaseguradoras con cartera regional (Munich Re, Swiss Re, SCOR, Hannover Re, Gen Re)
- Producto de data: USD 50-150K/año por reaseguradora
- **TAM: ~USD 250K-750K ARR** — pequeño en volumen, pero estratégico: una reaseguradora puede condicionar el uso de SafeGuard a sus cedantes en múltiples países

**SAM — Lo accesible con el modelo actual en 5 años**
- 30 aseguradoras industriales medianas-grandes en Argentina
- ~120.000 pólizas en ese segmento
- **SAM: ~USD 5.8M ARR**

**SOM — Lo capturable en 3 años**
- 9 aseguradoras activas, ~55.000 pólizas
- **SOM Año 3: ~USD 2.7M ARR** (solo recurrente, conservador)

### 5.2 Catalizadores del Mercado

| Catalizador | Impacto en SafeGuard |
|---|---|
| Inflación de siniestralidad (materiales, mano de obra) | Cada siniestro evitado vale más → mayor ROI del producto |
| Litigiosidad creciente (Art. 56 Ley 17.418) | El costo del rechazo sin evidencia aumenta |
| Presión de reaseguradoras sobre loss ratio | Aseguradoras buscan herramientas para mejorar selección |
| Digitalización del sector seguros post-2020 | Mayor receptividad a soluciones insurtech |
| SSN requiriendo mejor gestión de reservas técnicas | Empuja documentación de riesgo |

---

## 6. ANÁLISIS COMPETITIVO

### 6.1 El Competidor Real: El Status Quo

Antes de analizar competidores directos, hay que nombrar al verdadero oponente: **lo que las aseguradoras hacen hoy en lugar de SafeGuard**.

| Práctica Actual | Costo para la Aseguradora | Limitación |
|---|---|---|
| Inspector externo pre-suscripción | USD 200-500 por evento | Solo captura el momento de la visita |
| Declaración jurada del asegurado | ~USD 0 | Sin verificación, frágil ante juicio |
| Revisión de perito post-siniestro | USD 500-2.000 + tiempo | Reactiva, no preventiva |
| No hacer nada (absorber riesgo) | USD 0 up front | Siniestros evitables a precio de mercado |

**SafeGuard no compite con una app. Compite con estas cuatro prácticas. El pitch siempre empieza aquí.**

### 6.2 Competidores por Categoría

**Categoría 0: Sistemas internos de grandes empresas (no compiten — validan)**

Empresas como Coca-Cola, YPF, Arcor o Techint ya resolvieron este problema internamente con SAP EHS, IBM Maximo o Intelex, con equipos HSE dedicados. Esto tiene dos implicaciones:

| Implicación | Qué significa |
|---|---|
| Valida que el problema es real y costoso | Si grandes empresas invierten en sistemas propios, el dolor existe |
| Define el target con precisión | El target es la empresa mediana y PyME que no puede ni podrá tener un SAP EHS |

Gap que ningún sistema interno resuelve: **ninguno conecta los datos de cumplimiento con el underwriting de la aseguradora**. Incluso Coca-Cola tiene datos de cumplimiento perfectos que su aseguradora no ve.

**Segmentación del mercado por tamaño:**

| Segmento | Sistema actual | Target SafeGuard |
|---|---|---|
| Grandes corporaciones (Coca-Cola, YPF, Arcor) | SAP EHS, equipo HSE dedicado | No — ya tienen solución interna |
| Empresas medianas (50-300 empleados) | Excel + inspector externo esporádico | Sí — target principal |
| PyMEs industriales (<50 empleados) | Nada estructurado | Sí — vía canal aseguradora |

**Categoría 1: Software de mantenimiento PCI — España**

Ripci.app, Cofrai, Protecnus/Asolvi. Todos venden a instaladores con normativa española (RIPCI). No compiten: mercado diferente, cliente diferente, normativa diferente.

**Categoría 2: Plataformas genéricas de inspección**

| Competidor | Fortaleza | Por qué no gana en este espacio |
|---|---|---|
| SafetyCulture (iAuditor) | 70.000+ clientes, USD 1.8B valuación | Genérico, sin normativa argentina, sin integración con aseguradoras, sin marketplace, sin tarificación diferenciada |
| Fulcrum | Flexible, mobile-first | Ídem: cero especialización sectorial |

**La respuesta a "¿y si SafetyCulture entra?"**: para cuando entren, habrá contratos firmados con exclusividad, 3 años de data propietaria, y una red de instaladores que requiere tiempo operacional para construir. El moat no está en la tecnología — está en el dataset y las relaciones.

**Categoría 3: Insurtechs argentinas**

Del inSURmap de la Cámara Insurtech Argentina (~50 startups), ninguna está en prevención de riesgo industrial + cumplimiento normativo + underwriting. Las categorías activas son: core systems, cobranzas, inspección post-siniestro, EPP digital, telemática.

**Categoría 4: Consultoras grandes**

PwC, Deloitte, KPMG ofrecen "risk management" pero a precios inaccesibles para PyMEs, sin plataforma digital escalable, sin red de instaladores, sin conocimiento de campo.

### 6.3 Mapa de Posicionamiento

| Capacidad | SafetyCulture | PCI España | Insurtechs AR | **SafeGuard** |
|---|---|---|---|---|
| Normativa argentina (NAG/IRAM) | — | — | — | **Si** |
| Integración con aseguradoras | — | — | — | **Si** |
| Certificación anti-rechazo de siniestro | — | — | — | **Si** |
| IoT + monitoreo continuo de activos | Parcial | — | — | **Si** |
| Tarificación diferenciada habilitada | — | — | — | **Si** |
| Marketplace de instaladores certificados | — | — | — | **Si** |
| Data products para reaseguradoras | — | — | — | **Si** |
| Precio accesible para PyMEs | Si | Si | — | **Si** |

### 6.4 Barreras de Entrada Reales

| Barrera | Por qué es sostenible |
|---|---|
| **Motor normativo propietario** | Las reglas NAG/IRAM están codificadas en software. Adrián puede irse; el engine queda. Actualizable cuando cambia la normativa. |
| **Contratos con switching cost** | La integración con sistemas core de la aseguradora genera un costo de migración de 6-12 meses de esfuerzo interno. |
| **Red de instaladores certificados** | Efecto red: más instaladores → mejor cobertura → más valor → más aseguradoras. Requiere tiempo operacional. |
| **Data propietaria de riesgo** | Cada inspección enriquece el modelo. 3 años de datos = ventaja actuarial que nadie puede comprar. |
| **First mover en canal reaseguradoras** | Los reaseguradores trabajan con un proveedor de data por mercado. El primero en cerrar ese contrato lo mantiene. |
| **Tarificación diferenciada como mecanismo** | Requiere historial actuarial conjunto con la aseguradora. No se replica de un día para el otro. |

---

## 7. CANALES DE DISTRIBUCIÓN

El modelo tiene **tres canales activos** que se refuerzan mutuamente, más un canal institucional de largo plazo:

### Canal 1: Top-Down (Aseguradoras)
La aseguradora incluye SafeGuard como requisito o valor agregado en sus pólizas industriales.
- Velocidad: media (ciclo de ventas 4-7 meses)
- Escala: alta (1 contrato = 5.000 empresas)
- Owner: Adrián + César

### Canal 2: Bottom-Up (Empresas que quieren calificar para mejor tarifa)
Una empresa con historial SafeGuard puede presentarlo a su aseguradora para calificar para tarificación diferenciada. Esto genera demanda pull que llega a la aseguradora desde sus propios clientes.
- Velocidad: lenta al inicio, creciente con masa crítica
- Escala: media (una empresa a la vez)
- Owner: Marketing + red de instaladores

### Canal 3: Instaladores (Fuerza de Venta Indirecta)
Los técnicos de la red SafeGuard tienen incentivo para instalar el sistema en cada cliente que atienden: más trabajo recurrente, mayor propuesta de valor, diferenciación frente a competidores.
- Velocidad: alta cuando la red está construida
- Escala: media
- Owner: Adrián (construcción de red en primeros 6 meses)

### Oportunidad Futura: Autoridades
Bomberos, municipios, y organismos como ENRE podrían recomendar o requerir el Sello SafeGuard en habilitaciones. Este canal no es una prioridad operativa — requiere años de burocracia — pero su impacto potencial es estructural si ocurre. No se incluye en las proyecciones financieras.

**Estrategia de entrada:** Canal 1 primero. Canal 3 en paralelo. Canal 2 se activa cuando haya 2+ aseguradoras ofreciendo tarificación diferenciada.

---

## 8. GO-TO-MARKET

### 8.1 El Principio que Rige Todo

**No vender el producto. Vender la conversación.**

Las aseguradoras no compran software en una reunión. Compran relaciones, confianza, evidencia. El objetivo de la primera interacción es abrir, no cerrar. El objetivo del piloto no es ingresos — es el caso de estudio que permite vender a las siguientes.

### 8.2 Contacto Prioritario: Diego Emilio Gornati — Sancor Seguros

Después de analizar perfiles del mercado, el primer contacto recomendado es:

| | |
|---|---|
| **Nombre** | Diego Emilio Gornati |
| **Empresa** | Sancor Cooperativa de Seguros Ltda |
| **Cargo** | Gerente Siniestros — Daños Materiales |
| **Antigüedad en el cargo** | 11+ años (desde Diciembre 2014) |
| **LinkedIn** | [linkedin.com/in/diego-emilio-gornati-4053025a](https://www.linkedin.com/in/diego-emilio-gornati-4053025a) |

**Por qué es el primer contacto:**
- **Ramo exacto:** Daños Materiales cubre incendio, maquinaria, y todo riesgo operativo — el corazón de SafeGuard
- **Background único:** 7 años en Prevención ART desarrollando políticas de seguridad industrial para empresas aseguradas y construyendo redes de ingenieros especialistas. Ya operó con la lógica de prevención + seguros industriales
- **Ingeniero técnico:** Ingeniero Electrónico (UTN) + Especialista en Ingeniería Ambiental. Entiende NAG/IRAM sin que se lo expliques
- **MBA:** Magister en Dirección de Empresas (UCC). Habla lenguaje técnico y de ROI
- **Peso interno:** 18+ años en Sancor. Puede avanzar un piloto sin múltiples aprobaciones
- **Alcance regional:** Gestiona siniestros en Argentina, Paraguay, Uruguay y Brasil

**El argumento de apertura:**
> *"Estuviste 7 años en Prevención ART desarrollando exactamente esto: prevención industrial integrada con seguros. SafeGuard trae esa misma lógica al ramo de Daños Materiales, que hoy no la tiene."*

### 8.3 A Quién Llamar en Cada Aseguradora

No al CEO. La puerta de entrada es el **Gerente de Siniestros**.

| Por qué el Gerente de Siniestros | Detalle |
|---|---|
| Tiene el dolor más inmediato | Vive el Art. 56 todos los días |
| Puede cuantificar su problema | Sabe cuántos juicios abiertos tiene y cuánto cuestan |
| Puede autorizar un piloto | No necesita aprobación del directorio para 50 pólizas |
| Se convierte en campeón interno | Una vez convencido, vende SafeGuard hacia arriba |

Secundariamente: Gerente de Underwriting (tarificación) y Gerente Comercial (diferenciación).

**Aseguradoras target en Córdoba / región:**
- **Sancor Seguros** — Sunchales/Córdoba, fuerte en ramos patrimoniales. Contacto: Diego Emilio Gornati
- **San Cristóbal Seguros** — Rosario, cartera industrial significativa
- **La Segunda** — Rosario, ramos patrimoniales y técnicos
- **Federación Patronal** — presencia en Córdoba, ramos industriales

### 8.4 Cómo Abre Adrián la Puerta

La primera llamada no es de ventas. Es de opinión experta.

**El guión:**
> *"Estoy desarrollando algo nuevo junto a un ingeniero de software con experiencia en MercadoLibre. Antes de construirlo, quiero entender si el problema que veo desde el sector técnico también lo ven desde el seguro. ¿Podemos tomar un café 30 minutos? Solo quiero tu opinión."*

Sus 8 años en 2A Ingeniería con proyectos como la Central Nuclear Embalse abren puertas que ningún pitch deck abre.

### 8.5 Qué Mostrar Cuando No Hay Producto

La demo existe antes que el producto. Es la herramienta de venta hasta que existe el caso de estudio real.

**La Demo Visual (semanas 1-3, antes de cualquier reunión):**

No es un prototipo técnico — es una historia visual en Figma o React con datos simulados. Tres momentos:

**Momento 1 — El problema hoy:**
Mapa de Córdoba con 200 fábricas. Todos los puntos en gris. *"¿Cuántos de estos cumplen con NAG/IRAM hoy?"* La respuesta: no saben.

**Momento 2 — SafeGuard en funcionamiento:**
El mismo mapa con colores: verde (cumple), amarillo (vencimientos próximos), rojo (alerta activa). En tiempo real: *"Empresa X — caída de presión en red PCI. Técnico asignado. Reparación en 48hs."*

**Momento 3 — El siniestro con y sin SafeGuard:**
Sin SafeGuard: declaración jurada, el perito descubre incumplimientos, dilema legal. Con SafeGuard: 18 meses de historial certificado, la aseguradora actúa con evidencia sólida en cualquier dirección.

### 8.6 El Guión de la Primera Reunión

**Primeros 10 minutos: escuchar.**

- *"¿Cómo sabés hoy si tus asegurados industriales cumplen con NAG/IRAM entre inspecciones?"*
- *"¿Cuántos siniestros industriales terminan en litigio después de un rechazo?"*
- *"¿Cuánto le cuesta a la compañía un juicio por Art. 56?"*

Dejar que describan el dolor. No interrumpir.

**Siguientes 15 minutos: mostrar la demo.** No explicar funcionalidades — contar la historia de los tres momentos.

**El cierre:**
> *"Lo que te mostré no es el producto terminado — es la dirección. Lo que propongo es: tomamos 50 de tus clientes industriales durante 90 días, y definimos juntos qué deberías ver al final para que esto te resulte valioso. No te pido un contrato — te pido que co-diseñes el piloto conmigo."*

### 8.7 Estructura del Piloto Fundacional

| Parámetro | Detalle |
|---|---|
| Duración | 90 días |
| Alcance | 50-100 pólizas industriales de la cartera existente |
| Costo para la aseguradora | Gratuito o a costo (USD 5-10K) |
| KPIs co-diseñados | % empresas con cumplimiento documentado, alertas detectadas, tiempo de certificación |
| Entregable | Reporte: riesgos detectados, comparación antes/después |
| Objetivo real de SafeGuard | El caso de estudio que vende las siguientes 5 aseguradoras |

### 8.8 De la Segunda Aseguradora en Adelante

| Etapa | Sin caso de estudio | Con caso de estudio |
|---|---|---|
| Primera reunión | "Creemos que puede funcionar" | "En Sancor detectamos X, evitamos Y" |
| Ciclo de decisión | 6-9 meses | 3-5 meses |
| Objeción principal | "¿Funciona en la práctica?" | "¿Funciona para nuestra cartera?" |
| Piloto necesario | Siempre | Negociable |

---

## 9. EQUIPO

### 9.1 César — Fundador / Tech Lead

| Aspecto | Detalle |
|---|---|
| Experiencia | 15+ años en desarrollo de software enterprise |
| Posición actual | Senior Software Engineer, MercadoLibre (Seller Central) |
| Stack técnico | .NET, Java, C#, Azure, arquitecturas cloud, APIs, integraciones B2B |
| Formación | Ingeniero en Sistemas, UTN Córdoba |
| Emprendimiento | Co-fundador HydroVision AG (AgTech), fundador OCUPA |

### 9.2 Adrián Avaro — Co-Fundador / Chief Domain Officer (Propuesto)

| Aspecto | Detalle |
|---|---|
| Formación | Ingeniero Industrial, UTN (1999-2006) |
| Experiencia | 8+ años, Gerente Técnico Comercial en 2A Ingeniería |
| Conocimiento normativo | NAG-200/201, IRAM, NFPA adaptadas, auditorías ISO 9000 |
| Proyectos | Central Nuclear Embalse, centrales termoeléctricas |
| Red | Contactos en aseguradoras, instaladores PCI y gas, parques industriales |

**El rol crítico de Adrián en los primeros 6 meses:** Codificar su expertise en el motor normativo. Cada checklist que define, cada regla que parametriza, es IP que queda en la plataforma — independientemente de lo que pase después.

### 9.3 Complementariedad del Equipo

| Capacidad | César | Adrián |
|---|---|---|
| Plataforma SaaS y arquitectura cloud | Si | — |
| Integraciones B2B con sistemas de aseguradoras | Si | — |
| Motor normativo configurable | Si (construcción) | Si (contenido) |
| IoT gateway y protocolos de sensores | Si | — |
| Checklists NAG/IRAM/NFPA | — | Si |
| Red en sector industrial/asegurador | Parcial | Si |
| Credibilidad técnica ante aseguradoras | Parcial (tech) | Si (ingeniería de campo) |
| Construcción de red de instaladores | — | Si |

### 9.4 Plan de Contrataciones

| Posición | Cuándo | Perfil |
|---|---|---|
| Sales Executive | Mes 8 | Experiencia en venta B2B a aseguradoras |
| Técnico normativo junior | Mes 10 | Soporte a Adrián en onboarding y actualizaciones |
| Data Analyst | Año 2 Q2 | Análisis de riesgo, data products para reaseguradoras |
| Expansion Lead LATAM | Año 3 | Adaptación regional, gestión de partners locales |

---

## 10. RIESGOS Y MITIGACIONES

| Riesgo | Prob. | Impacto | Mitigación |
|---|---|---|---|
| Ciclo de ventas más largo de lo esperado | Alta | Alto | Piloto como PoC sin compromiso comercial. Reduce la barrera de entrada. |
| Aseguradoras no ven urgencia suficiente | Media | Alto | Cuantificar el costo del rechazo sin evidencia con casos reales (Art. 56). Llevar números de su propia cartera. |
| SafetyCulture o actor global entra | Baja | Medio | Contratos exclusivos + data propietaria + red de instaladores. Moat = tiempo de operación, no tecnología. |
| Adrián no puede comprometerse al nivel requerido | Media | Alto | Compromisos mínimos documentados. Motor normativo construido en los primeros 90 días reduce dependencia. |
| Resistencia a instalar sensores (Track B) | Media | Bajo | Track A funciona sin sensores. IoT es un upgrade, no un requisito. |
| Cambios regulatorios (NAG/IRAM) | Baja | Bajo | Motor normativo versionado. Los cambios se convierten en valor: "actualización automática incluida". |
| Riesgo cambiario | Alta | Medio | Contratos en pesos ajustados por CVS con revisión semestral. Costos en pesos, targets en USD equivalente. |
| SSN no valida la tarificación diferenciada | Baja | Medio | El modelo de tarificación diferenciada es estándar actuarial a nivel mundial. La validación actuarial es parte del proceso de adopción con la aseguradora. |

---

## 11. FINANCIAMIENTO

### 11.1 ¿Se Necesita Inversión Externa?

No en Año 1, bajo el escenario bootstrappeado.

**Supuestos del escenario bootstrappeado:**
- César mantiene empleo en MercadoLibre y dedica 20 hrs/semana (desarrollo MVP y demos)
- Adrián: 10-15 hrs/semana (definición normativa + apertura de puertas)
- Primer setup fee (USD 40-65K) financia el desarrollo inicial
- **Break-even operativo estimado: Mes 16-20** (sin contar salarios de fundadores a full-time)

*Nota: Si César pasa a full-time antes del Mes 8, el break-even se extiende a Mes 20-24. Ese es el punto a definir con Adrián en la primera conversación.*

**Si se busca inversión:** La ronda tiene más sentido en Año 2, cuando hay caso de estudio, 2+ aseguradoras activas, y el modelo de tarificación diferenciada validado. En ese momento el riesgo es de escala, no de concepto.

**Uso de capital si se levanta Año 1 (~ USD 200K):**
- 50%: Salarios (Adrián full-time desde Mes 4, César full-time desde Mes 6)
- 25%: Desarrollo IoT (sensores piloto, infraestructura)
- 15%: Sales & marketing (eventos de seguros, materiales)
- 10%: Legal y estructura societaria

---

## 12. PRÓXIMOS PASOS

| Paso | Acción | Timing | Owner |
|---|---|---|---|
| 1 | Constituir SAS (Sociedad por Acciones Simplificada) — necesaria antes del primer contrato de piloto | Semana 1-2 | César |
| 2 | Reunión de alineación con Adrián: rol, equity, vesting, compromisos mínimos | Semana 1 | César + Adrián |
| 3 | Adrián define primeros 3 checklists (NAG-200, IRAM 3543, extintores) | Semana 2-3 | Adrián |
| 4 | César construye demo visual (Figma + datos simulados): mapa de riesgo + simulador de alertas | Semana 1-3 | César |
| 5 | Adrián contacta a Diego Emilio Gornati (Sancor) + 2 aseguradoras más | Semana 3-5 | Adrián |
| 6 | César desarrolla MVP: app de inspección mobile + dashboard básico + PDF de certificado | Semana 2-7 | César |
| 7 | Demos con 3 aseguradoras target | Semana 6-9 | César + Adrián |
| 8 | Firmar PoC fundacional: 50-100 pólizas, 90 días, KPIs co-diseñados | Mes 2-3 | Ambos |
| 9 | Ejecutar PoC, documentar hallazgos, construir caso de estudio | Mes 3-6 | Ambos |
| 10 | Usar caso de estudio para cerrar segunda aseguradora + iniciar conversación con reaseguradora | Mes 6-9 | Adrián + Sales |

---

## ANEXOS

### A.1 Mercado Asegurador Argentino

| Dato | Valor | Fuente |
|---|---|---|
| Total aseguradoras autorizadas | 206 entidades | SSN, Junio 2024 |
| Aseguradoras patrimoniales/mixtas | 124 entidades (64.9%) | SSN, Junio 2024 |
| Producción total del mercado | ~ARS 13.552B | SSN, 2023/2024 |
| Participación en PBI | 3.7% | SSN, 2024 |
| Productores de seguros | 49.433 individuales + 1.010 sociedades | SSN, Junio 2024 |

### A.2 Normativa de Referencia

| Norma | Alcance | Aplicación |
|---|---|---|
| NAG-200 | Instalaciones de gas natural industrial | Diseño, construcción, mantenimiento |
| NAG-201 | Requisitos para instaladores de gas | Certificación de técnicos |
| IRAM 3501-3546 | Protección contra incendios | Extintores, rociadores, hidrantes |
| NFPA (adaptadas) | Estándares internacionales PCI | Complemento a IRAM |
| Ley 17.418 Art. 56 | Ley de Seguros Argentina | 30 días para pronunciarse. Silencio = aceptación |

### A.3 Comparativa de Modelos de Revenue

| Modelo | Ventaja | Riesgo |
|---|---|---|
| Fee por póliza (principal) | Predecible, escala con la cartera | Depende de renovación del contrato |
| Hardware (Track B) | Alto margen, lock-in físico | Complejidad operativa, soporte |
| Certificaciones directas | Revenue sin intermediario | CAC alto sin pull del Sello |
| Data products reaseguradoras | Muy alto margen, estratégico | Ciclo largo, requiere dataset maduro (Año 2+) |
| Revenue share (descartado) | Alineación de incentivos | Imposible atribuir causalidad. Fricciones contractuales |

### A.4 Glosario

| Término | Definición |
|---|---|
| B2B2C | Vendemos a aseguradoras que distribuyen el valor a sus clientes empresariales |
| Loss Ratio | Siniestros pagados / primas cobradas. 65% = por cada $100 de prima, $65 en siniestros |
| Combined Ratio | Loss ratio + expense ratio. Si > 100%, la aseguradora pierde dinero operativamente |
| Underwriting | Evaluación y suscripción de riesgos para determinar precio de póliza |
| PCI | Protección Contra Incendios: sistemas de detección, alarma y extinción |
| Reaseguro | El seguro del seguro. Reaseguradoras cubren a aseguradoras para riesgos de alta severidad |
| Motor normativo | Software que codifica reglas de cumplimiento y evalúa instalaciones automáticamente |
| Sello SafeGuard | Certificación visible de cumplimiento activo. Activo de marca de largo plazo |
| Track A / Track B | A = SaaS sin hardware. B = SaaS + IoT (habilita tarificación diferenciada) |
| SAS | Sociedad por Acciones Simplificada. Estructura societaria recomendada para la startup |
| CVS | Coeficiente de Variación Salarial. Índice de ajuste para contratos en pesos |
| Tarificación diferenciada | Risk-based pricing: menor prima para empresas con menor riesgo demostrado |

---

*SafeGuard Industrial © 2026 | Documento confidencial — Versión 2.1*
