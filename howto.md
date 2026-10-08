# Understand

## 🧭 Understand the sales pipeline

> From first contact to live client: which object and which pipeline to use at each step.

> 🛑 **Your job stops at Closed won.** **Onboarding**, **Contract is live** and **Contract has expired** are set **automatically** by HubSpot. **Never move a deal to these stages yourself**: it can break the onboarding, subscription and billing automations.

**1. Prospecting happens on the LEAD** (outbound: pipeline *New leads* · inbound: pipeline *Inbound & Lead Gen*)

New / attempting → **Contacted** (set automatically when you log an outreach) → … → **Qualified** ⭐ (creates the deal) — or **Disqualified** / **Not pursuing**, always with a reason. Never leave a lead stuck on *Contacted*.

**2. Selling happens on the DEAL.** Pick the pipeline with one question: *does this replace an existing contract?*

| | **CarCutter - New business** | **CarCutter - Renewals & upsells** |
|---|---|---|
| Use it for | New client, new location with its own contract, new showroom | Anything that **cancels and replaces** an existing contract: renewal, upsell, downsell, amendment |
| Stages | Qualification call → Demo → Testing → Negotiation / Trade → **Closed won** / Closed lost | Deal created → Client informed → Discussion scheduled → Negotiation / Trade → Contract sent → **Closed won** / Churned |

**3. After Closed won, automation takes over:** Onboarding → Contract is live → Contract has expired. 🛑 **Hands off: never move these stages yourself.**

**What each New business stage means**

- **Qualification call** — confirm ICP fit, use case, number of locations, DMS, decision maker, buying process. Not a fit → *Closed lost* with the reason.
- **Demo** — log the demo meeting on the deal, contact and company.
- **Testing** — run the agreed test.
- **Negotiation / Trade** — quote + line items, contract duration, billing email.
- **Closed won** — set **automatically when the quote is signed**. Do your checks before sending the contract: see *Close a deal as won*.

⚠️ Fill the mandatory fields **when you move the deal**, not at the end. HubSpot blocks the stage change if they are missing.

## 👥 Your role as a US Account Executive

> You run the full cycle yourself, from first call to signature. There is no BDR behind you.

| Who | Does | Owns in HubSpot |
|---|---|---|
| **You (AE US)** | Prospecting, qualification, demo, negotiation, closing | Leads, companies & contacts (incl. qualification info), parent/child structure, deals, quotes, Top 100 accounts clean |
| **CSM** | Onboarding after Closed won, retention, renewals | Data quality after signature, renewals |
| **Sales Ops** | Imports and data monitoring | Slack **#cc-import-requests** |

Because you have no BDR, the company and contact info a BDR would normally fill is **yours to fill**: see *Qualify a prospect*.

# Create

## 🏢 Create a company

> Add a new dealership or group to HubSpot without creating a duplicate.

1. **Search HubSpot first** (name *and* website). If it exists, don't create a duplicate.
2. Companies → **Create company**.
3. **Domain / website**: always fill it. HubSpot matches companies by domain.
4. **Name** it with the convention:
   - Group HQ: `Group name - HQ` (e.g. *AutoNation - HQ*)
   - Location: business name (e.g. *AutoNation Miami*)
5. Part of a group? The **HQ is the Parent company**, at the top; every rooftop is a **Child** of the HQ. In **Associate company with**, search the HQ and set the label **Parent Company** directly in the form.
6. Fill the key fields: **Client type**, **Total number of dealerships in group** (1 if single store, filled on the HQ), **DMS / IMS**, **Affiliated brands** (official franchises only), **Country**.

⚠️ Many companies to add (a whole group)? Use the **Company Importer**: see *Add the locations of a group*.

## 🏬 Add the locations of a group

> Create the child companies of a dealer group and link them to the HQ.

**Every location must exist as a company in HubSpot**, even when the contract is signed centrally by the HQ.

**A few locations** — create them yourself:
1. Open the **HQ company** → Companies section → **+ Add**.
2. Create each location (business name + website) with the label **Child Company**.

**Many locations** — use the **[Company Importer](https://lead-import-production.up.railway.app/)**: it creates companies in bulk and checks for duplicates before importing.

Stuck? Post in Slack **#cc-import-requests** with the HQ name, HQ address, expected number of locations and website.

⚠️ Never use HubSpot's own import tool: duplicates and mistakes are hard to undo.

✅ Check: the number of child companies should match **Total number of dealerships in group** on the HQ.

## 🎯 Create a lead or handle an inbound

> Start prospecting the right way so your activity and conversions are tracked.

**New outbound lead**
1. Top right **Create → Lead**, linked to the contact (or company).
2. Pipeline **New leads**, stage **New/Attempting**, lead type **New business**, vertical **Carcutter**, owner = you.
3. Make sure a **contact** is attached (needed for sequences).

**Inbound lead** — you get a notification when one is assigned to you (**1 contact · 1 company · 1 lead**)
1. **Treat it within 2 hours max.**
2. Find it: **CRM → Leads → Pipeline *Inbound & Lead Gen* → Lead type = Inbound**.
3. Log your outreach: the lead moves to **Contacted** automatically.
4. Then **always** move it on: **Qualified**, **Disqualified** or **Not pursuing**, with a reason. At **Qualified**, HubSpot opens the deal creation form.

> 🛑 **Never leave a lead stuck on "Contacted".** Marketing uses your qualifications to improve targeting: no qualification = no visibility for them.

⚠️ **Never create a deal directly from an inbound**: always go through the lead, otherwise inbound conversion is lost.

## ✅ Qualify a prospect

> No BDR qualifies for you: these checks and fields are on you, before the demo.

**On the call, confirm the 4 points** — all 4 yes → move forward, otherwise close it early:

| | Ask yourself |
|---|---|
| **ICP fit** | Dealer group (our core target) or OEM used-car program? Right size? |
| **Authority** | Am I talking to a decision maker or strong influencer, not just a user? |
| **Need** | Is there a clear need around imaging and performance? |
| **Budget** | Budget allocated? How much, what timeframe? If not, how do they get one? |

**Then fill the qualification info** (the fields a BDR would normally fill) — company:

| Field | Rule |
|---|---|
| Client type | Independent dealership / Dealership group HQ / From a group |
| Imaging solution | Competitor app → select it + competitor name. Unknown → update later |
| Number of cars on lot | Website estimate, confirm on the call |
| Total number of dealerships in group | On the HQ, 1 if single store |
| DMS / IMS | From the list. "Other" only temporarily |
| Dedicated budget | Confirmed / Process underway / No clear budget. Already paying a competitor = confirmed |
| Affiliated brands | Official franchises only |
| Website URL | Copy-paste |

Contact: **Job title in English** and **Buying role** (several if needed).

## 💼 Create a deal

> The fields to fill so the deal is right from day one.

@video https://www.loom.com/share/2e434bd4fb7c4f5ba589b75abb4bb9ff

1. From a **Qualified lead** (recommended), or **Sales → Deals → Create deal**.
2. Pipeline **CarCutter - New business**, stage **Qualification call**.
3. Fill in:

| Field | What to enter |
|---|---|
| Deal name | Company name |
| HQ name | If part of a group |
| Total number of dealerships in group | Whole group, **1** if single location |
| Number of dealerships involved in this deal | Locations covered by **this** contract, **1** if single. Never more than the group |
| [Cars] Products | App, API, 360… |
| DMS | The dealership's DMS |
| Affiliated brands | Official franchises only |
| [CC] Company legal name | Legal name printed on the invoice |

4. Associate the **contact** and the right **companies**:

| Contract | Associate the deal with |
|---|---|
| **Localized** (one rooftop signs and pays) | **The rooftop company only**. Don't link it to the HQ. |
| **Centralized** (the HQ signs for several locations) | **The HQ AND every location company** the contract covers |

⚠️ Existing client buying more? That's not a new deal: see *Create an upsell*.

## 📅 Book and log a demo

> Log your demo so it shows on the deal and in the dashboards.

**Book it** from the lead or the deal:
1. **Schedule a meeting** (or the prospect books through your meeting link: HubSpot logs it automatically).
2. **Meeting type = Demo**.
3. Associate **Lead + Deal + Contact + Company**.

**After the demo**: set the outcome to **Completed** (contact page → meeting → Actions → Edit, or Sales Workspace → Meetings → Log outcome).

⚠️ Never write internal notes in *Meeting description*: the prospect sees it. Use **Team notes**.

## 🧾 Build the quote and line items

> Line items drive the deal amount, the ARR, your signings and your bonus.

1. In the deal → **Create quote** → **Add line item → Select from product library**.
2. Pick the right **folder**, **language** and **tier** (use **your pricing tool**).
3. On each line item:
   - Discount → **Unit discount** (never edit the unit price)
   - **Term** = contract duration in months
   - **Commitment type** and **Billing frequency** → pick the row matching the contract:

| Contract | Commitment type | Billing frequency in HubSpot | How Finance bills |
|---|---|---|---|
| **API, price per car or price per image** (minimum number of cars/images per year) | **Minimum commitment** | **Annually** | Monthly, on actual consumption |
| **Upfront payment** of a number of cars/images | **Credit pack** (only for upfront payments) | Annually (upfront) | Upfront at signature, then overconsumption |
| **No commitment** | **PayG**: avoid it, **VP approval only** | | On consumption |
| **Flat monthly fee** (location or group subscription) | **Flat rate monthly** (standard) | Monthly | Monthly flat fee |
| Flat annual fee | **Flat rate annually**: avoid it | | |

4. HQ pays for all locations → **one quote** on the parent. Each location pays → **one deal and one quote per location**.
5. **New business: always add a showroom** line item (Standard, Custom or Tailor-made Showroom).
6. **"Set-up fees only (no recurring)" = Yes**: tick it **only** when the deal sells nothing but one-off services:
   - ✅ **Showroom**, **integration** (IMS/DMS, FTP/SFTP, Cloud server) or **inventory reprocessing** (*Standing inventory processing fee*)
   - ❌ **No ARR, no recurring amount**: no subscription, flat fee, price per car or API on the deal
   - ⚠️ These deals **don't create a subscription and never renew**. If the client also buys anything recurring, leave it unticked.
   - 🔗 Add-on for an existing client (e.g. a new showroom)? **Associate** the deal with the existing deal, but **never label it as a Child deal**: a child cancels and replaces its parent.

💡 **Minimum commitment set to Annually** shows the full commitment on the quote, even though Finance bills monthly on consumption. Add a comment to the buyer to clarify that billing is monthly.

🚨 **One-time is only for non-recurring items** (e.g. set-up fees). A subscription billed One-time doesn't count as recurring revenue, so the deal won't appear in your signings or bonus.

# Close

## 🏆 Close a deal as won

> Check everything **before you send the contract for signature**: once signed, the deal closes itself.

> 🛑 **The deal moves to Closed won automatically when the quote is signed.** From that point you **don't have to do anything** with the deal: HubSpot and the CSM take over (Onboarding, then Contract is live). So **all the checks below happen before sending the contract**.

**Before sending the contract for signature:**

1. **Line items** are on the quote and the deal (no line items = no ARR, no subscription).
2. Fill these fields (no blanks, no defaults):
   - **Number of dealerships in group** (company) and **Number of dealerships involved in this deal** (deal)
   - **is multi-location deal?**
   - **DMS** (avoid "Other")
   - **Affiliated brands**
   - **Revoke auto-renew?** only if the client wants to renew manually: set it to Yes. Otherwise leave it empty.
3. Recommended: add a **pinned note** for the CSM:
   - Operational contact (name, role, email, phone)
   - Single or multi-location, specifics per site
   - Features to activate or not (Next gen 360, Stock images, Shotlist, Hotspots…)
   - Standing inventory interest (one-time fee)
   - Anything else the CSM should know
**After signature, watch one thing: the contract duration**
- **Contract duration (in months)** is filled **automatically by the Data team within 2 hours**. If it's still empty, you get a **notification**: fill it in.
- **Multi-duration contract** (e.g. 2 months at €249, then 10 months at €299)? It can't be filled automatically: **fill it in yourself**.
- Missing or wrong duration = no end date = **no renewal deal**.

**Only exception: contract signed outside HubSpot** (paper, email). There is no e-signature to trigger the automation, so set Deal → View all properties → **Customer procurement process = Yes**, otherwise onboarding never starts.

⚠️ Never move the deal to **Onboarding** or **Contract is live** yourself: it can break the onboarding, subscription and billing automations.

## ❌ Close lost or disqualify

> Close cleanly so we know why, and can come back later.

**Deal lost** → stage **Closed lost** + **Closed lost reason** and its category.

**Lead not converting** — choose carefully:
- **Disqualified** = never a fit: Not a good fit, Outside automotive, Duplicate, Scam, Low volume, Not the right contact.
- **Not pursuing** = good lead, wrong moment: Not the right timing, No budget, With a competitor, Not interested right now, Ghosting.

Always add a **note** with context (e.g. "Less than 100 cars on lot").

# Existing clients

## 📈 Create an upsell, downsell or amendment

> The new deal (child) cancels and replaces the old one (parent): it must contain the full contract.

@video https://www.loom.com/share/766ec4c162c844509a73288d56a1870d

1. Create the deal in **CarCutter - Renewals & upsells** (never New business).
2. Set **Renewal type** yourself (no automation sets it):
   - **Renewal - upsell**: the contract grows (more products, more locations, more value).
   - **Renewal - downsell**: the contract shrinks.
   - **Contract amendment**: the contract changes without being an upsell or downsell (e.g. rooftop contracts merged into a group agreement, a legal entity or contract name change, a change of terms). It still cancels and replaces the old contract.
3. Quote with **all line items of the new contract** (existing products + new ones), not only what's added.
4. Link the deals: open the **original deal** → **More → Edit association labels → Parent deal → Update**. The original is the parent, the new deal the child.
   - **A child usually has one parent**: Year 1 is Year 2's parent, Year 2 is Year 3's parent.
   - Only link deals that **directly replace** each other.
5. Associate the **company** (and contact).
6. **Configuration ticket: nothing to do.** Any Renewal type other than *Flat renewal* creates it automatically, which is why step 2 matters.

When the upsell is won, HubSpot automatically stops the old contract (old deal → Contract has expired). Without the Parent deal link, **the client can be billed twice**.

**Exception: several rooftop deals merged into one centralized deal.** Each rooftop deal is a **Parent** of the new central deal (the **Child**), so the central deal has several parents.

> 🛑 **Not a replacement = not a child.** A set-up fee or add-on deal (e.g. a new showroom) is only **associated** to the existing deal, never labelled Child.

**Client close to renewal?**
- HubSpot creates the **renewal deal 40 days before the contract ends**. It belongs to the **CSM**: you help close the upsell when asked.
- Don't hold a renewal open past its start date to negotiate an upsell: the CSM closes the renewal as Closed won, then **you open a separate upsell deal**.
- Never move a deal to a stage after Closed won: it's automated.

## 📍 Add a location to a contract

> Two cases depending on who pays for the new location.

**First: create the location** as a child company of the HQ (see *Add the locations of a group*).

**Case A — the new location gets its own contract** (it pays separately, nothing is replaced)
1. New deal in **CarCutter - New business** on the **new location's company**.
2. Number of dealerships involved in this deal = **1**.
3. Normal flow: quote, Closed won, handover.
4. It doesn't replace anything: **don't link** it to the group's existing deal. Several contracts can live together for different sub-companies.

**Case B — the location joins the existing contract** (the HQ pays for everyone)
1. It replaces the current contract → follow *Create an upsell* (Renewals & upsells, renewal type **Renewal - upsell**, **Parent deal** link).
2. The quote covers **all locations**, including the new one.
3. Update **Number of dealerships involved in this deal** to the new total and set **is multi-location deal? = Yes**.
4. Associate the deal with the HQ **and every location** covered, including the new one.

## 🔎 Check if a company is already a client

> Avoid prospecting a client as if it were a new lead.

Look at two properties on the company:

| Property | Means |
|---|---|
| **Group status** | At least one dealership of the group is a client |
| **Company status** | This company itself is a client |

- Group *Active* but company *Inactive* → the group is a client, this location isn't. Talk to the CSM before prospecting.
- A CSM on the company is another sign it's a client.
- Client buying more → *Create an upsell*, not a New business deal.

# Daily work

## 📞 Log calls, emails and notes

> Activity logged in the wrong place is invisible, and you look inactive.

- Log from the **lead page** (best) or the **contact page**.
- ❌ Never from the **company page**: it won't show on the lead or in dashboards.
- Logged on the company by mistake? Open the activity → **Associations** → add the lead.
- Tag every call in **Modjo** and remove other recording bots.

## 📊 Check your data

> A quick look each week catches the mistakes that block onboarding, billing and renewals.

1. Open the **[Data Integrity Dashboard](https://app-eu1.hubspot.com/reports-dashboard/26533299/view/111940634)** in HubSpot and filter on your name.
2. Run **My deals** in this app: each issue links to the how-to that fixes it.
3. Fix your deals directly in HubSpot (each deal in My deals has a ↗ HubSpot link).

## ✉️ Enroll leads in a sequence

> Put prospects into an automated outreach cadence.

1. Each lead needs an **associated contact**. Error *"select one or more partner accounts with a primary contact"* = no contact on the lead → add one from the lead record.
2. Lead view → filter → select the leads → **Enroll in sequence**.
3. Max **50 leads** per batch.
