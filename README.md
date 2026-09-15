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

| Skill | What it does | How to run it |
| --- | --- | --- |
| `write-simply` | Makes the agent write documents and answers in plain English, so a human can read them without effort. | `/plum:write-simply` |

Every skill here runs on request only. Claude never picks one on its own, so
you stay in control of when it changes its style.

### Usage

Type the command and add your request after it. You can also point to a file
with `@`.

```
/plum:write-simply Explain react hooks
```

```
/plum:write-simply Summarize @design-doc.md
```

```
/plum:write-simply Rewrite the intro of @README.md for a new reader
```

## Local development

```
git clone git@github.com:maciejsmolinski/plum-marketplace.git
claude plugin marketplace add ./plum-marketplace
claude plugin install plum@plum-marketplace
```

## License

MIT. See [LICENSE](LICENSE).
