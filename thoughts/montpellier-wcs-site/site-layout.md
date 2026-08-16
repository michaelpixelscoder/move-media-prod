
# Site Layout

## Audience journeys and information priority

The six proposed audiences do not need six separate websites. They cluster around three jobs:

1. **Understand and begin** — people who do not yet know the dance or do not know how to start locally.
2. **Plan** — students comparing a season of classes, teachers, schedules, prices, and locations.
3. **Dance soon** — local regulars and visitors asking what is happening tonight, this week, or on a specific date.

Community subscription supports all three jobs, but it is a continuation action rather than the main reason most people arrive.

Traffic volume and frequency are hypotheses until analytics and interviews exist. The relative estimates below are useful for deciding prominence, not for forecasting audience size.

| Audience | Situation and likely question | Likely arrival | Expected volume | Frequency per person | Homepage treatment | Durable destination |
| --- | --- | --- | --- | --- | --- | --- |
| Curious non-dancer | “I want to learn a social dance; what is WCS and would I enjoy it?” | Broad search such as “cours danse couple Montpellier”, a short dance video, a friend’s link, or an open-day post | Potentially high, but weakly qualified | One or a few visits before deciding | A compact emotional introduction with a real dance image/video and a clear “Découvrir le WCS” path; do not make the whole homepage an explanation | `/decouvrir` evergreen guide, then `/debuter` |
| WCS-aware newcomer | “I want to start WCS; can I come alone, which level, and where do I begin?” | Specific search, teacher/studio social post, recommendation, or a shared direct link | Medium to high, especially August–October and January | Several visits during comparison, then rarely | Primary “Commencer” action plus the next beginner-friendly opportunities | `/debuter` decision guide, feeding filtered `/cours?niveau=debutant` and beginner events |
| Prospective yearly student | “Which class fits my level, weekday, teacher, budget, and commute?” | Search, a teacher link, QR code at an open day, or a returning bookmark | High but strongly seasonal | Repeated comparison over days or weeks near registration | A visible “Cours & planning” action; during registration season, a temporary status strip may promote open days and deadlines | `/cours` comparison view, actor profiles, place pages/map, authoritative registration links |
| Regular local dancer | “Where can I dance this week, and did anything change?” | Bookmark/direct URL, installed shortcut, WhatsApp/Messenger link, social post, or search for a named event | Smaller unique audience but highest repeat usage | Weekly, sometimes several times per week | “À danser cette semaine” must be immediately visible, fresh, and terse | `/agenda` with Today/This week filters and event detail pages |
| Visiting dancer | “Is there WCS while I am in Montpellier, and can I get there?” | Date-specific search, Google, a national event directory, an organizer link, or a link from another dancer | Low to medium, irregular | One or two visits around the trip | A small but clear “De passage ?” shortcut near the weekly agenda, not a large permanent section | `/agenda` with date range plus `/visiter` practical guide and map |
| Community subscriber | “Which channel should I join so I stop missing information?” | Usually after another successful journey; sometimes via an invite link or QR code | Medium; cumulative rather than recurring page traffic | Usually one decisive visit | A compact recurring “Rester informé” module after useful content and in the footer; avoid a modal before trust is earned | `/communaute` explaining purpose, audience, posting frequency, privacy, and owner of each channel |

### What each audience is really trying to reduce

- The curious non-dancer needs **uncertainty and intimidation reduced**. A long calendar is noise before they understand the activity.
- The WCS-aware newcomer needs **decision anxiety reduced**. They need plain answers about partners, roles, clothing, level, trial classes, and starting mid-year before teacher biographies.
- The prospective student needs **comparison effort reduced**. A beautiful profile cannot substitute for a normalized timetable and map.
- The local regular needs **time-to-answer reduced**. They should not scroll through introductory copy to find tonight’s social.
- The visitor needs **local ambiguity reduced**. “Montpellier” may include surrounding communes; distance, tram/parking, event status, language, payment, and registration availability matter.
- The subscriber needs **channel ambiguity reduced**. Listing five social icons without explaining the difference transfers the decision problem to the user.

### Probable arrival paths

The website should assume that many visits start below the homepage:

```text
Broad search / short dance video
  → What is WCS?
  → Can I try it?
  → Beginner class or initiation
  → Organizer's registration source

Specific “cours WCS Montpellier” search
  → Beginner guide or class comparison
  → Teacher and venue details
  → Organizer's registration source

Social or messaging link
  → Exact event page
  → This week's related events
  → Community channel or calendar subscription

Direct / bookmark / home-screen shortcut
  → This week
  → Exact event details and source

Date-specific visitor search
  → Agenda already filtered to the visit dates
  → Venue/transport details
  → Source or organizer contact
```

Every class and event detail therefore needs enough context to work as a landing page: what it is, when, where, for whom, current status, last verification, authoritative source, and the next related action. Breadcrumbs and links back to the relevant filtered list are more useful than forcing a return to the homepage.

## Proposed website structure

The first version should be a guide plus shared calendar, with a small structured directory underneath it. “Guide”, “calendar”, and “directory” describe the content model; they do not all need equal weight in navigation.

### Primary navigation

Use five plain-language items:

- **Découvrir** — what WCS is and whether it may suit the visitor
- **Commencer** — the shortest path from interest to a first experience
- **Cours** — compare the current season’s courses
- **Agenda** — find practices, socials, workshops, and larger events
- **Communauté** — choose an information channel and understand who runs the site

On desktop, show all five in the header with a visually stronger **Cette semaine** action. On mobile, keep a compact header and make **Cette semaine** the most reachable action in the menu or a small sticky bottom action. A five-item persistent bottom navigation would be disproportionate for a content site unless repeat-use testing supports it.

Teachers, organizers, and places should not occupy the top navigation initially. They are supporting entities reached from courses, events, search, and the footer. A dedicated directory index can exist at `/acteurs`, but promoting it as a primary destination would put the ecosystem’s internal structure ahead of user tasks.

### Homepage `/`

The homepage must serve both first-time discovery and fast repeat lookup. The solution is not to give every audience an equal-sized block; it is to order sections by urgency and connect them.

1. **Utility/status strip, only when warranted.** A short line for time-sensitive community-wide information: “Inscriptions 2026–27 ouvertes”, a cancellation, or a holiday schedule. It should disappear when there is no real alert. It must not become permanent promotional inventory.
2. **Compact hero.** One strong, authentic image or muted short loop showing social WCS rather than competition spectacle. Over it or beside it: one sentence explaining the local value proposition, a primary **Voir où danser cette semaine** button, and a secondary **Je veux commencer** link. Keep this to roughly one mobile viewport; regulars should see useful event information with one scroll or less.
3. **À danser cette semaine.** Three to five chronological event rows, not large marketing cards. Each row shows day/date, time, type, venue/commune, audience/level, status, and “vérifié le…”. Include **Voir tout l’agenda** and a subtle **De passage ? Choisir mes dates** link. If nothing is scheduled, say so explicitly and show the next known event rather than leaving an empty grid.
4. **Choose-your-path pair.** Two balanced cards: **Découvrir cette danse** and **Trouver mon cours**. The former uses a warm editorial image and answers emotional objections; the latter previews the normalized timetable and map. This prevents introductory content from obscuring the weekly utility while keeping newcomer acquisition prominent.
5. **Beginner-friendly next step.** A narrow module showing the next initiation, trial class, or beginner intake. This is drawn from the same activity data as the agenda, not maintained as duplicate homepage copy.
6. **Monthly highlights.** Two or three larger visual cards for notable workshops, weekends, or exceptional socials. These may carry organizer artwork if legible; the site should still render date, location, and type as text outside the poster. Weekly recurring activities should not consume this image-heavy space.
7. **Rester informé.** One sentence plus a **Choisir mon canal** button. If one channel is clearly the public default, it may also have a direct join action. Messenger, Facebook, WhatsApp, and email should not appear as four unexplained equal icons.
8. **Trust and contribution.** A concise neutrality statement, current coverage/last global update, and **Signaler une correction ou proposer une activité** link.

The homepage should not contain the full teacher directory, full annual class grid, long WCS history, a conventional chronological blog feed, or every social channel. Those additions would push the repeated high-urgency task—finding the next dance—too far down while making comparison harder.

### Discover page `/decouvrir`

This page is for someone who may not yet know the phrase “West Coast Swing”. It should feel invitational rather than encyclopedic.

- Open with a short, representative dance video or wide image and a plain description: modern partner dance, varied music, improvisation, social setting.
- Follow with “Est-ce pour moi ?” answers: no prior dance experience, coming alone, roles/partner rotation, age or accessibility only where verified, music, clothing, and expected learning curve.
- Show “What a first evening looks like” as three or four steps with real photos: arrival, lesson, partner rotation, social/practice.
- Use a small FAQ for objections, not a long history lesson.
- End with two context-aware paths: **Essayer lors d’une initiation** and **Voir les cours débutants**.

This page can rank for broad discovery searches and be shared with a curious friend. It should link into current activities, while the activity data remains owned by the agenda/course system.

### Start page `/debuter`

This is a decision guide, not a second promotional landing page.

- Start with a short chooser: “Je veux essayer une fois”, “Je cherche un cours annuel”, or “J’ai déjà dansé ailleurs”.
- Answer the practical questions before listings: partner required, how levels work, when the season begins, whether mid-year entry is possible, trial/open-day policy, likely equipment, and who to contact when unsure.
- Show the next beginner-friendly dates in a compact list.
- Show a pre-filtered comparison of beginner courses with day, time, area, teacher/organization, price basis, trial status, and registration status.
- Finish with **Compare all beginner classes** and an optional “help me choose” contact route only if someone is committed to maintaining it.

The `/decouvrir` page creates desire; `/debuter` converts desire into a safe first action. Combining both into one very long page would make the path less scannable and weaken their different search intents.

### Courses page `/cours`

This is the main seasonal planning tool. Default to the current teaching season and state the coverage date clearly.

- Place a season selector/status at the top: “Saison 2026–27 · vérifiée le …”. Archive past seasons from search and comparison by default.
- On mobile, start with list filters; on desktop, use a synchronized list and map. Useful filters are level, weekday, time, area/commune, teacher/organization, trial availability, and registration status. Do not begin with an enormous week-grid on a narrow screen.
- Offer a **Planning semaine** view for users who think by availability and a **Comparer les cours** view for users who think by provider. Both views must use the same records.
- Each course row/card shows normalized facts first. Teacher portrait and short bio are secondary links, not the card’s dominant content.
- The map shows only currently filtered courses and gives transit/parking context where verified. It must not be the only way to access location information.
- Registration always links to the provider’s authoritative page and is labelled accordingly. The community site should not imply it owns availability or payment.

A course detail page is only necessary when shared attributes cannot fit cleanly in the comparison. Otherwise, link straight from the row to teacher, place, and official registration sources to avoid creating thin duplicate pages.

### Agenda page `/agenda`

The agenda serves the highest-frequency audience and needs the lowest interaction cost.

- Default to **Cette semaine**, with quick switches for **Aujourd’hui**, **Ce week-end**, **30 jours**, and **Choisir des dates**.
- Separate occurrence from series: show the exact Thursday occurrence in the chronological list, while linking to a recurring-series explanation. Never make a visitor infer whether “every Thursday” applies during holidays.
- Filters should cover activity type, beginner-friendly, location radius/area, and possibly level. Too many dance-community taxonomies will make the page brittle.
- Use dense chronological rows on mobile; optional calendar and map views are secondary. Posters may appear on event detail pages, not as the only readable agenda surface.
- Past or cancelled items remain accessible from shared links with an unmistakable status and a path to upcoming alternatives.
- Provide share, add-to-calendar, directions, and authoritative source actions on event detail. “Add to calendar” should capture the verified occurrence, not a vague recurring promise.

Each event detail page should lead to two related destinations: more events in the same date window and the organizer/place profile. This serves visitors who arrived from social media without requiring homepage navigation.

### Visitor guide `/visiter`

This is a short utility page, reached mainly from the agenda rather than the top navigation.

- Start with a date-range input that returns matching agenda entries.
- Explain the geographic scope: Montpellier proper versus nearby communes, with approximate transit context only when verified.
- Include venue-specific directions, late-night transport or parking facts, payment/registration expectations, and organizer contact on the relevant event/place rather than in generic prose.
- Add a small “No event found?” fallback: broaden dates, see nearby areas if supported, and choose a community channel where short-notice announcements appear.
- Offer French first and concise English practical labels if visitor evidence supports it. A fully translated editorial site is not necessary to make event facts understandable.

### Community page `/communaute`

Organize this around channel purpose, not platform brand:

| Need | Channel information to show before joining |
| --- | --- |
| Fast changes and discussion | Who may post, typical volume, moderation, visibility of phone number/profile, and invite link |
| Public event announcements | What is covered, whether an account is required, and who maintains it |
| A low-noise digest | Frequency, examples of content, privacy statement, and unsubscribe mechanism |

The page should also explain who maintains the website, its neutral listing rules, how to submit/correct information, and what the site does not replace. If email does not yet exist, do not display a disabled signup form; offer only the maintained channels and test demand for a digest separately.

### Actor, organizer, and place pages

These pages support comparison and trust but should be generated from structured records rather than written like blog profiles.

- **Teacher/organization:** name, role, teaching locations, current courses, upcoming events, short factual introduction, official links, and last verification. Use one consistent portrait or logo slot; do not let different promotional assets create paid-looking visual hierarchy.
- **Place:** address, map, tram/bus/parking/accessibility facts where verified, current activities, and external directions link. A venue image is useful for arrival recognition, especially when the entrance is difficult to find.
- **Organizer:** upcoming and recurring events, contact/source links, and correction ownership.

Avoid subjective ranking, “best teacher” labels, popularity sorting, or unmarked featured placement. Default orders should be temporal, alphabetical, geographic, or based on the user’s explicit filters.

### Articles and evergreen editorial content

A blog is not a primary section for the first version. Core facts such as schedules, locations, recurring parties, teacher data, and channel links belong in structured pages because they change and must be reusable.

Use articles only for genuine evergreen or occasional editorial questions that have their own search value—for example “How to choose your first social dance”, “What happens at a WCS social?”, or a documented seasonal guide. Articles should link to live course and event modules; they should never embed copied schedules that will silently become stale.

## How the journeys connect without competing

- The homepage gives **urgency** to current events, **prominence** to starting, and **depth** to dedicated pages. This balances high-frequency regulars with potentially higher-volume newcomers.
- Beginner-friendly activities are one tagged subset of the agenda. The same record can appear on `/agenda`, `/debuter`, and the homepage without three editorial copies.
- Courses connect to teachers and places, but comparison remains centered on the student’s constraints. The directory does not interrupt the choice with long biographies.
- Event detail pages connect social-media arrivals to the wider local calendar and community channel. This turns a one-off shared link into discovery without blocking the immediate answer.
- The subscription prompt appears after value has been delivered. It supports retention without obscuring discovery or event details.
- Notable-event imagery creates energy, while dense text rows preserve speed for weekly lookup. Using poster grids everywhere would privilege organizers’ artwork and make dates harder to compare.

## Mobile, direct access, and app hypothesis

The repeat journey is naturally mobile: a dancer checks plans from a message thread, in transit, or shortly before leaving. The site should therefore be fast, installable as a Progressive Web App if inexpensive, and capable of opening directly to `/agenda?periode=semaine` from a saved home-screen shortcut.

A dedicated mobile app is not justified in the first version. It would add installation friction and maintenance before proving repeat demand. Reconsider it only if analytics show strong weekly retention and interviews reveal a need for native notifications, saved events, offline access, or personalized filters that a lightweight web experience cannot serve.

## Content priority and freshness rules

The architecture depends more on trust than visual polish:

| Content | Change rate | Verification expectation | Failure behavior |
| --- | --- | --- | --- |
| One-time event occurrence | High near event date | Check at publication and again shortly before occurrence when feasible | Mark unverified/cancelled clearly; retain source link |
| Weekly or monthly series | Medium and seasonal | Confirm exceptions, holidays, and end date | Never extrapolate indefinitely |
| Annual course planning | High around rentrée, then medium | Verify with provider for each season | Show season and last-verified date prominently |
| Teacher/organizer profile | Low | Periodic review and correction link | Keep factual; remove stale activity claims |
| WCS introduction/FAQ | Low | Editorial review | Link practical claims to current sources where appropriate |
| Community channel links | Medium | Periodic invite and ownership check | Hide expired joins rather than leave broken primary actions |

The site should never present a guessed recurring occurrence as confirmed. Every activity needs an authoritative source, an owner or provider, a last-checked date, and a clear distinction between “scheduled”, “confirmation pending”, “cancelled”, and “past”.

## Initial public discovery observations

A lightweight search check on 2026-08-16 supports the fragmentation hypothesis but does not validate user demand:

- Search results for beginner classes lead to provider-specific pages such as [Alma Dance](https://almadance.fr/cours-de-danse/west-coast-swing-montpellier/) and [Studio Archipel / Guilhem Danse](https://www.archipel-montpellier.fr/guilhem-danse-rock-west-coast-swing/). These pages explain the dance and their own offer well, but are not neutral comparison tools.
- A [Montpellier Maison pour Tous listing](https://mpt.montpellier.fr/activites/voltaire/west-coast-swing) exposes day, level, provider, address, and tram information in a compact form, showing the value of normalized practical facts.
- Event discovery appears across organizer/studio archives such as [Urban Latino Dance Studio](https://urbanlatinodance-montpellier.fr/category/soirees-mensuelles/) and broader aggregators such as [Danzly’s Montpellier view](https://danz.ly/swing-in-montpellier-france). The latter mixes several swing forms, which reinforces the need for clear WCS-specific filtering and source verification.

These observations suggest that search will be important for acquisition and social/messaging links for individual events, while direct access may grow only after the weekly agenda proves dependable. Actual entry channels, traffic volumes, and use of private groups still require interviews and analytics.

## Recommended first release boundary

Build around four complete journeys rather than many shallow pages:

1. Search visitor understands WCS and reaches a real beginner opportunity.
2. Prospective student compares the current season’s classes by schedule, level, and location, then reaches the provider’s registration source.
3. Local dancer finds a verified event this week in seconds.
4. Visiting dancer filters by travel dates, understands the location, and reaches the authoritative event source.

The minimum public surface is therefore `/`, `/decouvrir`, `/debuter`, `/cours`, `/agenda`, event detail, `/visiter`, `/communaute`, and supporting actor/place views. Do not launch all of them half-populated: a dependable agenda and course comparison are more valuable than a large empty directory.