# Social deduction game data formats

This repository describes file formats for storing social deduction game data.
It describes a social deduction metadata format (SDM), which is specific to a particular social deduction game.
It also describes a general social deduction game format (SDG), which contains information about an instance of a social deduction game.
Check the SDG file descriptions in [`sdg_formats`](sdg_formats) and metadata formats in [`sdm_formats`](sdm_formats).
Check examples in [`examples`](examples).

The purpose of SDM and SDG file formats is to encourage data analysis in social deduction games, for example by making interesting post-game data visualizations.
All contributions are very warmly welcome! Feel free to open issues and submit pull requests :)

Some cool ideas:
- add SDG examples for your favourite social deduction games
- create some example visualizations of SDG files
- read through the SDG file format description and check that it contains all key data fields
- create a program that automatically creates SDG files (for example, by parsing video recordings)