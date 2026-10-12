# Plan vs. Build Directive

The directive reads like a spec for a custom app (database tables, admin dashboard). Our decision is self-hosted WordPress. Mapping: "tables" become custom post types and plugin data; "admin dashboard" becomes wp-admin with custom roles. This meets the intent (no code editing for volunteers) but is not literal custom tables. CONFIRM WITH OWNER.

Status: OK = covered by plan | CHANGE = plan needs revising | NEW = not in plan

| Directive item | Status | WordPress approach / what changes |
|---|---|---|
| Brand: warm, Wyoming, not rustic; real photos | OK | Palette fine. Kit is a safari/zoo template; use only for layout/styles, drop animal imagery. Needs real Box H photos from owner. |
| Mobile-first, big CTAs | OK | Already in design notes. Must test on phone. |
| 9-item primary nav | CHANGE | Plan had no nav. Create: Home, Events & Calendar, Reserve the Park, Get Involved, Support Box H, Our Story, Fairview Resources, News/Community, About/Contact. Header Footer Elementor + WP menu. |
| Homepage (8 sections) | CHANGE | Draft has 6 and different copy. Add: Community Message, Park Reservation ("Planning a gathering?"), Welcome to Fairview, 3 Get Involved cards; hero text/buttons per directive; newsletter with Name + Email. |
| Events DB + calendar + list | OK/CHANGE | The Events Calendar (free): title, dates, venue, organizer, category, featured image, calendar + list views, past events auto-archive. Replaces the manual "Past Events" category in the plan. Registration/volunteer/donation links and featured flag via extra fields. |
| Volunteer system (spots filled, export) | CHANGE | A plain form is not enough. Need a sign-up-sheet plugin with slots ("18 of 25"), admin list, CSV export, email to coordinator. |
| Donations: categories, Stripe, recurring, admin records | CHANGE (decision) | Plan said Zeffy. Directive wants Stripe + donation records visible to admins. GiveWP + Stripe fits that (records in WP, funds, recurring, but Stripe fees ~2.9%+30c). Zeffy is free for nonprofits and supports recurring, but records live in Zeffy dashboard, not WP. OWNER DECIDES. |
| Reservations: date/time, types, editable fees, statuses, manual entry, blocked dates, emails | CHANGE (cost risk) | Hardest feature. Free booking plugins are mostly day-based or appointment-oriented and may lack approval workflow, blocked/maintenance states or hourly rentals. Likely needs a paid plugin (check price and features before choosing). Request-and-approve confirmed. Deposit only after approval. |
| Email notifications (submitted/approved/declined/cancelled/reminder) | NEW | Needs an SMTP/transactional service (Brevo, SendGrid, Postmark or similar) plus an SMTP plugin; GoDaddy mail is unreliable. |
| Our Story timeline | NEW | Page with visual timeline (containers or ElementsKit Lite widget). Facts from directive marked NEEDS ADMIN VERIFICATION until board confirms. |
| History/Archive with filters | NEW | Custom post type "History" with categories (Events, Improvements, Community, Fundraising, Volunteer, History, Photos) + fields (year, people, sources, related links). Filtering/grid is easy with Elementor Pro Loop Grid; on free Elementor use a filter plugin or category archives. |
| Fairview Resources (structured, categories) | CHANGE | Plan had one static page. Make a "Resource" custom post type with 6 categories so volunteers add/edit entries. |
| News/Posts with related event/volunteer/campaign | CHANGE | Native posts + categories + year archives; related-item links via a custom fields plugin. |
| Admin dashboard (events, reservations, volunteers, donations, settings...) | CHANGE | Plan only had "Editor accounts". Editors cannot manage plugin settings. Create a "Box H Admin" role (role editor plugin), optional dashboard widget, and a Park Settings options page (fees, rules, facilities, policies) via custom fields plugin. |
| Photos system | NEW | Media library + folders plugin; uploads by admins only; no third-party photos downloaded. |
| Newsletter (Name+Email, external provider) | OK | Mailchimp (preferred over MailPoet to avoid sending from the host). Add Name field. |
| Facebook supplements site | OK | Smash Balloon free feed + site owns content. |
| SEO, OG, schema, sitemap, robots, analytics | NEW | SEO plugin (Rank Math or Yoast), Site Kit/analytics, image optimization, caching. Keep noindex until launch. |
| Security / backups / speed | NEW | Security plugin + 2FA for admins, UpdraftPlus backups, caching. |
| Content inventory spreadsheet (SVI-NEWS, Facebook, etc.) | NEW | Build CSV/XLSX with columns Year, Date, Event, Category, Description, Source, Photo Available?, Website Destination, Verification Needed?. Original summaries only, link sources, mark NEEDS ADMIN VERIFICATION. Facebook is NOT reachable from my build environment; owner must paste/export it. |
| Future-ready features | OK | Not built now; WP plugin ecosystem allows adding later. |

## Biggest risks
1. Reservation plugin likely needs a paid license; verify features first.
2. Donation platform choice (Zeffy vs GiveWP+Stripe) changes the admin-records requirement.
3. Elementor Pro (~$60/yr) may become worthwhile for History/Resources filtering. Current rule: only if a real blocker appears.
4. Historical facts (Hugh Bagley, 1980/1992/2022/2023/2024, $92,000, 500+ hours) are unverified.
5. Kit look is safari/zoo; heavy restyle needed to feel like "our park".
