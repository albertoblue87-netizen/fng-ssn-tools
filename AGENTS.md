# AGENTS.md

## Project Overview
PHP US Social Security Number Generator and Validator (fngssn). A single-class PHP library with a demo entry point (`example.php` / `index.php`).

## Running the Project
- Uses `docker-compose.base44.yml` with `php:8.2-cli` and PHP's built-in dev server on port 3000.
- Source is bind-mounted at `/var/www/html`; edits are reflected immediately (PHP re-reads files per request — no watcher needed).
- Start: `docker compose -f docker-compose.base44.yml up -d`
- The entry point `index.php` includes `example.php`, which demonstrates `generateSSN()` and `validateSSN()`.

## No External Dependencies
- No database, no external services, no secrets required.
- No Composer dependencies.

## Verification
- `curl http://localhost:3000/` should return HTML with a generated SSN and a validation result.
