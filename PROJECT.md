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
- [ ] 1. Inventory kit templates; flag Elementor Pro-dependent ones (likely header, footer, forms, post grids)
- [ ] 2. Import templates, build Home page, note locked Pro widgets
- [ ] 3. Static front page, Blog page, global colors/fonts, logo
- [ ] 4. Header/footer without Theme Builder (Customizer or Header Footer Elementor)
- [ ] 5. The Events Calendar, volunteer form, newsletter, donations, Facebook feed
- [ ] 6. Reservations (last, after policy decisions)

## Open decisions for the owner
- Reservations: instant booking or request-and-approve (recommended: request-and-approve)?
- What is reservable (pavilion, fields, whole park) and fee for each?
- Nonprofit or town-owned? (donation platform, receipts, payment account owner)
- Permanent domain and hosting: who owns them (organization, owner as admin)?
- Park rules, use agreement, damage-deposit policy before reservations go live.
- Envato license terms (single purchase vs. Elements subscription).

## Migration notes
- Keep test site private: "Discourage search engines" on, SSL on.
- Do not import unneeded demo content.
- Migrate with All-in-One WP Migration, Duplicator, or UpdraftPlus; do a test run first.
- Real Stripe/PayPal/Zeffy and newsletter accounts belong to the organization, not the owner personally. Reconnect the Facebook feed on the final domain.
