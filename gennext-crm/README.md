# GenNext CRM — MVP

A small-team CRM for PLM business development. It tracks companies, contacts, leads, owners, activities, follow-ups and a sales pipeline.

## Stack
- React + Vite frontend
- Express API
- SQLite database
- JWT login

## Local setup
Requirements: Node.js 20+.

```bash
npm install
npm run install-all
npm run dev
```

Open http://localhost:5173

Default login:
- Email: admin@gennext.local
- Password: Admin@123

Change the password and JWT secret before production use.

## Production architecture
For a first internal deployment, run the API on a small VPS and the frontend on a static host. Set `VITE_API_URL` to the public API URL and set `JWT_SECRET` and `DB_FILE` on the API server.

For a larger team, migrate SQLite to PostgreSQL and add object storage for attachments, audit logs, email/calendar integration, backups, and SSO.

## Suggested next features
1. Edit/delete contacts and activities
2. Lead detail page + full activity timeline
3. Excel/CSV import and export
4. Role permissions (admin/manager/sales)
5. Email/calendar integration
6. Notifications for due follow-ups
7. File attachments
8. Monthly sales activity dashboard
9. Duplicate detection
10. PostgreSQL migration + automated backups
