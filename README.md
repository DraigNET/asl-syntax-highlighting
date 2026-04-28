# Quest ASLX Syntax Highlighting

Syntax highlighting and editing support for Quest ASLX files in Visual Studio Code.

## Features

- XML highlighting for Quest ASLX files (`.aslx`)
- Embedded Quest script highlighting inside common ASLX script elements
- Highlighting for Quest text processor placeholders, formatting codes, and expressions
- Language configuration for comments, brackets, pairs, and folding
- Starter snippets for common ASLX blocks

## Supported Files

- `.aslx` - Quest 5 XML game and library source

## Usage

Open any `.aslx` file and VS Code will select the Quest ASLX language mode automatically.

The extension includes snippets for common constructs. Start typing prefixes such as `aslx-game`, `object`, `function`, or `script` to insert them.

## Development

To try the extension locally:

1. Open this folder in VS Code.
2. Press `F5` or run the `Extension` launch configuration.
3. Open a `.aslx` file in the extension development host window.

Before packaging, validate the JSON files:

```powershell
node -e "for (const f of ['package.json','syntaxes/asl.tmLanguage.json','syntaxes/aslx.tmLanguage.json','language-configuration-aslx.json','snippets/aslx.code-snippets']) JSON.parse(require('fs').readFileSync(f,'utf8')); console.log('JSON OK')"
```

Package with `vsce package` if you have `@vscode/vsce` installed.

## Credits

- [Quest documentation](https://docs.textadventures.co.uk/quest/) for the ASL/ASLX language reference
- Visual Studio Code for the extension APIs and TextMate grammar support

## License

MIT
