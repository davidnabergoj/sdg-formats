# Social deduction game (SDG) file format

A social deduction game (SDG) file is a JSON file suited for describing a social deduction game.
This document describes key elements of a SDG file with examples for easier interpretation.
This is valid for SDG version 1.0.

## Key concepts

- system event: an action executed by the system
- player event: a message sent by the player or an action executed by the player
- environment: sequence of player and system events
- game: a sequence of environments

System and player events inherit from a parent `event` object.

## Syntax

Each game file is a JSON file with the following fields:

- `metadata: list[object]`
- `game: list[object]`- list of `environment` objects

### Metadata

The `metadata` object contains the following fields:

- `version: str` - SDG file version
- `players: list[object]` - player data for each player

Each entry of `players` contains the following fields:

- `id: int` - all players have a unique ID.
- `name: str` - all players have a unique name.
- `role_id: int` - all players have a role ID.

### Game

Each `game` entry contains an `environment` object with the following fields:

- `id: int` - unique integer ID for the environment
- `instance_id: int` - unique integer ID for this instance of the environment; each environment type can have several
  unique instances
- `start_time: float` - time in seconds since the start of the game when this environment appeared
- `events: list` - list of events in this environment

Each `events` entry contains an `event` object with the following fields:

- `type: str` - "system" or "player"
- `time: float` - time in seconds since the environment start time
- `data: object`

## Examples