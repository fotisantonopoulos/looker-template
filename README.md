# Elegant Metric Card - Looker Studio Community Visualization

A sophisticated, professionally designed metric card visualization for Looker Studio featuring elegant typography, smooth animations, and a refined color palette.

## Design Features

- **Elegant Typography**: Combines Cormorant Garamond serif for dramatic impact with Montserrat sans-serif for clarity
- **Sophisticated Color Palette**: Uses cream (#fbfbf9), vibrant yellow (#ffeb00), and deep charcoal (#282829)
- **Smooth Animations**: Carefully orchestrated entrance animations with staggered timing
- **Professional Styling**: Clean shadows, subtle hover effects, and refined spacing
- **Responsive Design**: Adapts beautifully to different screen sizes

## Installation

### Method 1: Using Looker Studio Community Visualizations

1. Go to [Looker Studio](https://lookerstudio.google.com/)
2. Open your report or create a new one
3. Click **Add a chart** → **Community visualizations and components**
4. Click **Explore more** → **Build your own visualization**
5. Click **+ Create a new component**
6. Upload the `manifest.json` and `looker-viz.html` files
7. Submit for approval (for personal use, you can use in dev mode)

### Method 2: Development Mode (Quickest)

1. Host the files on a web server (GitHub Pages, Firebase Hosting, etc.)
2. In Looker Studio, add a community visualization
3. Click **Explore more** → **Build your own**
4. Enter the manifest URL
5. Add to your report

## Configuration

### Data Fields

The visualization accepts the following data fields:

- **Metric Value** (required): The primary metric to display (e.g., revenue, user count)
- **Change Percentage** (optional): Percentage change from previous period
- **Metric Label** (optional): Custom label for the metric (defaults to "Total Revenue")
- **Description Text** (optional): Supporting description text

### Style Options

Customize the visualization with these options:

- **Primary Color**: Accent color for highlights (default: #ffeb00)
- **Secondary Color**: Text and emphasis color (default: #282829)
- **Background Color**: Card background (default: #fbfbf9)
- **Value Font Size**: Choose from Small, Medium, Large, or Extra Large
- **Enable Animations**: Toggle entrance animations on/off

## Usage Examples

### Basic Revenue Metric
```
Metric Value: SUM(revenue)
Change Percentage: (SUM(revenue) - SUM(previous_revenue)) / SUM(previous_revenue) * 100
Metric Label: "Total Revenue"
Description: "Outstanding performance this quarter"
```

### User Growth Metric
```
Metric Value: COUNT(DISTINCT user_id)
Change Percentage: User growth rate
Metric Label: "Active Users"
Description: "Monthly active users across all platforms"
```

### Conversion Rate
```
Metric Value: Conversion_Rate
Change Percentage: Change in conversion rate
Metric Label: "Conversion Rate"
Description: "Improvement in user acquisition efficiency"
```

## Customization

### Changing Colors

The visualization uses CSS custom properties. To modify colors:

1. Open `looker-viz.html`
2. Locate the `:root` section in the `<style>` tag
3. Update the color values:
```css
:root {
  --color-cream: #fbfbf9;   /* Background/cream color */
  --color-yellow: #ffeb00;   /* Accent/highlight color */
  --color-dark: #282829;     /* Text/dark color */
}
```

### Adjusting Typography

To change fonts:

1. Update the Google Fonts import link in the `<head>` section
2. Modify the font-family declarations in CSS
3. Adjust font sizes in the respective classes

### Animation Timing

To adjust animation speed:
- Locate `@keyframes` and animation properties in CSS
- Modify duration values (e.g., `0.8s` to `1.2s` for slower)
- Adjust `animation-delay` for staggered timing

## Browser Compatibility

- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support
- Mobile browsers: Responsive design adapts automatically

## Performance

The visualization is optimized for performance:
- CSS-only animations (no JavaScript animation libraries)
- Minimal DOM manipulation
- Efficient number formatting
- Smooth 60fps animations

## Support

For issues or questions:
1. Check that your data fields are correctly mapped
2. Verify the manifest.json is properly configured
3. Ensure files are hosted and accessible
4. Check browser console for any errors

## License

This community visualization is provided as-is for use in Looker Studio reports.

## Credits

Design: Professional Analytics Team
Fonts: Cormorant Garamond (Google Fonts), Montserrat (Google Fonts)
