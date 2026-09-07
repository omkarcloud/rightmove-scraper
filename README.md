# Rightmove Scraper

Rightmove Scraper gets you 🎯 accurate, 🔍 detailed Rightmove data as clean JSON in **Real-Time**.

No selectors, no proxies, no data cleaning. Just the data.

[**Try it now in the playground**](https://www.omkar.cloud/tools/rightmove-scraper/playground) - See the data quality for yourself in one click, **No sign-up required**.

**Build on it free:** 1,000 calls every month, no credit card ❤️

[![Rightmove Scraper API playground — run a live request in your browser, free, no sign-up](https://raw.githubusercontent.com/omkarcloud/rightmove-scraper/master/playground.png)](https://www.omkar.cloud/tools/rightmove-scraper/playground)

## What can I get

- 🏠 **Live UK listings for sale, to rent, new homes & student lets** — price, beds, size, tenure, agent phone; 24 per page, filter & sort
- 📋 **Full property details** — key features, floor plans, EPC documents, nearest stations, council tax, broadband, plus similar homes nearby
- 💷 **Sold house prices** — HM Land Registry records with full transaction history; 1.9M+ sold records for London alone
- 🧑‍💼 **Estate agents & commercial property** — every branch in a location with phone & listings; commercial units for sale and to rent

## Why Rightmove Scraper

Most other Rightmove APIs fail you in one of four ways:

- 🗄️ **Inaccurate, cached, stale data**
- 🧩 **Low-detail endpoints** — a few fields per call, never the full picture
- 💸 **Pay more to get the same data**
- 🪦 **Works today, breaks next month** — nobody maintains it

Rightmove Scraper is scraped live on every call, priced honestly, and actively maintained.

## Example: A Full Rightmove Property

```json
{
  "id": 90076491,
  "link": "https://www.rightmove.co.uk/properties/90076491",
  "channel": "sale",
  "title": "6 bedroom end of terrace house for sale in Mercers Road, Islington, London, N19",
  "address": { "display": "Mercers Road, Islington, London, N19", "outcode": "N19", "incode": "4PW", "uk_country": "England" },
  "property_type": "End of Terrace",
  "bedrooms": 6,
  "bathrooms": 1,
  "price": { "amount": 2500000, "currency": "GBP", "display": "£2,500,000", "qualifier": "Guide Price", "per_sqft_display": "£729.93 per sq ft" },
  "sizes": { "sqft": { "min": 3425, "max": 3425 }, "sqm": { "min": 318, "max": 318 } },
  "tenure": { "type": "FREEHOLD" },
  "is_premium_listing": true,
  "key_features": ["Substantial Victorian terraced residence", "Six bedrooms", "Approximately 3,425 sq ft"],
  "description": "An exceptional six-bedroom Victorian residence of rare scale and character, offering over 3,400 sq ft, elegant period detail, private gardens, cellar, garage and outstanding potential...",
  "listing_history": "Added on 24/06/2026",
  "location": { "latitude": 51.559124, "longitude": -0.125572 },
  "nearest_stations": [
    { "name": "Upper Holloway Station", "types": ["LONDON_OVERGROUND"], "distance_miles": 0.36 },
    { "name": "Tufnell Park Station", "types": ["LONDON_UNDERGROUND"], "distance_miles": 0.56 }
  ],
  "features": { "parking": ["Yes"], "garden": ["Yes"] },
  "living_costs": { "council_tax_band": "TBC" },
  "images": [
    { "link": "https://media.rightmove.co.uk/property-photo/b897ccbcb/90076491/b897ccbcb2f613f34636d34f7564017d.jpeg", "caption": "Picture No. 02" },
    { "link": "https://media.rightmove.co.uk/property-photo/df08deefb/90076491/df08deefb3045f3162bfe3464ea8ace1.jpeg", "caption": "Picture No. 65" }
  ],
  "floorplans": [
    { "link": "https://media.rightmove.co.uk/property-floorplan/0b6f20d53/90076491/0b6f20d537383a9ef2ff7ff1ba6ddd2a.jpeg", "type": "IMAGE" }
  ],
  "virtual_tours": [ { "link": "https://youtu.be/_JGGYE_QyLA", "caption": "Virtual Tour 1" } ],
  "epc_documents": [ { "link": "https://media.rightmove.co.uk/property-epc/680c8a318/90076491/680c8a31875c85073aca9647e86fd168.png", "caption": "EPC Rating Graph" } ],
  "agent": {
    "branch_id": 54266,
    "name": "Drivers & Norris, Islington - Sales",
    "company": "Drivers & Norris",
    "address": "407-409 Holloway Road, London, N7 6HP",
    "link": "https://www.rightmove.co.uk/estate-agents/agent/Drivers-and-Norris/Islington---Sales-54266.html",
    "logo_link": "https://media.rightmove.co.uk/partner-logo/7608860-LOGO-1765976116.jpeg"
  },
  "contact": { "method": "EMAIL", "phone": "020 3834 8624" }
}
```

*Trimmed for readability.*

## Get Started with 1,000 Free Calls

Start in the [playground](https://www.omkar.cloud/tools/rightmove-scraper/playground) — try any endpoint with one click, no sign-up required.

Once you're happy with the data, start with the free plan for 1,000 free calls every month:

1. [Sign up on Omkar Cloud](https://www.omkar.cloud/auth/sign-up?redirect=/tools/rightmove-scraper/playground) — free, no credit card.
2. Open the [Rightmove Scraper playground](https://www.omkar.cloud/tools/rightmove-scraper/playground) and enter any UK town or postcode you like. Click **Get Live Data**.
3. Enjoy your data 😎.

## Endpoints

15 endpoints cover everything you need.

| Endpoint | Path | Returns |
|---|---|---|
| Location Autocomplete | `/rightmove/locations/auto-complete` | Any UK place name → the location identifier every search accepts |
| Search For Sale / To Rent / New Homes / Student | `/rightmove/properties/search-sale`, `/rightmove/properties/search-rent`, `/rightmove/properties/search-new-homes`, `/rightmove/properties/search-student` | 24 listings per page; filter by price, beds, type, radius, keywords; sortable |
| Search Commercial For Sale / To Rent | `/rightmove/commercial/search-sale`, `/rightmove/commercial/search-rent` | Commercial units with size, price, classification and photos |
| Property Details | `/rightmove/properties/details` | Everything about one listing in a single call |
| Similar Properties | `/rightmove/properties/similar` | Comparable homes Rightmove shows next to a listing |
| Property Broadband | `/rightmove/properties/broadband` | Broadband types available at the property's address |
| Sold House Prices | `/rightmove/house-prices/search` | HM Land Registry sold records for any UK area, 25 per page |
| Sold House Price Details | `/rightmove/house-prices/details` | Full transaction history and location for one sold property |
| Search Estate Agents | `/rightmove/agents/search` | Branches in a location with phone, brand and sales/lettings flags |
| Estate Agent Details | `/rightmove/agents/details` | Full branch profile with address, postcode and coordinates |
| Estate Agent Listings | `/rightmove/agents/listings` | A branch's live listings, for sale or to rent |

## Pricing

High value, Low price.

| Plan | Price | Calls / month | Per 1,000 |
|---|---|---|---|
| **Basic** | **Free** | **1,000** — the most generous free plan | $0 |
| **Pro** | $16/mo | 20,000 | $0.80 |
| **Ultra** | $48/mo | 100,000 | $0.48 |
| **Mega** | $148/mo | 400,000 | $0.37 |

Need a bigger plan? Ask on [WhatsApp](https://api.whatsapp.com/send?phone=918178804274&text=I%20need%20a%20custom%20plan%20for%20the%20Rightmove%20Scraper%20API.) or [Email](mailto:happy.to.help@omkar.cloud?subject=Custom%20plan%20for%20Rightmove%20Scraper%20API&body=I%20need%20a%20custom%20plan%20for%20the%20Rightmove%20Scraper%20API.).

- [**90 Day 2 Click Refund Guarantee**](https://www.omkar.cloud/refund-process)
- This is an excellent API made by Omkar Cloud, which is Rated Excellent — [4.7 based on 30 reviews on Trustpilot](https://www.trustpilot.com/review/omkar.cloud).

👉 [Start with Free Plan](https://www.omkar.cloud/auth/sign-up?redirect=/tools/rightmove-scraper/playground) — 1,000 free calls/month

## 💬 Have Questions? We Have Answers.

You're a developer — we know how hard completing a project can be. So we offer full support: just message us and we'll reply ✅ with a solution within 1 working day.

[![Message Us on WhatsApp about Rightmove Scraper](https://raw.githubusercontent.com/omkarcloud/assets/master/images/whatsapp-us.png)](https://api.whatsapp.com/send?phone=918178804274&text=I%20need%20help%20using%20the%20Rightmove%20Scraper%20API.)

[![Ask Us by Email about Rightmove Scraper](https://raw.githubusercontent.com/omkarcloud/assets/master/images/ask-on-email.png)](mailto:happy.to.help@omkar.cloud?subject=Help%20with%20Rightmove%20Scraper%20API&body=I%20need%20help%20using%20the%20Rightmove%20Scraper%20API.)

## Popular Scrapers by Omkar Cloud

- [**Google Maps Scraper (3,100+ GitHub Stars)**](https://github.com/omkarcloud/google-maps-scraper) — type "estate agents in London", get every business as a ready-to-call lead list: phones, emails, websites & reviews. Up to 100K free leads/month.
- [**Zoopla Scraper**](https://www.omkar.cloud/tools/zoopla-scraper) — UK property search, details, house prices & agents
- [**Website Email Contact Scraper**](https://www.omkar.cloud/tools/website-email-contact-scraper) — emails, phones & socials from any website
- [**AliExpress Scraper**](https://www.omkar.cloud/tools/aliexpress-scraper) — live product details, SKU variants, stock & shipping
- [**Booking Scraper**](https://www.omkar.cloud/tools/booking-scraper) — Booking.com hotels: prices, ratings, rooms & amenities
- [**IMDb Scraper**](https://www.omkar.cloud/tools/imdb-scraper) — movies, TV, ratings, cast, charts & box office

👉 [Start with Free Plan](https://www.omkar.cloud/auth/sign-up?redirect=/tools/rightmove-scraper/playground) — 1,000 free calls/month
