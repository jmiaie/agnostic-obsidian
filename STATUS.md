# Status — agnostic-obsidian

**Updated:** 2026-09-30 (PT)  
**Visibility:** public  
**Maturity:** duplicate public mirror / historical name (not the active OMPA remote)  
**Canonical product remote:** [`jmiaie/ompa`](https://github.com/jmiaie/ompa) (PyPI `ompa`, active development — tip refreshed 2026-09-30)

## Honest positioning

This repository is an **older public tree** for the same agent-memory package family (directory still named `ompa/`, `pyproject.toml` name `ompa`). The **GitHub repo name** `agnostic-obsidian` and some release docs still talk about publishing under that historical label.

| Surface | Use |
|---------|-----|
| [`jmiaie/ompa`](https://github.com/jmiaie/ompa) | **Canonical** — continue features, tags, CI, PyPI |
| `jmiaie/agnostic-obsidian` | Historical / portfolio mirror — **do not dual-maintain** |

Companion stack (also not this remote): `locus`, `cognition-os`, `pliamem` (recall router — related, **not** merged into OMPA).

## Offline notes

A full `pip install -e ".[dev]" && pytest` against **this** tip may still run on a machine with deps, but results here are **not** the release gate — use `ompa` for that. This advance does not re-cut a PyPI release from this mirror.

## What is **not** claimed

- That this remote is ahead of `ompa`  
- That RELEASE.md “publish agnostic-obsidian to PyPI” is current process (canonical package is **ompa**)  
- New LongMemEval / R@5 figures beyond historical attributions already in README

## Next (owner)

1. Keep public for portfolio optics **or** archive / mark read-only  
2. Add Topics/description pointing at `ompa` if kept  
3. Avoid new feature commits here — open them on `ompa` instead
