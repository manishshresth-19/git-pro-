# *Conventional Commits*
- Conventional commits is a lightweight specification for writing structured and meaningful commit messages in version control system like Git.
- The Specification was designed to improve the clarity of project histories and enable automation tools to generate changelogs, determine version numbers (eg: using Semantic Versioning) and steamline release process.

## Semantic Versioning (SemVer)
Semantic Versioning is a versioning system used to clearly communicate changes in software releases. 

> Version Format: MAJOR.MINOR.PATCH

Eg: 2.4.1

**1.MAJOR Version**:<br>Increased when you `make breaking changes`. Changes that are not backward compatible.
Eg: 1.0.0 &#8594; 2.0.0

**2.MINOR Version**:<br>
Increased when you `add new features`. Backward compatible changes.
Eg: 1.2.0 &#8594; 1.3.0

**3.PATCH Version**: <br>
Increased when you `make bug fixes`. No breaking changes, no new features.
Eg: 1.2.3 &#8594; 1.2.4

**Basic Format of conventional commits**
> \<type> (optional scope): short description

Eg: feat(auth): add user login validation

## Common Commit Types
1. **feat**: A new feature
    - *feat: add user registration page*
2. **fix**: A bug fix
    - *fix: resolve login validation error*
3. **docs**: Documentation Changes
    - *docs: update README with setup instructions*
4. **Style**: Code style changes (formatting, spacing, no logic changes)
    - *style: format code using prettier*
5. **refactor**: Code changes that neither fix a bug nor add a feature
    - *refactor: optimize database query*
6. **test**: Adding or updating tests
    - *test: add unit tests for auth service*
7. **chore**: Maintenace tasks (dependencies, configs)
    - *chore: update npm dependencies*

## Scope

In Conventional Commits, the scope is an optional part that specifies which part of the project is affected by the change.

*Common Scope Examples*
*auth: Authentication-related changes*<br>
*ui: User interface changes*<br>
*api: Backend or API changes*<br>
*db: Database changes*<br>
*config: Configuration files*<br>
*docs: Documentation section*<br>
*test: Test-related code*<br>

*Examples of Commits with Scope*
- fix(login): resolve password validation issue
- feat(ui): add dark mode toggle
- refactor(api): optimize user endpoint
- docs(readme): update installation steps
- chore(deps): update laravel dependencies.

When to use Scope
1. Lareg projects with multiple modules
2. Team projects
3. Monorepos
4. When you want clearer commit history

> The description and optional footers provide more detail about the commit and highlight important changes like breaking updates.<br>
A description is a short, clear summary of what the commit does; within in present tense; start with a lowercase letter; no period at the end.

Eg: feat(auth): add email verification<br>
    fix(ui): resolve button alignment issue

**Optional Footers**: Footers come after the body and are used for important metadata.

**BREAKING CHANGE footer**: Used when the commit introduces a breaking change.<br
eg: feat(api): Update authentication endpoint<br>
BREAKING CHANGE: The /login API now requires an email instead of a username

**Commit Body (Optional)**: Used when more explanation is needed. 
Eg: feat(auth): add email verification <br>
This change ensures users verify their email before accessing the dashboard. it improves security and prevents fake account creation.

**Full Commit Example**: 
feat(auth): update login validation <br>
Improved password validation logic & error handling.
BREAKING CHANGE: Passwords must now be at least 12 characters long.

> Commit message with `!` to draw attention to breaking change.

Eg: feat!: Send an email to the customer when a product is shipped.


*Why use Conventional commits*
1. Automatically generating CHANGELOGS
2. Automatically determining a sementic version bump (based on types of commits landed)
3. Communicating the nature of changes to teammates, the public, and other stakeholders.
4. Triggering build & publish processes.
5. Making it easier for people to contribute to your projects, by allowing them to explore a more structured commit history.

**Benefits of Conventional Commits**
1. Clean and Readable commit history
2. Improved Team communication
3. Supports Semantic Versioning
4. Better Project Maintenance

