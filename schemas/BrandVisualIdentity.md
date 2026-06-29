
## JSON Schema
```
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "title": "BrandVisualIdentity",
  "description": "Defines the core visual identity system for a brand, including color palettes, typography scales, layout spacing, asset paths, and compliance levels as specified in the design documentation.",
  "type": "object",
  "required": [
    "@type",
    "validFrom",
    "validTo",
    "colorPrimary",
    "colorSecondary",
    "colorNeutral",
    "typographyH1FontFamily",
    "typographyH1FontSize",
    "typographyBodyFontFamily",
    "typographyBodyFontSize"
  ],
  "properties": {
    "@type": {
      "description": "The schema type identifier.",
      "type": "string",
      "const": "BrandVisualIdentity"
    },
    "validFrom": {
      "description": "The start date from which this visual identity version is effective.",
      "type": "string",
      "format": "date"
    },
    "validTo": {
      "description": "The expiration date of this visual identity version.",
      "type": "string",
      "format": "date"
    },
    "colorPrimary": {
      "description": "The brand's dominant primary color in CSS RGB format.",
      "type": "string",
      "pattern": "^rgb\\(\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*,\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*,\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*\\)$"
    },
    "colorSecondary": {
      "description": "The brand's secondary accent color in CSS RGB format.",
      "type": "string",
      "pattern": "^rgb\\(\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*,\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*,\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*\\)$"
    },
    "colorTertiary": {
      "description": "An optional tertiary accent color for highlight elements, in CSS RGB format.",
      "type": "string",
      "pattern": "^rgb\\(\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*,\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*,\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*\\)$"
    },
    "colorNeutral": {
      "description": "The canvas, background, or body text neutral shade in CSS RGB format.",
      "type": "string",
      "pattern": "^rgb\\(\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*,\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*,\\s*([0-1]?\\d{1,2}|2[0-4]\\d|25[0-5])\\s*\\)$"
    },
    "colorSuccess": {
      "description": "System UI status color indicating positive operations.",
      "type": "string"
    },
    "colorWarning": {
      "description": "System UI status color indicating caution.",
      "type": "string"
    },
    "colorError": {
      "description": "System UI status color indicating failure or danger.",
      "type": "string"
    },
    "colorDarkPrimary": {
      "description": "The inverted primary canvas variant optimized for dark mode interfaces.",
      "type": "string"
    },
    "colorDarkNeutral": {
      "description": "The inverted neutral layout variant optimized for dark mode typography/surfaces.",
      "type": "string"
    },
    "typographyH1FontFamily": {
      "description": "The designated font stack for primary page headers (H1).",
      "type": "string"
    },
    "typographyH1FontSize": {
      "description": "The sizing unit for H1 elements.",
      "type": "string",
      "pattern": "^\\d+(px|rem|em)$"
    },
    "typographyH1FontWeight": {
      "description": "The font weight descriptor for H1 typography.",
      "type": "string"
    },
    "typographyH2FontFamily": {
      "description": "The designated font stack for subheaders (H2).",
      "type": "string"
    },
    "typographyH2FontSize": {
      "description": "The sizing unit for H2 elements.",
      "type": "string",
      "pattern": "^\\d+(px|rem|em)$"
    },
    "typographyH2FontWeight": {
      "description": "The font weight descriptor for H2 typography.",
      "type": "string"
    },
    "typographyH3FontFamily": {
      "description": "The designated font stack for section titles (H3).",
      "type": "string"
    },
    "typographyH3FontSize": {
      "description": "The sizing unit for H3 elements.",
      "type": "string",
      "pattern": "^\\d+(px|rem|em)$"
    },
    "typographyH3FontWeight": {
      "description": "The font weight descriptor for H3 typography.",
      "type": "string"
    },
    "typographyBodyFontFamily": {
      "description": "The primary legibility font stack applied to long-form body paragraphs.",
      "type": "string"
    },
    "typographyBodyFontSize": {
      "description": "The sizing unit for standard body text.",
      "type": "string",
      "pattern": "^\\d+(px|rem|em)$"
    },
    "typographyBodyFontWeight": {
      "description": "The standard body weight descriptor.",
      "type": "string"
    },
    "typographyButtonFontSize": {
      "description": "The sizing unit allocated specifically for interactive UI triggers.",
      "type": "string"
    },
    "typographyButtonFontWeight": {
      "description": "The font weight dedicated to action links and button components.",
      "type": "string"
    },
    "spacingBaseUnit": {
      "description": "The foundational geometric increment underpinning layout calculations (e.g., '4px').",
      "type": "string"
    },
    "borderRadiusSmall": {
      "description": "Corner clipping boundary for micro-elements like tags or badges.",
      "type": "string"
    },
    "borderRadiusMedium": {
      "description": "Standard container layout rounding applied to inputs, alerts, and buttons.",
      "type": "string"
    },
    "borderRadiusLarge": {
      "description": "Extended corner treatment targeted for modal layouts and surface structural blocks.",
      "type": "string"
    },
    "breakpointMobile": {
      "description": "Maximum width threshold defining mobile viewport adaptations.",
      "type": "string"
    },
    "breakpointTablet": {
      "description": "Maximum width threshold defining responsive tablet viewports.",
      "type": "string"
    },
    "breakpointDesktop": {
      "description": "Minimum design canvas baseline targeted for responsive grid scaling.",
      "type": "string"
    },
    "logoPathPrimary": {
      "description": "Relative storage system or CDN pointer referencing the default brand asset logomark.",
      "type": "string"
    },
    "logoPathDark": {
      "description": "Inverted asset variation optimized exclusively for high contrast execution against dark structural fields.",
      "type": "string"
    },
    "faviconPath": {
      "description": "Asset URI mapping standard contextual system navigation layout icons.",
      "type": "string"
    },
    "wcagComplianceLevel": {
      "description": "The baseline digital product accessibility requirement threshold targeting WCAG constraints.",
      "type": "string",
      "enum": ["A", "AA", "AAA"]
    }
  }
}
```
