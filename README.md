# MorphHomeX

A neumorphic theme for [Home Assistant](https://www.home-assistant.io/) that brings soft shadows, rounded surfaces, and a tactile 3D feel to your dashboards.

## Screenshots

### Light
![morphhomex-light](screenshots/MorphHomeX%20Light.png)
![morphhomex-light-inset](screenshots/MorphHomeX%20Light%20Inset.png)

### Dark
![morphhomex-dark](screenshots/MorphHomeX%20Dark.png)
![morphhomex-dark-inset](screenshots/MorphHomeX%20Dark%20Inset.png)

## Theme variants

MorphHomeX ships with **10 theme variants** across two styles:

| Style | Light | Dark | Dark Taupe | Dark Graphite | Dark Ash |
|-------|-------|------|------------|---------------|----------|
| **Raised** | `morphhomex-light` | `morphhomex-dark` | `morphhomex-dark-taupe` | `morphhomex-dark-graphite` | `morphhomex-dark-ash` |
| **Inset** | `morphhomex-light-inset` | `morphhomex-dark-inset` | `morphhomex-dark-taupe-inset` | `morphhomex-dark-graphite-inset` | `morphhomex-dark-ash-inset` |

- **Raised** variants give cards and elements a soft, extruded look — the classic neumorphic style.
- **Inset** variants flip the effect so elements appear pressed into the surface.

> [!NOTE]
> **Inset themes and the Settings page**
>
> The inset theme variants do not apply to the main Settings page. The Settings page is part of Home Assistant's core UI and is rendered differently from dashboard views, which means theme tools like card-mod cannot reach it. Every other page — including all dashboard views and all Settings sub-pages — themes correctly.

## Prerequisites

- **Home Assistant** 2023.9.0 or newer
- **[card-mod](https://github.com/thomasloven/lovelace-card-mod)** — install it through HACS before installing MorphHomeX

## Installation

### HACS (recommended)

1. Open HACS in your Home Assistant instance.
2. Go to **Frontend** (the three-dot menu in the top right).
3. Select **Custom repositories**.
4. Add the URL of this repository ( https://github.com/robex2005/MorphHomeX ) and choose **Theme** as the category.
5. Search for **MorphHomeX** in HACS and install it.
6. Restart Home Assistant.

### Manual

1. Download the `themes/` folder from this repository.
2. Copy `morphhomex.yaml` and `morphhomex-inset.yaml` into your Home Assistant `config/themes/` directory.
3. Restart Home Assistant.

## Configuration

Make sure your `configuration.yaml` includes the frontend integration with the card-mod resource:

```yaml
frontend:
  themes: !include_dir_merge_named themes
  extra_module_url:
    - /hacsfiles/lovelace-card-mod/card-mod.js
```

After restarting, go to **Settings → General** and pick a MorphHomeX variant from the **Theme** dropdown — or set it per-dashboard in the dashboard settings.

## Variant details

### Raised (default neumorphic)
- `morphhomex-light` — light raised neumorphic (bg #f0f0f0, accent indigo)
- `morphhomex-dark` — dark raised neumorphic (bg #1e2128, accent teal)
- `morphhomex-dark-taupe` — warm dark raised (bg #26211e, accent copper)
- `morphhomex-dark-graphite` — deep dark raised (bg #121212, accent blue)
- `morphhomex-dark-ash` — medium dark raised (bg #1e1e1e, accent blue)

### Inset (recessed elements)
- `morphhomex-light-inset` — light inset neumorphic
- `morphhomex-dark-inset` — dark inset neumorphic
- `morphhomex-dark-taupe-inset` — warm dark inset
- `morphhomex-dark-graphite-inset` — deep dark inset
- `morphhomex-dark-ash-inset` — medium dark inset

## License

MIT
