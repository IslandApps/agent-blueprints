# Agent Blueprints

A collection of useful CLAUDE.md rules that I create along the way. I'll be adding more as I find them to help the AI work better.

## Workflows
- **fail-fast.md**: If the AI tries to fix something and it doesn't work, this rule makes it automatically revert its changes before trying again. This prevents code bloat and keeps things from breaking.

## How to Implement
To get the best results, follow this order:

1. **Initialize:** Run `/init` in your project terminal. This lets the AI analyze your code to find your specific build and test commands.
2. **Apply Blueprints:** Open the `CLAUDE.md` file that was just created and paste your chosen rules (like `fail-fast.md`) at the bottom.
3. **Go to Work:** The AI will now respect these rules.

---

## License
MIT
