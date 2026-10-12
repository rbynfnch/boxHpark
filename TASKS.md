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
- [ ] Board review of content-inventory.csv history facts (NEEDS ADMIN VERIFICATION)

## B. Site build (in order)
1. Header + footer (step 4)
   - [ ] Install Header Footer Elementor (free); header: logo + menu in cream, slate text, Sunshine hover/focus
   - [ ] Footer: Dark Slate, contact, social, quick links, newsletter placeholder
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
   - [ ] Our Story timeline (verification flags)
   - [ ] Volunteer: sign-up sheet plugin, Get Involved page
   - [ ] Support Box H: Stripe links, categories; use the photo + floating stat card + checklist layout (see PROJECT.md design note)
   - [ ] Fairview Resources: structured resource type + 6 categories
   - [ ] History archive (events tagged box-h-history)
   - [ ] About / Contact + contact form
5. Reservations (RESERVATIONS_PLAN.md)
   - [ ] Request form + Reserved calendar + fee table + rules
6. Plumbing
   - [ ] Newsletter (Mailchimp), Smash Balloon feed, SEO plugin + sitemap, SMTP email service, security + backups, Box H Admin role, share buttons
   - [ ] Remove Hello Dolly/Akismet if unused; trash unused kit templates

## C. Before launch
- [ ] Accessibility/contrast pass, mobile pass, speed
- [ ] Board approval, then migrate to permanent domain (org-owned), turn off noindex
