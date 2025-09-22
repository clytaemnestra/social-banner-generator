# Platform Banner Configurations

This file contains all supported platforms with their dimensions, safe areas, and specific requirements.

## Supported Platforms

### Social Media Platforms

#### Twitter/X
- **Dimensions:** 1500 x 500 px
- **Logo Display:** Circle (uploaded as square)
- **Safe Area:** x: 600, y: 0, width: 900, height: 500
- **Template:** twitter-header-1500x500px-safe-area-template.svg
- **Notes:** Use safe-area template to not overlap with the logo
- **Status:** ✅ Implemented

#### Mastodon
- **Dimensions:** 1500 x 500 px
- **Logo Display:** Square
- **Safe Area:** x: 600, y: 0, width: 900, height: 500
- **Template:** mastodon-cover-1500x500px-safe-area-template.svg
- **Notes:** Use safe-area template to not overlap with the logo
- **Status:** ✅ Implemented

#### Bluesky
- **Dimensions:** 1500 x 500 px
- **Logo Display:** Circle (uploaded as square)
- **Safe Area:** Full canvas (centered logo)
- **Notes:** Same as Twitter
- **Status:** ✅ Implemented

#### Instagram
- **Dimensions:** No banner
- **Logo Display:** Circle (uploaded as square)
- **Status:** ❌ No banner support needed

#### TikTok
- **Dimensions:** No banner needed
- **Logo Display:** Square
- **Status:** ❌ No banner support needed

#### LinkedIn Company
- **Dimensions:** 1128 x 191 px
- **Logo Display:** Square
- **Safe Area:** x: 300, y: 0, width: 828, height: 191
- **Template:** linkedin-company-header-1128x191px-safe-area-template.svg
- **Notes:** Use safe-area template to not overlap with the logo
- **Status:** ✅ Implemented

#### LinkedIn Group
- **Dimensions:** 1774 x 444 px
- **Logo Display:** Square
- **Safe Area:** Full canvas (centered logo)
- **Notes:** No safe area template mentioned
- **Status:** ✅ Implemented

#### YouTube
- **Dimensions:** 2560 x 1440 px
- **Logo Display:** Circle (uploaded as square)
- **Safe Area:** x: 757, y: 423, width: 1046, height: 594
- **Template:** youtube-banners-2560x1440px-safe-areas-template.svg
- **Notes:** Use safe-area template for details (Mobile: 1546x423 safe area)
- **Status:** ✅ Implemented

#### Telegram
- **Dimensions:** No banner
- **Logo Display:** Circle (uploaded as square)
- **Status:** ❌ No banner support needed

#### Facebook
- **Dimensions:** 851 x 315 px
- **Logo Display:** Circle (uploaded as square)
- **Status:** ❌ Excluded as requested

### Developer/Content Platforms

#### Dev.to
- **Dimensions:** 1000 x 420 px
- **Logo Display:** Square
- **Safe Area:** x: 0, y: 0, width: 1000, height: 420 (full canvas)
- **Notes:** Post cover
- **Status:** ✅ Implemented

#### EP Blog
- **Dimensions:** 1900 x 550 px
- **Logo Display:** Square
- **Safe Area:** x: 600, y: 0, width: 1300, height: 550
- **Template:** ep-blog-header-1600x550px-safe-area-template.svg
- **Notes:** Renders responsively (1080p display), use safe-area template for 4k display
- **Additional Info:** Change primary and secondary font colours at https://blog.europython.eu/ghost/#/settings/code-injection
- **Status:** ✅ Implemented

#### Pretalx
- **Dimensions:** 1129 x 191 px
- **Logo Display:** Square
- **Safe Area:** x: 300, y: 0, width: 829, height: 191
- **Template:** pretalx-header-1128x191px-safe-area-template.svg
- **Notes:** Renders responsively, use safe-area template to render correctly on mobile and big screen
- **Status:** ✅ Implemented

### Forms and Utilities

#### Google Form
- **Dimensions:** 1600 x 400 px
- **Logo Display:** Square
- **Safe Area:** x: 0, y: 0, width: 1600, height: 400 (full canvas)
- **Status:** ✅ Implemented

#### Social Cards (Website)
- **Dimensions:** 1686 x 888 px
- **Logo Display:** Square
- **Safe Area:** x: 0, y: 0, width: 1686, height: 888 (full canvas)
- **Status:** ✅ Implemented

### Print/Document Formats

#### A4 Letterhead
- **Dimensions:** 3307 x 630 px (400 DPI)
- **Logo Display:** Square
- **Safe Area:** Full canvas (centered logo)
- **Status:** ✅ Implemented

## Logo vs Banner Distinction

This generator creates **banners** (logo with background) for various platforms. There are two separate use cases:

1. **Logo Only:** Square logo files for direct use
2. **Banner/Header:** Logo placed on colored background for platform headers

This tool handles the second case - creating banners with logos on backgrounds.

### Display Types:
- **Square:** Logo displayed as-is
- **Circle:** Logo displayed in circular crop (uploaded as square)

## Safe Area Guidelines

Safe areas ensure content doesn't overlap with platform UI elements:
- **Full Canvas:** Safe area covers entire banner
- **Custom Safe Area:** Specific rectangular area where content should be placed
- Use provided SVG templates for visual reference

## Implementation Status

✅ **Fully Implemented:** 12 platforms
❌ **Excluded:** 5 platforms (no banners or excluded by request)

## Adding New Platforms

To add a new platform:

1. Update this file with platform specifications
2. Add platform to `platformConfigs` object in `index.html`
3. Add option to platform selector in HTML
4. Include safe area template if available

### Platform Config Format:
```javascript
platform_name: {
    width: [width_in_px],
    height: [height_in_px],
    safeArea: {
        x: [x_offset],
        y: [y_offset],
        width: [safe_width],
        height: [safe_height]
    }
}
```