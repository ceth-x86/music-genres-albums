# Music Genres Albums — Project Instructions

## Project Structure
- `utils/classification.yaml` — genre hierarchy/taxonomy
- `utils/prompt.txt` — prompt template for generating album lists
- `README.md` — index with links to all genre files

## Workflow: Processing a Genre File

When the user gives a filename:

1. **Convert to Markdown** — the file is CSV-like (Artist,Album,Year,Description). Convert it into a proper markdown table:
   ```
   | Artist | Album | Year | Why it defines the genre |
   | :--- | :--- | :--- | :--- |
   ```

2. **Classify and move** — look up the genre in `utils/classification.yaml` to determine the full parent hierarchy. Create directories for all parent categories, but NOT for the leaf genre itself (it becomes the file). Examples:
   - Slowcore (under Indie Rock) → `Indie Rock/slowcore.md`
   - Atmospheric Black Metal (under Metal → Black Metal) → `Metal/Black Metal/atmospheric-black-metal.md`
   Create directories as needed.

3. **Update README.md** — add a link to the file in `README.md` at the project root, organized by category.
