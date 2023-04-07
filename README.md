# Git Conventions

In this document, I will explain some common git conventions for code organization and management.

## Branches

- **Main (master)**: The main branch with production code.
- **Staging**: A branch to test and review code before merging.
- **Develop**: A long-lived branch to integrate different feature and bugfix branches.
- **Feature**: Short-lived branches for specific features or functionalities.
- **Bugfix**: Similar to feature branches, but for bug fixes or issues.
- **Hotfix**: Urgent branches for critical bug fixes or issues in production.
- **Release**: A long-lived branch to prepare a new version of the software for release.
- **Experimental**: Branches to try out new ideas or technologies.
- **WIP (work in progress)**: Branches to save your work temporarily.

## Branch Name

`<author>/<branch-type>/<branch-name>`

where:

- `<author>` is your username or initials
- `<branch-type>` is one of the branch types mentioned above (e.g., `feature`, `bug-fix`, `hot-fix`, `release`, `experimental`, `wip`)
- `<branch-name>` is a short and descriptive name for the branch (e.g., `login-form`, `fix-typo`, `update-readme`)

e.g: `alice/feature/login-form`

## Commit Message

`<type>(<scope>): <subject>`

where:

- `<type>` is one of these categories:
  - `feat`: A new feature
  - `fix`: A bug fix
  - `docs`: Documentation changes
  - `style`: Code formatting changes
  - `refactor`: Code restructuring changes
  - `test`: Test changes
  - `chore`: Other maintenance changes
- `<scope>` is an optional identifier that specifies what part of the codebase is affected by the change (e.g., `login`, `navbar`, `utils`)
- `<subject>` is a concise and imperative summary of the change in present tense (e.g., `add login form`, `fix typo in readme`, `update dependencies`)
  - Use imperative, present tense (eg: use "add" instead of "added" or "adds")
  - Don't use dot(.) at end
  - Don't capitalize first letter

e.g: `fix(docs): fix typo in readme`

### Notes

  - `<type>` is lowercase
  - `<subject>` must immediately follow the colon and space after the type/scope prefix

## Workflow

1. Fetch all branch
```bash
git fetch –all
```

2. Checkout into develop branch
```bash
git checkout develop
```

3. Update Branches
```bash
git pull origin develop
```

4. Make new `feature`, `bug fix`, `hot fix` and … branch from develop
```bash
git checkout -b 'amirhossein/feature/new-time-zone'
```

5. Implement feature and make commit
```bash
git commit -m 'feat(time-zone): add time zone config'
git commit -m 'fix(time-zone): change time zone config'
```

6. Push to github/gitlab/... repository
```bash
git push origin amirhossein/feature/new-time-zone
```
