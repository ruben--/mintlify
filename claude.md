# Creating Content with Mintlify Markdown

**A comprehensive guide for Claude when building documentation pages.**

This document serves as a reference for the structure, components, and tone used in our Mintlify documentation. When creating new pages, follow this guide to maintain consistency.

---

## Document Structure

Every documentation page should follow this proven structure (as seen in espen.mdx):

### 1. Frontmatter
```yaml
---
title: "Page Title"
description: "Brief description for SEO and previews"
icon: "icon-name"  # Font Awesome icon name
noindex: "true"    # Optional: prevent search engine indexing
---
```

### 2. Hero Section
- **Bold headline** that captures attention
- **Tagline** with product/feature name and value proposition
- **Hero image** with proper attributes
- **Opening paragraph** explaining the core value

Example:
```markdown
# The End of the Energy Bill as You Know It.

**Espen. Smart energy, made simple.**

<img
  src="/images/espen1.png"
  alt="Energy Flexibility Adapter Box"
  noZoom={true}
  height="300"
  className="rounded-xl"
/>

Espen is the small, smart box that slashes your bill...
```

### 3. "Who it's for" Section
Clear target audience definition. Be specific.

Example:
```markdown
## Who it's for

Perfect for homeowners in **Sweden** with any combination of **solar panels**, a **home battery**, or an **EV charger** who are tired of unpredictable energy bills.
```

### 4. Value Propositions (How it works)
Use a consistent icon-based format:
- ↓ for cost reduction
- ↑ for revenue/growth
- ✓ for ease/completion

Example:
```markdown
## How Espen makes it happen

### ↓ It slashes your bill

Espen's AI constantly monitors hourly prices...\
**Result:** reduce monthly energy costs by **up to 50%**.
```

### 5. Technical Explanation
- Diagram with explanation
- Numbered steps
- Clear, simple language

### 6. App/Dashboard Showcase (if applicable)
- Screenshots in a grid
- CardGroup highlighting key features

### 7. Social Proof
- Real testimonials (or realistic examples)
- Specific metrics and results
- Photos
- CardGroup with key results

### 8. Compatibility/Integration Section
- Logo grid showing supported brands
- Note about additional integrations

### 9. Pricing Section
- Clear pricing table
- Comparison (with/without product)
- Specific numbers and ROI

### 10. Installation/Setup Details
- CardGroup with key information
- Answer: Who, How Long, What's Required, etc.

### 11. Additional Benefits
- Environmental impact
- Secondary advantages

### 12. FAQ Section
- AccordionGroup with common questions
- Cover objections proactively

### 13. Call to Action
- Button or CardGroup linking to next steps

---

## Mintlify Components to Use

### CardGroup and Card

Used for organizing information in a grid layout.

```markdown
<CardGroup cols={2}>
  <Card title="Live View" icon="analytics">
    See exactly where your energy is coming from and going—grid, solar, or battery—in real-time.
  </Card>
  <Card title="Earnings Tracker" icon="dollar-circle">
    Watch your savings and earnings grow day by day with simple, intuitive graphs.
  </Card>
</CardGroup>
```

**Common icon names:**
- `analytics`, `chart-line`, `gauge-high` - for data/metrics
- `dollar-circle`, `piggy-bank`, `money-bill-wave` - for financial
- `bolt`, `plug`, `battery-full` - for energy
- `user-gear`, `screwdriver-wrench` - for technical/setup
- `clock`, `timer`, `hourglass` - for time-related
- `leaf`, `seedling` - for environmental
- `rocket`, `sparkles` - for performance/benefits

### AccordionGroup and Accordion

Used for FAQs and expandable content.

```markdown
<AccordionGroup>
  <Accordion title="Is there a subscription fee?">
    No. The 990 SEK is a one-time hardware cost. Espen's intelligence and updates are included.
  </Accordion>
  <Accordion title="What happens if my internet connection goes down?">
    If your internet connection is lost, Espen will default to a safe mode...
  </Accordion>
</AccordionGroup>
```

### Images

**Single image:**
```markdown
<img
  src="/images/espen1.png"
  alt="Descriptive alt text"
  noZoom={true}
  height="300"
  className="rounded-xl"
/>
```

**Image grid:**
```markdown
<div className="grid grid-cols-1 md:grid-cols-2 gap-4">
![Dashboard screenshot](/images/app-dashboard.png)

![Report screenshot](/images/app-report.png)

</div>
```

**Logo grid:**
```markdown
<div className="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-5 gap-6 items-center">
![SolarEdge](/images/logos/solaredge.svg)

![Tesla](/images/logos/tesla.svg)

![LG](/images/logos/lg.svg)

</div>
```

### Callouts

**Success callout (for testimonials):**
```markdown
<success>
  "I don't understand all the tech, but I understand my bank account. My electricity bill is the lowest it's been in years."\
  — Mikael L., Nacka
</success>
```

**Other callout types:**
- `<info>` - informational
- `<warning>` - caution
- `<tip>` - helpful hint
- `<note>` - general note

### Buttons

```markdown
<Button href="/get-started" variant="primary" className="mt-4">
  Get Espen Today
</Button>
```

### Tables

Use standard markdown tables:

```markdown
| Metric                    | Without Espen  | With Espen    |
| ------------------------- | -------------- | ------------- |
| Avg. Monthly Grid Cost    | 2,500 SEK      | 1,250 SEK     |
| Monthly Grid Earnings     | 0 SEK          | 300 SEK       |
| **Net Monthly Cost/Gain** | **-2,500 SEK** | **-950 SEK**  |
```

---

## Tone of Voice Guidelines

### 1. Be Bold and Confident
- Use strong declarative statements
- "That era is over" (not "That era might be over")
- "This isn't magic; it's just incredibly smart"

### 2. Use Specific Numbers
- "Up to 50%" (not "significantly lower")
- "990 SEK" (not "affordable pricing")
- "Less than one hour" (not "quick")

### 3. Focus on Results
- Always follow features with results
- Use the format: "Feature explanation...\**Result:** specific outcome"

### 4. Make it Personal
- Use "your" frequently
- "Your home can now be an intelligent participant"
- "Your battery shouldn't just store energy"

### 5. Address Objections Directly
- "This isn't a futuristic dream"
- "This isn't magic"
- "Forget paying over 10,000 kr"

### 6. Use Active Voice
- "Espen slashes your bill" (not "Your bill is slashed by Espen")
- "We handle everything" (not "Everything is handled")

### 7. Create Urgency (When Appropriate)
- "Take control before the cold sets in"
- "Start earning today"
- "Turn your storage investment into a high-performing income asset starting now"

---

## Content Patterns to Follow

### Headlines
- Short, punchy, benefit-focused
- Often challenge the status quo
- "The End of the Energy Bill as You Know It"
- "Your Battery Shouldn't Just Store Energy. It Should Make Money"
- "Energy Costs Shouldn't Be Your Biggest Unpredictable Expense"

### Subheadings
- Use descriptive, benefit-oriented language
- "How It Works: The Brains Behind the Savings"
- "A Price That Changes Everything"
- "Works with brands you trust"

### Body Copy
- Keep paragraphs short (2-3 sentences max)
- Use line breaks for emphasis
- Alternate between explanation and impact

### Lists
- Use numbered lists for processes/steps
- Use bullet points sparingly
- Prefer CardGroups for feature lists

---

## Technical Writing Guidelines

### When Explaining Technical Concepts

1. **Start simple:** "Espen isn't magic; it's just incredibly smart"
2. **Use analogies:** "acts as the brain for your solar, battery, and EV charger"
3. **Show the process:** Connect → Analyze → Execute
4. **Provide specifics:** "P1/HAN port", "Nord Pool spot price feed", "FCR-D"

### When Presenting Data

- Always provide context (timeframe, conditions)
- Use realistic examples: "a home with a 10 kWh battery during a winter month"
- Show before/after comparisons in tables
- Include multiple metrics (savings, payback period, ROI)

### When Addressing Technical Audiences

- Don't dumb down unnecessarily
- Use proper terminology (FCR-D, FCR-N, mFRR, arbitrage)
- Explain implications, not just features
- Provide depth in FAQ sections

---

## Common Mistakes to Avoid

### ❌ Don't:
- Use vague language ("many", "some", "various")
- Bury the value proposition
- Make unsubstantiated claims
- Use passive voice excessively
- Create walls of text
- Forget mobile responsiveness (use responsive grids)
- Neglect alt text for images
- Skip the FAQ section

### ✅ Do:
- Use specific numbers and timeframes
- Lead with benefits, follow with features
- Back claims with examples/testimonials
- Use active, engaging language
- Break content into scannable chunks
- Use responsive grid layouts
- Provide descriptive alt text
- Anticipate and answer questions

---

## Formatting Best Practices

### Emphasis
- Use **bold** for key terms and results
- Use *italics* sparingly
- Use `code blocks` for technical terms/commands
- Use > blockquotes for important notes

### Spacing
- Use `---` horizontal rules to separate major sections
- Add blank lines between components
- Use `\` for line breaks within paragraphs when needed

### Links
- Use descriptive link text
- Internal links: `/page-name`
- External links: `https://...`
- Button links for CTAs

---

## SEO and Metadata

### Frontmatter Fields
```yaml
---
title: "Concise, Keyword-Rich Title (50-60 chars)"
description: "Compelling meta description with key benefits (150-160 chars)"
icon: "relevant-icon"
noindex: "true"  # Only if you don't want search engines indexing
---
```

### Content Optimization
- Use H1 for main headline (only one per page)
- Use H2 for major sections
- Use H3 for subsections
- Include keywords naturally in headers and first paragraph
- Add descriptive alt text to all images

---

## Example Template

Here's a minimal template to start from:

```markdown
---
title: "Your Product Name"
description: "Brief compelling description"
icon: "icon-name"
---

# Bold, Benefit-Driven Headline

**Product Name. Clear value proposition.**

<img
  src="/images/hero.png"
  alt="Product description"
  noZoom={true}
  height="300"
  className="rounded-xl"
/>

Opening paragraph that explains the transformation...

---

## Who it's for

Target audience description with **specific** details.

---

## How [Product] makes it happen

### ↓ First Benefit

Explanation of feature and how it works.\
**Result:** specific, measurable outcome.

### ↑ Second Benefit

Explanation of feature and how it works.\
**Result:** specific, measurable outcome.

---

## How It Works: [Descriptive Subtitle]

![Diagram](/images/diagram.png)

1. **Step One:** Description
2. **Step Two:** Description
3. **Step Three:** Description

---

## Social Proof Section

<success>
  "Compelling quote with specific results"\
  — Name, Location/Title
</success>

<CardGroup cols={2}>
  <Card title="Key Metric 1" icon="icon-name">
    Specific number/result
  </Card>
  <Card title="Key Metric 2" icon="icon-name">
    Specific number/result
  </Card>
</CardGroup>

---

## Pricing Section

| Metric        | Without Product | With Product |
| ------------- | --------------- | ------------ |
| Cost/Savings  | X SEK           | Y SEK        |

---

## Frequently Asked Questions

<AccordionGroup>
  <Accordion title="Common question?">
    Clear, helpful answer.
  </Accordion>
</AccordionGroup>

---

## Call to Action

<Button href="/get-started" variant="primary">
  Action Text
</Button>
```

---

## Final Checklist

Before finalizing any documentation page, verify:

- [ ] Frontmatter is complete and accurate
- [ ] Hero section is compelling and clear
- [ ] Target audience is explicitly defined
- [ ] Benefits are specific and measurable
- [ ] Technical explanations are clear
- [ ] Social proof includes real/realistic examples
- [ ] Pricing is transparent and detailed
- [ ] FAQ addresses common objections
- [ ] All images have alt text
- [ ] All links work correctly
- [ ] Mobile layout is considered (responsive grids)
- [ ] Tone is consistent with brand voice
- [ ] No grammatical or spelling errors
- [ ] Call to action is clear and prominent

---

## Quick Reference: Component Syntax

```markdown
# Components Quick Reference

## CardGroup
<CardGroup cols={2}>
  <Card title="Title" icon="icon-name">Content</Card>
  <Card title="Title" icon="icon-name">Content</Card>
</CardGroup>

## Accordion
<AccordionGroup>
  <Accordion title="Question">Answer</Accordion>
</AccordionGroup>

## Image
<img src="/path" alt="description" noZoom={true} height="300" className="rounded-xl" />

## Button
<Button href="/path" variant="primary">Text</Button>

## Callout
<success>Content</success>
<info>Content</info>
<warning>Content</warning>
<tip>Content</tip>

## Grid
<div className="grid grid-cols-1 md:grid-cols-2 gap-4">
Content
</div>

## Logo Grid
<div className="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-5 gap-6 items-center">
![Logo](/path)
</div>
```

---

**Remember:** Consistency is key. When in doubt, reference espen.mdx, savings-pack.mdx, or earnings-pack.mdx as working examples of this structure in action.
