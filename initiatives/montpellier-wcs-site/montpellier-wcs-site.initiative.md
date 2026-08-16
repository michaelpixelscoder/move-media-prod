---
title: "Launch the Montpellier WCS community website"
status: active
owner: michael
created: 2026-08-16
updated: 2026-08-17
target_date: 2026-09-30
budget: null
related_thoughts:
  - thoughts/montpellier-wcs-site/montpellier-wcs-site.explore.md
  - thoughts/montpellier-wcs-site/site-layout.md
related_stories: []
related_actors: []
tags:
  - community-website
  - west-coast-swing
  - montpellier
  - classes
  - events
  - directory
---

# Launch the Montpellier WCS community website

## 1. Problem

- **Affected actors:** People discovering West Coast Swing, beginners choosing a course, current local dancers, visiting dancers, teachers, studios, event organizers, and community contributors.
- **Current situation:** Public information about Montpellier WCS classes, locations, teachers, recurring socials, and one-time events is distributed across provider websites, public directories, event aggregators, social networks, and private messaging groups. The sources use different formats and may not expose freshness, exceptions, or comparable practical details.
- **Impact:** Newcomers expend effort understanding the dance and comparing classes; regular and visiting dancers expend effort finding a current event; organizers repeat information across channels; and inaccurate recurring information can undermine trust.
- **Evidence:** The source exploration records provider-specific search results, a municipal listing, event archives, and a broader event aggregator. This supports fragmentation but does not yet establish demand or sustainable maintenance. See [the source thought](../../thoughts/montpellier-wcs-site/montpellier-wcs-site.explore.md) and [site-layout research](../../thoughts/montpellier-wcs-site/site-layout.md).

This initiative commits to building and testing a neutral public reference. It does not treat the underlying demand, provider participation, or maintenance model as already proven.

## 2. Completion criteria

Baselines marked “not measured” must be established during Milestone 1 before public launch. Targets are provisional until the baseline study is complete; changing one requires a decision-log entry.

| Measure | Baseline | Target | Evidence source | Measurement window |
| --- | --- | --- | --- | --- |
| Beginner task success | Not measured | At least 4 of 5 representative newcomers find an appropriate first action in under 2 minutes without assistance | Moderated task-test notes and timestamps | Pre-launch acceptance test |
| Weekly-event task success | Not measured | At least 4 of 5 local or visiting dancers find a verified relevant event in under 45 seconds | Moderated task-test notes and timestamps | Pre-launch acceptance test |
| Course comparison completeness | No neutral baseline recorded | Every published current-season class has level, schedule, place, teacher or organization, authoritative source, status, and last-verified date | Data-quality report | At launch and weekly for the first 8 weeks |
| Event freshness | No shared service level | At least 90% of upcoming published occurrences comply with the defined verification service level | Scheduled freshness report | Weekly for the first 8 weeks |
| Provider coverage | Public source inventory not complete | At least 80% of confirmed in-scope providers are represented or have explicitly declined inclusion | Source inventory and outreach log | At launch |
| Contributor workflow | No contributor workflow | At least 2 non-admin contributors create and update their own listing without being able to mutate another contributor’s listing | Audit log and acceptance tests | Pilot before public launch |
| Favorite persistence | No account feature | An authenticated user can favorite and unfavorite classes/events and recover the same set in a new session | End-to-end test | Every release |
| Repeat utility | No site traffic | Establish weekly returning-user baseline, then achieve at least 20 returning users in 2 separate weeks | Privacy-respecting analytics | First 8 weeks after launch |

All required completion criteria:

- [ ] Baseline source inventory and representative user-task timings are recorded.
- [ ] The four primary journeys pass their task-success targets: discover/start, compare classes, find an event this week, and plan a visit.
- [ ] All public listings meet the required data-completeness and freshness rules.
- [ ] Server-side authorization tests prove every role boundary, including contributor ownership.
- [ ] At least two contributors complete the pilot workflow successfully.
- [ ] The launched site meets the event-freshness target during the observation period.
- [ ] Repeat use reaches the target or produces enough qualitative evidence to justify a documented correction cycle.

## 3. Constraints and stop conditions

### Constraints

- **Time:** The internal first version is due Sunday 2026-08-23. It must be presented to community actors no later than 2026-08-31 so they can review and complete their information. Public release is due during September 2026 and no later than 2026-09-30.
- **Budget:** No monetary budget is committed. Paid hosting, maps, email, analytics, media licensing, and authentication costs require approval before selection.
- **Capacity:** Plan for one primary maintainer and a small number of volunteer contributors. The public scope must remain maintainable without a full-time editor.
- **Technical or operational constraints:** Mobile-first, accessible, search-indexable, privacy-conscious, timezone-safe, and capable of preserving authoritative source links and verification history. Authorization must be enforced on the server, never only in the interface.
- **Must preserve:** Neutral ordering, transparent attribution, visible freshness, correction paths, contributor ownership boundaries, and the existing four-journey information architecture.

### Delivery deadlines

| Gate | Deadline | Required result |
| --- | --- | --- |
| Internal first version | 2026-08-23 | Deployable responsive vertical slice with the selected homepage, public class planning/map, basic agenda/event display, authentication, favorites, seeded actors/places/classes/events, ownership-scoped contributor CRUD, administration access, and draft copy for Discover and Community Rules |
| Actor review version | 2026-08-31 | Private preview shared with identified teachers, studios, and organizers; contributors can claim/review their actor profile and fill or correct their owned classes/events; feedback and missing information are tracked |
| Public release | 2026-09-01 through 2026-09-30 | Actor corrections incorporated, launch inventory verified, copy approved, accessibility/security/recovery gates passed, public domain enabled, and first observation cycle started |

The 2026-08-23 version is a complete testable vertical slice, not the final content-complete release. If schedule pressure requires scope reduction, retain authorization, source/freshness data, mobile usability, and actor review; defer secondary editorial or convenience features before weakening those controls.

### Stop or reconsider if

- [ ] Fewer than three in-scope providers agree that their public data may be represented after the initial outreach round.
- [ ] The inventory shows that a trustworthy launch requires more than two maintainer-hours per week and the work cannot be distributed.
- [ ] Upcoming-event freshness remains below 90% for two consecutive weekly reviews.
- [ ] Authorization tests reveal an unresolved path for one contributor to mutate another contributor’s content.
- [ ] Fewer than 3 of 5 participants complete either primary task in the pre-launch usability test.
- [ ] No credible maintainer or administrator is available before public launch.
- [ ] Privacy, image rights, community safety, or disputed-listing concerns cannot be resolved through documented rules.

When a condition is met, pause public expansion, keep the smallest safe read-only version if useful, and choose one of: reduce coverage, remove the affected feature, redesign the contribution workflow, or discard the initiative. Do not compensate for unmaintainable data with unsupported automation.

## 4. Possible solutions

### Option A — Static editorial guide

- **Description:** Publish evergreen discovery, beginner, course-directory, and community pages without accounts or a live event workflow.
- **Expected effect:** Improves search discovery and beginner orientation with low technical complexity.
- **Cost and effort:** Low build effort and moderate seasonal editorial maintenance.
- **Risks:** Does not fully serve repeat local/visitor event lookup; schedules can still become stale.
- **How it would be tested:** Measure beginner task success and referral clicks during a short release.

### Option B — Guide, class planner, shared agenda, and controlled contribution

- **Description:** Build the editorial guide, normalized class planning/map views, event agenda, accounts with favorites, and ownership-scoped contributor tools.
- **Expected effect:** Serves all four primary journeys and distributes some data maintenance while retaining administrative oversight.
- **Cost and effort:** Moderate product, content, authentication, mapping, and operational effort.
- **Risks:** Role security, stale recurring data, contributor adoption, map cost, moderation, and a larger pre-launch content burden.
- **How it would be tested:** Automated authorization and data-quality checks, pre-launch journey tests, contributor pilot, and an eight-week observation cycle.

### Option C — Full community platform

- **Description:** Add social profiles, messaging, ticketing, notifications, broad directories, reviews, and organizer analytics.
- **Expected effect:** Could consolidate more community activity if adoption is strong.
- **Cost and effort:** High and continuous.
- **Risks:** Premature scope, community fragmentation, privacy and moderation burden, and competition with established channels.
- **How it would be tested:** Not selected for initial testing; revisit only after sustained use of Option B.

### Option D — Take no action

- **Likely consequence:** Existing provider sites and messaging groups continue to serve the community; Move Media avoids maintenance but gains no direct evidence about the shared-reference hypothesis.
- **When this is the correct choice:** Provider participation is insufficient, existing channels already meet the observed needs, or accurate coverage cannot be maintained safely.

## 5. Selected solution

- **Decision:** Build Option B in staged releases, beginning with a trustworthy read experience and adding contribution only after ownership and moderation tests pass.
- **Why this option:** It addresses newcomer acquisition, seasonal class planning, repeat event lookup, visitor needs, and retention through favorites without taking on ticketing or social-network behavior.
- **Assumptions being made:** Public source data can be normalized; providers will permit or help maintain listings; users value account-backed favorites; and a small contributor group can keep high-change information current.
- **Known risks:** The solution may be larger than actual demand; recurring schedules are easy to misrepresent; map and authentication choices may introduce cost; community neutrality can be disputed; and contributor permissions can create security or moderation failures.
- **In scope:** Public editorial pages, classes, weekly planning, map/list view, events and occurrences, visitor guidance, teachers/organizations/places as reference data, authentication, favorites, contributor CRUD for owned classes/events, administrator control, freshness/status handling, audit history, corrections, responsive design, accessibility, SEO, analytics, and copywriting.
- **Out of scope:** Ticket sales, payments, private messaging, social feeds, reviews or rankings, user-generated comments, native mobile apps, push notifications, automated scraping from every provider, and unlabelled sponsored placement.

### 5.1 Information architecture

| Route or surface | Primary job | Main content | Access |
| --- | --- | --- | --- |
| `/` | Orient and answer “what can I do now?” | Compact hero, this week, newcomer/course paths, footer | Public |
| `/decouvrir` | Understand WCS | What the dance is, representative media, objections, first-evening explanation | Public |
| `/debuter` | Choose a first action | Trial/initiation/course paths, practical FAQ, beginner opportunities | Public |
| `/cours` | Compare classes | Search, filters, planning/list/map views, source and freshness | Public; favorites require account |
| `/agenda` | Find something to dance | Today/weekend/date-range views and filters | Public; favorites require account |
| `/evenements/[slug]` | Act on a shared event link | Exact occurrence, status, place, directions, source, related dates | Public |
| `/visiter` | Plan around travel dates | Date-range entry, map context, transport and fallback channels | Public |
| `/communaute` | Choose a channel and understand rules | Channel purposes, neutrality, inclusion, moderation and correction rules | Public |
| `/connexion` | Authenticate | Login and account-recovery flow | Public |
| `/compte/favoris` | Recover saved items | User’s favorite classes and events | User or higher |
| `/contribution` | Manage owned listings | Contributor’s classes/events, create/edit/archive workflows | Contributor or administrator |
| `/administration` | Govern all content | Users, roles, reference data, listings, pages, audit and disputes | Administrator |

Teachers, studios, organizers, and places are supporting reference pages reached from classes and events. They are not primary navigation items in the first release.

Selected visual references:

- Homepage: [desktop](../../thoughts/montpellier-wcs-site/mockup-simple-desktop.png) and [mobile v2](../../thoughts/montpellier-wcs-site/mockup-simple-mobile-v2.png)
- Course planning: [desktop](../../thoughts/montpellier-wcs-site/mockup-classes-planning-desktop.png) and [mobile](../../thoughts/montpellier-wcs-site/mockup-classes-planning-mobile.png)
- Course map: [desktop](../../thoughts/montpellier-wcs-site/mockup-classes-map-desktop.png) and [mobile](../../thoughts/montpellier-wcs-site/mockup-classes-map-mobile.png)

These mockups establish hierarchy and visual direction, not final copy, accessibility behavior, data density, or interaction specifications.

### 5.2 Technical data model

The following is a logical relational model. Exact database and framework selection is a Milestone 1 decision, but the resulting implementation must preserve these entities and authorization invariants.

#### Identity and authorization

**`users`**

- `id`: internal immutable identifier
- `auth_subject`: unique identifier from the authentication provider
- `email`: normalized and unique when supplied by the provider
- `display_name`
- `avatar_url`: nullable
- `role`: enum `user | contributor | administrator`; anonymous visitors have no row/session role
- `status`: enum `active | suspended | deleted`
- `created_at`, `updated_at`, `last_login_at`

Role changes are administrator-only and must be audited. The client must never be trusted to supply or elevate a role.

**`favorites`**

- `user_id`
- `listing_id`
- `created_at`
- Composite primary key or unique constraint on `(user_id, listing_id)`

Favorites are private account data. A user may read, create, and delete only their own favorites.

#### Media

**`media_assets`**

- `id`, `storage_key`, `mime_type`, `width`, `height`, `byte_size`
- `alt_text`, `credit`, `source_url`, `license_or_permission`
- `focal_x`, `focal_y`: nullable crop focal point
- `uploaded_by_user_id`, `created_at`, `deleted_at`

A **badge image** is the compact square or portrait/logo representation used in lists, pins, and identity blocks. A **hero image** is the wide visual used on detail and editorial pages. Actors, places, classes, events, and editorial pages support both where relevant. Every published image requires alt text plus provenance or usage permission.

#### Shared public reference data

**`actors`**

- `id`, `slug`, `name`
- `user_id`: nullable relation to the user allowed to edit this actor profile; assignment and transfer are administrator-only
- `summary`, `website_url`, `contact_url`
- `badge_media_id`, `hero_media_id`: nullable relations to `media_assets`
- `status`: enum `draft | published | archived`
- `last_verified_at`, `created_at`, `updated_at`

An actor has no type or kind attribute. “Teacher”, “studio”, “studio owner”, and “event organizer” are roles derived from the actor’s relations to classes, events, and other actors. The same actor may hold any combination of these roles.

**`places`**

- `id`, `slug`, `name`
- Structured address fields, `latitude`, `longitude`
- `transport_notes`, `parking_notes`, `accessibility_notes`, `arrival_notes`
- `badge_media_id`, `hero_media_id`: nullable relations to `media_assets`
- `status`, `last_verified_at`, `created_at`, `updated_at`

**`levels`**

- `id`, `slug`, `label`, `description`, `sort_order`, `color_token`

**`seasons`**

- `id`, `label`, `starts_on`, `ends_on`, `is_current`

Places, levels, and seasons are shared resources. Contributors may reference them and request a missing/corrected reference, but only administrators mutate them in the first release. An actor may be edited by its linked `user_id` or an administrator. This prevents one contributor from changing shared reference data or an unclaimed actor profile.

#### Classes and events

**`listings`** — common public and ownership fields

- `id`, `slug`
- `kind`: enum `class | event`
- `title`, `summary`, `description`
- `owner_user_id`: authorization owner; set from the authenticated server context, never from client input
- `source_url`, `registration_url`
- `badge_media_id`, `hero_media_id`: nullable relations to `media_assets`
- `status`: enum `draft | published | cancelled | archived`
- `verification_status`: enum `unverified | contributor_verified | administrator_verified | stale`
- `last_verified_at`, `published_at`
- `created_at`, `updated_at`, `deleted_at`
- `version`: optimistic-concurrency integer

**`classes`** — one-to-one child of `listings(kind=class)`

- `listing_id`: primary and foreign key
- `season_id`, `level_id`
- `trial_available`
- `registration_status`: enum `unknown | open | waitlist | closed`
- `price_summary`: nullable display value; source remains authoritative

**`events`** — one-to-one child of `listings(kind=event)`

- `listing_id`: primary and foreign key
- `event_type`: enum `social | practice | workshop | festival | competition | open_day | other`
- `beginner_friendly`
- `registration_required`

#### Relationship-defined actor roles

**`class_teachers`**

- `class_listing_id`, `actor_id`, `sort_order`
- Composite unique constraint on `(class_listing_id, actor_id)`

A class may have multiple teachers, and an actor becomes a teacher by being related to at least one class.

**`class_studios`**

- `class_listing_id`, `studio_actor_id`, `sort_order`
- Composite unique constraint on `(class_listing_id, studio_actor_id)`

An actor becomes a studio by being referenced through a studio relation. A class may be associated with multiple studios when the real arrangement requires it.

**`studio_owners`**

- `studio_actor_id`, `owner_actor_id`, `sort_order`
- Composite unique constraint on `(studio_actor_id, owner_actor_id)`
- Check constraint preventing an actor from directly owning itself

A studio may have multiple owners. An owner may also teach classes or organize events through the other relations.

**`event_organizers`**

- `event_listing_id`, `actor_id`, `sort_order`
- Composite unique constraint on `(event_listing_id, actor_id)`

An event may have multiple organizers, and an actor becomes an organizer through this relation.

#### Place relationships and map behavior

**`listing_places`**

- `listing_id`, `place_id`
- `is_primary`, `sort_order`
- Composite unique constraint on `(listing_id, place_id)`

Classes and events may relate to one or more places. Their map presence always comes from `listing_places` and the exact schedule/occurrence place described below, never from an actor’s address.

#### Scheduling and exceptions

**`schedule_rules`**

- `id`, `listing_id`
- `place_id`: required relation to a place also present in `listing_places`
- `timezone`: always explicit; default presentation zone is `Europe/Paris`
- `frequency`: enum `once | weekly | monthly`
- `weekdays`, `local_start_time`, `local_end_time`
- `starts_on`, `ends_on`
- `source_text`: preserves the human-readable schedule supplied by the source

**`occurrences`**

- `id`, `listing_id`, `schedule_rule_id`: nullable for manually created occurrences
- `place_id`: exact occurrence place; defaults from the rule and may override it for a moved occurrence
- `starts_at`, `ends_at`: stored as timezone-aware instants
- `status`: enum `scheduled | confirmation_pending | cancelled | completed`
- `exception_note`, `source_url`, `last_verified_at`
- Unique occurrence key preventing duplicate materialization

Rules describe recurrence; occurrences are the exact dates shown in the agenda and calendar exports. Generate only a bounded future window and preserve exceptions. Never infer that a weekly activity continues after the rule’s end date. Map queries use the occurrence place for date-specific event results and the schedule-rule places for class-planning results, so a moved or multi-venue activity appears at the correct coordinates.

#### Editorial, contribution, and audit data

**`content_pages`**

- `id`, `slug`, `title`, `summary`, `body_markdown`
- `badge_media_id`, `hero_media_id`: nullable relations to `media_assets`
- `seo_title`, `seo_description`
- `status`: enum `draft | published | archived`
- `published_at`, `updated_by_user_id`, `created_at`, `updated_at`

Editorial pages are administrator-managed in the first release. Draft copy may begin in version-controlled files and be imported after review.

**`reference_requests`**

- `id`, `requester_user_id`
- `kind`: enum `new_actor | actor_correction | new_place | place_correction | listing_dispute`
- `payload`, `status`, `reviewed_by_user_id`, `reviewed_at`, `created_at`

**`audit_log`**

- `id`, `actor_user_id`, `action`, `resource_type`, `resource_id`
- `before_snapshot`, `after_snapshot`, `created_at`
- Append-only to application roles; retention and sensitive-field redaction must be defined before launch

#### Required indexes and query behavior

- Index published listings by `(kind, status)` and occurrences by `(status, starts_at)`.
- Index classes by `season_id` and `level_id`; index listings by `owner_user_id`; index `listing_places` by both `listing_id` and `place_id`.
- Index schedule rules and occurrences by `place_id`; use the related place coordinates for spatial lookup.
- Support text search across listing title, actor names, place names, and descriptions with a documented fallback if full-text search is unavailable.
- Support map bounding-box or radius queries over related place coordinates; map results and list results must share one filter query and return the same listing IDs for equivalent filters.
- Add uniqueness constraints for user favorites, slugs, auth subjects, and generated occurrences.
- Exclude soft-deleted, draft, stale-by-policy, or cancelled records from default public queries unless the product explicitly shows their status.

### 5.3 Roles and permissions

“Anonymous” is the canonical name for the unauthenticated role.

| Capability | Anonymous | User | Contributor | Administrator |
| --- | --- | --- | --- | --- |
| Read published pages, actors, places, classes, and events | Yes | Yes | Yes | Yes |
| Read drafts or archived content | No | No | Own classes/events only | All |
| Create, read, and delete favorites | No | Own only | Own only | All, with access audited |
| Create classes and events | No | No | Yes; owner set to self | Yes; may assign or transfer ownership |
| Edit classes and events | No | No | Own only | All |
| Publish/unpublish classes and events | No | No | Own only | All |
| Cancel or archive classes and events | No | No | Own only | All |
| Permanently delete classes and events | No | No | No; soft delete only | Yes, audited and subject to retention rules |
| Edit actor profiles | No | No | Actor whose `user_id` is self | All |
| Assign or transfer an actor’s linked user | No | No | No | Yes |
| Manage teachers/studios/places on a class or organizers/places on an event | No | No | Own class/event only | All |
| Manage studio-owner relations | No | No | No; may submit a reference request | Yes |
| Create/edit places, levels, and seasons | No | No | No; may submit a reference request | Yes |
| Edit editorial pages and community rules | No | No | No | Yes |
| Assign roles, suspend users, transfer ownership | No | No | No | Yes |
| Review reference requests and disputes | No | No | Own submitted requests | All |
| Read audit history | No | No | Own listing activity where exposed | All |

Authorization invariants:

1. Every mutation is authorized server-side using the authenticated user and persisted role.
2. On contributor create, `owner_user_id` is derived from the session. Client-supplied ownership is ignored or rejected.
3. On contributor update, publish, cancel, archive, or delete, the query must require both the target ID and `owner_user_id = authenticated_user.id`.
4. A contributor may edit an actor profile only when `actor.user_id = authenticated_user.id`. Actor `user_id` is never self-assignable or contributor-editable.
5. A contributor may add or remove teachers, studios, organizers, and places only through relations belonging to a class/event they own. This does not grant permission to edit the related actor or place.
6. `owner_user_id`, role, audit fields, verification actor, and timestamps are not contributor-editable.
7. Deletion by contributors is soft deletion. Administrators can restore, transfer, or permanently remove according to retention policy.
8. Public reads return only public fields from records in a public state. They never expose email, auth subject, private favorites, drafts, or audit snapshots.
9. Administrator access is explicit and audited; it is not implemented as hidden client behavior.
10. Suspending a user prevents authentication and all mutations without deleting public records they previously created.
11. Public teacher, studio, owner, or organizer relations never grant listing ownership. Only the internal `owner_user_id` controls contributor writes to a class/event.
12. Favorites do not affect neutral public ranking. “Most favorited” is not a default sort or promotional signal.

### 5.4 Content and copywriting plan

Copy is a release dependency, not post-build polish. Each task needs a named writer, factual reviewer, community reviewer where appropriate, and final administrator approval.

| Copy task | Required result | Review concerns |
| --- | --- | --- |
| Homepage | Value proposition, primary actions, short freshness and neutrality language | Does not privilege one provider; works for newcomers and regulars |
| “Découvrir la danse” | Plain-language explanation, representative music/context, “is it for me?”, and first-evening expectations | Avoids stereotypes, unsupported accessibility claims, and competition-only framing |
| “Commencer” | Practical FAQ about partner requirements, roles, clothing, trial classes, level, and mid-year starts | Provider differences are labelled rather than generalized |
| Courses | Filter labels, level explanations, registration/source disclaimers, empty states, stale-data states | Comparison remains factual and neutral |
| Agenda and visitor guide | Event types, date/status language, cancellation messages, transport/payment/source prompts | Dates and geographic scope cannot be misunderstood |
| Community rules | Inclusion criteria, neutral ordering, sponsorship disclosure, contributor responsibilities, correction/dispute process, moderation, image rights, prohibited content, and consequences | Must be accepted by pilot contributors before access is granted |
| Channel guide | Purpose, posting frequency, privacy implications, account/phone-number visibility, and ownership of each channel | No unexplained platform-icon list |
| Authentication and favorites | Login value, privacy, save/unsave feedback, logged-out prompts, account deletion | No dark patterns or inflated promises |
| Contributor workflow | Ownership explanation, source requirements, verification checklist, recurring-schedule warning, deletion consequences | A contributor understands they cannot edit another owner’s record |
| Legal and trust | Privacy notice, analytics/cookie disclosure if required, terms, image credits/licences, contact, and site ownership | Legal review proportionate to selected services and jurisdiction |
| SEO and sharing | Unique titles/descriptions, social share copy, structured-data descriptions, image alt text | No keyword stuffing or misleading freshness claims |
| Badge and hero media | Shot/asset list for actors, places, classes, events and editorial pages; crop guidance; alt text; credits and permissions | Every entity works with a missing-image fallback; no image is published without rights and accessibility metadata |

Every dynamic state also needs reviewed microcopy: no results, filtered-out favorites, closed registration, confirmation pending, cancelled, stale, archived, unauthorized, validation failure, offline/network failure, and destructive-action confirmation.

## 6. Implementation plan

| Milestone or task | Result | Dependencies | Status | Completion check |
| --- | --- | --- | --- | --- |
| 1. Inventory sources and establish baselines | Confirmed provider/activity inventory, current channels, baseline journey timings, data-change rates, consent notes | Source thought | pending | Inventory reviewed; baselines in Section 2 replaced; provider coverage denominator defined |
| 2. Confirm governance and operating owner | Named administrator, contributor eligibility, inclusion/ordering rules, freshness service levels, disputes and image-rights process | Milestone 1 | pending | Written policy approved by owner and pilot contributors |
| 3. Select technical stack and operating budget | Documented choices for web framework, database, auth, maps, search, hosting, analytics, media storage, backups, and monitoring | Milestones 1–2 | pending | Decision record includes recurring cost and export/exit path |
| 4. Finalize design system and responsive flows | Approved homepage, planning, map, agenda, event, auth, favorites, contribution, and admin flows | Existing mockups; Milestone 2 | pending | Desktop/mobile states cover loading, empty, stale, cancelled, unauthorized and error cases |
| 5. Produce copy deck and media plan | Draft then approved French copy for all public, trust, legal, authentication and contributor surfaces; badge/hero shot list, fallbacks and rights workflow | Milestone 2; factual interviews | pending | Draft Discover and Community Rules copy exists by 2026-08-23; all Section 5.4 tasks and launch media are approved before public release |
| 6. Scaffold application and delivery pipeline | Reproducible local app, environments, CI, preview deployments, migrations and seed data | Milestone 3 | active | Clean checkout installs, migrates, seeds, builds and tests from documented commands |
| 7. Implement authentication and authorization | Login/logout, user badge, roles, suspension, ownership guards and audit logging | Milestone 6 | active | Full permission matrix passes automated tests; negative ownership tests included |
| 8. Implement reference and listing data | Actors without type enums, actor-role relations, places and listing-place relations, levels, seasons, listings, schedules, occurrences, badge/hero media, source/freshness/status fields | Milestones 6–7 | active | Migrations prove multiple teachers, studio owners, event organizers and places; map fixtures resolve the exact schedule/occurrence place |
| 9. Implement contributor and admin tools | Contributor CRUD for owned classes/events and linked actor profile; relation management on owned listings; admin global CRUD, actor-user assignment, studio owners, roles, requests and disputes | Milestones 7–8 | pending | Two seeded contributors cannot access each other’s writes or actors; linked actor user can edit only that actor; admin can manage all |
| 10. Build public editorial experience | Homepage, Discover, Start, Community, Visitor and supporting reference pages | Milestones 4–5, 8 | active | Responsive routes render approved copy/media and pass content/accessibility review |
| 11. Build courses planning and map | Shared filters, search, weekly planning, synchronized map/list, class detail/source links | Milestones 4, 8 | active | Filter parity tests pass; every visible class maps to one source record |
| 12. Build accounts and favorites | Favorite stars, login transformation, account favorites page and cross-session persistence | Milestones 7–8, 11 | pending | User can save/unsave; anonymous prompt works; privacy and ownership tests pass |
| 13. Build agenda and event details | Date filters, occurrence generation, cancellations/exceptions, event details, sharing, directions and calendar export | Milestones 4, 8 | active | Timezone/recurrence/cancellation fixtures pass and shared links preserve exact occurrence |
| 14. Complete SEO, accessibility, privacy and performance | Metadata, structured data, sitemap, keyboard/focus behavior, contrast, consent/analytics, budgets | Milestones 10–13 | pending | Automated gates pass and human assistive-technology review has no launch blocker |
| 15. Import and verify launch content | Complete current-season classes, upcoming events, actor relations, places, map coordinates, sources, badges/heroes, permissions and media rights | Milestones 2, 5, 8–13 | pending | Data-quality report meets launch thresholds; every mapped listing resolves to a place; each contributor confirms owned records and media |
| 16. Pilot and security review | Closed pilot with representative users and contributors, authorization abuse tests, recovery and backup rehearsal | Milestones 7–15 | pending | Completion targets pass or correction cycle is documented; restore test succeeds |
| 17. Public release and observation | Monitored public site, support/correction route, weekly freshness review and analytics | Milestone 16 | pending | Eight-week observation recorded in Section 8 with a continue/correct/pause decision |

Delivery-gate allocation:

- **By 2026-08-18:** Lock stack, schema, authorization rules, visual direction, route inventory, seed fixture format, and the internal-v1 scope.
- **By 2026-08-23:** Complete the internal vertical slice across Milestones 4–13 with representative seed data and draft Discover/Community Rules copy. Secondary states may remain incomplete only when listed explicitly in the preview release notes.
- **2026-08-24 to 2026-08-31:** Complete actor onboarding, actor-profile editing, relationship review, content completion, badge/hero collection, source verification, and structured feedback. Each invited actor receives a clear deadline and ownership instructions.
- **During September, no later than 2026-09-30:** Resolve review feedback, finish Milestones 14–16, verify launch data and media rights, release publicly, and start Cycle 2.

## 7. Test instructions

### Prerequisites

- Technical stack selected and documented
- Supported runtime and package manager installed
- Local test database with deterministic migrations and seed fixtures
- Test identities for one user, two contributors with different listing ownership and actor links, one administrator, and one suspended user
- Map/search providers replaced by deterministic fixtures in automated tests
- No production credentials in test configuration

### Automated verification

The scaffold must expose these stable commands from the repository root; exact underlying tools may vary:

```bash
npm run lint
npm run typecheck
npm run test
npm run test:e2e
npm run test:accessibility
npm run build
```

Expected result:

- Exit code: `0` for every command
- Unit/integration tests cover multi-teacher classes, multi-owner studios, multi-organizer events, listing-place relations, occurrence place overrides, map resolution, recurrence, timezone conversion, freshness, full-text/filter composition, map/list parity, favorites uniqueness, soft deletion, and data visibility.
- Authorization tests attempt every forbidden transition, including forged ownership, forged actor-user assignment, direct API calls, another contributor’s listing or actor IDs, unauthorized relation changes, role changes, unpublished reads, and permanent deletion.
- End-to-end tests cover the four public journeys, login-to-user-badge transition, cross-session favorites, contributor CRUD on owned listings, administrator global CRUD, and cancellation visibility.
- Build output contains no placeholder copy, broken internal links, missing required metadata, or uncredited launch media.

### Human acceptance checks

- [ ] Five representative newcomers attempt to understand the dance and choose a first action.
- [ ] Five local/visiting dancers attempt to find an appropriate event for a stated date.
- [ ] At least two prospective students compare classes using level, location, teacher, text, and favorite filters on desktop and mobile.
- [ ] Two contributors create, edit, publish, cancel/archive, and soft-delete their own records, then confirm they cannot alter the other contributor’s records.
- [ ] A linked contributor edits their actor badge, hero, biography and links, but cannot edit another or unclaimed actor.
- [ ] A class with two teachers, a studio with two owners, and an event with two organizers render all relationships without duplicating actors.
- [ ] A class/event attached to multiple places and an occurrence moved to a different place produce the correct list and map results.
- [ ] One administrator resolves a reference request, transfers ownership, restores a deleted record, and reviews its audit history.
- [ ] Keyboard-only and screen-reader checks cover navigation, filters, timetable/list alternatives, map alternatives, stars, authentication, forms, errors, and destructive confirmations.
- [ ] Community representatives review discovery copy, terminology, inclusion rules, neutral ordering, dispute language, and representative imagery.
- [ ] A maintainer performs backup restoration and documents the recovery time.

### Outcome measurement

- Use privacy-respecting analytics to measure route entry, anonymous/authenticated distinction where lawful, filter use, authoritative-source clicks, favorites, returns, and correction submissions without collecting unnecessary personal data.
- Run moderated journey tests before launch using the thresholds in Section 2.
- Generate the content-completeness and freshness report weekly during the first eight weeks.
- Record contributor activity and estimated maintainer time weekly.
- Compare results at weeks 2, 4, and 8; do not declare completion from deployment alone.

## 8. Release, observation, and correction cycles

### Cycle 1 — Actor review and contributor pilot, 2026-08-24 to 2026-08-31

- **Released:** Authenticated preview with seeded public pages, classes, events, favorites, contributor tools, and administration.
- **Audience:** Project owner, two contributors, one newcomer, one regular local dancer, and one visitor-profile tester.
- **Expected result:** Core journeys are understandable, ownership rules hold, and contributors can maintain records without administrator intervention.
- **Observation period:** From preview handoff through 2026-08-31, followed by correction work in September.
- **Measurements:** Task timings, failed tasks, authorization suite, corrections, maintainer time, completeness, and freshness.
- **Feedback:** Pending.
- **Unexpected effects:** Pending.
- **Correction or decision:** Pending.
- **Next review date:** Set when the pilot starts.

### Cycle 2 — Public minimum release, September 2026

- **Released:** Corrected public site with verified launch inventory and controlled contribution.
- **Audience:** Montpellier WCS community and search visitors.
- **Expected result:** Users complete the four primary journeys and begin returning for current information.
- **Observation period:** Eight weeks.
- **Measurements:** Section 2 completion measures, correction volume, provider coverage, return use, outbound source clicks, freshness and maintenance effort.
- **Feedback:** Pending.
- **Unexpected effects:** Pending.
- **Correction or decision:** Pending.
- **Next review date:** Weeks 2, 4, and 8 after public release.

## 9. Decision log

| Date | Decision | Evidence and rationale |
| --- | --- | --- |
| 2026-08-16 | Initiative planned from the Montpellier WCS exploration | The project owner chose to proceed from information-architecture exploration to a measurable build-and-test initiative |
| 2026-08-16 | Select a staged guide, class planner, shared agenda, accounts, and controlled contribution | Covers the four primary user journeys while excluding ticketing and social-network scope |
| 2026-08-16 | Use four application roles | Anonymous reads public content; users add favorites; contributors manage only owned classes/events; administrators have global read/write |
| 2026-08-16 | Separate authorization ownership from public actor attribution | Prevents a teacher/organizer label from implicitly granting write access and permits audited ownership transfer |
| 2026-08-16 | Treat copywriting and community rules as implementation dependencies | Discovery, trust, safety, neutrality and contributor behavior cannot be completed through interface code alone |
| 2026-08-16 | Derive actor roles from relations rather than an actor type enum | One actor may simultaneously teach, own a studio, and organize events; explicit many-to-many relations preserve that reality |
| 2026-08-16 | Add explicit listing-place, schedule-place and occurrence-place relations | Classes and events must resolve to the correct place coordinates in planning and date-specific map results |
| 2026-08-16 | Support badge and hero media on display entities | Actors, places, classes, events and editorial pages need consistent compact and detail imagery with rights and accessibility metadata |
| 2026-08-16 | Set staged delivery deadlines | Internal v1 is due 2026-08-23, actor review by 2026-08-31, and public launch during September no later than 2026-09-30 |
| 2026-08-17 | Start the initiative with an ignored nested application repository | Keep planning records and the independently versioned `projects/wcsmontpellier-site` checkout together. The parent ignores `/projects/`; ordinary parent checkout, reset, and clean operations leave it untouched, while `git clean -ffdx` remains an accepted explicit risk |
| 2026-08-17 | Select the initial application stack | Use Vite, React and TypeScript with Convex for data, authentication and storage; Tailwind and shadcn for interface primitives; and MapLibre for maps |
| 2026-08-17 | Implement the first read-only vertical slice with explicit demo data | Add server-side authorization helpers, idempotent internal fixtures, bounded indexed public queries, and live homepage, course planning/map, and agenda surfaces; all fixture content is labelled fictitious |

## 10. Closure

- **Final status:** Open
- **Closed on:** Not applicable
- **Completion results:** Pending
- **Resources used:** Pending
- **Reason for completing or discarding:** Pending
- **What we learned:** Pending
- **Follow-up records:** Pending
