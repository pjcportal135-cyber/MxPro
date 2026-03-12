# AeroMaint Pro SaaS

A multi-tenant aviation maintenance SaaS starter that you own and can deploy outside Replit.

## What's in this version

- Multi-tenant PostgreSQL schema
- Organization onboarding
- JWT authentication
- Role-based access control
- Protected API routes
- Public landing page
- App dashboard shell
- Aircraft module starter
- Seed data for a demo organization
- iPad-friendly setup notes

## Stack

- Web: React + TypeScript + Vite + Tailwind
- API: Node.js + Express + TypeScript
- Database: PostgreSQL
- Auth: JWT + bcrypt

## Project structure

```text
apps/
  web/
  api/
database/
docs/
```

## Quick start

### 1. Start PostgreSQL

Use your own PostgreSQL server, or run locally with Docker:

```bash
docker compose up -d
```

### 2. Create the schema

Run `database/schema.sql` against your PostgreSQL database.

### 3. Start the API

```bash
cd apps/api
cp .env.example .env
npm install
npm run seed
npm run dev
```

API default URL:

```text
http://localhost:4000/api
```

### 4. Start the web app

```bash
cd apps/web
cp .env.example .env
npm install
npm run dev
```

Web default URL:

```text
http://localhost:5173
```

## Demo login after seed

```text
Email: admin@skybridge.aero
Password: ChangeMe123!
```

## Main product model

This version is built for SaaS and supports:

- many organizations
- many users per organization
- organization-level data isolation
- company admin, manager, technician, inspector roles

## Recommended next phase

- create and edit forms
- work order flows
- squawk to work order conversion
- attachments and document storage
- cryptographic e-signatures
- audit events on all writes
- billing and subscriptions
- forecast engine for due dates / hours / cycles

## iPad workflow

Because you're using an iPad, the easiest workflow is:

1. keep this project in GitHub
2. run the API and database on a VPS
3. open the web app from Safari
4. use Termius on iPad for server commands

See `docs/ipad-deploy.md` for the exact flow.

## Important note

This is a serious SaaS foundation, but it is **not** a production-certified aviation records system yet. Before live operational use, add formal compliance, secure signatures, audit retention, document controls, and regulatory review.
