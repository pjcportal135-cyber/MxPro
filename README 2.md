# AeroMaint Pro SaaS v2

This is Phase 2 of the multi-tenant aviation maintenance SaaS build.

## New in v2

- inspections module
- squawks module
- work orders module
- squawk → work order conversion
- dashboard operations metrics
- create screens for all Phase 2 modules
- richer demo seed data

## Demo login

- Email: `admin@skybridge.aero`
- Password: `ChangeMe123!`

## iPad-friendly quick start

1. Run PostgreSQL with `docker compose up -d`
2. Apply `database/schema.sql`
3. In `apps/api`, copy `.env.example` to `.env`, then run `npm install`, `npm run seed`, `npm run dev`
4. In `apps/web`, copy `.env.example` to `.env`, then run `npm install`, `npm run dev`
5. Open the web URL in Safari on your iPad

## Recommended next phase

- attachments and document storage
- technician signatures and release-to-service records
- edit/update actions
- maintenance forecast engine
- customer billing and subscription plans
