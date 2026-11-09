# Pani Indo | പണി ഇവിടെ

Pani Indo is a local-work discovery concept for Kerala. It helps people post a work requirement or find nearby work opportunities.

## Features

- Post a request for workers or offer available work.
- Add work details, location, PIN code, wage, and contact number.
- Browse and search local posts.
- Display posts from the Supabase `pani_posts` table.
- Malayalam-first interface with English helper labels.

## Technology

- HTML, CSS, and vanilla JavaScript.
- Supabase JavaScript client.
- Supabase database for job posts.

## Backend setup

The current frontend connects to a Supabase project and queries the `pani_posts` table.

To run a separate instance:

1. Create a Supabase project.
2. Configure the project URL and publishable/anon key in `index.html`.
3. Create the `pani_posts` table with columns matching the fields used by the application.
4. Configure Row Level Security policies for reading and creating posts.
5. Validate and rate-limit submissions on the backend. Do not rely on browser-side checks to protect the database.

The browser key is a public client key, not a secret. Never expose a Supabase service-role key in this repository.

## Run locally

```bash
python -m http.server 8000
```

Open http://localhost:8000.

## Deployment

The project is a static frontend and can be hosted with GitHub Pages. Supabase provides the database backend.

## License

No license is currently specified. All rights remain with the repository owner unless a license is added.
