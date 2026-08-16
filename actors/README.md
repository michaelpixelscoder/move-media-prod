# Actors

This directory is a lightweight, file-based CRM for real people and organizations in the movement ecosystem.

An actor may be a potential client, current client, partner, community, studio, teacher, organizer, merchandiser, volunteer group, or service provider. Only create profiles for real actors; general persona descriptions belong in business or research documentation.

## Structure

Give each actor a directory containing one main profile:

```text
actors/
└── actor-name/
    ├── actor-name.actor.md
    └── supporting-files...
```

Supporting files might include public references, meeting notes, briefs, or approved assets. Do not store secrets, payment details, identity documents, private student data, or unnecessary personal information in this repository.

Copy `_template/` when adding an actor, then rename both the directory and main file. Use the actor's recognizable public name in lowercase kebab-case. If names collide, add a city, discipline, or organization qualifier.

Examples:

- `actors/movement-studio-paris/movement-studio-paris.actor.md`
- `actors/alex-martin-salsa/alex-martin-salsa.actor.md`

## Why Markdown profiles

One profile per actor is easy to search, review, link, and version. YAML front matter gives important CRM fields a predictable structure, while the body remains flexible enough for context and relationship notes. This structure can later be parsed and imported into a dedicated CRM.

Avoid maintaining a separate spreadsheet index for now: it would duplicate information and become stale. An index or dashboard can be generated from the profile front matter when the number of actors makes it useful.

## Actor types

Use one or more of these initial values in `types`:

- `regular-teacher`
- `event-teacher`
- `studio`
- `event-organizer`
- `merchandiser`
- `volunteer`
- `service-provider`
- `community`
- `student`
- `partner`
- `other`

The list may evolve when real profiles reveal better categories.

## Relationship stages

Use one of these values for `stage`:

- `identified`: known but not yet qualified
- `researching`: gathering enough context to assess relevance
- `qualified`: plausible fit with an understood need
- `contacted`: outreach or a first introduction has happened
- `conversation`: needs and fit are being discussed
- `proposal`: a concrete offer has been made
- `client`: active paying client
- `past-client`: previous paying client
- `partner`: active non-client collaboration
- `not-a-fit`: intentionally not pursuing

Record meaningful interactions in the profile's interaction log. Keep notes factual, respectful, and useful for the relationship.
