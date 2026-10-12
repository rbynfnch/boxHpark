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
