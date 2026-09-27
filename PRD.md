# PRD: PrintYourDay for wedding planners

Version 1. A static site for one audience. HTML, CSS, no JavaScript needed, on
GitHub Pages.

## Goal

Give wedding planners in Westchester and the New York area a page that answers
"can these people do big photo boards for my event, and how do I book it" in one
scroll, and gets them to call Adam.

## Audience and key action

- Wedding planners and venue coordinators, usually on a phone, between two other
  vendors, deciding whether to make a call.
- Couples the planner forwards the link to.

Key action: tap the phone number and call. Every page has it in the header.

## Pages

1. Home (`index.html`). What the boards are, one wedding photo, three reasons a
   planner should care (proof before print, 48 hour rush, delivery to the venue),
   the call button.
2. Gallery (`gallery.html`). Six real photos of boards at events, each with a
   caption saying the event and the size.
3. How it works and pricing (`how-it-works.html`). Upload a photo, approve a proof,
   pickup or delivery. The Three $500, The Five $750, Jumbo 5 by 10 foot by quote,
   48 hour rush add $50 per board. One line: planner rates by phone.
4. Contact (`contact.html`). Phone, email, studio in Mount Vernon NY, delivery
   zones (Westchester, the Bronx, Fairfield, NYC), hours from Adam.

## Navigation

One nav on every page: Home, Gallery, How it works, Contact, then the phone number
as a button. Footer repeats the phone and email.

## Content

**Have**

- Board spec: 40 by 60 inch rigid foam board, printed in the Mount Vernon NY studio.
- Process: upload, digital proof, free reprint if it does not match the proof.
- Prices: The Three $500, The Five $750, Jumbo by quote, rush $50 per board.
- Delivery: free studio pickup, $75 Westchester, Bronx and Fairfield, $100 NYC.
- Phone 914-478-2061, email hello@printyourday.com.
- Six photos in `images/`: wedding install, five pack in studio, graduation easels,
  couple on the beach board, birthday board, stand close up.

**Missing**

- Planner or trade pricing and minimum order. From Adam.
- Studio hours and street address to show publicly. From Adam.
- One quote from a planner or couple who used the boards. From Adam.
- More wedding photos. Only one of the six is a wedding. From Adam.

## Look

PrintYourDay's existing colours and font, so it reads as the same brand.

```
:root {
  --bg: #faf3eb;            /* cream, the page background */
  --text: #1a1612;          /* dark ink */
  --accent: #5a6a45;        /* sage green, used for the phone button and links */
  --font-body: "Outfit", system-ui, sans-serif;
  --space: 16px;            /* every gap is a multiple of this */
  --radius: 12px;           /* one corner radius, everywhere */
}
```

Photo-led, lots of white space, one price per product, nothing animated.
References: Minted's wedding pages for the photo and price layout, The Knot vendor
profiles for gallery first and one contact action.

## Checks

1. On a phone, a visitor can tap the phone number from any page without scrolling.
2. A visitor can find the price of The Five in under ten seconds from the home page.
3. Every photo in the gallery has a caption naming the event.
4. Nothing on the site mentions EastCoast MuralPros.
5. The site works with no horizontal scroll at 390 pixels wide.

## Out of scope

- Online ordering, upload, checkout.
- Consumer audiences (prom, graduation, birthdays).
- A blog, reviews widget, or Instagram feed.

## Later

- A quote request form (needs a server or a form service).
- Planner price list once Adam confirms it.
- Testimonials once Adam sends them.
- A matching version of this site for restaurants and storefronts.
