# Investigation Log — payoff

## 2026-02-27 — First Pull

### Finding 1: The cross-domain wallets exist
Two wallets show digital + physical commerce from the same anonymous human:
- **Wallet A (USDEBT)**: Suno.com $10 (AI music sub) + Green Valley Grocery (Shell) + Costco $90 + Pepper Lunch $32 + Terrible Herbst $40 + Sojo Ramen $52 + The Taco Stand $23
- **Wallet B (EF_Hutton)**: Shopify $300 (merchant sub) + Jewel-Osco (×5) + Costco (×3) + Home Depot (×2) + Trader Joe's + Walgreens + dog grooming $200 + legal $535 + Burger King $5.90

**Why it matters**: This is the dataset that doesn't exist anywhere else. Visa sees "STRIPE $10" — the receipt says "Suno.com monthly subscription." And the same wallet also bought gas and groceries. Cross-ecosystem, cross-category, identity-free.

### Finding 2: The one SaaS receipt is Suno
14-day category breakdown: 540 grocery, 278 restaurants, 126 gas... 1 SaaS subscription ($10). It's Suno — an AI music generation tool. The only verified AI tool subscription in 3,285 receipts. The digital intelligence layer is 0.03% of the dataset.

**Why it matters**: The whole agent thesis (help humans submit SaaS receipts) is targeting a category that's essentially zero right now. The opportunity is entirely ahead. Agents ARE the missing distribution for digital commerce verification.

### Finding 3: Receipt stacks build personas without identity
EF_Hutton's stack: Shopify + Jewel-Osco + Costco + Home Depot + dog grooming + legal bill + Burger King. Without knowing who this is, the receipts say: small business owner, suburban, has a dog, does DIY, eats fast food. That persona is worth money to brands — and it was built from receipts alone.

### Finding 4: Store normalization at scale
- McDonald's: 20+ aliases (#38045, #1710, Bannockburn, Northbrook, Restaurant #13749...)
- Starbucks: 20+ aliases (HMSHost STLSTA16, @ Luxor Registration, Planet Hollywood #17666...)
- Green Valley Grocery: 10+ aliases (#60, #64, #74, Shell-branded variants)

The hard problem isn't verification. It's normalization.

### Finding 5: Correction rate 85.5%
851 verified, 728 corrected in 7 days. Almost 1:1. GPT vision fixes what OCR gets wrong.

### Finding 6: 175-day streak
BiglyMoney: 175 consecutive days. stardustminer: 85. MexicanMagician: 59 (longest ever: 88). The distribution is power-law — a few obsessive uploaders, then a steep drop.

### Finding 7: USDEBT's 1,502 logins
62 spends across 1,502 logins. 24:1 login-to-spend ratio. What are they doing? Checking balance? Watching the leaderboard? The engagement pattern suggests the app is sticky beyond just uploading.

### Finding 8: Las Vegas clustering
USDEBT's receipts cluster in Las Vegas: Green Valley Grocery (Shell), Terrible Herbst (LV chain), Pepper Lunch, Sojo Ramen, Empanada Factory, The Taco Stand, Kaizen. Physical location emerges from receipt patterns without GPS.

### Finding 9: Feb 13-14 signup spike
48 new users in 2 days vs 5.3/day average. 9x spike. Correlates with stardustminer's referral burst (25+ ghost referrals on those dates).

### Finding 10: 50% activation rate
322 total users. 161 activated (submitted at least 1 spend). 161 dropped after first login. Half never scan a single receipt.

---

## Data Sources
- MCP: recent-spends, recent-activity, get-leaderboard, treasury-summary, users-dashboard, lookup-store, search-spends, get-reward-policy
- Public API: api.crinkl.xyz/api/public/gmv/cumulative, /distribution/trailing/summary, /spend/merchants/summary
