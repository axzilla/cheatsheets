# Goilerplate Commit & Release Cheatsheet

## Commit Message Format

`<type>`: `<description>`

## Types

- `feat`: New feature or component
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Changes that do not affect the meaning of the code (white-space, formatting, etc)
- `refactor`: Code change that neither fixes a bug nor adds a feature
- `perf`: Code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `chore`: Changes to the build process or auxiliary tools and libraries

## Examples

- `feat: add Button component`
- `fix: correct Card component padding on mobile`
- `refactor: simplify Modal component logic`

## Breaking Changes

Add `!` after the type for breaking changes:

- `feat!: redesign Form component API`

## Versioning Strategy (0.x.y)

- 0: Remains 0 until the first stable version (1.0.0)
- x: For major changes or feature sets (e.g., 20)
- y: For minor changes, bugfixes, and incremental updates

## Version Increments

- Increase second number (x) for:
  - New major features
  - Significant API or functionality changes
- Increase third number (y) for:
  - Bugfixes
  - Small feature additions
  - Documentation changes
  - Performance optimizations
  - Other minor changes

## Release Process

1. Commit changes:

   ```
   git add .
   git commit -m "feat: implement XYZ feature"
   ```

2. Tag and push version:

   ```
   git tag -a v0.20.2 -m "Release v0.20.2"
   git push origin main --tags
   ```

3. Create GitHub Release:
   - Go to GitHub > Releases > "Draft a new release"
   - Select the created tag
   - Title: "Release v0.20.2"
   - Description: Brief summary of main changes
   - Publish the release

## Go Module Usage

- Install latest version:
  ```
  go get github.com/axzilla/goilerplate@latest
  ```
- Install specific version:
  ```
  go get github.com/axzilla/goilerplate@v0.20.2
  ```
- Install development version:
  ```
  go get github.com/axzilla/goilerplate@main
  ```

Remind users to run `go mod tidy` after changes.

## Transition to 1.0.0

Switch to 1.0.0 when the project:

- Has a stable API
- Is sufficiently tested
- Is ready for production environments
- Offers a solid feature base
