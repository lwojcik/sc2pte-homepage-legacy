---
title: Changelog
---

# Changelog

Only versions released on Twitch are mentioned here. Changes which don't trigger Twitch review process may be omitted.

For more details on current state of the project see the [Kanban board](https://github.com/orgs/lukemnet/projects/1) or source repositories: [Frontend](https://github.com/lukemnet/sc2profile-twitch-extension-frontend), [Backend](https://github.com/lukemnet/sc2profile-twitch-extension-api).

## v1.1.0 (27 Nov 2018)

* **Migrated from [old Mashery API](https://dev.battle.net/) to [new StarCraft II Community APIs](https://develop.battle.net/documentation/api-reference/starcraft-2-community-api)**
* Simplified configuration form: only a profile URL is required (e.g. [https://starcraft2.com/en-us/profile/2/1/5593296](https://starcraft2.com/en-us/profile/2/1/5593296))
* No support for legacy profile URLs (e.g. [http://eu.battle.net/sc2/en/profile/5593296/1/Lukem/](http://eu.battle.net/sc2/en/profile/5593296/1/Lukem/)) any more
* **Draws aren't displayed in the extension.** StarCraft II APIs don't expose this information any more. [I submitted this to Blizzard](https://us.battle.net/forums/en/bnet/topic/20769759674#post-12) and I'll reintroduce the feature if they bring relevant data back
* **Introduced known issue: Stats for archon players aren't displayed.** Instead, they're added up to 2v2 stats, thus rendering this datapoint inaccurate. The bug has to do with APIs labelling archon ladders as '2v2' and [I submitted this to Blizzard](https://us.battle.net/forums/en/bnet/topic/20769759674#post-10). I'll decide what to do depending on their answer
* Portrait frames are now determined correctly based on current solo or team rank, whichever is better
* Portraits should now be displayed correctly

## v1.0.4 (19 Oct 2018)

* Modified configuration form: support for new StarCraft II profile URLs (e.g. [https://starcraft2.com/en-us/profile/2/1/5593296/](https://starcraft2.com/en-us/profile/2/1/5593296/)) while retaining support for legacy URLs (e.g. [http://eu.battle.net/sc2/en/profile/5593296/1/Lukem/](http://eu.battle.net/sc2/en/profile/5593296/1/Lukem/))

## v1.0.3 (11 Oct 2018)

* First public release
* Optimizing Webpack build process while keeping generated code non-obfuscated as per Twitch guidelines

## v0.0.2 (8 Oct 2018)

* Initial version, available only for a testing group
