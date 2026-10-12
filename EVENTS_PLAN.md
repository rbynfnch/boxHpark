# Events & Community Calendar: plan (free plugins only)

One record per event: The Events Calendar (free) event post. History = the same record, tagged `box-h-history`, so nothing is duplicated.
Lifecycle: Draft/Scheduled -> Published -> (date passes) automatically moves to Past/Archive -> editor adds recap + photos + History tag -> appears in History archive.

| Requirement | How (free) | Gap / note |
|---|---|---|
| Admin create/edit/publish/schedule/delete events | TEC event editor, WP scheduling, Editor/"Box H Admin" role | Fine |
| Title, descriptions, image, gallery, category, start/end, all-day | TEC + WP block editor (gallery block) | Fine |
| Location, address, map | TEC Venues (map needs a Google Maps API key) | Key needed from the org |
| Organizer, contact | TEC Organizers | Fine |
| Cost / free / admission | TEC cost field | Fine |
| Featured event (fallback to next upcoming) | TEC "Feature event" checkbox + shortcode `[tribe_events view="list" featured="true" ...]`; if none featured, show next event | Fallback needs a small snippet or a second shortcode; verify on site |
| Calendar/list toggle, default list on mobile | TEC view switcher; set mobile default view to List | Fine |
| Event cards (date, time, location, image, category) | TEC list view, styled with palette | Fine |
| Categories (11 initial) + admin-editable | TEC event categories | Fine |
| Filters: category, month, year | Category pills link to category views; TEC date picker/month nav; "Past" view for years | Dropdown category filter bar is a paid add-on (Filter Bar) |
| Own URL per event, SEO, schema, OG | TEC single URLs + Event JSON-LD; SEO plugin (Rank Math/Yoast free) for OG/meta | Fine |
| Add to calendar (Google/iCal) | Built into TEC single event | Fine |
| Register / capacity / deadline | Event Tickets (free) RSVP with capacity and attendee list | Fine; no payments (use Stripe link) |
| Volunteer integration with "18 of 25 filled" | Volunteer Sign Up Sheets plugin; place its shortcode on the event page | Linked by shortcode, not a database relation |
| Donate / Reserve / Directions / Website / Contact buttons | Button blocks added per event (only the ones that apply); Directions via TEC venue map link | Not automatic; editor adds them. Reusable block patterns provided |
| Reservation relationship / no double-booking | Reserved/blocked dates are TEC events in "Reserved" category shown on Reserve calendar; community events marked | No automatic conflict blocking in the request form |
| Share (Facebook, copy, email, native) | Free share-buttons plugin or small snippet (WPCode) | Native mobile share needs snippet |
| Photos + recap after event | Edit same event: gallery + recap section | Fine |
| Past events auto-archive, filters by year/category | TEC Past view + category views; History page lists `box-h-history` | Fine |
| Recurring events | NOT free (Events Calendar Pro) | Duplicate events with a free duplicate plugin; each occurrence editable/cancellable. Revisit if burdensome |
| Postponed / Cancelled / Location changed banner | Banner block pattern at top of event + title prefix | Manual; no automatic email to attendees (use Mailchimp/Event Tickets attendee email manually) |
| Submit/request an event (on/off) | Fluent Forms/WPForms Lite form emailing the board; show/hide the button | Does not auto-create events |
| Newsletter (Name + Email) | Mailchimp for WP free (or Mailchimp embed) | Needs the org's Mailchimp |
| Facebook posts below | Smash Balloon free feed | Token can expire |
| Event page header text, CTAs, history link, newsletter | Elementor page "Events" with shortcode widgets | TEC /events/ is plugin-rendered |

## Build order
1. Install TEC + Event Tickets; set default mobile view = List; create 11 categories + `box-h-history` tag.
2. Events page (Elementor): header, featured shortcode, list/calendar, category pills, Follow Along, newsletter placeholder, history link.
3. Style TEC with global colors (Park Green/Sunshine/Clay).
4. Sample draft events from content-inventory.csv (needs board verification).
5. Volunteer sheets, share buttons, SEO plugin, Mailchimp, Smash Balloon.
