# Vahnam Dealer & Admin Analytics Dashboard

## Overview

This project is a Power BI prototype designed for Vahnam, an independent
car-buying advisory and marketplace.

The objective is to transform marketplace and dealer-level data into
actionable business insights rather than simply displaying raw metrics.

The dashboard consists of two views:

1. Dealer Cockpit
2. Admin Cockpit

> Note: This prototype uses synthetic/mock data for demonstration.
> The figures shown should not be interpreted as actual Vahnam business
> performance.

---

## Business Problem

The original dashboard concept identified several gaps:

- Dealers were not clearly shown what actions required attention.
- Listing pricing and quality issues were difficult to identify quickly.
- Buyer funnel performance needed to be easier to interpret.
- Dealers needed visibility into buyer demand and unmet demand.
- Admin needed a marketplace-level view of supply, demand and platform
  health.
- Trust and listing-quality indicators needed to be surfaced in one place.

The prototype addresses these requirements through two role-based views.

---

## Dashboard Structure

### 1. Dealer Cockpit

The Dealer Cockpit answers:

> "What should the dealer act on today?"

It includes:

- Total listings
- Average asking price
- Average days listed
- Average photos
- Listings above the fair band
- Listings with insufficient photos
- Buyer funnel
- Funnel conversion rates
- Buyer searches
- Unmet demand
- Listing health
- Listings requiring attention
- Open buyer offers requiring response
- Accepted and sold offers
- Offer pipeline value

### 2. Admin Cockpit

The Admin Cockpit answers:

> "Where does the marketplace need attention?"

It includes:

- Total dealers
- Total listings
- Total sold
- Total views
- Listings above fair band
- Low-photo listings
- Buyer demand
- Dealer performance
- Listing-quality issues
- Trust-integrity indicators

---

## Key Prototype Insights

### Buyer Funnel

The prototype funnel shows:

Views → Saves → Messages → Test Drives → Sold

214 → 19 → 11 → 4 → 2

The largest proportional drop occurs between views and saves,
indicating that the top of the buyer funnel is the main conversion
opportunity in the prototype data.

### Listing Health

Listings are classified using business rules such as:

- Above Fair Band
- Low Photos
- Above Fair Band + Low Photos
- Stale Listing
- Good Value
- Healthy

This allows dealers to identify listings requiring attention.

### Buyer Demand

The dashboard highlights buyer searches that are not currently
matched by available inventory.

This can help dealers identify potential inventory sourcing
opportunities.

### Buyer Offers

Open offers are integrated with listing information so that the
dashboard can surface actionable items such as:

"Respond to Buyer Offer"

instead of requiring the dealer to interpret raw offer records.

---

## Data Model

The prototype uses the following primary tables:

- Dealers
- Listings
- Events
- Offers
- Buyer_Searches
- Subscription
- Fair_Band

The main relationships include:

Dealers → Listings
Dealers → Offers
Dealers → Subscription
Listings → Events
Listings → Offers

Power Query was used for data cleaning, transformation and combining
offer information with listing information.

---

## Power BI / DAX

DAX was used to create:

- Total Listings
- Average Ask Price
- Average Days Listed
- Average Photos
- Total Views
- Total Saves
- Total Messages
- Total Test Drives
- Total Sold
- Funnel Count
- View-to-Save %
- Save-to-Message %
- Message-to-Test-Drive %
- Test-Drive-to-Sold %
- Above Fair Band
- Low Photo Listings
- Open Offers
- Accepted Offers
- Sold Offers
- Offer Pipeline Value

Business-rule based calculated columns were also used for Listing Status
and Action Required.

---

## Tools Used

- Power BI
- Power Query
- DAX
- Microsoft Excel

---

## Data Disclaimer

This is a prototype built using synthetic/mock data.

The dashboard demonstrates the proposed analytical logic and user
experience. Production deployment would require integration with
Vahnam's actual database, event pipeline, VFM/fair-band engine,
subscription records and other production data sources.

Metrics such as ROI, gross margin, churn risk and detailed trust
signals should only be calculated after the required production data
is available and validated.

---

## Future Enhancements

Potential production enhancements include:

- Real ROI and attribution
- Gross-margin calculation
- Dealer churn-risk scoring
- Fair-band calibration against closed transactions
- Detailed trust-signal monitoring
- Buyer-to-listing matching
- WhatsApp weekly digest
- Real-time / scheduled refresh
- Production database integration
- Role-based access for Dealer and Admin users

---

## Outcome

The main objective of this prototype is to move from:

Raw Data → Metrics → Business Insight → Action

Examples:

Above Fair Band
→ Review Pricing

Low Photos
→ Improve Listing

Unmet Buyer Demand
→ Identify Inventory Opportunity

Open Buyer Offer
→ Respond to Buyer

This makes the dashboard a decision-support tool rather than a
collection of standalone charts.
