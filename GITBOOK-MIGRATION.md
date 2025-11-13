# Guía de Migración a GitBook

## Estado Actual

Este repositorio ha sido reestructurado de **Mintlify** a **GitBook**:

✅ **Completado:**
- `.gitbook.yaml` creado con configuración GitBook
- `SUMMARY.md` con navegación completa
- `README.md` como homepage
- Todos los archivos renombrados de `.mdx` → `.md`
- Eliminados `docs.json` e `index.mdx` (específicos de Mintlify)

⚠️ **Pendiente:**
- Simplificar componentes de Mintlify en archivos `.md`

## Componentes a Convertir

### 1. Cards → Listas o Tablas

**Mintlify:**
```mdx
<Card title="Título" icon="wallet">
  Contenido aquí
</Card>
```

**GitBook (opción A - Lista):**
```markdown
### 💰 Título
Contenido aquí
```

**GitBook (opción B - Tabla):**
```markdown
| Característica | Descripción |
|----------------|-------------|
| 💰 Título | Contenido aquí |
```

### 2. CardGroup → Sublistas

**Mintlify:**
```mdx
<CardGroup cols={2}>
  <Card title="Uno" icon="check">
    Texto 1
  </Card>
  <Card title="Dos" icon="star">
    Texto 2
  </Card>
</CardGroup>
```

**GitBook:**
```markdown
#### ✅ Uno
Texto 1

#### ⭐ Dos
Texto 2
```

### 3. Tabs → GitBook Tabs

**Mintlify:**
```mdx
<Tabs>
  <Tab title="Tab 1">
    Contenido 1
  </Tab>
  <Tab title="Tab 2">
    Contenido 2
  </Tab>
</Tabs>
```

**GitBook:**
```markdown
{% tabs %}
{% tab title="Tab 1" %}
Contenido 1
{% endtab %}

{% tab title="Tab 2" %}
Contenido 2
{% endtab %}
{% endtabs %}
```

### 4. Callouts → GitBook Hints

**Mintlify:**
```mdx
<Info>
  Mensaje informativo
</Info>

<Warning>
  Advertencia
</Warning>

<Tip>
  Consejo útil
</Tip>
```

**GitBook:**
```markdown
{% hint style="info" %}
Mensaje informativo
{% endhint %}

{% hint style="warning" %}
Advertencia
{% endhint %}

{% hint style="success" %}
Consejo útil
{% endhint %}
```

### 5. Frame → Imagen simple

**Mintlify:**
```mdx
<Frame>
  <img src="/path/image.png" alt="Descripción" />
</Frame>
```

**GitBook:**
```markdown
![Descripción](/path/image.png)
```

## Archivos que Necesitan Simplificación

Archivos con más componentes Mintlify:

- [ ] `strategy/moat.md` - Múltiples Card y Tabs
- [ ] `company/roadmap.md` - Tabs con timeline
- [ ] `company/architecture.md` - Tabs
- [ ] `company/gtm.md` - Tabs
- [ ] `resources/glossary.md` - CardGroup
- [ ] `resources/faq.md` - CardGroup
- [ ] `products/overview.md` - Cards
- [ ] `products/oruon.md` - Cards
- [ ] `products/ops.md` - Cards
- [ ] `products/removemycontent.md` - Cards
- [ ] `ai-strategy/manager-ai.md` - CardGroup
- [ ] `ai-strategy/integrity-ai.md` - CardGroup
- [ ] `company/mdly-holding.md` - CardGroup
- [ ] `investors/overview.md` - Cards
- [ ] `company/security.md` - Posiblemente Accordions

## Prioridad de Conversión

**Alta prioridad (Homepage y páginas principales):**
1. `products/overview.md` - Primera página de productos
2. `strategy/moat.md` - Página estratégica clave
3. `investors/overview.md` - Página para inversores

**Media prioridad:**
4. `company/roadmap.md` - Timeline importante
5. `ai-strategy/manager-ai.md` - Estrategia IA
6. `ai-strategy/integrity-ai.md` - Estrategia IA

**Baja prioridad:**
7. Resto de archivos

## Cómo Configurar en GitBook

1. Ve a https://app.gitbook.com
2. Crea un nuevo Space o selecciona uno existente
3. Ve a **Integrations** → **GitHub**
4. Conecta el repositorio: `modeltyapp/docs`
5. Branch: `main`
6. GitBook sincronizará automáticamente

## Sintaxis GitBook Soportada

GitBook soporta:
- ✅ Markdown estándar
- ✅ GitBook hints (`{% hint %}`)
- ✅ GitBook tabs (`{% tabs %}`)
- ✅ Frontmatter YAML
- ✅ Imágenes y assets
- ✅ Tablas
- ✅ Listas anidadas
- ✅ Code blocks
- ❌ Componentes React/MDX personalizados
- ❌ `<Card>`, `<CardGroup>` (Mintlify)
- ❌ `<Frame>` (Mintlify)
- ❌ `<Steps>` (Mintlify)

## Referencias

- [GitBook Docs](https://docs.gitbook.com)
- [GitBook Markdown](https://docs.gitbook.com/content-editor/blocks)
- [GitBook GitHub Integration](https://docs.gitbook.com/integrations/git-sync)
