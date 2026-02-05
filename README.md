# works-on-my-machine-badge
A badge that reports the truth from CI.

- Updates a repo-based `badge/status.json` to reflect CI status.
- Repo-only badge with no external services required.
- Optional PR comments plus configurable label, message, and color.

**Copy/paste**
```yaml
- uses: PetriLahdelma/works-on-my-machine-badge@v0
  with:
    state: ${{ job.status }}
```

**Demo**
Record a CI run and show the badge URL updating.

**Trust & safety**
This action commits a status file to your repo using `GITHUB_TOKEN`. Review workflow permissions and the target path.

Star if this saves you time.  
→ Buzz Kit: /buzz-kit

![CI](https://github.com/PetriLahdelma/works-on-my-machine-badge/actions/workflows/ci.yml/badge.svg) ![Release](https://img.shields.io/github/v/release/PetriLahdelma/works-on-my-machine-badge) ![License](https://img.shields.io/github/license/PetriLahdelma/works-on-my-machine-badge) ![Stars](https://img.shields.io/github/stars/PetriLahdelma/works-on-my-machine-badge)

![Hero](assets/hero.png?20260205)

## Quickstart

```yaml
- uses: PetriLahdelma/works-on-my-machine-badge@v0
  with:
    state: ${{ job.status }}
```

## Demo

```text
https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/PetriLahdelma/works-on-my-machine-badge/main/badge/status.json
```

## Why This Exists

Badges should reflect reality. This uses CI to update status.json.

## FAQ

- **Is it repo-only?** Yes, no external services.
- **Does it comment on PRs?** Optional.

## Contributing

See `CONTRIBUTING.md` for local development.

## License

MIT
