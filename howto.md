# Start here

## 💰 Build your offer and quote

> What to sell, at what price, for how long, and how to put it in the quote.

> 🛑 **Price with the pricing tool, never by hand.** It gives the right tier and every discount you're allowed to give.

### ✅ 1. Get the price

| Region | Pricing tool |
|---|---|
| **United States** | **[NorthAm pricing tool](https://carcutter-us-pricing-production.up.railway.app/)** |
| **Australia · Canada** | **[AU-CA pricing tool](https://aucanpricing-production.up.railway.app/)** |
| **Europe** | **[EU pricing tool](https://carcuttereupricing-production.up.railway.app/)** |

- Tier = number of vehicles (0-50, 50-100, 100-200…).
- Standard discount: **10%**, on every plan. Anything else: only what the tool proposes (based on number of stores and group inventory).
- All price lists, add-ons and set-up fees: **[CarCutter Pricing & Offers](https://app.notion.com/p/293ab682c9de8010b771c14e3f7d1d5b)** (Notion).

### 🔀 2. Pick the plan

| Plan | Images per car | Adds |
|---|---|---|
| **Basic** | 15 | App · overlays · IMS/DMS upload · Hub · Shotlist (NorthAm) |
| **Standard** | 20 | + Shotlist · Hotspots · Stock images (NorthAm) |
| **Premium** | Unlimited | + Next gen 360 · Standing inventory feed |

### 🔀 3. Pick the duration

| Model | When |
|---|---|
| **12-month commit** | Default |
| **12 months + 1 or 3 months free** | US strat accounts only (see step 5) |
| **1- or 3-month pilot + 12 months** | Client wants to try first: see *Sell a pilot* |
| **3 months, auto-renew** | US only · won't commit to 12 months |
| **6 months** | US only |
| **Multi-year (≥ 18 months)** | Big accounts: **+20% ARR** for your bonus |
| **1 month, auto-renew** | US only · larger accounts · **manager approval** |

### ✅ 4. Build the quote

1. Pick the quote **template** matching the duration (it sets the right T&Cs).
2. **Add line item → Product library** → your folder and language → the tier from the tool.
3. Discount in **Unit discount** · **Term** = contract duration (months).
4. Commitment and billing:

| Contract | Commitment type | Billing frequency |
|---|---|---|
| Flat monthly fee | **Flat rate monthly** | Monthly |
| API · price per car · per image | **Minimum commitment** (annual) | **Monthly** |
| Upfront payment | **Credit pack** | Annually |
| No commitment | **PayG**: VP approval only | |

   Minimum commitment: the client is **billed every month on actual usage**, with a **minimum commitment for the year**. If they use less than 100% over the year, the unused cars or images are billed.
5. New business: **always add a showroom**.

### ⭐ 5. US offer: 1 or 3 months free

- **Who**: **US strat accounts only**. Offering 3 months? **Talk to your manager first.**
- **What**: the client gets 1 or 3 months free, then pays 12 months (13 or 15 months in total).
- **How**:
  1. **Use the 12-month template, Term = 12**: the client is engaged for 13 or 15 months but **billed 12 times**.
  2. Add the subscription for 12 months as usual.
  3. Add the line item **CarCutter - 1 month free** or **CarCutter - 3 months free** ($0).
  4. **Write it in the quote comments box**, e.g. *"Includes 1 month free: billing starts 1 month after go-live, then 12 months."*
- **Dates are automatic**: the subscription start and billing are pushed back by 1 or 3 months by a workflow. Don't touch them.

### 💡 What counts in your ARR

- Recurring line items only. One-off fees and free months: no ARR.
- 12 months: full ARR · ≥ 18 months: ARR + 20% · pilot: only if it succeeds.
- 3 months: first 3 months + actuals of the next 9 · 1 month: first month + actuals of the next 11.

### ❌ Never

- Bill a subscription **"One-time"**: no ARR, no signing, no bonus.
- Edit the unit price, or give a discount the tool doesn't propose.
- Waive set-up fees for **US SMB Tier 1**: onboarding won't start.
- Sell Next gen 360 without checking the showroom: a **turntable** and a compatible floor are required.
- Offer free months outside US strat accounts, or 3 months without telling your manager.

# Understand

## 🧭 Understand the sales pipeline

> Lead → deal → signature. Your job stops at Closed won.

> 🛑 **Stop at Closed won.** Onboarding, Contract is live and Contract has expired are automatic. Never move a deal there.

### ✅ Do

1. **Prospect on the lead**: New / attempting → Contacted → … → **Qualified** (creates the deal).
2. **Sell on the deal**: Qualification call → Demo → Testing → Negotiation → **Closed won** (automatic when the quote is signed).
3. Fill the required fields **when you move the stage**.

### 🔀 Which pipeline?

| Situation | Pipeline |
|---|---|
| New client · new location with its own contract · new showroom | **New business** |
| The deal **replaces** an existing contract: upsell, downsell, amendment | **Renewals & upsells** |

### ❌ Never

- Leave a lead on *Contacted*.
- Move a deal after Closed won.

## 👥 Your role as an Account Executive

> You own the whole cycle, from first call to signature. No BDR.

### ✅ You own

- Leads, companies, contacts and their qualification info
- The parent / child structure of your groups
- Deals and quotes, until signature
- Your Top 100 accounts, clean

### 🤝 Others own

- **CSM**: onboarding, renewals and churn, after Closed won
- **Sales Ops**: imports and data checks → Slack **#cc-import-requests**

# Create

## 🏢 Create a company

> Add a dealership or a group, without creating a duplicate.

### ✅ Do

1. **Search HubSpot first** (name + website).
2. Companies → **Create company**, **website** filled in.
3. Name it: `Group name - HQ` for the HQ, business name for a location.
4. Location of a group? **Associate company with** the HQ → label **Parent Company**.
5. Fill **Client type**, **Total number of dealerships in group** (on the HQ, 1 if single store), **DMS / IMS**, **Country**.

### ❌ Never

- Create a duplicate.
- Create a whole group by hand: see *Add the locations of a group*.

## 🏬 Add the locations of a group

> Every location must exist as a company, even on a central contract.

### ✅ Do

- **A few locations**: HQ company → Companies → **+ Add** → label **Child Company**.
- **Many locations**: **[Company Importer](https://lead-import-production.up.railway.app/)** (bulk + duplicate check).
- Check: number of child companies = **Total number of dealerships in group**.
- Stuck? Slack **#cc-import-requests**.

### ❌ Never

- Use HubSpot's own import tool.

## 🎯 Create a lead or handle an inbound

> Inbound first, always within 2 hours.

> 🛑 **Inbound: call within 2 hours.**

### ✅ Inbound

1. You get a notification: 1 contact · 1 company · 1 lead.
2. Find it: **CRM → Leads → Inbound & Lead Gen → Lead type = Inbound**.
3. Call: the lead moves to **Contacted** by itself.
4. Move it to **Qualified** (opens the deal), **Disqualified** or **Not pursuing**, with a reason.

### ✅ Outbound

1. **Create → Lead**, with a **contact** attached.
2. Pipeline **New leads** · stage **New/Attempting** · type **New business** · vertical **Carcutter** · owner = you.

### ❌ Never

- Create a deal directly from an inbound.
- Leave a lead on *Contacted*.

## ✅ Qualify a prospect

> Before the demo: 4 yes, then fill the qualification fields.

### ✅ 4 questions on the call

| | |
|---|---|
| **ICP fit** | Dealer group or OEM used-car program, right size? |
| **Authority** | A decision maker in the room? |
| **Need** | A clear imaging need? |
| **Budget** | Budget and timeframe? |

Not 4 yes → close it early.

### ✅ Fields to fill

- **Company**: Client type · Imaging solution (+ competitor) · Number of cars on lot · Total dealerships in group · DMS / IMS · Dedicated budget · Affiliated brands (official franchises only) · Website
- **Contact**: Job title **in English** · Buying role

## 💼 Create a deal

> The right fields from day one.

@video https://www.loom.com/share/2e434bd4fb7c4f5ba589b75abb4bb9ff

### ✅ Do

1. From the **Qualified lead** → pipeline **New business** · stage **Qualification call**.
2. Fill in:

| Field | Rule |
|---|---|
| Deal name | Company name |
| Total number of dealerships in group | Whole group · 1 if single |
| Number of dealerships involved in this deal | This contract only · never more than the group |
| DMS | **Required** |
| HQ name · Products · Legal name · Affiliated brands | If you have them |

3. Associate the **contact** and the right **companies**:

| Contract | Associate with |
|---|---|
| **Localized** (one rooftop signs and pays) | The rooftop company only |
| **Centralized** (the HQ signs for several) | The HQ **+ every location** covered |

### ❌ Never

- Open a New business deal for an existing client buying more → *Create an upsell*.

## 📅 Book and log a demo

> Log it so it shows on the deal.

### ✅ Do

1. Schedule from the lead or the deal (or your meeting link).
2. Type = **Demo** · associate **Lead + Deal + Contact + Company**.
3. After the demo: outcome = **Completed**.

### ❌ Never

- Write internal notes in *Meeting description*: the prospect sees it. Use **Team notes**.

## 🧪 Sell a pilot

> A pilot = a paid first period, then a 12-month commit. Not a free trial.

### ✅ Do

1. Quote with **2 lines**: the pilot (e.g. 1 month at $299) + the contract (e.g. 12 months at $399).
2. On the deal: **Has a pilot? = Yes** · **Pilot monthly amount** · **Pilot duration in months** · **Pilot status = In pipeline or Negotiation**.
3. At the end of the pilot, come back to the deal: **Pilot status = Success** (goes on) or **Exit** (stops: token deactivated, deal Closed lost).

### 💡 Good to know

- Pilot only = 1 or 3 months **followed by at least 12 months**. Otherwise create a standard 1- or 3-month contract.
- Optional comment to the buyer: the pilot fee is due even if they withdraw; without cancellation, the commitment starts automatically. Integration fees are always due.

### ❌ Never

- Call it a pilot if there's no 12-month contract after it.
- Forget to set Success or Exit after the pilot: your ARR depends on it.

# Close

## 🏆 Close a deal as won

> Check before sending the contract: signature = Closed won, automatically.

> 🛑 **Once signed, hands off.** The deal closes itself and the CSM takes over.

### ✅ Before sending the contract

- [ ] Line items on the quote
- [ ] Dealerships in group · dealerships in this deal
- [ ] Is multi-location deal?
- [ ] **DMS** (not "Other")
- [ ] Revoke auto-renew = Yes **only** if the client wants to renew manually
- [ ] Pinned note for the CSM: contact, sites, features to activate, standing inventory

### 💡 After signature

- **Contract duration** fills in within 2 h. Got a notification? Fill it in.
- Contract with several durations (e.g. 2 months, then 10)? Fill the duration yourself.
- Signed outside HubSpot? **Customer procurement process = Yes**.

### ❌ Never

- Move the deal to Onboarding or Contract is live.

## ❌ Close lost or disqualify

> Always a reason, so we can come back.

### ✅ Deal lost

Stage **Closed lost** + **Closed lost reason** + category.

### ✅ Lead not converting

| | Reasons |
|---|---|
| **Disqualified** (never a fit) | Not a good fit · Outside automotive · Duplicate · Scam · Low volume · Not the right contact |
| **Not pursuing** (not now) | Timing · No budget · With a competitor · Not interested now · Ghosting |

Add a one-line note (e.g. "Less than 100 cars on lot").

# Existing clients

## 📈 Create an upsell, downsell or amendment

> The new deal replaces the old one: full contract, linked as Child.

@video https://www.loom.com/share/766ec4c162c844509a73288d56a1870d

> 🛑 **No Parent deal link = the client is billed twice.**

### ✅ Do

1. Pipeline **Renewals & upsells**.
2. Renewal type:

| Type | When |
|---|---|
| **Renewal - upsell** | The contract grows |
| **Renewal - downsell** | The contract shrinks |
| **Contract amendment** | It changes otherwise (group merge, name / entity, terms) |

3. Quote = **the full contract** (existing + new), not just the extra.
4. Old deal → **More → Edit association labels → Parent deal**. Rooftop deals merged into one central deal? Each one is a Parent.
5. Associate the company and the contact.

### ❌ Never

- Link a deal that doesn't replace the contract (new showroom, add-on, separate location contract).
- Hold the CSM's renewal open to negotiate: let it close, then open a separate upsell.

## 📍 Add a location to a contract

> Joins the central contract? Upsell. Its own contract? New deal, no link.

### ✅ First

Create the location as a **Child company** of the HQ.

### 🔀 Then

| The location… | Do |
|---|---|
| **Has its own contract** | New business deal on the location · 1 dealership · **no link** |
| **Joins the centralized contract** (e.g. Ed Napleton) | **Upsell**: quote for all locations · old central deal = Parent · update the dealership count · multi-location = Yes · associate HQ + all locations |

## 🔎 Check if a company is already a client

> Before prospecting, 10 seconds.

### ✅ Check

- A deal in **Contract is live** on the company or its group → client.
- A **CSM** on the company → client.

### ❌ Never

- Prospect a client as new business: talk to the CSM, or create an upsell.

# Daily work

## 📞 Log calls, emails and notes

> Not logged on the lead = you look inactive.

### ✅ Do

- Log from the **lead** (or the contact).
- Tag every call in **Modjo**.

### ❌ Never

- Log from the company page.

### 💡 Fix

Logged on the company? Activity → **Associations** → add the lead.

## 📊 Check your data

> 5 minutes a week.

### ✅ Every week

1. **My deals** (this app) → fix each issue with the ↗ HubSpot link.
2. **[Data Integrity Dashboard](https://app-eu1.hubspot.com/reports-dashboard/26533299/view/111940634)**, filtered on your name.

## 🛠️ Create a sequence

> Your own outreach cadence: emails + reminders.

### ✅ Do

1. **Automation → Sequences → Create sequence** → name it.
2. Add steps: automated email · email task · call task · LinkedIn task. Set the delays (business days).
3. **Settings**: business days, email send window.
4. **Save** and share it with your team.

### 💡 Good to know

- Max 10 email templates per sequence.
- A contact leaves the sequence as soon as they reply or book a meeting.

## ✉️ Enroll leads in a sequence

> Put your leads in a cadence in 3 clicks.

### ✅ Do

1. Each lead has a **contact** attached.
2. Lead view → select the leads → **Enroll in sequence**.

### 💡 Good to know

- Max 50 leads per batch.
- "Primary contact" error = no contact on the lead.
