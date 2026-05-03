# avandar-agent-skills

A collection of reusable agent skills for AI coding assistants.

## Installation

```bash
npx skills add AvandarLabs/avandar-agent-skills
```

To install a specific skill:

```bash
npx skills add AvandarLabs/avandar-agent-skills --skill supabase-declarative-schema
```

## Available Skills

### supabase-declarative-schema

Enforces a declarative schema workflow for Supabase database changes. Instead of manually writing migration files, you define the desired state in `supabase/schemas/*.sql` files and generate migrations with `supabase db diff`.

This skill takes priority over the base `supabase` skill for all schema-related operations.

**Key workflow:**

1. Define schema in `supabase/schemas/*.sql`
2. Run `supabase stop`
3. Run `supabase db diff -f <migration_name>`

### avandar-ava-model-creation

Documents Avandar's conventions for creating new models with the Ava CLI, including `shared/models`, `src/models`, Supabase-backed CRUD models, Dexie-backed browser models, parsers, schema migrations, and client wiring.

## Adding Skills

Each skill lives in its own directory under `skills/` and contains a `SKILL.md` file with frontmatter metadata and agent instructions.

## License

MIT
