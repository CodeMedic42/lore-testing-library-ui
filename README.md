# @acme/ui-kit

A small React component library. Nine components in a four-level composition
chain:

```
DateRangeSelector → DateSelector → TextField → FieldLabel
                                 ↘            ↘ HelperText
                                   Calendar   → CalendarDay
```

`Card` and `Button` compose nothing and stand on their own.

## Stack

TypeScript, SCSS, Rollup. Tested with Vitest and Testing Library; linted with
ESLint, Stylelint and Prettier.

```bash
npm run build     # rollup -c
npm test          # vitest run
npm run lint      # eslint src && stylelint 'src/**/*.scss'
```

Published as `@acme/ui-kit`, with `react` as a peer dependency. `classnames` and
`date-fns` are the only runtime dependencies.

## Conventions

- one component per file, default export, plus a named export from `src/index.ts`
- kebab-case filenames, PascalCase component names
- `.js` extensions on relative imports, per TypeScript's ESM resolution
- `*Props` interfaces exported alongside their components
- styles in `src/styles/`, tokens in `_tokens.scss`
