# Dev promotion plan

Deploy only from a reviewed application commit/image digest. Require passing backend, frontend, PostgreSQL RLS and container scanning gates. Use test AWS resources and non-production secrets from an approved secret manager. No dev cluster configured yet.
