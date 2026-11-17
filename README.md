# Pani Indo | പണി ഇവിടെ

Pani Indo is a Malayalam-first local work discovery concept for Kerala. It helps people post work requirements and discover nearby opportunities.

## Features

- Post a request for workers or offer available work.
- Add work details, location, PIN code, wage, and contact number.
- Browse and search local posts.
- Load posts from the Supabase `pani_posts` table.
- Malayalam-first interface with English helper labels.

## Technology

- HTML, CSS, and vanilla JavaScript.
- Supabase JavaScript client.
- Supabase database.

## Backend setup

The frontend connects to a Supabase project and reads and writes records in the `pani_posts` table.

To run your own instance:

1. Create a Supabase project.
2. Configure the project URL and publishable/anon key in `index.html`.
3. Create the `pani_posts` table with the columns expected by the application.
4. Enable Row Level Security and add policies for the required read and create actions.
5. Validate submissions and apply suitable rate limits on the backend.

The publishable/anon key is designed for browser use, but it does not replace database access policies. Never expose a Supabase service-role key in frontend code.

## Run locally

```bash
python -m http.server 8000
```

Open http://localhost:8000.

## Deployment

This is a static frontend that can be hosted with GitHub Pages. Supabase provides the database backend.

## Security status

Review the Supabase Row Level Security policies before using the project with real users or public data.

## License

No license is currently specified. All rights remain with the repository owner unless a license is added.
