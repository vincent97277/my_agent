# Quick Start

A minimal Google ADK agent project written in Go.

See the repo-level MOC in [`../README.md`](../README.md).

## What this exercise does

- Creates a Gemini model client with `gemini-2.5-flash`
- Builds a single `llmagent`
- Enables the built-in `google_search` tool
- Starts the ADK launcher in console or web mode

## Module

This directory is an independent Go module:

```go
module github.com/vincent97277/adk-go-lab/quick-start
```

## Prerequisites

- Go `1.25.7` or compatible
- A valid `GOOGLE_API_KEY`

## Setup

From the repo root:

```bash
cd quick-start
go mod tidy
export GOOGLE_API_KEY="<your_api_key>"
```

You can also use the example file:

```bash
source .example.env
```

## Run

From the repo root:

```bash
go -C quick-start run .
go -C quick-start run . console
go -C quick-start run . web api webui
```

From `quick-start/`:

```bash
go run .
go run . console
go run . web api webui
```

If startup fails, check:

- `GOOGLE_API_KEY` is set in your shell
- network access to Google APIs is available

## Files

- `agent.go`: app entrypoint and agent configuration
- `go.mod` / `go.sum`: module and dependencies
- `.example.env`: example environment variable setup
- `../.gitignore`: shared ignore rules for the repo
