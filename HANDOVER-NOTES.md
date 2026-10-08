# Bo7 handover notes

Running list of things found while rebuilding bo7.ie, to go through with Ryan at the end. Two sections: what we changed versus the current site, and things on their side that need fixing regardless.

## Things on their side to fix

- **Glofox consent, Blackrock branch.** The Killiney lead form (branch 6659f3a6…) has the email and SMS consent checkboxes. The Blackrock lead form (branch 681a3f74…) does not. Until that's set up in Glofox, all web leads go to the Killiney branch and the team routes Blackrock enquiries by hand.
- **Glofox form heading.** The embedded lead form shows its own "Register Your Interest" title, which duplicates the overlay heading. That text lives in Glofox, not on our page. Check whether the lead-capture form title can be changed or hidden in Glofox settings; if not, ask Glofox support.
- **Instagram link is broken.** The site links to instagram.com/bo7_gym, which shows "Profile isn't available". Need the correct handle from Ryan.
- **Placeholder pages are live.** /contact-1 shows Squarespace demo text (email@example.com, 123 Demo Street) and /testimonials opens with the template's "Maybe you have a creative project…" copy.
- **Store index is empty.** /store renders "No results found" even though three products exist (28-Day Challenge €200, Blue Label Whey €36, Clear Label Whey €32).
- **Orphan pages in the sitemap.** /learn-morebo7-1-1 and /learn-morebo7-1-2 are "First-Timers (Copy)" pages. /class-timetable is a duplicate of /booking-1.
- **No meta descriptions on any inner page**, and titles like "Contact 1" and "First-Timers (Copy)" are indexed.
- **Blackrock has no map pin or footer address** on the current site.

## What we built versus what they have

| Area | Current bo7.ie | New build |
|---|---|---|
| Platform | Squarespace 7.1 | Static HTML/CSS/JS, no CMS, no build step |
| Homepage length | ~12,500 px, body text 12 px | ~9,000 px at desktop, body 17–19 px |
| Hero | Looping video with headline, "Learn More" button to a page of two iframes | Same video, re-encoded (2–3.5 MB); headline, two CTAs, three facts. Video behind the copy on phones, own column on desktop |
| Primary CTA | "Learn More" → /learn-morebo7-1 (two Glofox iframes) | "Book a free consultation" → overlay: WhatsApp first, then the Glofox form |
| Location choice | Visitor picks Killiney or Blackrock before the form | No choice. One form (Killiney branch), routed by the team |
| WhatsApp | Text link at page bottom | Green WhatsApp button in the overlay and sticky bar, prefilled message |
| USPs | Five bold paragraphs on a photo | Four numbered points beside a photo |
| How it works | Three accordion items + repeated text | Three numbered steps |
| Testimonials | Separate page, 6 YouTube videos, placeholder intro | On the homepage as six portrait tiles, click to play |
| Locations | Killiney address and map only | Both gyms with address, eircode, book button and timetable link |
| FAQ | Six accordion items, same answers shown twice | Same six, rewritten tighter |
| Gallery | 19-photo flat grid | Photos used in context across sections instead |
| Store / voucher | Nav item + voucher promo block | Footer link only (gift vouchers) |
| Nav | First-Timers, Bo7, PT Blackrock, Testimonials, Class Timetable (Killiney/Blackrock), Store, Instagram | Why Bo7, How it works, Results, Locations, FAQ, Book |
| Fonts | Archivo Black + proxima-nova | DM Serif Display + DM Sans (Google Fonts) |
| Images | Up to 2500w JPEG from Squarespace CDN, ~17 MB | WebP at 1800w/900w, ~7 MB total, lazy-loaded |
| Mobile | Standard Squarespace stack | Static header with Book + menu, sticky bottom bar (Book + WhatsApp), bottom-sheet overlay |
| Pages | 13 (many near-empty) | 1 so far (homepage); Blackrock, Killiney, Results, Coaches, Pricing, Thank-you planned |
| Tracking | GTM-NJRHF7LZ, GA4 G-Z20JQXCC3R | Not added yet; add GTM before launch |
| Hosting | Squarespace, bo7.ie | bo7.thedowlings.co for review, then bo7.ie |

## Still needed from Ryan

- Correct Instagram handle
- Member count, years open, Google rating for the hero facts
- Coach names, bios, photos
- Blackrock photos
- Pricing
- Whether Ryan's 44 s message video should go on the page (it's downloaded and encoded)
