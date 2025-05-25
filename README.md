# Tailwind Font Variations

## Supported Variable Font Axes

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

## Installation

```bash
npm install @spencerwmiles/tailwind-font-variations
# or
yarn add @spencerwmiles/tailwind-font-variations  
# or
pnpm add @spencerwmiles/tailwind-font-variations
```

## Setup

Import the CSS in your main stylesheet 

```css
@import '@spencerwmiles/tailwind-font-variations';
```

## Usage

### Weight Axis (wght)

```html
<!-- Theme values -->
<p class="font-var-wght-300">Light text</p>
<p class="font-var-wght-400">Normal text</p>
<p class="font-var-wght-700">Bold text</p>

<!-- Semantic utilities -->
<p class="font-var-thin">Thin (100)</p>
<p class="font-var-light">Light (300)</p>
<p class="font-var-normal">Normal (400)</p>
<p class="font-var-bold">Bold (700)</p>
<p class="font-var-black">Black (900)</p>

<!-- Arbitrary values -->
<p class="font-var-wght-[450]">Custom weight</p>
```

### Width Axis (wdth)

```html
<!-- Theme values -->
<p class="font-var-wdth-75">Condensed (75%)</p>
<p class="font-var-wdth-100">Normal width (100%)</p>
<p class="font-var-wdth-125">Expanded (125%)</p>

<!-- Semantic utilities -->
<p class="font-var-condensed">Condensed</p>
<p class="font-var-normal-width">Normal</p>
<p class="font-var-expanded">Expanded</p>

<!-- Arbitrary values -->
<p class="font-var-wdth-[110%]">Custom width</p>
```

### Slant Axis (slnt)

```html
<!-- Theme values -->
<p class="font-var-slnt-0">No slant</p>
<p class="font-var-slnt-6">6° slant</p>
<p class="font-var-slnt-15">15° slant</p>

<!-- Negative slant -->
<p class="-font-var-slnt-6">-6° slant</p>

<!-- Arbitrary values -->
<p class="font-var-slnt-[8]">8° slant</p>
<p class="-font-var-slnt-[10]">-10° slant</p>
```

### Italic Axis (ital)

```html
<p class="font-var-ital">Italic on</p>
<p class="font-var-no-ital">Italic off</p>
```

### Optical Size Axis (opsz)

```html
<!-- Theme values -->
<p class="font-var-opsz-12">Small optical size</p>
<p class="font-var-opsz-24">Medium optical size</p>
<p class="font-var-opsz-48">Large optical size</p>

<!-- Arbitrary values -->
<p class="font-var-opsz-[18]">Custom optical size</p>
```

### Grade Axis (GRAD)

```html
<!-- Theme values -->
<p class="font-var-GRAD--25">Low emphasis</p>
<p class="font-var-GRAD-0">Normal</p>
<p class="font-var-GRAD-200">High emphasis</p>

<!-- Negative grades -->
<p class="font-var--GRAD-50">-50 grade</p>

<!-- Arbitrary values -->
<p class="font-var-GRAD-[75]">Custom grade</p>
```

### Custom Axes

For any variable font axis not covered by specific utilities:

```html
<!-- Custom axis with arbitrary name and value -->
<p class="font-var-SOFT-[0.7]">Softness axis</p>
<p class="font-var-WONK-[1]">Wonky axis</p>
<p class="font-var-TEMP-[500]">Temperature axis</p>
```

## Combining Multiple Axes

Multiple font variation utilities stack naturally:

```html
<!-- Simple combinations -->
<p class="font-var-bold font-var-condensed">
  Bold + Condensed
</p>

<!-- Complex combinations -->
<h1 class="font-var-wght-800 font-var-wdth-125 font-var-GRAD-100 font-var-opsz-48">
  Heavy + Expanded + High Grade + Large Optical Size
</h1>

<!-- With slant and arbitrary values -->
<p class="font-var-semibold font-var-slnt-6 font-var-GRAD-[75]">
  Semibold + 6° Slant + Custom Grade
</p>
```

## Transitions

Smooth animations between font variation states:

```html
<p class="font-var-transition hover:font-var-bold">
  Smooth weight transition on hover
</p>

<p class="font-var-transition-slow hover:font-var-expanded">
  Slow width transition on hover
</p>

<!-- Complex hover effects -->
<p class="font-var-transition hover:font-var-bold hover:font-var-GRAD-100">
  Weight and grade change on hover
</p>
```

## Reset Utility

Reset all font variations to default:

```html
<p class="font-var-bold font-var-condensed font-var-reset">
  All variations reset to normal
</p>
```

## Responsive Design

Use with Tailwind's responsive prefixes:

```html
<p class="font-var-normal md:font-var-bold lg:font-var-black">
  Responsive weight changes
</p>

<p class="font-var-condensed sm:font-var-normal-width lg:font-var-expanded">
  Responsive width changes
</p>

<!-- Complex responsive combinations -->
<h1 class="font-var-light font-var-condensed md:font-var-bold md:font-var-normal-width lg:font-var-black lg:font-var-expanded">
  Progressive enhancement across breakpoints
</h1>
```

## Variable Font Examples

### Google Fonts

```html
<!-- Inter (wght, slnt) -->
<link href="https://fonts.googleapis.com/css2?family=Inter:slnt,wght@-10..0,100..900" rel="stylesheet">
<p style="font-family: Inter" class="font-var-wght-500 font-var--slnt-5">
  Inter Medium Slanted
</p>

<!-- Recursive (wght, CASL, slnt, CRSV, MONO) -->
<link href="https://fonts.googleapis.com/css2?family=Recursive:slnt,wght,CASL,CRSV,MONO@-15..0,300..1000,0..1,0..1,0..1" rel="stylesheet">
<p style="font-family: Recursive" class="font-var-bold font-var-CASL-75 font-var-MONO-50">
  Recursive Bold Casual Semi-Mono
</p>

<!-- Anybody (wght, wdth, slnt) -->
<link href="https://fonts.googleapis.com/css2?family=Anybody:ital,wght@0,100..900;1,100..900" rel="stylesheet">
<p style="font-family: Anybody" class="font-var-semibold font-var-expanded font-var-slnt-3">
  Anybody Semibold Expanded Slanted
</p>
```

### System Fonts

```html
<!-- San Francisco (Apple) -->
<p style="font-family: -apple-system" class="font-var-wght-600 font-var-wdth-90">
  SF Pro Semibold Condensed
</p>
```

## Browser Support

Variable fonts are supported in:
- Chrome 62+
- Firefox 62+  
- Safari 11+
- Edge 17+

For older browsers, fonts fall back to their default appearance.

## API Reference

### Weight Utilities
- `font-var-wght-{100|200|300|400|500|600|700|800|900}`
- `font-var-wght-[value]`
- `font-var-{thin|extralight|light|normal|medium|semibold|bold|extrabold|black}`

### Width Utilities  
- `font-var-wdth-{50|62|75|87|100|112|125|150|175|200}`
- `font-var-wdth-[percentage]`
- `font-var-{ultra-condensed|extra-condensed|condensed|semi-condensed|normal-width|semi-expanded|expanded|extra-expanded|ultra-expanded}`

### Slant Utilities
- `font-var-slnt-{0|3|6|9|12|15}`
- `-font-var-slnt-{3|6|9|12|15}`
- `font-var-slnt-[degrees]`
- `-font-var-slnt-[degrees]`

### Italic Utilities
- `font-var-ital`
- `font-var-no-ital`

### Optical Size Utilities
- `font-var-opsz-{8|10|12|14|16|18|20|24|28|32|36|48|60|72|96|144}`
- `font-var-opsz-[size]`

### Grade Utilities
- `font-var-GRAD-{0|25|50|100|150|200|250|300}`
- `font-var--GRAD-{25|50|100|150|200}`
- `font-var-GRAD-[value]`
- `font-var--GRAD-[value]`

### Custom Axis Utilities
- `font-var-AXIS-[value]` (for any axis name)

### Transition Utilities
- `font-var-transition`
- `font-var-transition-slow`
- `font-var-transition-fast`

### Reset Utility
- `font-var-reset`

## Contributing

Contributions are welcome! This package aims to support all variable font axes and use cases.

## License

MIT License - see LICENSE file for details. 