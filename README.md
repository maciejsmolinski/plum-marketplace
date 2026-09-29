# Plum

A small collection of skills for Claude Code. Each one changes how the agent
handles a task, and you run them only when you want them.

## Installation

In the terminal:

```
claude plugin marketplace add maciejsmolinski/plum-marketplace
claude plugin install plum@plum-marketplace
```

Inside Claude:

```
/plugin marketplace add maciejsmolinski/plum-marketplace
/plugin install plum@plum-marketplace
```

To update or remove the plugin later:

```
claude plugin update plum@plum-marketplace
claude plugin uninstall plum@plum-marketplace
```

## Skills

| Skill | What it does | Command | Prompt phrase |
| --- | --- | --- | --- |
| `write-simply` | Makes the agent write documents and answers in plain English, so a human can read them without effort. | `/plum:write-simply` | `write simply` |
| `share-opinion` | Makes the agent give you a blunt, direct review. It tells you what is weak and why, instead of being polite. | `/plum:share-opinion` | — |

`share-opinion` runs only when you call it. `write-simply` also usually starts
on its own when you ask Claude to "write simply" in your prompt.

## Usage

Type the command and add your request after it. You can also point to a file
with `@`.

### write-simply

```
/plum:write-simply Explain react hooks
```

```
/plum:write-simply Summarize @design-doc.md
```

```
/plum:write-simply Rewrite the intro of @README.md for a new reader
```

```
What's the bulkhead pattern? Write simply
```

Expect short sentences and everyday words. The skill keeps the technical terms
it needs and drops the rest, so it changes the style, not the depth.

### share-opinion

```
/plum:share-opinion Review @README.md and tell me if anything is missing
```

```
/plum:share-opinion Is it worth splitting this plugin into two?
```

```
/plum:share-opinion Poke holes in the plan in @rfc-042.md
```

Expect straight answers. The skill is built to disagree with you when it has
reason to, so use it before you commit to a decision, not after.

## Local development

```
git clone git@github.com:maciejsmolinski/plum-marketplace.git
claude plugin marketplace add ./plum-marketplace
claude plugin install plum@plum-marketplace
```

## License

MIT. See [LICENSE](LICENSE).
