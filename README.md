# lore-testing-library-ui

A deliberately small React component library, used as a fixture for the manual
tests in [living-ai-knowledge](https://github.com/CodeMedic42/living-ai-knowledge).

Published as `@acme/ui-kit`. Nine components in a four-level composition chain:

```
DateRangeSelector → DateSelector → TextField → FieldLabel
                                 ↘ Calendar  → CalendarDay
```

Small on purpose. A real repository is a better test of whether an extractor
survives reality, and a worse test of everything else — too many components to hold
in your head, and no way to tell a wrong answer from an unfamiliar one.

It is written in the conventions that have broken extraction before, so it doubles
as a regression test: `.js` extensions on TypeScript imports, default exports,
kebab-case filenames with PascalCase components, an HOC-wrapped default export, and
`*Props` interfaces exported alongside their components.

`.lak.json` points any agent session in this repository at a throwaway graph, so
testing never writes to a real one.

## Branches

`main` is undocumented on purpose — the manual test writes context files into it
and resets afterwards. Branches hold variant starting states.
