# ADK Go Lab

This repository is a learning workspace for building agents with Google ADK in Go.

## Framework and Environment

- Go `1.25.7`
- `google.golang.org/adk` for agent orchestration
- `google.golang.org/genai` for Gemini access
- Gemini API key via `GOOGLE_API_KEY`
- Local launch modes through ADK launcher: console, REST API, and Web UI

## Purpose

- Learn the core ADK concepts in Go
- Keep each exercise isolated by topic
- Turn small experiments into reusable agent examples

## MOC

MOC here means Map of Content: the top-level guide for this repo.

1. [quick-start](quick-start/README.md): a minimal ADK Go agent using Gemini, `llmagent`, and `web api webui`.

## Current Structure

- `quick-start/`: the first runnable exercise
- `.gitignore`: shared ignore rules for the repo
- `.env`: local environment variables for development

## Next Topics

- Custom Go tools
- Multi-agent composition
- Session and memory handling
- Production-oriented API and deployment patterns
