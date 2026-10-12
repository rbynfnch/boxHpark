# Box H Park: task list for next session (target: 2026-10-13 after 22:40 UTC)

WPVibe free plan = 100 calls per rolling 24h. Plan ~15 calls per block; run `list_sites` first to check remaining.

## A. Needed from the owner/board (no WordPress calls)
- [ ] Pavilion, fields, whole-park fees (placeholders OK) + park rules / use agreement / deposit policy
- [ ] Facebook "About" text + recent event posts (Facebook is not reachable from the build environment)
- [ ] Park address, contact email/phone, current board names (permission to list)
- [ ] Org Mailchimp account (or choose MailPoet), org Stripe payment links (general, playground, events, maintenance; one-time + monthly)
- [ ] Google Maps API key (for event maps) if wanted
- [ ] Confirm Envato kit license; confirm this Safari & Zoo kit is the one purchased
- [ ] Better logo file (PNG, transparent background) and more park/family photos
- [ ] Board: list of current park needs still open (roof, grill, grandstand, sprinklers, lighting, other) and which Stripe fund each maps to
- [ ] Board review of content-inventory.csv history facts (NEEDS ADMIN VERIFICATION)

## B. Site build (in order)
1. Header + footer (step 4)
   - [ ] Install Header Footer Elementor (free); header: logo + menu in cream, slate text, Sunshine hover/focus
   - [ ] Footer: Dark Slate, contact, social, quick links; newsletter band above it per PROJECT.md design note (Park Green band, Name+Email side by side, Sunshine button)
   - [ ] Kit-wide button radius 7px (Site Settings > Buttons), cream page background, darker-blue link color #2F6580
2. Events page (EVENTS_PLAN.md)
   - [ ] TEC settings: default mobile view List, /events/ styling with palette
   - [ ] Events landing content: header, featured event, category buttons, Follow Along, newsletter, history link
   - [ ] Event Tickets (RSVP) installed
   - [ ] 3-5 sample DRAFT events from content-inventory.csv (movies, Pioneer Day, July 4)
3. Home page polish
   - [ ] Connect Upcoming Events and Latest News to live content (TEC shortcode, post list)
   - [ ] Mobile check; hero photo choice
4. Core pages
   - [ ] About Box H Park (one page, /about/ ID 122; see ABOUT_PLAN.md): story, timeline, playground, movies, photos, Meet the Board, partners, contact. Then: rename page 122 + menu item 131 to "About Box H Park", remove "Our Story" menu item 128, trash page 120
   - [ ] Volunteer: sign-up sheet plugin, Get Involved page
   - [ ] Support Box H: Stripe links, categories; use box-h-park.jpg (ID 113) + floating stat card + checklist of CURRENT needs (see PROJECT.md design note)
   - [ ] Fairview Resources: structured resource type + 6 categories
   - [ ] History archive (events tagged box-h-history)
   - [ ] Contact form + address on the About page (and footer)
5. Reservations (RESERVATIONS_PLAN.md)
   - [ ] Request form + Reserved calendar + fee table + rules
6. Plumbing
   - [ ] Newsletter (Mailchimp), Smash Balloon feed, SEO plugin + sitemap, SMTP email service, security + backups, Box H Admin role, share buttons
   - [ ] Remove Hello Dolly/Akismet if unused; trash unused kit templates

## C. Before launch
- [ ] Accessibility/contrast pass, mobile pass, speed
- [ ] Board approval, then migrate to permanent domain (org-owned), turn off noindex
