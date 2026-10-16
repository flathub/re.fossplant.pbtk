# `re.fossplant.pbtk`

This repository contains a Flatpak template for building the https://github.com/marin-m/pbtk GUI

## Utilities

These command will generate a `python3-modules.json` file that can serve as a template for the dependencies included from `re.fossplant.pbtk.yaml`:

```bash
cd
git clone git@github.com:flatpak/flatpak-builder-tools.git
git clone git@github.com:flathub/re.fossplant.pbtk.git

cd ~/flatpak-builder-tools/pip
uv add PyYAML
uv sync --all-groups --frozen
source .venv/bin/activate

cd ~/re.fossplant.pbtk
~/flatpak-builder-tools/pip/flatpak-pip-generator --yaml pbtk --checker-data -o python3-modules.yaml
```
