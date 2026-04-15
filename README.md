# AI Skills for Reaviz Projects

A collection of Claude Code skills providing AI-assistant reference guides for Reaviz ecosystem libraries. Skills contain component APIs, usage patterns, theming details, and code examples derived from source code and stories.

Each library lives in its own directory under the repo root. To add a new library, create a `<library>/` directory with a top-level `SKILL.md` and per-component skills underneath.

## Structure

```
skills/
├── README.md
└── reablocks/
    ├── SKILL.md                        # Library overview, theming, common rules
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
    ├── typography/
    │   └── SKILL.md                    # Typography: H1-H6, P, BlockQuote, Lead, Large, Small, Muted
    └── data/
        ├── SKILL.md                    # Data category overview
        ├── data-size/SKILL.md          # DataSize + formatSize
        ├── date-format/SKILL.md        # DateFormat (absolute, relative, toggle)
        ├── duration/SKILL.md           # Duration + formatDuration
        ├── ellipsis/SKILL.md           # Ellipsis (character/line truncation)
        ├── infinity-list/SKILL.md      # InfinityList + useInfinityList hook
        ├── pager/SKILL.md              # Pager (pagination controls)
        ├── pluralize/SKILL.md          # Pluralize + pluralize utility
        ├── redact/SKILL.md             # Redact (mask sensitive content)
        └── sort/SKILL.md              # Sort (column header with direction)
```

## Libraries

### Reablocks (`reablocks/`)

React UI component library with 50+ components built on Tailwind CSS and Framer Motion.

| Category | Components |
|----------|------------|
| **Elements** | Avatar, AvatarGroup, Badge, Button, Chip, CommandPalette, IconButton, Kbd, Loader, Navigation, Skeleton |
| **Form** | Calendar, Checkbox, DateInput, Input, Radio, Range, Select, Textarea, Toggle |
| **Layout** | Breadcrumbs, Card, Collapse, Divider, Field, List, Motion, Stepper, Tabs, Tree |
| **Layers** | Backdrop, Callout, ConfirmDialog, ContextMenu, Dialog, Drawer, Menu, Notification, Popover, Tooltip |
| **Typography** | H1-H6, P, BlockQuote, Lead, Large, Small, Muted |
| **Data** | DataSize, DateFormat, Duration, Ellipsis, InfinityList, Pager, Pluralize, Redact, Sort |

## Usage

These skills are automatically loaded by Claude Code when working in projects that reference the corresponding library. They provide contextual guidance on component APIs, props, theming, and best practices.

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
