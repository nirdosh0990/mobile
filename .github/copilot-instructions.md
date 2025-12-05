# GitHub Copilot Instructions – mobile

Extends the global instructions from [specs/.github/copilot-instructions.md](https://github.com/localstore-platform/specs/blob/v1.1-specs/.github/copilot-instructions.md).

## Repository Context

- **Repository:** mobile
- **Type:** Flutter 3.x Mobile App (iOS + Android)
- **Tech Stack:** Flutter 3.x, Dart 3.x, Riverpod 2.4, Dio + Retrofit, Hive, Firebase Cloud Messaging
- **Spec Version:** v1.1-specs
- **Spec Links:** See [docs/SPEC_LINKS.md](../docs/SPEC_LINKS.md)

## Specific Guidelines

### Code Style

- Follow [Effective Dart](https://dart.dev/guides/language/effective-dart) guidelines
- Use `dart format` for consistent formatting
- Prefer `const` constructors where possible
- Use named parameters for functions with 2+ parameters
- Follow Clean Architecture with feature-first folder structure

### Architecture Patterns

- **State Management:** Riverpod 2.4 with code generation
- **Networking:** Dio with Retrofit for type-safe API calls
- **Local Storage:** Hive for offline-first caching
- **Navigation:** go_router for declarative routing
- **DI:** Riverpod providers (no external DI container)

### Testing Requirements

- Unit tests for all business logic (providers, repositories)
- Widget tests for UI components
- Integration tests for critical user flows
- Minimum 80% coverage for core features

### Vietnamese Localization

- Use `vi-VN` locale for all Vietnamese text
- Currency format: `75.000₫` (dot separator, đồng symbol)
- Date format: `dd/MM/yyyy` (Vietnamese standard)
- All user-facing strings in `lib/l10n/`
- Reference [Glossary](https://github.com/localstore-platform/specs/blob/v1.1-specs/knowledge-base/glossary.md) for translations

## Git Workflow

**IMPORTANT**: Follow the git workflow defined in [docs/GIT_WORKFLOW.md](../docs/GIT_WORKFLOW.md).

Key rules:

- **Never commit directly to main branch**
- If on main, create a new branch before committing
- Branch naming: `<type>/<short-description>` (e.g., `feat/add-dashboard`)
- Commit changes logically (group related changes)
- After commits, push and create/update PR to main branch — **do not wait for confirmation**
- Use conventional commit messages

### Commit Granularity Principle

Each commit should answer ONE of these questions:

- "What single feature/fix does this add?"
- "What single purpose do these files serve together?"

**Rule of thumb:** If you need "and" to describe the commit, split it.

- ❌ `Add docs and config files` → Split
- ❌ `Update README and add environment template` → Split
- ✅ `Add GitHub PR template and CODEOWNERS` → OK (same purpose: GitHub config)
- ✅ `Add specification links documentation` → OK (single purpose)

## Common Tasks

### Adding a New Feature

1. Check SPEC_LINKS.md for relevant specifications
2. Load spec sections using semantic_search
3. Implement following spec exactly
4. Add tests matching spec examples
5. Update documentation

### Adding a New Screen

1. Create feature folder: `lib/features/<feature_name>/`
2. Add presentation layer: `presentation/screens/`, `presentation/widgets/`
3. Add domain layer: `domain/entities/`, `domain/repositories/`
4. Add data layer: `data/repositories/`, `data/datasources/`
5. Register providers in feature's `providers.dart`
6. Add route in `lib/core/router/`

### Updating API Contracts

1. Ensure contracts repository is updated first
2. Update this repository to use new contract version
3. Regenerate Retrofit clients
4. Run contract tests
5. Update API documentation

## Project Structure

```text
lib/
├── core/
│   ├── constants/
│   ├── router/
│   ├── theme/
│   └── utils/
├── features/
│   ├── auth/
│   ├── dashboard/
│   ├── menu/
│   └── settings/
├── l10n/
├── shared/
│   ├── providers/
│   └── widgets/
└── main.dart
```

## Related Documentation

- [Main Specs Repository](https://github.com/localstore-platform/specs)
- [Flutter Mobile App Spec](https://github.com/localstore-platform/specs/blob/v1.1-specs/architecture/flutter-mobile-app-spec.md)
- [AI Context Guide](https://github.com/localstore-platform/specs/blob/v1.1-specs/.github/AI_CONTEXT_GUIDE.md)
- [Spec Changelog](https://github.com/localstore-platform/specs/blob/v1.1-specs/SPEC_CHANGELOG.md)
