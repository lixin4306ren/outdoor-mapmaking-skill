# Outdoor Mapmaking Skill

Codex skill for creating and maintaining outdoor travel maps in an Obsidian/OneDrive notes workflow.

It covers:

- water-system maps with multiple production modes;
- road-trip route maps with selectable basemaps;
- peak check-in maps in DEM terrain and satellite modes;
- mountain terrain/ridge maps.

## Install

Clone or copy this repository into a Codex skills directory, for example:

```sh
git clone https://github.com/lixin4306ren/outdoor-mapmaking-skill.git ~/.codex/skills/outdoor-mapmaking
```

Or copy the repository folder into a workspace-level skill path:

```text
<workspace>/.codex/skills/outdoor-mapmaking/
```

## Important Usage Rule

If a map type has multiple modes or basemap choices, the agent must ask the user to choose before creating, downloading data, or rendering the map.

See `SKILL.md` and the files under `references/`.

## License

No license file is included yet. Add an explicit open-source license before encouraging broad reuse.
