This workspace includes Biome for formatting JavaScript/JSON but Biome does not support formatting HTML in the current configuration.

What I changed

- Added `.vscode/settings.json` to explicitly use the built-in VS Code HTML formatter and disable format-on-save for HTML files. That prevents the editor from invoking Biome for HTML and removes the error message:

  "Biome doesn't support this feature for the language HTML"

How to revert or alternatives

- If you prefer to let Biome handle only supported languages, remove or edit `.vscode/settings.json`.
- To keep Biome installed but make it ignore HTML files globally, you can add a `.biomeignore` file listing `**/*.html`.
- To disable Biome entirely in this project, remove `@biomejs/biome` from `devDependencies` in `package.json` and run your package manager to update lockfiles.

If you'd like, I can instead add `.biomeignore`, or adjust Biome config to avoid errors — tell me which option you prefer.
