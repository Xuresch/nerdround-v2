# Welcome to Remix!

- 📖 [Remix docs](https://remix.run/docs)

## Development

Run the dev server:

```shellscript
npm run dev
```

## Deployment

First, build your app for production:

```sh
npm run build
```

Then run the app in production mode:

```sh
npm start
```

Now you'll need to pick a host to deploy it to.

### DIY

If you're familiar with deploying Node applications, the built-in Remix app server is production-ready.

Make sure to deploy the output of `npm run build`

- `build/server`
- `build/client`

## Styling

This template comes with [Tailwind CSS](https://tailwindcss.com/) already configured for a simple default starting experience. You can use whatever css framework you prefer. See the [Vite docs on css](https://vitejs.dev/guide/features.html#css) for more information.

# Branching

This will help ensure better structure when creating new branches.

## Legend

| Instance | Branch   | Description                                                                 |
| -------- | -------- | --------------------------------------------------------------------------- |
| Stable   | `stable` | Accepts merges from Working and Hotfix branches                             |
| Working  | `main`   | Accepts merges from Features and Bugfix branches                            |
| Features | `feature/*` | Always branch off HEAD of Working (`main`)                               |
| Bugs     | `bugfix/*`  | Always branch off HEAD of Working (`main`), use ticket number             |
| Hotfix   | `hotfix/*`  | Always branch off HEAD of Stable (`stable`), use ticket number            |

## Main Branches

The main repository will always hold two branches:

- `main`
- `stable`

## Supporting Branches

The different types of branches we may use are:

- Feature branches
- Bugfix branches
- Hotfix branches

### Feature branches

Feature branches are used when developing a new feature.

**Naming conventions:** `feature/name-of-feature`

Feature branches should only be merged into the Working (`main`) branch.

### Bugfix branches

Bugfix branches are used when addressing specific bugs.

**Naming conventions:** `bugfix/ticket-number`

Bugfix branches should only be merged into the Working (`main`) branch after resolving the issue.

### Hotfix branches

Hotfix branches are used for critical fixes that need to be applied to the Stable (`stable`) branch immediately.

**Naming conventions:** `hotfix/ticket-number`

Hotfix branches are merged directly into the Stable (`stable`) branch and may also be merged back into the Working (`main`) branch to ensure consistency.

---

# Commit Message Convention

This will help ensure better structure when creating commit messages.

## Commit Formats

### Default

```plaintext
<type>(<optional scope>): <subject>

<optional body>

<optional footer>
```

### Types

- **API relevant changes:**
    - `feat`: Commits that add a new feature.
    - `fix`: Commits that fix a bug.
- **Code structure changes:**
    - `refactor`: Commits that restructure your code without changing its behavior.
    - `perf`: Commits that improve performance (a special type of `refactor`).
- **Non-functional changes:**
    - `style`: Commits that do not affect meaning (e.g., white-space, formatting).
    - `test`: Commits that add missing tests or correct existing tests.
    - `docs`: Commits that affect documentation only.
- **Build system or external dependencies:**
    - `build`: Commits that affect build components such as build tools, CI pipelines, or dependencies.
- **Operations-related changes:**
    - `ops`: Commits that affect operational components such as infrastructure, deployment, backup, or recovery.
- **Miscellaneous changes:**
    - `chore`: Miscellaneous commits (e.g., modifying `.gitignore`).

### Scopes

The `scope` provides additional context about the part of the project affected.
- It is **optional**.
- Allowed scopes depend on the specific project.
- Do not use issue identifiers as scopes.
- Examples of scopes:
    - `api`
    - `ui`
    - `database`

### Subject

The `subject` contains a concise description of the change.
- **Mandatory**.
- Use the imperative, present tense: "change" not "changed" or "changes".
  - Example: "This commit will add X functionality."
- Do not capitalize the first letter.
- Do not add a period (.) at the end.

### Body

The `body` should include the motivation for the change and contrast this with the previous behavior.
- **Optional**.
- Use the imperative, present tense: "change" not "changed" or "changes".
- Provide reasoning behind the change and its effect.
- Mention issue identifiers and their relations here, if applicable.
- Examples:
    - "This resolves an issue with improper validation."
    - "Improved performance by optimizing the database query."

### Footer

The `footer` should contain information about **Breaking Changes** and references to related issues.
- **Optional**.
- You can reference issues by their ID.
- **Breaking Changes** should start with `BREAKING CHANGES:` followed by a space or two newlines.
- Example:
    - `BREAKING CHANGES: ticket endpoints no longer support listing all entities.`
    - `refers to TICKET-1337`

### Examples
* ```
  feat(shopping cart): add the amazing button
  ```
* ```
  feat: remove ticket list endpoint
  
  refers to TICKET-1337
  BREAKING CHANGES: ticket endpoints no longer support listing all entities.
  ```
* ```
  fix: add missing parameter to service call

  The error occurred because of incorrect input format.
  ```
* ```
  build(release): bump version to 1.0.0
  ```
* ```
  refactor: implement calculation method as recursion
  ```
* ```
  style: remove empty line
  ```