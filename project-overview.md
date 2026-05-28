Act as an expert frontend developer and SEO specialist. Build a production-ready, single-page web utility application called "Freelance Fee Split & Invoice Calculator". 

The core purpose of this tool is to help global freelancers calculate platform transaction fees for Stripe and PayPal, featuring a toggleable "Reverse Mode" (How much to invoice a client to receive exactly X amount after fees). 

### 1. Technical Framework & Constraints
- Language: Semantic HTML5, CSS3 (Tailwind CSS preferred via CDN), and vanilla ES6+ JavaScript.
- Architecture: 100% Client-side. No databases, no external API keys, and no server-side backend required. All math must be executed instantly in the browser.
- Assets: Do not use any external image files. Use standard system fonts and lucide-react / SVG code inline for UI icons.
- Responsiveness: Designed strictly mobile-first. UI must be clean, responsive, and cross-browser compatible.

### 2. UI Layout & Visual Architecture (Top-to-Bottom)
- HEADER: Clean, professional layout with a main title ("Freelance Invoice Fee Calculator") and a one-sentence descriptive subtitle.
- PLATFORM SELECTOR: A beautifully stylized segmented control tab to switch seamlessly between [Stripe] and [PayPal].
- CALCULATOR CARD: A main dashboard area containing:
  - Input Field: "Amount" (Numeric input, pre-filled with 1000).
  - Mode Toggle Switch: A clean checkbox/toggle selector to switch between:
      a) "Standard Mode" (Calculate take-home pay from a gross payment)
      b) "Invoice Mode" (Reverse calculation: What to charge to walk away with this exact amount net)
  - Variable Options (Checkboxes/Select elements matching current 2026 fee tiers):
    * For Stripe:
      - Location: Dropdown [Domestic/US (2.9%), International (+1.5%)]
      - Currency Conversion: Checkbox [Apply FX Conversion (+1%)]
      - Billing Type: Checkbox [Stripe Invoicing Feature (+0.4%)]
    * For PayPal:
      - Payment Type: Dropdown [PayPal Checkout/Invoices (3.49% + $0.49), Standard Card (2.99% + $0.49), Standard Goods & Services (2.99% flat)]
      - Location: Dropdown [Domestic, International Cross-Border (+1.50%)]
- OUTPUT RESUTS DISPLAY Panel: A prominent, visually highlighted card showing:
  - Total Processing Fee ($)
  - Net Take-Home Pay ($)
  - Total Suggested Invoice Amount ($)
- ADSENSE PLACEHOLDERS: Inject explicitly labeled semantic layout elements to map out future ad placements. 
  - Place a 728x90 banner placeholder directly above the calculator interface.
  - Place a responsive banner placeholder right below the Output Results panel.

### 3. Financial Logic & Mathematical Formulas
Ensure all calculations run in real-time on every input input or toggle event without lagging.
- Fixed Fees: Stripe uses $0.30 domestic. PayPal uses $0.49 for merchant checkouts.
- Standard Calculation: 
  Fee = (Gross * Percentage) + FixedFee
  Net = Gross - Fee
- Reverse Calculation ("Invoice Mode"):
  To get the target net amount, reverse the math isolating the Gross variable:
  Gross = (TargetNet + FixedFee) / (1 - TotalPercentageAsDecimal)
- Add percentages cumulatively based on the checked variable configurations selected by the user. Round all terminal outputs strictly to 2 decimal places (.toFixed(2)).
### 4. SEO Wrapping Content (Crucial for AdSense Approval)
To prevent "Low Value / Thin Content" rejections from Google AdSense, generate high-quality educational text beneath the calculator using clean Markdown typography:
- "How to Use This Tool": 3 simple bullet points.
- "Understanding Platform Processing Fees": Clear, detailed explanations comparing Stripe's flat 2.9% + $0.30 structure to PayPal's 3.49% invoice tier.
- "The Reverse Invoice Formula": Write out the mathematical logic behind how the reverse calculation isolates target net income.
- "Frequently Asked Questions": Build a structured accordion or text block answering:
  1. What is the cheapest way to accept freelance payments?
  2. Who pays the Stripe transaction fee, the client or the freelancer?
  3. How do international currency conversions impact final payout numbers?

### 5. Delivery Requirements
Output the complete, fully formed layout in a single file or a clean split block set (HTML, CSS, JS). Do not use placeholders like "// Add code here later" or write incomplete loops. Provide the final raw code blocks cleanly.