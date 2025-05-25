# Tailwind Font Variations

Tailwind CSS v4 utilities for variable fonts with `variation-setting-*` namespace. Compatible with tailwind-merge.

## Installation

```bash
npm install @spencerwmiles/tailwind-font-variations
```

## Setup

Import the CSS in your main stylesheet:

```css
@import '@spencerwmiles/tailwind-font-variations';
```

## Usage

### Weight Axis (wght)

```html
<!-- Theme values -->
<p class="variation-setting-wght-300">Light text</p>
<p class="variation-setting-wght-400">Normal text</p>
<p class="variation-setting-wght-700">Bold text</p>

<!-- Arbitrary values -->
<p class="variation-setting-wght-[450]">Custom weight</p>
```

### Width Axis (wdth)

```html
<!-- Theme values -->
<p class="variation-setting-wdth-75">Condensed (75%)</p>
<p class="variation-setting-wdth-100">Normal width (100%)</p>
<p class="variation-setting-wdth-125">Expanded (125%)</p>

<!-- Arbitrary values -->
<p class="variation-setting-wdth-[110%]">Custom width</p>
```

### Slant Axis (slnt)

```html
<!-- Theme values -->
<p class="variation-setting-slnt-0">No slant</p>
<p class="variation-setting-slnt-6">6° slant</p>
<p class="variation-setting-slnt-15">15° slant</p>

<!-- Negative slant -->
<p class="-variation-setting-slnt-6">-6° slant</p>

<!-- Arbitrary values -->
<p class="variation-setting-slnt-[8]">8° slant</p>
<p class="-variation-setting-slnt-[10]">-10° slant</p>
```

### Italic Axis (ital)

```html
<p class="variation-setting-ital">Italic on</p>
<p class="variation-setting-no-ital">Italic off</p>
```

### Optical Size Axis (opsz)

```html
<!-- Theme values -->
<p class="variation-setting-opsz-12">Small optical size</p>
<p class="variation-setting-opsz-24">Medium optical size</p>
<p class="variation-setting-opsz-48">Large optical size</p>

<!-- Arbitrary values -->
<p class="variation-setting-opsz-[18]">Custom optical size</p>
```

### Grade Axis (GRAD)

```html
<!-- Theme values -->
<p class="variation-setting-GRAD--25">Low emphasis</p>
<p class="variation-setting-GRAD-0">Normal</p>
<p class="variation-setting-GRAD-200">High emphasis</p>

<!-- Negative grades -->
<p class="-variation-setting-GRAD-50">-50 grade</p>

<!-- Arbitrary values -->
<p class="variation-setting-GRAD-[75]">Custom grade</p>
```

### Custom Axes

For any variable font axis not covered by specific utilities:

```html
<!-- Custom axis with arbitrary name and value -->
<p class="variation-setting-SOFT-[0.7]">Softness axis</p>
<p class="variation-setting-WONK-[1]">Wonky axis</p>
<p class="variation-setting-TEMP-[500]">Temperature axis</p>
```

## Combining Multiple Axes

Multiple font variation utilities stack naturally:

```html
<!-- Simple combinations -->
<p class="variation-setting-wght-700 variation-setting-wdth-75">
  Bold + Condensed
</p>

<!-- Complex combinations -->
<h1 class="variation-setting-wght-800 variation-setting-wdth-125 variation-setting-GRAD-100 variation-setting-opsz-48">
  Heavy + Expanded + High Grade + Large Optical Size
</h1>

<!-- With slant and arbitrary values -->
<p class="variation-setting-wght-600 variation-setting-slnt-6 variation-setting-GRAD-[75]">
  Semibold + 6° Slant + Custom Grade
</p>
```

## Transitions

Smooth animations between font variation states using Tailwind's transition system:

```html
<!-- Basic font variation transitions -->
<p class="transition-font-variations duration-300 ease-in-out hover:variation-setting-wght-700">
  Smooth weight transition on hover
</p>

<p class="transition-font-variations duration-500 ease-out hover:variation-setting-wdth-125">
  Slow width transition on hover
</p>

<!-- Combine with other transition properties -->
<p class="transition-all transition-font-variations hover:variation-setting-wght-700 hover:scale-110">
  Transition font variations and transform together
</p>

<!-- Complex hover effects -->
<p class="transition-font-variations duration-200 hover:variation-setting-wght-700 hover:variation-setting-GRAD-100">
  Weight and grade change on hover
</p>
```

## Reset Utility

Reset all font variations to default:

```html
<p class="variation-setting-wght-700 variation-setting-wdth-75 variation-setting-reset">
  All variations reset to normal
</p>
```

## Responsive Design

Use with Tailwind's responsive prefixes:

```html
<p class="variation-setting-wght-400 md:variation-setting-wght-700 lg:variation-setting-wght-900">
  Responsive weight changes
</p>

<p class="variation-setting-wdth-75 sm:variation-setting-wdth-100 lg:variation-setting-wdth-125">
  Responsive width changes
</p>
```

## Supported Axes

- **wght** (Weight): 100-900, controls font weight
- **wdth** (Width): 50%-200%, controls font width/stretch  
- **slnt** (Slant): -15° to 15°, controls font slant
- **ital** (Italic): 0-1, controls italic on/off
- **opsz** (Optical Size): 8-144pt, optimizes for display size
- **GRAD** (Grade): -200 to 300, controls emphasis/thickness
- **CASL** (Casual): 0-1, casual style axis
- **CRSV** (Cursive): 0-1, cursive style axis  
- **MONO** (Monospace): 0-1, monospace axis
- Plus support for any custom axes


## License

MIT License - see LICENSE file for details. 