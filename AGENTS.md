# AGENTS.md

## Project Overview
PHP US Social Security Number generator/validator library (fngssn). A single class file with an example demo script. No database, no external dependencies, no framework.

## Running the App
- `docker compose -f docker-compose.base44.yml up -d` starts a `php:8.2-cli` container with PHP's built-in dev server on port 3000.
- Source is bind-mounted at `/var/www/html`; edits appear immediately (restart not needed).
- The web entry point is `/example.php` — it generates a California SSN and validates a sample SSN.

## Architecture
- `fngssn.class.php` — the library class with `generateSSN($state)` and `validateSSN($ssn)` methods.
- `example.php` — demo script that instantiates the class and prints output with HTML `<br />` tags.
- No external credentials required.

## Verification
- `curl -s http://localhost:3000/example.php` should output a generated SSN, two `<br />` tags, and a two-letter state code.
