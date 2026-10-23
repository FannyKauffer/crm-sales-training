# CarCutter CRM Guide

HubSpot is the single source of truth for all our accounts, prospects and customers. This guide summarises the rules every BDR, AE and SMB rep must follow. Source: *Sales Processes knowledge base* (Notion, CarCutter Sales Playbook).

## Who owns what

- **BDR**: owns prospecting data: company and contact BDR info, parent/child association and labels, child-company import requests for the accounts they hunt.
- **AE**: owns deal data: contract, stakeholders, number of dealerships in the deal, and parent/child association **at company level and at deal level**. AEs are also responsible for cleaning their Top 100 accounts.
- **CSM**: final owner of data quality on strategic accounts after signature.
- **Sales Ops**: runs imports (Slack channel **#cc-import-requests**), templates and data monitoring.

---

# Module 1: Contacts & companies

## Import requests

- **Never use HubSpot's own import.** Companies in bulk: use the **Company Importer** (https://lead-import-production.up.railway.app/), which checks for duplicates. Otherwise pick the right template, **make a copy**, fill it in and send it to your Sales Manager or Sales Ops (Romane).
- Templates: Contact import / Company import / Company + contact / BDR template (child companies of a parent).
- Companies are matched by **domain name**, not company name. A wrong or missing domain creates duplicates.
- Contacts are matched by **email**. If the email already exists (even as a secondary email), the import fails.
- More than 10 locations to add → post a request in **#cc-import-requests** with the parent company name, HQ address, expected number of locations and website.

## Naming convention

| Company type | Convention | Example |
|---|---|---|
| Parent / HQ | `Group name - HQ` | AutoNation - HQ |
| Child / location | Company business name | AutoNation Miami |

Wrong naming breaks automation, reporting and lead routing.

## Parent-child structure

- **HQ manages contract & billing** → one Parent Company, **one deal**, one quote covering all rooftops. Child companies exist for reference.
- **Each rooftop pays individually** → **one deal and one quote per Child Company**, each still linked to the Parent.
- Always link parent and child companies and use the **association labels** "Parent Company" / "Child Company".
- On creation: use "Associate company with" and set the label in the form. On an existing record: Companies section → More → **Edit association labels**.

## Seamless

- Always **check HubSpot first**: if the company already exists, do not create a duplicate.
- Seamless data is not 100% accurate: check that the email domain matches the company website before importing. No mass import without a quality check.

## Your HubSpot views

- Customise columns, then **clone and save the view**. Unsaved changes are lost on reload.
- Recommended prospecting columns: company name & owner, last activity date, Top account, Company status, Customer segment, number of associated deals, country.
- Useful filters: last activity before 6 months ago, Company status is not Active, Top account = Validated, Customer segment.

## Top 100 accounts

- Shared view of about 700 records (top 100 per market). It should only contain **parent companies (HQs)**. Flag any child company you see.
- **Total number of dealerships** must be filled at company level. It drives **group coverage** (e.g. 100 signed / 300 dealerships = 30%).
- **Group completeness**: if the number of linked child companies does not match the total dealerships, request a child-company import.

## Is this company already a client?

| Property | Meaning |
|---|---|
| **Group status** (old: Company activity status) | At least one dealership in the group is an active client |
| **Company status** (old: Customer activity status) | This specific company is an active client |

- Group Active + Company Inactive = the group is a client but this HQ/location is not. **Always check both.**
- A CSM attached to the company is a good sign it is a customer.
- A Closed Won deal ≠ active client: check that the subscription is still active.

---

# Module 2: Prospection & qualification

## Lead view

- Best access: **Sales → Sales Workspace → Prospects**.
- Stay on the **New Leads** pipeline. When filtering by stage, also filter on the pipeline (stages from all pipelines are mixed).
- Lead type priority: **Inbound** (highest) → Lead Generation → Outbound. Recycled / Closed-Lost / Qualified-Out / Churn lead types are legacy: ignore them.

## Creating a lead

| Field | Value |
|---|---|
| Pipeline | New leads |
| Stage | New/Attempting (change only if you already spoke to them) |
| Lead vertical | Carcutter |
| Lead type | New business (outbound) / Inbound / Lead gen |
| Lead level | Hot / Warm / Cold |
| Leadgen tool | Only if you used one (Seamless, Apollo…) |
| Lead owner | Yourself |

The **lead** tracks the prospecting journey; the **deal** tracks the transaction. Prospect from leads, not from company records.

## Lead stages

| Stage | Meaning |
|---|---|
| New / attempting | Never reached, or no answer |
| Contacted / reached | Spoke on the phone or got a reply |
| Engaged | Interest shown, ICP validated, pain identified, no meeting yet |
| Meeting scheduled | Meeting booked |
| No show to schedule | Booked but no-show → rebook |
| **Qualified** ⭐ | Opens deal creation automatically. Final BDR goal |
| Disqualified | Not relevant, never contact again |
| Not pursuing | Relevant but not now |

Stages are moved **manually**.

## Disqualified vs not pursuing

- **Disqualified** = not a good lead. Reasons: Not a good fit, Outside automotive sector, Duplicate, Scam, Low volume / potential, Not the right contact (create a new lead with the right contact).
- **Not pursuing** = good lead, wrong moment. Reasons: Not the right timing, No budget, Currently with a competitor, Not interested right now, Ghosting.
- Always add a **disqualification note** with context (e.g. "Less than 100 cars on lot").

## Inbound leads

- Inbounds land in New/attempting as `Inbound / [name]` and follow the same pipeline.
- ❌ **Never create a deal manually from an inbound.** Go through the lead, otherwise inbound conversion and attribution are lost.
- Shortcut allowed: move the lead directly to Qualified (or Disqualified) if you qualify it on the first call.
- Every inbound must move out of New/attempting.

## Sequences

- Sequences go to **people**: the lead needs an associated contact. Error "Please select one or more partner accounts with a primary contact" = no contact on the lead.
- Fix it on the lead record: associate or create the contact.
- Max **50 leads** per enrollment batch.

## Logging activities

- Log calls, emails and notes **on the lead page or the contact page**, never on the company page.
- Activity logged on the company only is invisible on the lead and in dashboards, so you look inactive.
- Fix: open the activity → Associations → add the lead.
- Lead name format: Company name + creation date. Do not rename it.

## Booking a demo (BDR)

- From the lead: Host = **User** (not rotation), Meeting type = **Demo**, add the AE as attendee, Team note "Booked by {BDR} for {AE}", associate **Lead + Deal + Contact + Company**.
- If the prospect booked through the AE's link: log a second meeting (Outcome = Scheduled, Type = Demo) with the attribution note, associated to at least Lead, Contact, Company.
- ❌ Never write internal info in **Meeting description / Attendee description**: the prospect sees them. Use **Team notes**.

## Marking a meeting as completed (AE)

- After each demo, set the outcome to **Completed** (contact page → Actions → Edit, or Sales Workspace → Meetings → Log outcome).
- Only **Completed** counts for the BDR target. If the deal is later moved to Qualified out, the meeting is removed from the BDR target.

## ICP and qualification

- **Dealer groups** (~90%, core), **OEMs** (~10%, used-car programs only), marketplaces / software vendors (opportunistic).
- Every discovery call must answer: **ICP fit, Authority, Need, Budget**. If not all confirmed, move on early.
- Aim for decision makers and strong influencers, not users only. Test budget early.

## BDR info (mandatory before the demo is marked completed)

Company level:

| Field | Rule |
|---|---|
| Client type | Independent dealership / Dealership group HQ / From a group |
| Imaging solution | If competitor: App (not CC) + competitor name. Unknown → update later |
| Number of cars on lot | Estimate from website, confirm after the call |
| Total number of dealerships in group | Fill at HQ level; 1 if single store |
| Total number of dealerships (parent company) | Automated, do not fill |
| DMS / IMS | From dropdown. "Other" only temporarily, flag missing providers to your manager |
| Dedicated budget | Confirmed / Process underway / No clear budget. Paying a competitor = confirmed |
| Affiliated brands | Official franchise brands only |
| Website URL | Copy-paste |

Contact level: **Job title in English**, **Buying role** (multi-select). The BDR score is computed automatically from these fields.

---

# Module 3: Deals & pipeline

## Creating a deal

Pipeline: **CarCutter - New Business**. Start at stage **Qualification call**.

| Field | Rule |
|---|---|
| Deal name | Prospect / company name |
| HQ name | If part of a group |
| DMS | The dealership management system |
| Affiliated brands | Official affiliations only, exclude used-car-only brands |
| Total number of dealerships in group | Whole group; 1 if single location |
| Number of dealerships involved in this deal | Locations covered by this contract; 1 if single location. Never more than the group total |
| [Cars] Products | App, API, 360… |
| [CC] Company legal name | Official legal name, printed on the invoice |
| Contact & Company | Always associate both |

Each stage has mandatory fields (gates). Fill them when you move the deal, not at the end.

## Quotes, line items & ARR

- Add line items **from the product library** (right folder, right language, right **tier** from the pricing grid).
- Apply discounts with **Unit discount**, never by editing the unit price.
- Set **Term (months)** to the contract duration.
- **Commitment type** (source: Notion "Quotes / line items creation"):
  - **Minimum commitment**: API, price-per-car and price-per-image contracts. **Billing frequency = Monthly**: the client is billed every month on actual usage, with a **minimum annual commitment**: if the client consumes less than 100% over the year, the unused cars or images are billed.
  - **Credit pack**: only for upfront payments.
  - **PayG**: no commitment. Avoid it: **VP approval only**.
  - **Flat rate monthly**: the standard option for monthly flat-rate contracts.
  - **Flat rate annually**: should generally be avoided.
  - Finance bills PayG and Minimum commitment contracts on consumption.
- 🚨 **One-time is only for non-recurring items** (e.g. set-up fees). One-time is not counted as recurring revenue: the deal won't appear in your signings or bonus.
- Deal amount (ARR) = recurring line items only. Set-up fees are excluded.

## Renewals & upsells

1. Create the deal in the **Renewals & upsells** pipeline, **never in New Business**.
2. Set the **Renewal type** (Flat renewal, Renewal - upsell, Renewal - downsell, Contract amendment, API Package renewal, Conversion to commit…):
   - **Renewal - upsell**: the contract grows (more products, more locations, more value).
   - **Renewal - downsell**: the contract shrinks.
   - **Contract amendment**: the contract changes without being an upsell or downsell (e.g. rooftop contracts merged into a group agreement, a legal entity or contract name change, a change of terms). It still cancels and replaces the old contract.
   - New locations under a separate contract that does not replace the previous one: **don't link** the deals. Several contracts can live together for different sub-companies.
   - But a location **added to a centralized contract** replaces that contract: it's an upsell, linked as Child (e.g. Ed Napleton).
3. The new deal must contain the **full updated contract** (existing + new line items), not only the added product.
4. Associate old and new deals: on the **original deal** → More → Edit association labels → **Parent deal**. The new deal is the child. Year 1 is parent of Year 2, Year 2 of Year 3. A child usually has one parent; exception: several rooftop deals merged into one centralized deal are all Parents of the central deal.
5. On the original deal: Actions → **Revoke auto-renew = Yes** with reason **Upsold**, **Downsold** or **Contract amendment**. Skipping this can bill the client twice.
6. Configuration ticket: created automatically for any Renewal type other than Flat renewal. No action needed.

## Handover to CSM

Before **Closed Won**, these must be filled (no blanks, no defaults):

| Property | Level | Watch-out |
|---|---|---|
| Number of dealerships in group | Company | Total group size, drives coverage |
| DMS | Deal & company | Avoid "Other", the CSM needs it for integration |
| Affiliated brands | Company | Official affiliations only |
| Number of dealerships involved in this deal | Deal | Exact locations of this contract |
| Revoke auto-renew | Deal | Yes if the client wants to renew manually |

- Leave a **pinned note** on the deal: operational POC (name, role, email, phone), showroom details, single vs multi-location, features to activate or not (Next gen 360, Stock images, Shotlist, Hotspots…), standing inventory interest (one-time fee), any other context. **No pinned note = incomplete handover.**
- Contract signed outside HubSpot → Deal → View all properties → **Customer procurement process = Yes** to trigger onboarding.

## Closed lost

- Always fill the **Closed lost reason** and its category so we can learn from lost deals.

## Pricing documentation and offers

Source: Notion "CarCutter Pricing & Offers" (https://app.notion.com/p/293ab682c9de8010b771c14e3f7d1d5b).

- **Pricing tools** (always price with them): United States https://carcutter-us-pricing-production.up.railway.app/ · Australia & Canada https://aucanpricing-production.up.railway.app/ · Europe https://carcuttereupricing-production.up.railway.app/
- Pricing grids (Americas and EU) and pricing slides are also linked in the Notion knowledge base, Module 3 § 5.
- **Tiers** are based on the number of vehicles: Tier 1 = 0-50, Tier 2 = 50-100, Tier 3 = 100-200, then +100 per tier.
- **Discount policy**: standard discount 10% off, applicable across all plans. Any other discount: use the pricing tool, which generates all acceptable discounts based on the number of stores in the group and the group's total inventory.
- **Plans**: Basic (up to 15 images per car, app, overlays, IMS/DMS upload, Hub, Shotlist in NorthAm) · Standard (up to 20 images, + Shotlist, manual Hotspots, Stock images in NorthAm) · Premium (unlimited images, + Next gen 360, Standing inventory feed).
- **Add-ons**: Next gen 360 (not all showrooms are compatible: only certain floor types, and a turntable is required; check the compatibility guidelines and Ops/Product before selling) · Shotlist.
- **Set-up / one-off fees** (same price in EUR, GBP, CAD, USD, AUD): Standard Showroom 99 · Custom Showroom 399 · Tailor-made Showroom 799 (Standard & Premium only) · Integration to Cloud Server 199 · Integration to IMS/DMS 299 · Integration to FTP/SFTP 199 · Training 150 (optional) · CarCutter Hub set-up 199 (optional).
- **US SMB Tier 1 set-up fees cannot be waived**: onboarding won't start and ARR won't be recognized until they are paid.
- **Quote templates** exist per language and contract duration (pattern `CARS - LANGUAGE - BILLING TYPE - DURATION`); picking the right duration puts the right T&Cs on the contract. In the US, Custom templates (with a comment box) go through manager approval; Standard ones don't.

### US offer: free months on a 12-month or 6-month contract

- **US strat accounts only.** Before offering 3 months free, the AE should **talk to their manager** (heads-up; no formal approval workflow, the standard template is used).
- **12-month contract**: the client gets 1 or 3 months free, then pays for 12 months (13 or 15 months in total), billed 12 times.
- **6-month contract**: the client gets 1 month free, then pays for 6 months (7 months in total), billed 6 times. No 3 months free on a 6-month contract.
- How: select the quote template of the **billed duration** (12-month or 6-month) with **Term = 12 or 6**, add the subscription as usual, then add the line item **CarCutter - 1 month free** (SKU CC1MONTHOFFER) or **CarCutter - 3 months free** (SKU CC3MONTHSOFFER), both at $0. The AE must **write the offer in the quote comments box** (e.g. "Includes 1 month free: billing starts 1 month after go-live, then 6 months").
- A workflow automatically pushes the subscription start date (and billing) by 1 or 3 months after onboarding completion when the deal contains these line items. Nothing to do for the AE; contract duration stays 12 or 6 months and the renewal is created at the right time.
- The free months are not part of ARR.

## Engagement models and contract durations

Source: Notion "Engagement models" (CarCutter Sales Playbook). Our engagement models:

1. 12-month commit (default)
2. 1-month pilot + 12-month commit contract
3. 3-month pilot + 12-month commit contract
4. 1-month with auto-renew (US only, larger accounts, manager approval required)
5. 3-month with auto-renew (US only)
6. 6-month contract (US)
7. Multi-year contract (≥ 18 months)

We do **not** accept pilots for month-over-month contracts.

**ARR recognition by commitment** (as of Q2 2024):

| Commitment | ARR recognition |
|---|---|
| 12-month contract | ARR |
| 1-month pilot then 12-month contract | If the pilot is successful, ARR is recognized excluding the pilot's MRR. If unsuccessful, nothing is recognized. |
| 3-month pilot then 12-month contract | If the pilot is successful, ARR is recognized excluding 3× the pilot's MRR. If unsuccessful, nothing is recognized. |
| 1-month contract | MRR of the first month at signature, plus the actuals of the next 11 months |
| 3-month contract | MRR of the first 3 months at signature, plus the actuals of the next 9 months |
| > 12 months (18, 24, 48 months) | ARR + 20% multiplier (for bonuses) |

## Pilots

Source: Notion "Pilots" (CarCutter Sales Playbook).

- A pilot is a **paid** first period (1 or 3 months), potentially at a lower price, that must convert into **at least a 12-month commit contract**. It is not a trial or a test: the client is onboarded and billed.
- A pilot contract contains the pilot period **followed by** the actual contract, as 2 line items. E.g. 1 month at $349, then 12 months at $449 (or the same price for both).
- If the contract doesn't look like this, it's not a pilot: create a standard 1- or 3-month contract.
- In HubSpot: set **Has a pilot? = Yes** (at deal creation, or at the Negotiation/trade stage at the latest), **Pilot monthly amount**, **Pilot duration in months**, **Pilot status = In pipeline or negotiation**.
- Pilot status values: *In pipeline or negotiation* (not signed) → *In progress* (signed, set automatically when the quote is signed) → *Success* (the client goes on with the 12-month contract) or *Exit* (the client stops: token deactivated, deal moves to Closed lost).
- The pilot period starts at **go-live** (the deal's Subscription start date): pilot end = Subscription start date + pilot duration.
- 1 or 3 months later, the AE must come back to the deal and set **Success** or **Exit**.
- If the whole deal is a pilot, its ARR is 0.
- After a pilot: more locations joining into a group agreement → Renewals & upsells pipeline; simply adding extra locations → New business.
- Optional comment to the buyer: "A xx-month pilot period begins on the go-live date (subscription start date). If the client notifies their intention to withdraw before the end of this period, the contract will be voided. However, the monthly subscription fee for the pilot month remains due. If no cancellation is received within this period, the contract will be automatically validated, and the client will be committed for a xx-month term. Integration fees are due in all cases."

---

# Module 4: Tools & reporting

## Modjo

- Admit the Modjo bot on Google Meet; click Record on HubSpot/AirCall calls. Remove other bots (Apollo, Fireflies…).
- **Tag every call**: tags trigger the AI prompts.
- Call reviews: 2 per month from your manager, and review at least 1 peer call per week, always with written comments.
- Modjo syncs to HubSpot only if the bot was admitted, the call tagged and the contact/company associated.

## HubSpot support

Click ❓ top right → Continue your chat → type **"talk to someone"** to reach a human.

## Dashboards

- AE EU dashboard / AE US dashboard: pipeline by stage, ARR signed, win rate (AEs and SMBs).
- BDR dashboard: leads worked, demos booked, meetings completed, conversion.
- Filter by your name (Owners → your name) and set it as your default view. Check it regularly, not only before your 1:1.
