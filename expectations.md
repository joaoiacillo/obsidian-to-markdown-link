# Expectations File

This file provides some expectations towards the functioning of this CLI.

## Basic Usage

```bash
$ cd OBSIDIAN_VAULT_PATH
$ python3 -m obs_to_md convert .
```

### Obsidian Files

```md
// note1.md

This note refers to [[note2]]

// note2.md

This note refers to [[note1]].
```

### Generated files

```md
// note1.md

This note refers to [note2](./note2.md)

// note2.md

This note refers to [not1](./note1.md)
```

## Aliases

```md
This note refers to [[note2|An awesome note]]
```

Turns into:

```md
This note refers to [An awesome note](./note2.md)
```
