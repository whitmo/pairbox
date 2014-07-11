# pairbox

A charm for spinning up a docker container for shared programming.

## Container criteria

 - must expose an ssh port
 - should expect the env vars for USERIDS_SSH as a list of variables
   compatible for feeding to `ssh-import-id` to set up pub keys ala:
   `gh:whitmo lp:bcsaller lp:johnsca`.

Inheritting from the basic pairbox container should take care of these
requirements.

## Usage

```
juju deploy lp:pairbox
juju set pub-keys="gh:whitmo" container-url=http://mybox.url
```
