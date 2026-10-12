# Box H Park community website (Fairview, WY)

WordPress site for Box H Park: community bulletin and park reservation portal.
Built on a TEST domain for board approval, then migrated to a permanent domain.

## Required features
- Community bulletin: upcoming events + past-event history (posts in a "Past Events" category)
- Volunteer sign-up form (emails coordinator, stores submissions)
- Monthly newsletter signup (Mailchimp or MailPoet), in footer + homepage
- Recent Facebook posts feed (Smash Balloon free; tokens expire, so also publish main news on the site itself)
- Donations (Zeffy or GiveWP w/ Stripe/PayPal)
- "Welcome to the Fairview community" resource page (town offices, services, emergency contacts; owner supplies real details)
- Park reservation portal: fee table, live availability calendar, online request/booking (Amelia or Booking Calendar)
- Backend so board members can post: Editor role accounts

## Decisions made
- Platform: self-hosted WordPress (not custom-coded).
- Theme: Envato "Touro/Tourago" travel template KIT (Template Kit Import plugin) on Hello Elementor + free Elementor. Travel-specific wording and booking widgets must be removed or renamed.
- Elementor Pro: NOT purchasing now. Only annual licenses exist; never use "lifetime"/nulled/GPL-repack copies. Revisit a ~$60/yr single-site license only if a real blocker appears.
- Elementor is for the homepage and a few key pages only. Posts use the normal editor. Events, forms, booking and donation plugins render their own pages; style them with global colors/fonts, do not rebuild them in Elementor.
- Design: large park hero photo; earthy palette (forest green, warm tan, sky blue); big high-contrast, readable text for older users; prominent buttons: Reserve the Park, Volunteer, Donate, Newsletter.
- Homepage order: hero > upcoming events > Get Involved buttons > latest news > Facebook feed > newsletter signup in footer.

## Current state
- Hosting: GoDaddy web hosting, Enhance control panel.
- Test site: testsite2.elevartemis.com (fresh WordPress). The main elevartemis.com site must NOT be touched; back it up before any server-level change.
- Hosting plan primary domain is robyn.dev (owner may not control it). Build nothing permanent on it.
- Installed/active: WordPress, Hello Elementor, free Elementor, Template Kit Import, the kit's required plugins, Touro kit zip uploaded.

## Build checklist
- [x] 1. Inventory kit templates (see KIT_INVENTORY.md)
- [x] 2. Kit templates imported to Elementor library (14, already present); Home page built as DRAFT (page ID 105) with placeholders for events, news, Facebook, newsletter. Pro-only widgets avoided.
- [x] 3. Done on test site: Home (ID 105) published as static front page (hero photo ID 110, since-1980 copy); "News & Community" page (ID 115) is the Blog page; logo (media 107) set; tagline set; kit global colors changed to forest green / tan / sky blue and body text raised to 20px. Logo is a JPG (check for white box); alt text added to logo + hero. Media IDs: 107 logo, 110/113 park, 108/109/111/112 drive-in.
- [ ] 4. Header/footer without Theme Builder (Customizer or Header Footer Elementor)
- [ ] 5. The Events Calendar, volunteer form, newsletter, donations, Facebook feed
- [ ] 6. Reservations (last, after policy decisions)

## Open decisions for the owner
- ~~Reservations: instant booking or request-and-approve?~~ DECIDED: request-and-approve (board approves each request).
- Reservable: pavilion, fields, and whole park (confirmed). Fee for each still needed.
- ~~Nonprofit or town-owned?~~ DECIDED: nonprofit. Use Zeffy (free for nonprofits, no platform fee); confirm EIN/501(c)(3) status for receipts and that the org (not the owner personally) holds the payment account.
- Permanent domain and hosting: who owns them (organization, owner as admin)?
- Park rules, use agreement, damage-deposit policy before reservations go live.
- Envato license terms (single purchase vs. Elements subscription).

## Migration notes
- Keep test site private: "Discourage search engines" on, SSL on.
- Do not import unneeded demo content.
- Migrate with All-in-One WP Migration, Duplicator, or UpdraftPlus; do a test run first.
- Real Stripe/PayPal/Zeffy and newsletter accounts belong to the organization, not the owner personally. Reconnect the Facebook feed on the final domain.

## Public info found (unverified, from web search; Facebook page not reachable from the build environment)
- Box H Park Inc., 501(c)(3), Fairview, WY, EIN 88-2628486. Mission: a community park with a ball field, playground, shelter and open space. Source: https://charitynavigator.org/ein/882628486
- Fairview is an unincorporated community in Lincoln County, WY (2020 pop. 277).
- Still needed from the owner: address, contact email/phone, rules, hours, events, board names. Paste Facebook "About" text or recent posts.

## Owner decisions (latest)
- No paid plugins. Reservations: free approach (see RESERVATIONS_PLAN.md). Elementor Pro: still no.
- Stripe account already exists (organization-owned). Donations via Stripe, no paid donation plugin.
- Theme colors will be changed and Box H's own photos supplied (do not use third-party photos, incl. SVI).
- Hero idea: "A gathering place for Fairview families, friends and neighbors since 1980." + "100% community supported."
- Content inventory started: content-inventory.csv (all rows need board verification).

## Palette and button system (owner directive; applied to test site)
- Park Green #557A5B (primary, headings, primary buttons) | Sky Blue #6FA1B8 (secondary sections, calendar, resources) | Sunshine #E4B94F (secondary CTAs, event dates, sparingly) | Clay #C66D4B (Donate/Support only, small areas) | Warm Cream #FAF7EF (main background) | Dark Slate #303A3D (text, footer).
- Buttons: Primary = Park Green bg + Cream text (View Events, Check Availability, Reserve). Secondary = Sunshine bg + Slate text (Volunteer, Get Involved, Newsletter). Support = Clay bg + Cream text (Donate, Support Box H). Corner radius 7px.
- Contrast notes (computed): Cream on Park Green 4.54 (ok), Slate on Sunshine 6.3, Slate on Cream 10.9, Cream on Clay 3.45 (large bold text only), Sky Blue on Cream 2.63 (never for text/links; use a darker blue like #2F6580 = 5.95 for link text), Slate on Park Green 2.4 (never).
- Availability statuses must use icon + text (Available / Pending / Reserved), not color alone.
- Applied: Elementor global colors set; Home page rebuilt with the section color plan (hero photo, cream events, green community message, sky-tint reservation, cream get-involved cards, deeper-cream news, sky-tint Facebook, cream Welcome to Fairview, green newsletter). Footer (Dark Slate) is built in step 4.
- Not yet done: kit-wide default button radius (new buttons need 7px set per button, or Site Settings > Buttons), page body background cream on non-Elementor pages, link color in kit, Info color, hover/focus states outside Home.

## Events system (see EVENTS_PLAN.md)
- Installed on test site: The Events Calendar 6.18.0 (free). Created event categories: Community, Family, Celebration, Fundraiser, Volunteer, Movies, Sports, Park, Meeting, Youth, Other, plus "Reserved (park in use)" for the reservation calendar; tag "Box H History" (box-h-history) marks events that become history records.
- NOT done yet: Event Tickets (registration), volunteer sign-up plugin, Events page layout/styling, TEC settings (mobile default = List), sample events, share buttons, SEO plugin, Mailchimp, Smash Balloon.
- Known gaps in free tier: recurring events, category dropdown filter bar, automatic attendee emails on cancellation, automatic volunteer-count link.
- WPVibe free plan allows 100 calls per rolling 24 hours; batch work.

## Navigation menu (done)
- "Main Menu" (ID 16) assigned to header location: Home, Events & Calendar (/events/, plugin page), Reserve the Park (/reservations/, ID 117), Get Involved (/volunteer/, 118), Support Box H (/donate/, 119), Our Story (/our-story/, 120), Fairview Resources (/fairview-resources/, 121), News / Community (/news/, 115), About / Contact (/about/, 122). Pages 117-122 are "coming soon" placeholders (published, site hidden from search engines).
- Verified in page HTML: desktop nav plus mobile toggle menu render. Header still uses theme default styling (not yet palette-styled); footer not built (Dark Slate, step 4).
- WPVibe free plan: 100 calls / rolling 24h; about 93 used at this point.

## Design note: donations section idea (from owner screenshot of kit's About section)
- Layout: large photo on the left with a floating white stat card overlapping its edge (big number, small label, dark bar below); on the right a big heading, short paragraph, two-column checkmark list, and one button.
- Adapt for "Support Box H": photo = playground/community (owner's own photo); floating card = a verified stat (e.g. "$92,000 playground, 500+ volunteer hours": NEEDS ADMIN VERIFICATION) instead of the star rating and "Top Company"; checklist = what gifts fund (playground, roof/grandstand repairs, lighting, sprinklers, events, maintenance); button = Clay "Support Box H".
- Buildable with free Elementor widgets (image, heading, text, icon list, button, nested containers). Use Park Green checkmarks, cream/white card, Dark Slate text.
- Also usable on Home ("Box H belongs to the community") and Our Story.
