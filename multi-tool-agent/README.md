# Multi Tool Agent

A follow-up Google ADK exercise written in Go.

See the repo-level MOC in [`../README.md`](../README.md).

## What this exercise does

- Creates a Gemini model client with `gemini-2.5-flash`
- Builds a single `llmagent`
- Enables the built-in `google_search` tool
- Starts the ADK launcher in console or web mode

## Why this directory exists

This module is the next step after `quick-start/`.
It keeps the same runnable skeleton, but frames the exercise around tool-enabled agents.

The current implementation still uses one tool:

- `google_search`

This makes it a good place to add more tools later without changing the beginner-friendly structure.

## Module

This directory is an independent Go module:

```go
module github.com/vincent97277/adk-go-lab/multi-tool-agent
```

## Prerequisites

- Go `1.25.7` or compatible
- A valid `GOOGLE_API_KEY`

## Setup

From the repo root:

```bash
cd multi-tool-agent
go mod tidy
export GOOGLE_GENAI_USE_VERTEXAI=FALSE
export GOOGLE_API_KEY="<your_api_key>"
```

You can also use the example file:

```bash
source .example.env
```

## Run

From the repo root:

```bash
go -C multi-tool-agent run .
go -C multi-tool-agent run . console
go -C multi-tool-agent run . web api webui
```

From `multi-tool-agent/`:

```bash
go run .
go run . console
go run . web api webui
```

If startup fails, check:

- `GOOGLE_API_KEY` is set in your shell
- `GOOGLE_GENAI_USE_VERTEXAI=FALSE` is set when using API key auth
- network access to Google APIs is available

## Files

- `agent.go`: app entrypoint and agent configuration
- `go.mod` / `go.sum`: module and dependencies
- `.example.env`: example environment variable setup
- `../.gitignore`: shared ignore rules for the repo

## Suggested Next Steps

- Add a second tool to `Tools: []tool.Tool{...}`
- Replace the generic instruction with tool-selection guidance
- Compare the behavior with `quick-start/` after each added tool
