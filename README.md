# Plum

A set of utilities for improving agentic outputs

## Skills

| Skill | What it does | How to run it |
| --- | --- | --- |
| `write-simply` | Makes the agent write documents and answers in plain English, so a human can read them without effort. | `/plum:write-simply` |

### Usage

Type the command and add your request after it. You can also point to a file with `@`.

```
/plum:write-simply Explain react hooks
```

```
/plum:write-simply Summarize @design-doc.md
```

```
/plum:write-simply Rewrite the intro of @README.md for a new reader
```

## Installation

### In the terminal


```
claude plugin marketplace add msmolinski/plum-marketplace
```

```
claude plugin install plum@plum-marketplace
```

### Inside Claude

```
/plugin marketplace add msmolinski/plum-marketplace
```

```
/plugin install plum@plum-marketplace
```


## Local development

```
git clone git@github.com:maciejsmolinski/plum-marketplace.git
```

```
claude plugin marketplace add ./plum-marketplace
```

```
claude plugin install plum@plum-marketplace
```
