<div align="center">
  <img src="banner-red.svg" alt="Felipe Barraza — Developer + IA & IoT. Chillán, Chile." width="100%">
</div>

<br>

Soy Felipe Barraza, Developer + IA & IoT.

Mi misión como profesional es transformar problemas reales en productos de software robustos, seguros y listos para escalar. Desde 2012 diseño arquitecturas, desarrollo y mantengo infraestructuras. Trabajo con agentes de IA como parte de mi equipo, en cada etapa del desarrollo, para construir productos más sólidos y de mejor calidad.

Lidero el área de software en una empresa de ingeniería y telemetría (IoT y automatización de gestión regulatoria), soy CTO y socio en Quality Net, y desarrollo mis propios productos en Y ARQ.

<p align="center">
  <a href="https://www.linkedin.com/in/luis-felipe-andr%C3%A9s-barraza-vega-56692551/"><img src="https://img.shields.io/badge/LinkedIn-32302f?style=flat-square&logo=linkedin&logoColor=8ec07c" alt="LinkedIn de Felipe Barraza"></a>
  &nbsp;
  <a href="mailto:felipe.barraza.vega@gmail.com"><img src="https://img.shields.io/badge/Email-32302f?style=flat-square&logo=gmail&logoColor=fabd2f" alt="Correo de Felipe Barraza"></a>
  &nbsp;
  <a href="CV_Felipe_Barraza.pdf"><img src="https://img.shields.io/badge/Curr%C3%ADculum%20(PDF)-32302f?style=flat-square&logo=adobeacrobatreader&logoColor=fe8019" alt="Currículum (PDF)"></a>
</p>

**Ahora** — Desde enero de 2021 soy Líder de Área de Software en [SmartHydro](https://smarthydro.cl), en Chillán. Trabajo de forma directa con el CTO. También soy CTO y socio en Quality Net, y desarrollo mis propios productos en Y ARQ.

**Qué hago** — En esa empresa de ingeniería y telemetría trabajo con IoT, IA aplicada y la automatización de la gestión regulatoria ante distintas entidades, entre ellas la DGA y la SMA. El objetivo es que la información de terreno sea confiable y llegue a quienes operan y a quienes deben cumplir y fiscalizar la normativa.

**Mi rol**

- **Estrategia y arquitectura** — Lidero la arquitectura de datos y de las plataformas de Operaciones y Ventas, en alineación directa con el CTO y las prioridades del negocio.
- **I+D en IA e IoT** — Desarrollo investigación aplicada en IA e IoT y prototipo agentes multimodales de IA para operaciones institucionales.
- **Desarrollo y liderazgo técnico** — Lidero el equipo de software en la revisión y la entrega a producción, con mejora continua.
- **Infraestructura y operación** — Administro la infraestructura en la nube y la operación cotidiana, para la continuidad y la confiabilidad de la telemetría.
- **Gestión y automatización interna** — Administro el espacio de trabajo, las automatizaciones internas y los servicios que sostienen la operación cotidiana.

**Stack**

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,django,fastapi,react,nextjs,flutter,postgres,redis,docker,githubactions,linux&theme=dark" alt="Python, Django, FastAPI, React, Next.js, Flutter, PostgreSQL, Redis, Docker, GitHub Actions, Linux">
</p>

<p align="center"><sub>MQTT · WebSockets · TimescaleDB · Apps Script · agentes de IA</sub></p>

**Sistema de agentes**

Orquesto el trabajo de software con un sistema de agentes. Cada entrega a producción se cierra con una revisión humana.

```mermaid
%%{init: {"theme":"dark","themeVariables":{"background":"#282828","primaryTextColor":"#ebdbb2","lineColor":"#8ec07c","fontFamily":"monospace"}}}%%
flowchart TB
  WORKIT["Workit — orquestador"]
  WORKIT --> BE["Backend"]
  WORKIT --> FE["Front"]
  WORKIT --> DO["DevOps"]
  WORKIT --> QA["QA"]
  WORKIT --> PR["Producto"]
  WORKIT --> AR["Arquitectura"]
  BE --> GH["GitHub"]
  FE --> GH
  DO --> GH
  QA --> GH
  PR --> GH
  AR --> GH
  GH --> CI["CI/CD"]
  CI --> PROD["Producción"]
  PROD --> HUM["Revisión humana"]
  HUM --> WORKIT
  classDef orch fill:#282828,stroke:#fe8019,stroke-width:2px,color:#fe8019
  classDef agent fill:#282828,stroke:#8ec07c,stroke-width:2px,color:#8ec07c
  classDef stage fill:#282828,stroke:#fabd2f,stroke-width:2px,color:#fabd2f
  class WORKIT orch
  class BE,FE,DO,QA,PR,AR agent
  class GH,CI,PROD,HUM stage
```

**Arquitectura IoT**

Así fluye la telemetría: desde el sensor hasta los reportes que deben llegar a las entidades reguladoras, entre ellas la DGA y la SMA.

```mermaid
%%{init: {"theme":"dark","themeVariables":{"background":"#282828","primaryTextColor":"#ebdbb2","lineColor":"#8ec07c","fontFamily":"monospace"}}}%%
flowchart LR
  SEN["Sensores / dataloggers"] --> GW["Gateway"]
  GW --> ING["Ingesta"]
  ING --> DB[("Base de datos")]
  ING --> Q[["Colas"]]
  DB --> DASH["Dashboards"]
  Q --> AL["Alertas"]
  DB --> REP["Reportes a entidades reguladoras (DGA, SMA)"]
  Q --> REP
  classDef io fill:#282828,stroke:#8ec07c,stroke-width:2px,color:#8ec07c
  classDef core fill:#282828,stroke:#fe8019,stroke-width:2px,color:#fe8019
  classDef out fill:#282828,stroke:#fabd2f,stroke-width:2px,color:#fabd2f
  class SEN,GW io
  class ING,DB,Q core
  class DASH,AL,REP out
```

**Plataformas de operación y telemetría**

Estas son las piezas del producto con las que trabajamos a diario en SmartHydro, y cómo se conectan hasta el cumplimiento ante la DGA y la SMA.

```mermaid
%%{init: {"theme":"dark","themeVariables":{"background":"#282828","primaryTextColor":"#ebdbb2","lineColor":"#8ec07c","fontFamily":"monospace"}}}%%
flowchart TB
  SHSEN["Sensores / dataloggers"] --> SHING["Ingesta de telemetría"]
  SHING --> SHNER["Nereus — telemetría y ERP"]
  SHING --> SHIKO["Ikolu — ERP de operación<br/>tickets, SLA y OT"]
  SHING --> SHCRM["CRM"]
  SHING --> SHMON["App y PWA de monitoreo"]
  SHAST["Agente de asistencia<br/>interna"] --> SHIKO
  SHNER --> SHREG["Reportes a entidades<br/>reguladoras (DGA, SMA)"]
  SHIKO --> SHREG
  classDef field fill:#282828,stroke:#8ec07c,stroke-width:2px,color:#8ec07c
  classDef core fill:#282828,stroke:#fe8019,stroke-width:2px,color:#fe8019
  classDef app fill:#282828,stroke:#8ec07c,stroke-width:2px,color:#8ec07c
  classDef gov fill:#282828,stroke:#fabd2f,stroke-width:2px,color:#fabd2f
  class SHSEN field
  class SHING,SHAST core
  class SHNER,SHIKO,SHCRM,SHMON app
  class SHREG gov
```

**Proyecto Y ARQ**

Y ARQ nació para no construir cada producto desde cero. Es un backend multi-tenant con un contrato compartido: una sola instalación atiende varias sucursales, cada una con sus datos aislados, y los módulos se activan según el plan. El contrato es el mismo para todas las aplicaciones, de modo que cada producto arma su interfaz sin reimplementar el núcleo. Así se pueden adoptar clientes de distintos sectores a partir de un mismo tronco.

- [Sitio de Y ARQ](https://github.com/felipebarraza6/yggdra-web) — portafolio técnico del backend y de las apps que lo usan · [sitio](https://felipebarraza6.github.io/yggdra-web/)
- [Muninn](https://github.com/felipebarraza6/muninn) — cliente para diseñar y operar agentes de IA · [demo](https://felipebarraza6.github.io/muninn/)
- [Frig](https://github.com/felipebarraza6/frig) — solución de gestión gastronómica integral: punto de venta, mesas, comandas de cocina, caja, inventario, recetas, finanzas y reportes · [sitio](https://frig.yggdra.cl)
- [Nxord](https://github.com/felipebarraza6/nxord) — plataforma de gestión hídrica y telemetría en tiempo real · [demo](https://felipebarraza6.github.io/nxord/)
- [HEIR](https://github.com/felipebarraza6/heir) — agenda, pagos y agente conversacional para profesionales de la salud · [demo](https://felipebarraza6.github.io/heir/)
- [Forja](https://github.com/felipebarraza6/forja) — plataforma para personal trainers: venta de servicios y gestión de alumnos · [demo](https://felipebarraza6.github.io/forja/)
- [Gungir](https://github.com/felipebarraza6/gungir) — comercio general y cotizador · [demo](https://felipebarraza6.github.io/gungir/)
- [Y Print](https://github.com/felipebarraza6/y-print) — agente de impresión nativo: se autentica contra el backend e imprime según los permisos de la sucursal

**Proyectos destacados**

Además de Y ARQ, he construido herramientas y sitios pensados para un uso concreto: el agua potable rural, un desafío de 90 días, o la presencia digital de una organización.

- [Cauce](https://github.com/felipebarraza6/nxrd_apr) — cliente web del ciclo de agua potable rural: socio, medidor, lectura, tarifa vigente y cobro del período, para la administración del comité, las lecturas en terreno y la caja · [sitio](https://cauce.smartapr.cl)
- [Proyecto 90](https://github.com/felipebarraza6/proyecto-90) — landing, inscripción, seguimiento del participante y panel del equipo para un desafío de 90 días
- [Valentino Automotora](https://github.com/felipebarraza6/web_valentino_automotora) — prototipo web estático de la automotora: ficha de vehículos y un asistente de consulta simulado en el navegador · [demo](https://felipebarraza6.github.io/web_valentino_automotora/)
- [Andean Labs](https://github.com/felipebarraza6/andean-labs-web) — sitio institucional estático, con noticias, convenios, galería y versiones en español, inglés y chino · [demo](https://felipebarraza6.github.io/andean-labs-web/)

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=felipebarraza6&show_icons=true&hide_title=true&hide_rank=true&bg_color=282828&title_color=fabd2f&text_color=ebdbb2&icon_color=8ec07c&border_color=3c3836&hide_border=false&include_all_commits=false" alt="Actividad pública en GitHub" height="140">
</p>

[felipe.barraza.vega@gmail.com](mailto:felipe.barraza.vega@gmail.com)
