# Reservations without a paid plugin (request-and-approve)

Recommended: free plugins only, board approves manually.
1. Request form: free form plugin (Fluent Forms or WPForms Lite). Fields: name, org, email, phone, facility (pavilion / fields / whole park), type, date, start/end, attendance, description, requests, rules agreement checkbox. Emails the board on submit and stores entries.
2. Public availability calendar: The Events Calendar (free). Board adds approved reservations as events in a "Reserved" category (one per facility). The public Reserve page shows the month view filtered to Reserved, so visitors see taken dates before asking.
3. Fee table: normal editable page/table (not hard-coded in code). Park rules and agreement text on the same page.
4. Approve/decline: board checks the form entry, replies by email (template provided), adds the event to the calendar. Pending requests stay in the entries list.
5. Whole-park reservations: board adds one event in each facility category.

Limits (honest): no automatic conflict check, no automatic approval/decline emails, no reminder emails, no deposit collection online (use a Stripe Payment Link sent in the approval email if a deposit is required).

Alternative to test before deciding: free Booking Calendar plugin (day-based, pending/approved, email notices). Free version likely limits multiple facility calendars; verify on the test site.
