# Goilerplate Commit & Release Cheatsheet
## Commit Message Format
`<type>`: `<description>`

## Main Types
- `feat`: New features, components, or intentional changes (including UI/design changes)
- `fix`: Bug fixes or corrections
- `refactor`: Code restructuring (including code formatting) that doesn't change behavior
- `docs`: Documentation changes only

Use the most impactful type if multiple apply (feat > fix > refactor > docs)

## Examples
- `feat: add Button component`
- `feat: update Card design`
- `fix: correct layout on mobile`
- `refactor: simplify component logic and update docs`
- `docs: improve API documentation`

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
