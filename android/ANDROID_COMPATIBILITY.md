# 9Router Android Compatibility

## Project Goal
Port the complete 9Router application into the Android environment used by Mobile Codex. Preserve the original provider registry, routing engine, dashboard, APIs, authentication, database, model management, usage analytics, logs, proxy features, cloud sync, media endpoints, CLI configuration features, and existing functionality.

## Source Baseline
- Repository: decolua/9router
- Fork: HasibBot4u/9router-android
- Working branch: android-compat
- Baseline commit: 1fe586bb1cf35e1ed0cb2150a8ef7d1db040b21d

## Target Environment
- Android ARM64
- Minimum Android API 29
- Mobile Codex bundled Android development tools
- Android-compatible Node.js runtime
- App-private storage
- Localhost-only server binding

## Critical Rule
Do not remove, replace, or silently disable an existing 9Router feature just because it does not work on Android. First identify its dependencies, document the incompatibility, and propose an Android adapter or optional Linux ARM runtime implementation.

## Required Compatibility Checks

| Component | Status |
|---|---|
| Next.js standalone server | NOT TESTED |
| Node.js version compatibility | NOT TESTED |
| SQL.js persistence | NOT TESTED |
| better-sqlite3 native module | NOT TESTED |
| node-machine-id | NOT TESTED |
| wreq-js | NOT TESTED |
| playwright-core | NOT TESTED |
| Browser automation | NOT TESTED |
| FFmpeg | NOT TESTED |
| OAuth callbacks | NOT TESTED |
| Localhost binding | NOT TESTED |
| Provider registry | NOT TESTED |
| Provider connections | NOT TESTED |
| OpenAI Chat Completions | NOT TESTED |
| OpenAI Responses API | NOT TESTED |
| Anthropic Messages API | NOT TESTED |
| Streaming and tool calls | NOT TESTED |
| Usage and request logging | NOT TESTED |
| Proxy and tunnel features | NOT TESTED |
| Media endpoints | NOT TESTED |
| Cloud sync | NOT TESTED |

## Preservation Requirements
Keep the complete original source tree. Do not delete provider executors, translators, handlers, dashboard pages, API routes, database models, CLI integrations, tests, or documentation.

## Testing Rules
A successful Linux build does not prove Android compatibility. Every runtime-dependent feature must eventually be tested inside the actual Android app.

## Final Acceptance
The Android build must preserve the original 9Router features and expose any platform-dependent limitations honestly. No fake UI-only implementations or placeholder success states are allowed.
