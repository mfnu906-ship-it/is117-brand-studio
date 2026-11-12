# PUREFORM — T-shirt Research

**Initial research date:** November 5, 2026  
**Source recheck date:** November 11, 2026  
**Project:** PUREFORM  
**Research status:** Competitor pages rechecked and linked below. This is desk research of public retailer pages, not customer interviews, a survey, or sales research.

## 1. Research question and method

**Research question:** How can PUREFORM present an everyday T-shirt so a visitor can understand the product, consider a simple outfit idea, and choose an option without an overwhelming shopping experience?

I reviewed the official US T-shirt or tops pages for UNIQLO, H&M, and Cotton On on November 11, 2026. I recorded what was visible on those pages and then wrote a separate interpretation for PUREFORM. Retailer pages can change, so the date matters. The observations describe the pages, not what all customers think or buy.

## 2. Original sources and observed evidence

### UNIQLO — product-first basics

- **Original source:** [UNIQLO US — Men's T-Shirts](https://www.uniqlo.com/us/en/men/tops/t-shirts)
- **Reviewed:** November 11, 2026
- **Evidence observed:** The page describes its T-shirts as designed for everyday comfort, easy layering, and versatile wear. The page separates short-sleeve and long-sleeve sections and provides sort choices including price low-to-high, price high-to-low, and top rated. It presents examples such as the Crew Neck T-Shirt and AIRism Cotton Oversized T-Shirt.
- **Interpretation:** This is a product-first way to organize basic T-shirts. The page gives visitors a straightforward category and product descriptions before asking them to compare more options.
- **PUREFORM decision:** Keep the first PUREFORM page focused on one white T-shirt, with the product image, product information, and size choices together. Do not turn the first page into a large catalog.
- **What this does not prove:** It does not prove PUREFORM customers want only one style or that a product-first layout will increase sales.

### H&M — breadth of fits and options

- **Original source:** [H&M US — Men's Basic T-Shirts](https://www2.hm.com/en_us/men/products/basics/t-shirts.html)
- **Reviewed:** November 11, 2026
- **Evidence observed:** The category page shows regular-fit, slim-fit, relaxed-fit, and oversized T-shirts. Its accompanying description mentions V-neck and crewneck styles, short and long sleeves, staple and brighter colors, and multipack options.
- **Interpretation:** H&M makes variety visible by offering several fit, style, color, and pack choices in the same category. This gives shoppers more ways to compare, but it also creates more options to scan.
- **PUREFORM decision:** For the current classroom prototype, keep the selection simple: one example shirt with S, M, L, and XL demo size choices. Keep the price and product data clearly labeled as fictional demonstration content.
- **What this does not prove:** The category does not establish which fit or size young adults prefer, and the product assortment is not evidence of demand for PUREFORM.

### Cotton On — styling in everyday situations

- **Original source:** [Cotton On US — Men's Tops](https://cottonon.com/US/co/men/mens-clothing/mens-tops/)
- **Reviewed:** November 11, 2026
- **Evidence observed:** The page has a section titled “How to Style Men’s T-Shirts and Tanks.” It describes outfit combinations such as an essential tee with straight denim and sneakers, or a tee with a hoodie or overshirt. It also gives examples for study, studio, gym, and casual situations.
- **Interpretation:** The retailer does more than list products; it gives context for how a basic tee could be worn in an ordinary day.
- **PUREFORM decision:** Add a short free styling tip and optional style goals to help visitors imagine a simple outfit or match the shirt with clothes they already own. Keep these ideas optional so a visitor can shop without selecting a goal.
- **What this does not prove:** It does not prove PUREFORM visitors need styling advice or that these combinations are preferred by our intended audience.

## 3. Comparison and alternatives

The three pages show different approaches:

- **UNIQLO:** a product-first basics page with sections and concise product descriptions.
- **H&M:** a broad range of fits, colors, sleeve types, and multipacks for comparison.
- **Cotton On:** product categories plus written outfit suggestions linked to everyday situations.

For the first PUREFORM version, I chose a mix of the UNIQLO and Cotton On approaches: keep the product presentation focused, then offer a small amount of optional styling help. I did not copy H&M's broader assortment because the current project is about one T-shirt and a clear first impression, not building a full retailer catalog.

I also considered two brand positions:

- **Affordable everyday basics:** simple T-shirts intended to feel accessible and easy to style. This fits the current PUREFORM brief and Everyman character.
- **Premium minimalist essentials:** minimalist T-shirts presented as more exclusive or higher-priced. I did not choose this because I want PUREFORM to feel friendly and accessible rather than exclusive.

The position is a learner decision, not a result proven by these retailer pages. The fictional product data and demo price on the storefront are not real market-price research.

## 4. Research-to-feature trace

### Finding 1: A focused product page can make the basic item easy to inspect

- **Source finding:** UNIQLO separates T-shirt types and provides short descriptions of the products.
- **Design decision:** PUREFORM uses a single main product area with a large shirt image, short description, and visible size choices.
- **Implementation:** [public/index.html](../public/index.html), product section.
- **Check:** Browser tests cover selecting a size, adding to the demo bag, emptying it, keyboard operation, and narrow-screen layout in [tests/browser/studio.spec.js](../tests/browser/studio.spec.js).
- **Evidence boundary:** These checks show the prototype interactions work; they do not show that customers prefer this layout.

### Finding 2: Too many product variations would expand the current scope

- **Source finding:** H&M presents several fits, colors, sleeve types, and multipack choices on one category page.
- **Design decision:** PUREFORM currently demonstrates one shirt and a short list of size choices rather than a large catalog.
- **Implementation:** [public/index.html](../public/index.html), size selector and fictional product-data disclaimer.
- **Check:** Browser tests verify the size controls and that adding without a size shows an error while leaving the demo bag empty.
- **Evidence boundary:** The current S, M, L, and XL choices are demo controls, not proof that these sizes or a particular fit meet customer needs.

### Finding 3: Outfit examples can make a basic T-shirt easier to imagine in context

- **Source finding:** Cotton On gives examples pairing a tee with denim, sneakers, a hoodie, or an overshirt in study and casual situations.
- **Design decision:** PUREFORM adds the free styling tip “Try a white tee with denim and a layer you already own” and two optional style goals: “Keep my outfit simple” and “Match this with clothes I own.”
- **Implementation:** [public/index.html](../public/index.html), styling tip and optional style-goal controls.
- **Check:** Browser tests verify each goal displays its matching suggestion and that shopping still works with no style goal selected. A peer retry is requested in [Issue #9](https://github.com/mfnu906-ship-it/is117-brand-studio/issues/9).
- **Evidence boundary:** The feature and automated tests show the interaction was implemented and tested. They do not prove that visitors find the tip useful or that the target audience is validated.

## 5. Audience hypotheses

These are planning hypotheses, not customer research.

**Persona A — College student (primary hypothesis)**  
A college student aged 18–25 who attends classes, meets friends, and wants a simple T-shirt that can work with everyday outfits. A possible concern is whether the shirt feels appropriate for different casual situations and fits within a budget.

**Persona B — Young adult building a minimalist wardrobe (secondary hypothesis)**  
A young adult aged 18–25 who prefers a consistent, simple wardrobe and wants versatile basics that coordinate with clothes they already own. A possible concern is whether the shirt works with their existing outfits.

**Chosen audience:** Young adults ages 18–25, especially college students. This is my working audience hypothesis. I have not validated it through customer interviews, a survey, or sales data.

## 6. Brand character, visual direction, and honest persuasion

PUREFORM uses the **Everyman** archetype and a friendly, simple, approachable voice. The intended character is relatable and useful for everyday people, not luxurious or intimidating.

The chosen visual direction is **modernist**: a clean layout, clear hierarchy, simple typography, open spacing, neutral colors, and rust-red accents. The intended benefit is to make the product and shopping information easy to scan. This is a design rationale, not a measured usability result.

PUREFORM should help visitors make an informed choice rather than pressure them. It should not invent reviews, limited stock, discounts, material details, sustainability claims, or product-performance claims. The product data and $28 price shown in the prototype are fictional classroom-demo content.

## 7. Assumptions and open questions

- I assume college students value affordable, easy-to-match basics; I have not validated this with a survey.
- I assume a clean, minimal website will make the product easier to understand; this needs peer or user feedback.
- I have not confirmed whether the target audience prefers regular or oversized fit.
- I have not established what price customers would actually pay.
- I have not tested whether the optional styling ideas are useful to visitors.

## 8. Peer feedback, decisions, and review status

**Feedback received in the PUREFORM repository:**

- [Issue #5 — homepage wording](https://github.com/mfnu906-ship-it/is117-brand-studio/issues/5): accepted. The homepage wording was updated while keeping the classroom-demo disclaimer. The reviewer checked the updated text on `main` and confirmed it addressed the feedback.
- [Issue #6 — style-guide status](https://github.com/mfnu906-ship-it/is117-brand-studio/issues/6): accepted. The status wording was clarified to distinguish approved identity decisions from audience assumptions. The reviewer checked the updated style guide.
- [Issue #7 — studio logo alt text](https://github.com/mfnu906-ship-it/is117-brand-studio/issues/7): accepted. The alt text was changed to “PUREFORM logo” and merged through [PR #8](https://github.com/mfnu906-ship-it/is117-brand-studio/pull/8). The reviewer checked the logo description and homepage link.

**Feedback given to a classmate:** Three constructive issues were filed in the classmate's THE EDIT repository: [Issue #5](https://github.com/grrvbwpv6g-create/is117-brand-studio/issues/5), [Issue #6](https://github.com/grrvbwpv6g-create/is117-brand-studio/issues/6), and [Issue #7](https://github.com/grrvbwpv6g-create/is117-brand-studio/issues/7). The first two were addressed in merged PRs #8 and #9; the logo-introduction suggestion was deferred with a design rationale. The issues and classmate's responses remain the review record.

**New source-trace reviewer request:** [Issue #9 in the PUREFORM repository](https://github.com/mfnu906-ship-it/is117-brand-studio/issues/9) asks a reviewer to open the Cotton On source, trace the finding to the styling feature, and retry the published interaction. It remains open until the reviewer records that retry. Do not mark this step resolved before then.

## 9. Verification and AI assistance

The previous successful GitHub Actions run [#42719488758](https://github.com/mfnu906-ship-it/is117-brand-studio/actions/runs/42719488758) reported a successful check and publish workflow, including 7 server tests and 12 browser tests. That run verifies the code at its recorded commit; the latest documentation changes and the added research-page test route still need a fresh run after they are committed.

The learner also recorded personal browser checks in [LEARNING.md](../LEARNING.md), including homepage first impression, keyboard navigation, mobile layout at 390 × 844, style-guide accuracy, optional style-goal behavior, and the demo-bag interaction. These are learner-reported checks for the specific pages and interactions described, not universal accessibility or customer-preference evidence.

AI helped organize the research notes, compare the source-page content, draft the documentation structure, and prepare the implementation and browser-test changes. The learner remains responsible for checking the sources, deciding which findings matter, and approving the final claims.
