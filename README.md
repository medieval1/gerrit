gerrit
======

gerrit hooks

patchset-created:
  This hook watches for patch set create events and then posts details to hipchat.

change-merged:
  This hook watches for patch set merges and then posts details to hipchat

Setup
=====
In the GERRIT_SITE directory there contains a hooks directory. Place the gerrit hooks into this directory.

The config file (hipchat-hook.cfg) goes to GERRIT_SITE/etc

Edit the config file to add your HipChat API Token and then configure the project/room associations.

Next, configure gerrit to use the hooks. Edit GERRIT_SITE/etc/gerrit.config and add the [hooks] section:

```
  [hooks]
        patchsetCreatedHook = patchset-created
```

Restart gerrit and you're good to go!