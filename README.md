# Ansible role for the RFID Jukebox

Installs and configures the [RFID Jukebox](https://github.com/scheleaap/rfid-jukebox).

## Requirements

<!-- Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required. -->


## Role Variables

<!-- A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well. -->

### `rfid_jukebox_albums`

A mapping from RFID tag ids to Mopidy URLs.
Example:
```yaml
rfid_jukebox_albums:
  "042abc4a325e81": "spotify:album:2WT1pbYjLJciAR26yMebkH"  # The Dark Side Of The Moon
  "0426bc4a325e81": "spotify:album:02Ast9sM8awNiA2ViVjO4Q"  # Nightfall in Middle Earth
  "042ebc4a325e81": "spotify:album:1YaUAkNsLKXtJfb0FVZcyu"  # New York - Addis - London
```

### `rfid_jukebox_commands`

A mapping from RFID tags to commands. Currently, the only supported command is `stop`.
Example:
```yaml
rfid_jukebox_commands:
  "ebd1a421": "stop"  # Big chipcard
```


## Dependencies

None


## Example Playbook

See included `playbook.yml`.
