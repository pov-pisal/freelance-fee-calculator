# Freelance Fee Split & Invoice Calculator

A production-ready, single-page web utility application for global freelancers to calculate platform transaction fees and invoice amounts instantly.

## Features

✨ **Core Functionality**
- **Platform Support**: Calculate fees for both Stripe and PayPal
- **Dual Calculation Modes**: 
  - Standard Mode: Calculate net take-home from a gross payment
  - Invoice Mode (Reverse): Determine exact client invoice amount to keep your target net income
- **Multi-Currency Support**: USD, EUR, GBP, JPY, AUD, CAD, INR
- **Dynamic Fee Configuration**:
  - **Stripe**: Location selection (Domestic/International), FX conversion, Invoicing feature
  - **PayPal**: Payment type selection, Cross-border support

🔒 **Security & Reliability**
- 100% Client-side processing (no backend, no external APIs, no data collection)
- Input validation with automatic sanitization (removes commas, currency symbols, multiple decimals)
- Edge case protection (prevents negative payouts)
- Smart warning system for amounts below minimum thresholds

🎨 **User Experience**
- Mobile-first responsive design
- Copy-to-clipboard buttons for quick invoice use
- Real-time calculation on every input change
- Clear visual feedback (success message on copy)
- Professional gradient UI with smooth transitions
- Updated fee badge showing "Fees updated for 2026"

📱 **AdSense Ready**
- Comprehensive SEO content (How-to guide, Formula explanations, FAQ)
- High-quality educational content for Google AdSense approval
- WCAG accessibility compliance (proper contrast, readable typography)
- AdSense placeholder integration for ad placement planning

## Technical Stack

- **HTML5**: Semantic markup with SEO-optimized structure
- **CSS3**: Tailwind CSS (via CDN) with custom styling
- **JavaScript**: Vanilla ES6+ (no frameworks, zero dependencies)
- **Architecture**: 100% client-side, no server required

## Fee Structure (2026)

### Stripe
- Domestic (US): 2.9% + $0.30
- International: 2.9% + $0.30 + 1.5%
- Currency Conversion: +1%
- Invoicing Feature: +0.4%

### PayPal
- Checkout/Invoices: 3.49% + $0.49
- Standard Card: 2.99% + $0.49
- Goods & Services: 2.99% flat
- International Cross-Border: +1.5%

## Usage

1. Open `index.html` in any modern web browser
2. Select your payment platform (Stripe or PayPal)
3. Choose your currency and enter the amount
4. Configure platform-specific options (location, payment type, features)
5. Toggle between Standard and Invoice Mode as needed
6. Use the Copy button to save results to clipboard

## Mathematical Formulas

### Standard Mode (Gross → Net)
```
Fee = (Gross × Percentage) + FixedFee
Net = Gross − Fee
```

### Inverse Mode (Net → Invoice)
```
Gross = (TargetNet + FixedFee) / (1 − TotalPercentageAsDecimal)
```

## Browser Compatibility

- Chrome/Chromium 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile browsers (iOS Safari, Chrome Mobile)

## Files

- `index.html` - Complete single-file application (HTML, CSS, JavaScript)
- `.gitignore` - Git ignore rules
- `README.md` - This file
- `project-overview.md` - Original project specifications

## License

This project is open source and available for personal and commercial use.

## Support & Contribution

For improvements, bug reports, or feature requests, please open an issue or submit a pull request.

---

**Last Updated**: May 2026  
**Status**: Production Ready ✅
