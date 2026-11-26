# Krillion GD (Render fork starter)

A Geometry Dash-themed Krillion-style rarity trivia game, with solo play, versus/co-op rooms, an admin question editor, categories, and persistent PostgreSQL storage.

## Easy deploy

1. Upload this folder to a GitHub repository.
2. On Render, choose **New > Blueprint** and connect that repo (Render reads `render.yaml`).
3. When prompted for `ADMIN_PASSWORD`, set a long password. Do not share it.
4. Approve the Blueprint. Render creates the web service and database.
5. Visit the service URL. Admin is available from the main screen.

The database is created and seeded on first server start. The seed contains starter prompts across Geometry Dash, gaming, music, geography, science, food, movies and sports. You can add more categories, questions and accepted answers from the admin panel.

## Answer tiers

`plankton` (10), `tooClever` (15), `schooler` (30), `rare` (60), `deepCut` (85), `gem` (100).

Admin answers are entered one per line as `answer | tier`.

## Multiplayer

Choose Versus or Co-op, enter a player name, and optionally a room code. An empty room code creates a room. Share the generated code with others. The room creator can start the seven-question session. Rooms are currently in-memory, so rooms reset if the service restarts; persistent question data does not.

## Notes / limitations

This is a compact starter fork rather than a feature-for-feature port of OpenKrillion. Multiplayer is realtime WebSocket room play, but room state is not persisted. Co-op currently shares a room and prompt progression; additional team scoring/UI polish is a future improvement. This fork does not copy Krillion's daily puzzle data. It includes its own starter prompt set. Use a persistent Render database; free-tier availability/retention is subject to Render's current terms.
