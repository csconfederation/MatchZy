# CSC MatchZy fork

This is [Counter Strike Confederation's](https://github.com/csconfederation) fork of
[upstream MatchZy](https://github.com/shobhit-pathak/MatchZy). CSC maintains the changes below
for its servers; they may not be present in upstream releases. `dev` is the working branch and
`main` is the release branch.

## CSC changes

- Builds against the official CounterStrikeSharp API `1.0.375` release on .NET 10.
- Records demos using an absolute path under `csgo/`, avoiding Metamod's relative write path.
- Fixes `removeplayer` for team2, spectators, and duplicate Steam IDs; player-list arrays hold Steam IDs.
- Adds optional scoreboard clan tags from [upstream PR #407](https://github.com/shobhit-pathak/MatchZy/pull/407).

To show `[Ready]` and `[Unready]` during warmup, set `matchzy_clan_tags_enabled true` in
`cfg/MatchZy/config.cfg`. It is off by default. Leave `team1.tag` and `team2.tag` out of the match
JSON, or set them to `""`, to leave clan tags blank during live play. The MatchZy integration still
needs a live match test before enabling it on CSC servers.

The original MatchZy README follows.

---

MatchZy - Match Plugin for CS2!
==============

MatchZy is a plugin for CS2 (Counter Strike 2) for running and managing practice/pugs/scrims/matches with easy configuration!

[![Discord](https://discordapp.com/api/guilds/1169549878490304574/widget.png?style=banner2)](https://discord.gg/2zvhy9m7qg)

## Feature Highlights:

* Pug mode with simple commands to manage!
* Support of [Get5 Panel!](https://shobhit-pathak.github.io/MatchZy/get5/)
* Support BO1/BO3/BO5 and Veto when using Match configuration or Get5 Panel!
* [Setting up matches](https://shobhit-pathak.github.io/MatchZy/match_setup/) and locking players into their team
* Practice Mode with `.bot`, `.spawn`, `.ctspawn`, `.tspawn`, `.nobots`, `.rethrow`, `.last`, `.timer`, `.clear`, `.exitprac` and many more commands!
* Knife round (With expected logic, i.e., team with most players win. If same number of players, then team with HP advantage wins. If same HP, winner is decided randomly)
* Automatically starts demo recording and stop recording when match is ended (Make sure you have tv_enable 1)
* Automatically uploads demo on map end on the given URL.
* Players whitelisting (Thanks to [DEAFPS](https://github.com/DEAFPS)!)
* Coaching system
* Damage report after every round
* Support for round restore (Currently using the vanilla valve's backup system)
* Ability to create admin and allowing them access to admin commands
* Database Stats and CSV Stats! MatchZy stores data and stats of all the matches in a local SQLite database (MySQL Database is also supported!) and also creates a CSV file for detailed stats of every player in that match!
* Provides easy configuration
* And much more!!


## Documentation

## [shobhit-pathak.github.io/MatchZy/](https://shobhit-pathak.github.io/MatchZy/)

## Donation

Buy Me A Coffee:

[!["Buy Me A Coffee"](https://cdn.buymeacoffee.com/buttons/default-blue.png)](https://www.buymeacoffee.com/shobhitwd)

Steam Tradelink: 

https://steamcommunity.com/tradeoffer/new/?partner=194101533&token=1TI76S3p

## Want CS2 Server with MatchZy?

Buy it from DatHost (MatchZy can be installed directly on DatHost servers by using their 1-click installer from mods and plugins section!):
https://dathost.net/r/matchzy 

## License
MIT

## Credits and thanks!
* [Get5](https://github.com/splewis/get5) - A lot of functionalities and workings have been referred from Get5 and they did an amazing job for managing matches in CS:GO. Huge thanks to them!
* [G5V](https://github.com/PhlexPlexico/G5V) and [G5API](https://github.com/PhlexPlexico/G5API) - Amazing work with the web panel for managing the servers!
* [eBot](https://github.com/deStrO/eBot-CSGO) - Amazing job in CS:GO and then provided this great panel again in CS2 which is helping a lot of organizers now. Some logics have been referred from eBot as well!
* [CounterStrikeSharp](https://github.com/roflmuffin/CounterStrikeSharp/) - Amazing job with development of CSSharp which gave us a platform to build our own plugins and also sparked my interest in plugin development!
* [AlliedModders and community](https://alliedmods.net/) - They are the reason this whole plugin was possible! They are very helpful and inspire a lot!
* [LOTGaming](https://lotgaming.xyz/) - Helped me a lot with initial testing and provided servers on different systems and locations!
* [CHR15cs](https://github.com/CHR15cs) - Helped me a lot with the practice mode!
* [K4ryuu](https://github.com/K4ryuu) - Awesome job on damage report!
* [DEAFPS](https://github.com/DEAFPS) - Great contribution for Practice mode!
