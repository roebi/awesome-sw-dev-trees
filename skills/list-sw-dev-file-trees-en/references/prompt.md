# Aider Prompt — list-sw-dev-file-trees-en

This is the exact `--message` text passed to aider by the GitHub Actions workflow.
Edit here to tune what the LLM does each bi-weekly run.

---

```
Follow the instructions in skills/list-sw-dev-file-trees-en/SKILL.md exactly.

Today's date is {TODAY}.

1. Regenerate the ranked list of the 25 most-used file tree structures in
   software development, re-ranking if ecosystem adoption has shifted.
2. Overwrite README.md with the fresh table using the exact format defined
   in the skill (include updated "Last updated: {TODAY}" line).
3. Append a new dated entry at the top of CHANGELOG.md describing any
   rank changes, additions, or removals compared to the current content.
   If nothing changed, still append an entry stating "No ranking changes this run."
4. Do not modify any other file.
```

---

The workflow substitutes `{TODAY}` with the actual date via `sed` before passing
the message to aider. See `.github/workflows/update-trees.yml`.
