# works-on-my-machine-badge

A GitHub Action that updates a repo-based badge JSON to reflect real CI status.

Tagline: Ship the truth. A badge that matches the build.

## Quickstart
Add this action after your tests:
```yaml
- name: Update badge
  uses: PetriLahdelma/works-on-my-machine-badge@v0
  with:
    state: ${{ job.status }}
    status-file: badge/status.json
    comment-on-pr: true
```

## Demo
The action writes a JSON file for shields.io dynamic badges.

## Screenshots
Placeholder: add screenshots in `docs/` and link them here.

## Badge JSON
`badge/status.json` looks like:
```json
{
  "schemaVersion": 1,
  "label": "works on my machine",
  "message": "apparently",
  "color": "green",
  "state": "pass",
  "updated": "2026-02-04T00:00:00.000Z"
}
```

## Shields.io dynamic JSON badge
Use a dynamic JSON badge pointing at the raw file:
```text
https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/PetriLahdelma/works-on-my-machine-badge/main/badge/status.json
```

## Inputs
- `state` accepts `success`, `failure`, or `neutral`
- `status-file` path to JSON file
- `label`, `message`, `color`
- `comment-on-pr` (`true` or `false`)
- `github-token` (optional)

## Humorous variants
See `docs/variants.md` for ready-to-use message presets.

## Manual publish steps (optional)
```bash
npm login
npm publish --access public
```
If the name is taken, consider scoped naming like `@petri-lahdelma/works-on-my-machine-badge`.

## License
MIT
