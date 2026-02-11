---
name: create-article
description: Guide for creating articles using templates. Use when asked to create a new NPC, session, faction, location, or similar entry for the Blood & Dust campaign site.
---

## Activation
- Trigger when a request mentions creating a new NPC, session, faction, or location entry for the Blood & Dust site.
- Look for keywords like "new npc", "add faction", "session notes", or "location article" in the user prompt.

## Behavior
1. Determine the entity type (NPC, Session, Faction, Location) from the prompt.
2. Select the matching template from `_templates/`:
   - NPC ➜ `_templates/npc.md`
   - Session ➜ `_templates/session.md`
   - Faction ➜ `_templates/faction.md`
   - Location ➜ `_templates/location.md`
3. Ask the user for specific details and clarifying information to flesh out the article's content.
4. Replace the placeholder text (bracketed hints) with concrete content that reflects the new entry. Preserve the section headings so future contributors know where to add details.
5. Save the new article in the correct folder:
   - NPCs ➜ `_world/npcs/` with a slug-based filename (e.g., `marcus-severus.md`).
   - Sessions ➜ `_sessions/` with a numbered slug (e.g., `session-01-first-blood.md`).
   - Factions ➜ `_world/factions/` (e.g., `house-of-tigers.md`).
   - Locations ➜ `_world/locations/` (e.g., `grand-arena.md`).
6. Update `summary`, `title`, `topic`, and any metadata so the front matter matches the document. Ensure `layout: page` remains in place.
7. Mention in the response which template was used and the destination path, so reviewers can verify placement.

## Notes
- Keep the tone consistent with existing lore.
- If the request includes a specific session index or title, reflect that in both the front matter and document body.
- When in doubt about the folder structure, follow the patterns shown in the current `_world` and `_sessions` directories.
- Always ask for more details if the initial prompt is vague, to ensure the article is rich and informative.
