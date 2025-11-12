# 📚 Guía de Configuración GitBook

Esta guía te ayudará a configurar correctamente la documentación de Modelty en GitBook.

---

## 🚀 Paso 1: Conectar Repositorio a GitBook

### Opción A: Desde GitBook Dashboard

1. **Accede a GitBook** → https://app.gitbook.com
2. **Crea un nuevo espacio** o selecciona uno existente
3. **Ve a Integrations** → GitHub
4. **Conecta tu repositorio:**
   - Organización: `modeltyapp`
   - Repositorio: `docs`
   - Branch: `main`
5. **Selecciona el directorio raíz** del proyecto

### Opción B: Desde GitHub

1. **Instala la GitHub App de GitBook** desde:
   https://github.com/apps/gitbook-com
2. **Autoriza el acceso** al repositorio `modeltyapp/docs`
3. GitBook detectará automáticamente el repositorio

---

## 📁 Paso 2: Estructura de Archivos

Tu repositorio debe tener esta estructura:

```
docs/
├── docs.json                 # Configuración principal
├── investors.json            # Config para tab de inversores
├── index.mdx                 # Homepage
├── products/
│   ├── overview.mdx
│   ├── oruon.mdx
│   ├── ops.mdx
│   └── removemycontent.mdx
├── ai-strategy/
│   ├── manager-ai.mdx
│   └── integrity-ai.mdx
├── company/
│   ├── mdly-holding.mdx
│   ├── roadmap.mdx
│   ├── security.mdx
│   ├── architecture.mdx
│   └── gtm.mdx
├── strategy/
│   └── moat.mdx
├── investors/
│   └── overview.mdx
├── resources/
│   ├── faq.mdx
│   └── glossary.mdx
├── assets/                   # Imágenes y media
└── logo/                     # Logos light/dark
    ├── light.svg
    └── dark.svg
```

---

## 🎨 Paso 3: Configurar Branding

### 3.1 Logos

Crea archivos SVG en `/logo/`:

**logo/light.svg** - Logo para modo claro
**logo/dark.svg** - Logo para modo oscuro

Dimensiones recomendadas: **120x40px** o similar

### 3.2 Favicon

Coloca tu favicon en `/favicon.svg` (formato SVG recomendado)

### 3.3 Colores

Los colores ya están configurados en `docs.json`:
- **Primary:** #7C3AED (Púrpura)
- **Light:** #A78BFA
- **Dark:** #5B21B6

---

## 📊 Paso 4: Configurar Analytics (Opcional)

### Google Analytics 4

1. **Crea una propiedad GA4** en https://analytics.google.com
2. **Copia tu Measurement ID** (formato: G-XXXXXXXXXX)
3. **Actualiza en docs.json:**

```json
"analytics": {
  "ga4": {
    "measurementId": "TU-MEASUREMENT-ID"
  }
}
```

---

## 🖼️ Paso 5: Agregar Imágenes

### 5.1 Subir a /assets/

Sube las siguientes imágenes a `/assets/`:

- `ecosystem-flywheel.png` - Diagrama del flywheel
- `oruon-dashboard.png` - Screenshot del wallet
- `oruon-subwallets-topology.png` - Diagrama de sub-wallets
- `sasha-signal-loop.png` - Diagrama de señales de Ops
- `rmc-triage.png` - Workflow de Vault
- `moat-layers.png` - Capas del moat
- `architecture-highlevel.png` - Arquitectura
- `roadmap-swimlanes.png` - Roadmap visual

### 5.2 Formato Recomendado

- **Formato:** PNG (con transparencia)
- **Resolución:** 1200px de ancho mínimo
- **Tamaño:** < 500KB optimizado
- **Aspect Ratio:** 16:9 para diagramas

---

## ⚙️ Paso 6: Configurar Domain (Opcional)

### Opción A: Subdominio de GitBook

Por defecto obtendrás: `modelty.gitbook.io`

### Opción B: Dominio Personalizado

1. **Ve a Settings** → Custom Domain
2. **Agrega tu dominio:** `docs.modelty.app`
3. **Configura DNS:**

```
Tipo: CNAME
Nombre: docs
Valor: hosting.gitbook.io
```

4. **Verifica** en GitBook (puede tomar 24-48h)

---

## 🔧 Paso 7: Configuraciones Avanzadas

### 7.1 Habilitar Feedback

Ya configurado en `docs.json`:
```json
"feedback": {
  "suggestEdit": true,
  "raiseIssue": true,
  "thumbsRating": true
}
```

### 7.2 SEO

GitBook genera automáticamente:
- Meta tags desde `description` en frontmatter
- Sitemap XML
- robots.txt

**Optimiza cada página con:**
```yaml
---
title: Título SEO-friendly
description: Descripción clara y concisa (150-160 caracteres)
---
```

### 7.3 Social Cards

GitBook genera automáticamente social cards (Open Graph) para Twitter/LinkedIn.

Para personalizar, puedes agregar imágenes OG en el frontmatter:
```yaml
---
title: Tu Página
description: Descripción
image: /assets/og-image.png
---
```

---

## 🔄 Paso 8: Proceso de Actualización

### Flujo de Trabajo

1. **Edita archivos** en tu repositorio local
2. **Commit y push** a GitHub
3. **GitBook sincroniza automáticamente** (30-60 segundos)
4. **Revisa en preview** antes de publicar

### Comandos Git

```bash
# Editar localmente
git add .
git commit -m "Update documentation"
git push origin main

# GitBook detecta cambios automáticamente
```

---

## 🎯 Paso 9: Verificar Navegación

### Estructura de Navegación Actual

**Tab Principal: Documentation**
```
📚 Getting Started
   └─ Homepage

📦 Products
   ├─ Overview
   ├─ Oruon (Wallet)
   ├─ Ops (AI)
   └─ RemoveMyContent (Vault)

🤖 AI Technology
   ├─ Manager AI
   └─ Integrity AI

🏢 Company
   ├─ MDLY Holding
   ├─ Roadmap
   └─ Go-to-Market

🔒 Trust & Security
   ├─ Security & Compliance
   └─ Platform Infrastructure

🎯 Strategy
   └─ Competitive Moat

📚 Resources
   ├─ FAQ
   └─ Glossary
```

**Tab Secundario: For Investors**
```
💼 Investment Opportunity
   └─ Metrics & Overview
```

---

## 🎨 Paso 10: Personalización Visual

### Componentes GitBook Disponibles

**Cards:**
```mdx
<Card title="Título" icon="wallet">
  Descripción del contenido
</Card>
```

**CardGroup:**
```mdx
<CardGroup cols={3}>
  <Card title="Card 1">...</Card>
  <Card title="Card 2">...</Card>
  <Card title="Card 3">...</Card>
</CardGroup>
```

**Tabs:**
```mdx
<Tabs>
  <Tab title="Tab 1">Contenido 1</Tab>
  <Tab title="Tab 2">Contenido 2</Tab>
</Tabs>
```

**Callouts:**
```mdx
<Info>Información importante</Info>
<Warning>Advertencia</Warning>
<Tip>Consejo útil</Tip>
<Note>Nota adicional</Note>
```

**Steps:**
```mdx
<Steps>
  <Step title="Paso 1">Descripción</Step>
  <Step title="Paso 2">Descripción</Step>
</Steps>
```

---

## ✅ Checklist de Configuración

Usa esta checklist para verificar que todo está configurado:

- [ ] Repositorio conectado a GitBook
- [ ] `docs.json` configurado correctamente
- [ ] Logos (light.svg y dark.svg) subidos
- [ ] Favicon configurado
- [ ] Todas las imágenes en /assets/ subidas
- [ ] Colores de marca configurados
- [ ] Analytics configurado (opcional)
- [ ] Dominio personalizado configurado (opcional)
- [ ] Navegación verificada en preview
- [ ] Enlaces externos funcionando
- [ ] Social sharing cards verificados
- [ ] Mobile responsive verificado

---

## 🐛 Troubleshooting

### Problema: GitBook no sincroniza

**Solución:**
1. Verifica permisos de GitHub App
2. Chequea branch correcta (main)
3. Verifica que `docs.json` es válido JSON
4. Revisa GitBook logs en Settings → Integrations

### Problema: Imágenes no se muestran

**Solución:**
1. Verifica rutas: `/assets/nombre.png`
2. Asegúrate que estén en el repo
3. Chequea mayúsculas/minúsculas
4. Verifica formato soportado (PNG, JPG, SVG)

### Problema: Navegación rota

**Solución:**
1. Verifica paths en `docs.json`
2. Asegúrate que todos los archivos .mdx existen
3. Chequea frontmatter válido en cada archivo
4. Valida JSON en https://jsonlint.com

### Problema: Estilos no se aplican

**Solución:**
1. GitBook tiene cache - espera 5 minutos
2. Limpia cache del navegador
3. Verifica sintaxis de componentes MDX
4. Revisa que colores estén en formato HEX

---

## 📞 Soporte

**GitBook Documentation:**
https://docs.gitbook.com

**Mintlify Documentation:**
https://mintlify.com/docs

**Modelty Support:**
Email: tech@modelty.app

---

## 🎉 ¡Listo!

Tu documentación de Modelty está configurada y lista para GitBook.

**Próximos pasos:**
1. Revisa el preview en GitBook
2. Ajusta contenido según necesites
3. Configura dominio personalizado
4. Agrega analytics
5. Publica a producción

**URL de documentación:**
- Preview: `https://modelty.gitbook.io`
- Producción: `https://docs.modelty.app` (si configuras dominio)
