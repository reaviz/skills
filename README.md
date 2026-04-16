# AI Skills for Reaviz Projects

A collection of Claude Code skills providing AI-assistant reference guides for Reaviz ecosystem libraries. Skills contain component APIs, usage patterns, theming details, and code examples derived from source code and stories.

Each library lives in its own directory under the repo root. To add a new library, create a `<library>/` directory with a top-level `SKILL.md` and per-component skills underneath.

## Structure

```
skills/
├── README.md
├── reagraph/
│   ├── SKILL.md                        # Library overview, data shapes, setup
│   ├── graph/
│   │   ├── SKILL.md                    # Graph category overview
│   │   ├── graph-canvas/SKILL.md       # GraphCanvas (main entry, all props, ref methods)
│   │   ├── nodes/SKILL.md             # Sphere, SphereWithIcon, SphereWithSvg, Svg, Badge
│   │   ├── edges/SKILL.md             # Edge config, arrows, dashed, curved, aggregation
│   │   ├── labels/SKILL.md            # Label visibility, fonts, styling
│   │   └── clusters/SKILL.md          # Cluster grouping, custom rendering
│   ├── layout/
│   │   ├── SKILL.md                    # Layout category overview
│   │   └── layouts/SKILL.md           # 16 layout algorithms + custom + overrides
│   ├── interaction/
│   │   ├── SKILL.md                    # Interaction category overview
│   │   ├── selection/SKILL.md         # useSelection, lasso, single/multi/path
│   │   ├── camera/SKILL.md            # CameraControls, modes, centering, zoom
│   │   ├── context-menu/SKILL.md      # RadialMenu, RadialSlice
│   │   └── collapse/SKILL.md          # useCollapse, expand/collapse hierarchies
│   └── styling/
│       ├── SKILL.md                    # Styling category overview
│       ├── themes/SKILL.md            # lightTheme, darkTheme, Theme interface
│       └── sizing/SKILL.md            # SizingType: pagerank, centrality, attribute
├── reaviz/
│   ├── SKILL.md                        # Library overview, data shapes, common patterns
│   ├── common/
│   │   ├── SKILL.md                    # Common category overview
│   │   ├── axis/SKILL.md              # LinearXAxis, LinearYAxis, ticks, labels
│   │   ├── brush-zoom/SKILL.md        # ChartBrush, ChartZoomPan
│   │   ├── color-schemes/SKILL.md     # Named palettes, ColorSchemeType
│   │   ├── gradient-mask/SKILL.md     # Gradient, GradientStop, Mask, Stripes
│   │   ├── gridline/SKILL.md          # GridlineSeries, Gridline, GridStripe
│   │   ├── legend/SKILL.md            # DiscreteLegend, SequentialLegend
│   │   ├── markers/SKILL.md           # LinearValueMarker, RadialValueMarker, MarkLine
│   │   └── tooltip/SKILL.md           # ChartTooltip, TooltipArea, TooltipTemplate
│   └── charts/
│       ├── SKILL.md                    # Charts category overview
│       ├── area-chart/SKILL.md         # AreaChart (standard, grouped, stacked, normalized)
│       ├── bar-chart/SKILL.md          # BarChart (+ stacked, marimekko, histogram, waterfall)
│       ├── bar-list/SKILL.md           # BarList (horizontal ranking bars)
│       ├── bubble-chart/SKILL.md       # BubbleChart (packed circles)
│       ├── funnel-chart/SKILL.md      # FunnelChart (default, layered)
│       ├── gauge/SKILL.md             # LinearGauge, RadialGauge
│       ├── heatmap/SKILL.md           # Heatmap + CalendarHeatmap
│       ├── map/SKILL.md               # Map + MapMarker
│       ├── meter/SKILL.md             # Meter (segmented column strip)
│       ├── pie-chart/SKILL.md         # PieChart (pie, donut, exploded)
│       ├── radar-chart/SKILL.md       # RadarChart (spider, radial axes)
│       ├── sankey/SKILL.md            # Sankey (flow diagram, nodes + links)
│       ├── scatter-plot/SKILL.md      # ScatterPlot (points, bubbles, symbols)
│       ├── sparkline/SKILL.md         # Sparkline, AreaSparkline, BarSparkline, Sonar
│       ├── sunburst-chart/SKILL.md   # SunburstChart (hierarchical radial)
│       ├── tree-map/SKILL.md         # TreeMap (rectangular hierarchical)
│       ├── venn-diagram/SKILL.md    # VennDiagram (venn, euler, starEuler)
│       └── word-cloud/SKILL.md     # WordCloud (tag cloud)
│       └── line-chart/SKILL.md        # LineChart (line-only, no area fill)
└── reablocks/
    ├── SKILL.md                        # Library overview, theming, common rules
    ├── data/
    │   ├── SKILL.md                    # Data category overview
    │   ├── data-size/SKILL.md          # DataSize + formatSize
    │   ├── date-format/SKILL.md        # DateFormat (absolute, relative, toggle)
    │   ├── duration/SKILL.md           # Duration + formatDuration
    │   ├── ellipsis/SKILL.md           # Ellipsis (character/line truncation)
    │   ├── infinity-list/SKILL.md      # InfinityList + useInfinityList hook
    │   ├── pager/SKILL.md              # Pager (pagination controls)
    │   ├── pluralize/SKILL.md          # Pluralize + pluralize utility
    │   ├── redact/SKILL.md             # Redact (mask sensitive content)
    │   └── sort/SKILL.md              # Sort (column header with direction)
    ├── elements/
    │   ├── SKILL.md                    # Elements category overview
    │   ├── avatar/SKILL.md             # Avatar + AvatarGroup
    │   ├── badge/SKILL.md              # Badge
    │   ├── button/SKILL.md             # Button + ButtonGroup
    │   ├── chip/SKILL.md               # Chip (badge/tag types)
    │   ├── command-palette/SKILL.md    # CommandPalette + Section + Item
    │   ├── icon-button/SKILL.md        # IconButton
    │   ├── kbd/SKILL.md                # Kbd (keyboard shortcuts)
    │   ├── loader/SKILL.md             # DotsLoader
    │   ├── navigation/SKILL.md         # NavigationBar + NavigationButton
    │   └── skeleton/SKILL.md           # Skeleton
    ├── form/
    │   ├── SKILL.md                    # Form category overview
    │   ├── calendar/SKILL.md           # Calendar (dates, ranges, time, presets)
    │   ├── checkbox/SKILL.md           # Checkbox (animated SVG, intermediate)
    │   ├── date-input/SKILL.md         # DateInput (input + calendar popup)
    │   ├── input/SKILL.md              # Input + DebouncedInput + InlineInput
    │   ├── radio/SKILL.md              # Radio + RadioGroup
    │   ├── range/SKILL.md              # RangeSingle + RangeDouble
    │   ├── select/SKILL.md             # Select (single, multi, creatable)
    │   ├── textarea/SKILL.md           # Textarea (auto-resize)
    │   └── toggle/SKILL.md             # Toggle (on/off switch)
    ├── layout/
    │   ├── SKILL.md                    # Layout category overview
    │   ├── breadcrumbs/SKILL.md        # Breadcrumbs (composable sub-components)
    │   ├── card/SKILL.md               # Card (container with header)
    │   ├── collapse/SKILL.md           # Collapse (animated expand/collapse)
    │   ├── divider/SKILL.md            # Divider (horizontal/vertical)
    │   ├── field/SKILL.md              # Field (label, hint, error wrapper)
    │   ├── list/SKILL.md               # List + ListItem + ListHeader
    │   ├── motion/SKILL.md             # MotionGroup + MotionItem
    │   ├── stepper/SKILL.md            # Stepper + Step (dots/numbered)
    │   ├── tabs/SKILL.md               # Tabs + TabList + Tab + TabPanel
    │   └── tree/SKILL.md               # Tree + TreeNode
    ├── layers/
    │   ├── SKILL.md                    # Layers category overview
    │   ├── backdrop/SKILL.md           # Backdrop
    │   ├── callout/SKILL.md            # Callout (+ Success/Error/Warning/Info variants)
    │   ├── confirm-dialog/SKILL.md     # ConfirmDialog + useConfirmDialog
    │   ├── context-menu/SKILL.md       # ContextMenu (right-click)
    │   ├── dialog/SKILL.md             # Dialog + slots + useDialog
    │   ├── drawer/SKILL.md             # Drawer + slots + useDrawer
    │   ├── menu/SKILL.md               # Menu (dropdown)
    │   ├── notification/SKILL.md       # Notifications + useNotification
    │   ├── popover/SKILL.md            # Popover (click-triggered)
    │   └── tooltip/SKILL.md            # Tooltip (hover, delays, follow-cursor)
    └── typography/
        └── SKILL.md                    # Typography (headings, text styles)
```

## Libraries

### Reagraph (`reagraph/`)

WebGL node-based graph visualization for React built on Three.js and D3.

| Category | Components |
|----------|------------|
| **Graph** | GraphCanvas, Sphere, SphereWithIcon, SphereWithSvg, Svg, Badge, Edge, Arrow, Label, Cluster |
| **Layout** | forceDirected2d/3d, circular, concentric, tree, radial, hierarchical, nooverlap, forceatlas2, custom |
| **Interaction** | useSelection, Lasso, CameraControls, useCenterGraph, RadialMenu, useCollapse |
| **Styling** | lightTheme, darkTheme, SizingType (pagerank, centrality, attribute) |

### Reaviz (`reaviz/`)

React data visualization library built on D3.js and Framer Motion.

| Category | Components |
|----------|------------|
| **Common** | Axis, Gridline, Tooltip, Legend, Gradient, Mask, Brush, ZoomPan, ColorSchemes, ValueMarker, MarkLine |
| **Charts** | AreaChart, BarChart, BarList, BubbleChart, FunnelChart, LinearGauge, RadialGauge, Meter, Heatmap, CalendarHeatmap, LineChart, Map, PieChart, RadarChart, Sankey, ScatterPlot, SparklineChart, AreaSparklineChart, BarSparklineChart, SonarChart, SunburstChart, TreeMap, VennDiagram, WordCloud |

### Reablocks (`reablocks/`)

React UI component library with 50+ components built on Tailwind CSS and Framer Motion.

| Category | Components |
|----------|------------|
| **Data** | DataSize, DateFormat, Duration, Ellipsis, InfinityList, Pager, Pluralize, Redact, Sort |
| **Elements** | Avatar, AvatarGroup, Badge, Button, Chip, CommandPalette, IconButton, Kbd, Loader, Navigation, Skeleton |
| **Form** | Calendar, Checkbox, DateInput, Input, Radio, Range, Select, Textarea, Toggle |
| **Layout** | Breadcrumbs, Card, Collapse, Divider, Field, List, Motion, Stepper, Tabs, Tree |
| **Layers** | Backdrop, Callout, ConfirmDialog, ContextMenu, Dialog, Drawer, Menu, Notification, Popover, Tooltip |
| **Typography** | H1-H6, P, BlockQuote, Lead, Large, Small, Muted |

## Integration with Claude Code (Reablocks example)

Claude Code discovers skills automatically from specific filesystem locations. Choose one of the methods below to make these skills available in your project.

### Option 1: Project-level (recommended for teams)

Copy or symlink the desired library directory into your project's `.claude/skills/` folder:

```bash
# From your project root
mkdir -p .claude/skills

# Symlink the entire reablocks skill tree
ln -s /path/to/reaviz/skills/reablocks .claude/skills/reablocks
```

Skills placed in `.claude/skills/` are committed to version control and shared with all team members.

### Option 2: User-level (personal, all projects)

Copy or symlink skills into `~/.claude/skills/` to make them available across all your projects:

```bash
mkdir -p ~/.claude/skills

# Symlink the library
ln -s /path/to/reaviz/skills/reablocks ~/.claude/skills/reablocks
```

User-level skills are not shared with other team members.

### Option 3: `--add-dir` flag (per-session)

Point Claude Code to this repository at launch. Skills inside `.claude/skills/` of added directories are discovered automatically:

```bash
claude --add-dir /path/to/reaviz/skills
```

This grants file access for the current session only.

### Verifying installation

Once installed, Claude Code will automatically load the relevant `SKILL.md` files when it encounters Reaviz components in your code. You can verify by asking Claude Code about a specific component:

```
> How do I use the reablocks Select component?
```

Claude Code should respond with API details, props, and examples sourced from the skill files.

## Adding Skills

### New component in an existing library

1. Create `<library>/<category>/<component>/SKILL.md` (e.g. `reablocks/form/checkbox/SKILL.md`)
2. Document: import, props table, usage examples (from stories), theme interface, and customization patterns
3. Base all content on actual source files — do not rely on AI knowledge
4. Update the parent category `SKILL.md` if needed

### New library

1. Create a `<library>/` directory at the repo root
2. Add a top-level `<library>/SKILL.md` with library overview, installation, and common patterns
3. Organize component skills into category subdirectories
4. Update this README with the new library entry
