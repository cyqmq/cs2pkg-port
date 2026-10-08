# 源仓库清单(SOURCES)

> 本文档记录 cs2pkg-port 移植的插件与其**真实上游源仓库**的对应关系,
> 供后续更新/重新打包时定位源码与 Release 资产。
> 注意:**部分插件可能未适配当前 CS2 版本**,移植前需甄别(见状态列)。
> 最后更新:2026-10-09

## 状态说明

| 状态 | 含义 |
| --- | --- |
| `framework` | 核心框架(非插件包),cs2lm 不管理 |
| `ported` | 已在本仓库打包为 `.cs2pkg` |
| `packageable` | 源仓库存在且有 zip Release 资产,可移植打包 |
| `no_assets` | 源仓库存在但最新 Release 没有 zip 资产(或只有源码) |
| `archived` | 源仓库已被归档(停止维护) |
| `not_found` | 仓库不存在/已改名/无法访问,需人工确认 |

> 状态基于 `gh api` 实况核查(最后核查:2026-10-09)。

## 插件与源仓库

| 插件 | 源仓库 | 框架 | 状态 | 备注 |
| --- | --- | --- | --- | --- |
| Metamod:Source | [alliedmodders/metamod-source](https://github.com/alliedmodders/metamod-source) | ? | `framework` | 需人工核查 |
| CounterStrikeSharp | [roflmuffin/CounterStrikeSharp](https://github.com/roflmuffin/CounterStrikeSharp) | ? | `framework` | 需人工核查 |
| MatchZy | [shobhit-pathak/MatchZy](https://github.com/shobhit-pathak/MatchZy) | CounterStrikeSharp | `ported` | MatchZy is a plugin for CS2 (Counter Strike 2) for running and managing practice; ★504; 更新于 2026-10-03; 最新 0.9.1; 发布于 2026-10-03; 最近推送 2026-10-03 |
| CS2-SimpleAdmin | [daffyyyy/CS2-SimpleAdmin](https://github.com/daffyyyy/CS2-SimpleAdmin) | CounterStrikeSharp | `ported` | Manage your Counter-Strike 2 server with simple commands!; ★189; 更新于 2026-10-02 |
| cs2-retakes | [B3none/cs2-retakes](https://github.com/B3none/cs2-retakes) | CounterStrikeSharp | `ported` | CS2 implementation of retakes written in C# for CounterStrikeSharp. Based on the |
| CS2Fixes | [Source2ZE/CS2Fixes](https://github.com/Source2ZE/CS2Fixes) | Metamod | `ported` | A plugin with tons of fixes and features aimed but not limited to zombie escape.; ★363; 更新于 2026-09-30; 最新 v2.0; 发布于 2026-09-30; 最近推送 2026-09-30 |
| cs2kz-metamod | [KZGlobalTeam/cs2kz-metamod](https://github.com/KZGlobalTeam/cs2kz-metamod) | Metamod | `ported` | KZ plugin for cs2. WIP, not ready for release.; ★206; 更新于 2026-10-05; 最新 v0.0.182; 发布于 2026-10-05; 最近推送 2026-10-08 |
| CS2Surf/Timer | [CS2Surf/Timer](https://github.com/CS2Surf/Timer) | ? | `no_assets` | 最近推送 2026-09-28 |
| Jailbreak | [edgegamers/Jailbreak](https://github.com/edgegamers/Jailbreak) | ? | `packageable` | 最新 4.7.0; 发布于 2026-10-02; 最近推送 2026-10-02 |
| cs2-store | [schwarper/cs2-store](https://github.com/schwarper/cs2-store) | CounterStrikeSharp | `packageable` | A store plugin designed to enhance your gameplay by providing a dynamic credit s; ★14; 更新于 2026-07-19; 最新 v33; 发布于 2026-07-19; 最近推送 2026-07-19 |
| CS2-Retake-Suite | [NeuTroNBZh/CS2-Retake-Suite](https://github.com/NeuTroNBZh/CS2-Retake-Suite) | ? | `no_assets` | 最近推送 2026-10-02 |
| MEngZy | [MEngYangX/MEngZy](https://github.com/MEngYangX/MEngZy) | ? | `archived` | 已归档; 最新 0.0.2; 发布于 2025-04-02; 最近推送 2025-04-03 |
| CS2-InfoTop-COFYYE | [cofyye/CS2-InfoTop-COFYYE](https://github.com/cofyye/CS2-InfoTop-COFYYE) | ? | `packageable` | 最新 1.3; 发布于 2025-12-03; 最近推送 2025-12-03 |
| CS2-FullTeamFix | [ShookEagle/CS2-FullTeamFix](https://github.com/ShookEagle/CS2-FullTeamFix) | ? | `packageable` | 最新 v1.0.0; 发布于 2024-06-10; 最近推送 2024-06-10 |
| CS2-HideAndSeekPlugin | [ShookEagle/CS2-HideAndSeekPlugin](https://github.com/ShookEagle/CS2-HideAndSeekPlugin) | ? | `packageable` | 最新 1.1.0; 发布于 2024-06-11; 最近推送 2024-06-11 |
| CS2-AntiDLL | [KillStr3aK/CS2-AntiDLL](https://github.com/KillStr3aK/CS2-AntiDLL) | CounterStrikeSharp | `packageable` | This plugin is similar to the CS:GO version.; ★19; 更新于 2025-04-03; 最新 1.0.4; 发布于 2025-04-03; 最近推送 2025-04-03 |
| CS2-BotAI | [Austinbots/CS2-BotAI](https://github.com/Austinbots/CS2-BotAI) | CounterStrikeSharp | `packageable` | Improves the built in bots AI.; ★16; 更新于 2025-09-08; 最新 V1.3; 发布于 2025-09-08; 最近推送 2025-09-08 |
| cs2-quake-sounds | [Kandru/cs2-quake-sounds](https://github.com/Kandru/cs2-quake-sounds) | CounterStrikeSharp | `packageable` | This is a simple Quake Sound plugin for your server. It supports all types of so; ★19; 更新于 2026-08-11; 最新 26.08.1; 发布于 2026-08-11; 最近推送 2026-08-11 |
| CS2-Playervotes | [asapverneri/CS2-Playervotes](https://github.com/asapverneri/CS2-Playervotes) | CounterStrikeSharp | `no_assets` | Lightweight and efficient voting system for CS2 without anything pointless, allo; ★16; 更新于 2025-12-03; 最新 v2.5; 发布于 2025-12-03; 最近推送 2025-12-03 |
| K4-Systems | [K4ryuu/K4-Systems](https://github.com/K4ryuu/K4-Systems) | ? | `not_found` | 需人工核查 |
| WeaponRestrict | [CS2Plugins/WeaponRestrict](https://github.com/CS2Plugins/WeaponRestrict) | ? | `no_assets` | 最新 2.1; 发布于 2026-01-28; 最近推送 2026-01-28 |
| CS2-Practice-Plugin | [CHR15cs/CS2-Practice-Plugin](https://github.com/CHR15cs/CS2-Practice-Plugin) | ? | `packageable` | 最新 v1.0.0.3; 发布于 2024-04-27; 最近推送 2025-02-01 |
| cs2-WeaponPaints | [Nereziel/cs2-WeaponPaints](https://github.com/Nereziel/cs2-WeaponPaints) | CounterStrikeSharp | `ported` | A plugin to change weapon paints, gloves, agents and etc.; ★415; 更新于 2026-10-04; 最新 build-466; 发布于 2026-10-04; 最近推送 2026-10-04 |
| SharpTimer | [SharpTimer/SharpTimer](https://github.com/SharpTimer/SharpTimer) | ? | `not_found` | 需人工核查 |
| 1v1Slay | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| AdminList | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| Ads | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| AntiCapsLock | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| AntiTeamFlash | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| BhopDoorFix | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| BringGoto | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| Cekilis | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| ChatCleaner | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| Cit | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| CommandMaker | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| CTBan | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| CTKit | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| CTKov | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| CTPerk | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| CTRev | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `ported` | 需人工核查 |
| cs2-Fix-Multi-1v1 | [oqyh/cs2-Plugins-For-Community](https://github.com/oqyh/cs2-Plugins-For-Community) | ? | `packageable` | 最新 Give-Weapons-1.0.0; 发布于 2024-04-04; 最近推送 2025-06-04 |
| cs2-Give-Healthshot-GoldKingZ | [oqyh/cs2-Plugins-For-Community](https://github.com/oqyh/cs2-Plugins-For-Community) | ? | `packageable` | 最新 Give-Weapons-1.0.0; 发布于 2024-04-04; 最近推送 2025-06-04 |
| cs2-Give-Taser | [oqyh/cs2-Plugins-For-Community](https://github.com/oqyh/cs2-Plugins-For-Community) | ? | `ported` | 最新 Give-Weapons-1.0.0; 发布于 2024-04-04; 最近推送 2025-06-04 |
| cs2-Give-Weapons | [oqyh/cs2-Plugins-For-Community](https://github.com/oqyh/cs2-Plugins-For-Community) | ? | `ported` | 最新 Give-Weapons-1.0.0; 发布于 2024-04-04; 最近推送 2025-06-04 |
| cs2-Restart-Round-Player-GoldKingZ | [oqyh/cs2-Plugins-For-Community](https://github.com/oqyh/cs2-Plugins-For-Community) | ? | `packageable` | 最新 Give-Weapons-1.0.0; 发布于 2024-04-04; 最近推送 2025-06-04 |
| Retakes-Zones | [oscar-wos/Retakes-Zones](https://github.com/oscar-wos/Retakes-Zones) | ? | `packageable` | 最新 1.2.1; 发布于 2026-05-04; 最近推送 2026-05-04 |
| cs2-jailbreak | [exkludera-cssharp/cs2-jailbreak](https://github.com/exkludera-cssharp/cs2-jailbreak) | ? | `archived` | 已归档; 最新 0.5.1; 发布于 2025-01-30; 最近推送 2025-02-12 |
| cs2surf-metamod | [rcnoob/cs2surf-metamod](https://github.com/rcnoob/cs2surf-metamod) | ? | `ported` | 最新 v0.0.29; 发布于 2026-09-28; 最近推送 2026-09-28 |
| CS2-KZ (Base) | [CS2-KZ/CS2-KZ](https://github.com/CS2-KZ/CS2-KZ) | ? | `not_found` | 需人工核查 |
| SharpTimer (girlglock) | [girlglock/SharpTimer](https://github.com/girlglock/SharpTimer) | ? | `archived` | 已归档; 最新 v0.2.6; 发布于 2024-05-19; 最近推送 2024-06-14 |
| CS2-Deathmatch | [NockyCZ/CS2-Deathmatch](https://github.com/NockyCZ/CS2-Deathmatch) | CounterStrikeSharp | `packageable` | A plugin to implement deathmatch gamemode.; ★133; 更新于 2026-10-02; 最新 v1.3.5; 发布于 2026-10-02; 最近推送 2026-10-02 |
| AIO-1v1-Plugin-CS2 | [j4asper/AIO-1v1-Plugin-CS2](https://github.com/j4asper/AIO-1v1-Plugin-CS2) | ? | `no_assets` | 最近推送 2024-08-19 |
| CS2-Multi-1v1 | [rockCityMath/CS2-Multi-1v1](https://github.com/rockCityMath/CS2-Multi-1v1) | ? | `no_assets` | 最近推送 2024-07-20 |
| CS2JumpStatistics | [anthev-stack/CS2JumpStatistics](https://github.com/anthev-stack/CS2JumpStatistics) | ? | `no_assets` | 最新 jumpstats; 发布于 2025-09-22; 最近推送 2025-09-22 |
| cs2-gungame | [ssypchenko/cs2-gungame](https://github.com/ssypchenko/cs2-gungame) | CounterStrikeSharp | `ported` | GunGame is a gameplay plugin inspired by the SourceMode GunGame plugin.; ★30; 更新于 2026-09-26; 最新 v1.2.4; 发布于 2026-07-11; 最近推送 2026-09-26 |
| HNS-Freeze | [lhunter3/HNS-Freeze](https://github.com/lhunter3/HNS-Freeze) | ? | `packageable` | 最新 v.0.0.4; 发布于 2024-01-12; 最近推送 2025-01-25 |
| ZombieSharp | [oylsister/ZombieSharp](https://github.com/oylsister/ZombieSharp) | ? | `archived` | 已归档; 最新 stable-2.2.0; 发布于 2025-02-06; 最近推送 2025-11-08 |
| PropHunt | [devinjc213/PropHunt](https://github.com/devinjc213/PropHunt) | ? | `no_assets` | 最近推送 2024-07-08 |
| CS2-Duels | [TomiksOfficial/-CS2-Duels](https://github.com/TomiksOfficial/-CS2-Duels) | ? | `no_assets` | 最新 v0.1.1; 发布于 2024-01-04; 最近推送 2024-01-04 |
| cs2-Knife-Round-GoldKingZ | [oqyh/cs2-Knife-Round-GoldKingZ](https://github.com/oqyh/cs2-Knife-Round-GoldKingZ) | ? | `ported` | 最新 1.1.5; 发布于 2025-03-14; 最近推送 2025-03-14 |
| cs2-native-mapvote | [Kandru/cs2-native-mapvote](https://github.com/Kandru/cs2-native-mapvote) | ? | `packageable` | 最新 26.05.1; 发布于 2026-05-30; 最近推送 2026-05-30 |
| GG1MapChooser | [ssypchenko/GG1MapChooser](https://github.com/ssypchenko/GG1MapChooser) | ? | `ported` | 最新 1.8.1; 发布于 2026-10-04; 最近推送 2026-10-04 |
| umbrella-multimod-interface-cs2 | [Ayrton09/umbrella-multimod-interface-cs2](https://github.com/Ayrton09/umbrella-multimod-interface-cs2) | ? | `packageable` | 最新 v1.0.3; 发布于 2026-09-28; 最近推送 2026-09-28 |
| cs2-scuffed-anticheat | [exkludera-cssharp/cs2-scuffed-anticheat](https://github.com/exkludera-cssharp/cs2-scuffed-anticheat) | ? | `archived` | 已归档; 最近推送 2024-08-24 |
| CS2FOW | [karola3vax/CS2FOW](https://github.com/karola3vax/CS2FOW) | ? | `archived` | 已归档; 最新 v0.3.6; 发布于 2026-08-04; 最近推送 2026-10-06 |
| CallAdminSystem-CS2 | [wiruwiru/CallAdminSystem-CS2](https://github.com/wiruwiru/CallAdminSystem-CS2) | ? | `packageable` | 最新 v2.1.3; 发布于 2026-07-04; 最近推送 2026-07-29 |
| CS2-CallAdmin | [1Mack/CS2-CallAdmin](https://github.com/1Mack/CS2-CallAdmin) | ? | `packageable` | 最新 V1.1.3; 发布于 2024-06-11; 最近推送 2024-06-11 |
| discord-relay-report | [imp87/discord-relay-report](https://github.com/imp87/discord-relay-report) | ? | `packageable` | 最新 v1.0.4; 发布于 2024-08-31; 最近推送 2024-08-31 |
| simplediscordrelay | [Tsukasa-Nefren/simplediscordrelay](https://github.com/Tsukasa-Nefren/simplediscordrelay) | ? | `ported` | 最新 v1.1; 发布于 2026-06-05; 最近推送 2026-06-05 |
| CS2-Discord-Utilities | [NockyCZ/CS2-Discord-Utilities](https://github.com/NockyCZ/CS2-Discord-Utilities) | ? | `packageable` | 最新 v2.1.0; 发布于 2024-10-09; 最近推送 2026-07-18 |
| CS2-ChatRelay | [asapverneri/CS2-ChatRelay](https://github.com/asapverneri/CS2-ChatRelay) | CounterStrikeSharp | `no_assets` | Lightweight plugin to send your cs2 server chat messages to discord channel usin; ★6; 更新于 2025-05-25; 最新 v1.2; 发布于 2025-05-25; 最近推送 2025-05-25 |
| cs2-challenges | [Kandru/cs2-challenges](https://github.com/Kandru/cs2-challenges) | CounterStrikeSharp | `packageable` | This plugin allows you to create Challenges for players. Challenges are tasks th; ★11; 更新于 2026-10-06; 最新 26.10.2; 发布于 2026-10-08; 最近推送 2026-10-08 |
| CS2Skin | [dyshay/CS2Skin](https://github.com/dyshay/CS2Skin) | ? | `ported` | 最新 1.0.4-b; 发布于 2024-01-24; 最近推送 2024-01-27 |
| CS2-PlayerModelChanger | [samyycX/CS2-PlayerModelChanger](https://github.com/samyycX/CS2-PlayerModelChanger) | CounterStrikeSharp | `packageable` | A cssharp plugin to change player models.; ★138; 更新于 2025-08-30; 最新 release-v1.8.6; 发布于 2025-01-27; 最近推送 2025-08-30 |
| equipments | [exkludera-cssharp/equipments](https://github.com/exkludera-cssharp/equipments) | ? | `packageable` | 最新 2.0.0; 发布于 2025-11-30; 最近推送 2025-12-07 |
| EndRoundSounds | [GianniKoch/EndRoundSounds](https://github.com/GianniKoch/EndRoundSounds) | ? | `packageable` | 最新 1.1.0; 发布于 2025-11-01; 最近推送 2025-11-01 |
| cs2-MVP-Sounds-GoldKingZ | [oqyh/cs2-MVP-Sounds-GoldKingZ](https://github.com/oqyh/cs2-MVP-Sounds-GoldKingZ) | ? | `archived` | 已归档; 最新 1.0.5; 发布于 2024-05-13; 最近推送 2024-12-17 |
| CS2-SpawnPorter | [CS2-SpawnPorter](https://github.com/CS2-SpawnPorter) | ? | `not_found` | 需人工核查 |
| cs2-Spawn-Loadout-GoldKingZ | [oqyh/cs2-Spawn-Loadout-GoldKingZ](https://github.com/oqyh/cs2-Spawn-Loadout-GoldKingZ) | ? | `ported` | 最新 1.0.8; 发布于 2025-02-03; 最近推送 2025-08-04 |
| cs2-map-modifiers | [Kandru/cs2-map-modifiers](https://github.com/Kandru/cs2-map-modifiers) | ? | `packageable` | 最新 26.05.1; 发布于 2026-05-30; 最近推送 2026-05-30 |
| cs2-Team-Identity-Manager | [ZeSpama/cs2-Team-Identity-Manager](https://github.com/ZeSpama/cs2-Team-Identity-Manager) | ? | `packageable` | 最新 v1.0.1; 发布于 2025-02-11; 最近推送 2025-02-12 |
| cs2-teambalancer | [Kandru/cs2-teambalancer](https://github.com/Kandru/cs2-teambalancer) | ? | `packageable` | 最新 26.05.1; 发布于 2026-05-30; 最近推送 2026-05-30 |
| CS2-Advanced-TeamBalance | [Mesharsky/CS2-Advanced-TeamBalance](https://github.com/Mesharsky/CS2-Advanced-TeamBalance) | ? | `ported` | 最新 v6.0.0; 发布于 2026-07-10; 最近推送 2026-07-10 |
| Economy | [gerod220/Economy](https://github.com/gerod220/Economy) | SwiftlyS2 | `packageable` | The base economy plugin for your server.; ★6; 更新于 2026-03-14; 最新 v0.2-alpha; 发布于 2023-12-03; 最近推送 2023-12-03 |
| cs2-cosmetics | [Kandru/cs2-cosmetics](https://github.com/Kandru/cs2-cosmetics) | ? | `packageable` | 最新 26.05.1; 发布于 2026-05-30; 最近推送 2026-05-30 |
| RollTheDice | [Quantor97/CS2-RollTheDice-Plugin](https://github.com/Quantor97/CS2-RollTheDice-Plugin) | ? | `ported` | 最新 2.1.1; 发布于 2023-11-19; 最近推送 2023-11-19 |
| CS2-Hybrid-DamageInfo | [HybridMind1337/CS2-Hybrid-DamageInfo](https://github.com/HybridMind1337/CS2-Hybrid-DamageInfo) | ? | `packageable` | 最新 5.0.0; 发布于 2026-04-27; 最近推送 2026-04-27 |
| CS2-GameHUD | [darkerz7/CS2-GameHUD](https://github.com/darkerz7/CS2-GameHUD) | ? | `ported` | 最新 CS2-GameHUD-v.1.DZ.4; 发布于 2026-05-31; 最近推送 2026-07-17 |
| CS2Stats | [sarim-hk/CS2Stats](https://github.com/sarim-hk/CS2Stats) | ? | `ported` | 最新 v3.1.0; 发布于 2026-09-20; 最近推送 2026-09-20 |
| CS2-STATPLAY | [NeuTroNBZh/CS2-STATPLAY](https://github.com/NeuTroNBZh/CS2-STATPLAY) | CounterStrikeSharp | `ported` | Production-ready stats plugin — captures kills, rounds, objectives and grenades; ★2; 更新于 2026-10-01; 最新 v1.1.2; 发布于 2026-10-01; 最近推送 2026-10-01 |
| CS2-CustomVotes | [imi-tat0r/CS2-CustomVotes](https://github.com/imi-tat0r/CS2-CustomVotes) | ? | `ported` | 最新 v1.1.4; 发布于 2025-11-11; 最近推送 2025-11-11 |
| VoteSystem | [KingBroo/VoteSystem](https://github.com/KingBroo/VoteSystem) | ? | `ported` | 最新 release; 发布于 2026-02-13; 最近推送 2026-05-27 |
| MapChooser | [Alleyv2/Counterstrikesharp-plugin-MapChooser-for-CS2](https://github.com/Alleyv2/Counterstrikesharp-plugin-MapChooser-for-CS2) | SwiftlyS2 | `no_assets` | A powerful and customizable map voting system for SwiftlyS2.; ★14; 更新于 2026-09-13; 最近推送 2026-04-18 |
| CS2-MapManager-COFYYE | [cofyye/CS2-MapManager-COFYYE](https://github.com/cofyye/CS2-MapManager-COFYYE) | ? | `packageable` | 最新 v1.4; 发布于 2026-01-17; 最近推送 2026-01-17 |
| cs2-advanced-weapon-system | [CounterStrike2-Plugins-Archive/cs2-advanced-weapon-system](https://github.com/CounterStrike2-Plugins-Archive/cs2-advanced-weapon-system) | ? | `archived` | 已归档; 最新 v1.11; 发布于 2025-10-17; 最近推送 2025-10-17 |
| cs2-retakes-weapon-allocator | [Ravid-A/cs2-retakes-weapon-allocator](https://github.com/Ravid-A/cs2-retakes-weapon-allocator) | ? | `ported` | 最新 v3.2.6; 发布于 2026-09-27; 最近推送 2026-09-27 |
| Serex-CS2-Practice-Mod | [TPP-cs/Serex-CS2-Practice-Mod](https://github.com/TPP-cs/Serex-CS2-Practice-Mod) | ? | `no_assets` | 最近推送 2026-01-06 |
| CS2PracticeMod | [ProxTricky/CS2PracticeMod](https://github.com/ProxTricky/CS2PracticeMod) | ? | `packageable` | 最新 v2.0.2; 发布于 2025-03-08; 最近推送 2025-03-08 |
| cs2-practice-mode | [Phi-S/cs2-practice-mode](https://github.com/Phi-S/cs2-practice-mode) | ? | `no_assets` | 最新 0.0.18; 发布于 2026-01-21; 最近推送 2026-01-29 |
| CS2-Plugins-For-Community | [oqyh/cs2-Plugins-For-Community](https://github.com/oqyh/cs2-Plugins-For-Community) | ? | `packageable` | 最新 Give-Weapons-1.0.0; 发布于 2024-04-04; 最近推送 2025-06-04 |
| ByDexterTR/CS2Plugins | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | ? | `no_assets` | 最近推送 2026-10-08 |

## 按源仓库归并

| 源仓库 | 插件 |
| --- | --- |
| [alliedmodders/metamod-source](https://github.com/alliedmodders/metamod-source) | Metamod:Source |
| [roflmuffin/CounterStrikeSharp](https://github.com/roflmuffin/CounterStrikeSharp) | CounterStrikeSharp |
| [shobhit-pathak/MatchZy](https://github.com/shobhit-pathak/MatchZy) | MatchZy |
| [daffyyyy/CS2-SimpleAdmin](https://github.com/daffyyyy/CS2-SimpleAdmin) | CS2-SimpleAdmin |
| [B3none/cs2-retakes](https://github.com/B3none/cs2-retakes) | cs2-retakes |
| [Source2ZE/CS2Fixes](https://github.com/Source2ZE/CS2Fixes) | CS2Fixes |
| [KZGlobalTeam/cs2kz-metamod](https://github.com/KZGlobalTeam/cs2kz-metamod) | cs2kz-metamod |
| [CS2Surf/Timer](https://github.com/CS2Surf/Timer) | CS2Surf/Timer |
| [edgegamers/Jailbreak](https://github.com/edgegamers/Jailbreak) | Jailbreak |
| [schwarper/cs2-store](https://github.com/schwarper/cs2-store) | cs2-store |
| [NeuTroNBZh/CS2-Retake-Suite](https://github.com/NeuTroNBZh/CS2-Retake-Suite) | CS2-Retake-Suite |
| [MEngYangX/MEngZy](https://github.com/MEngYangX/MEngZy) | MEngZy |
| [cofyye/CS2-InfoTop-COFYYE](https://github.com/cofyye/CS2-InfoTop-COFYYE) | CS2-InfoTop-COFYYE |
| [ShookEagle/CS2-FullTeamFix](https://github.com/ShookEagle/CS2-FullTeamFix) | CS2-FullTeamFix |
| [ShookEagle/CS2-HideAndSeekPlugin](https://github.com/ShookEagle/CS2-HideAndSeekPlugin) | CS2-HideAndSeekPlugin |
| [KillStr3aK/CS2-AntiDLL](https://github.com/KillStr3aK/CS2-AntiDLL) | CS2-AntiDLL |
| [Austinbots/CS2-BotAI](https://github.com/Austinbots/CS2-BotAI) | CS2-BotAI |
| [Kandru/cs2-quake-sounds](https://github.com/Kandru/cs2-quake-sounds) | cs2-quake-sounds |
| [asapverneri/CS2-Playervotes](https://github.com/asapverneri/CS2-Playervotes) | CS2-Playervotes |
| [K4ryuu/K4-Systems](https://github.com/K4ryuu/K4-Systems) | K4-Systems |
| [CS2Plugins/WeaponRestrict](https://github.com/CS2Plugins/WeaponRestrict) | WeaponRestrict |
| [CHR15cs/CS2-Practice-Plugin](https://github.com/CHR15cs/CS2-Practice-Plugin) | CS2-Practice-Plugin |
| [Nereziel/cs2-WeaponPaints](https://github.com/Nereziel/cs2-WeaponPaints) | cs2-WeaponPaints |
| [SharpTimer/SharpTimer](https://github.com/SharpTimer/SharpTimer) | SharpTimer |
| [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1v1Slay, AdminList, Ads, AntiCapsLock, AntiTeamFlash, BhopDoorFix, BringGoto, Cekilis, ChatCleaner, Cit, CommandMaker, CTBan, CTKit, CTKov, CTPerk, CTRev, ByDexterTR/CS2Plugins |
| [oqyh/cs2-Plugins-For-Community](https://github.com/oqyh/cs2-Plugins-For-Community) | cs2-Fix-Multi-1v1, cs2-Give-Healthshot-GoldKingZ, cs2-Give-Taser, cs2-Give-Weapons, cs2-Restart-Round-Player-GoldKingZ, CS2-Plugins-For-Community |
| [oscar-wos/Retakes-Zones](https://github.com/oscar-wos/Retakes-Zones) | Retakes-Zones |
| [exkludera-cssharp/cs2-jailbreak](https://github.com/exkludera-cssharp/cs2-jailbreak) | cs2-jailbreak |
| [rcnoob/cs2surf-metamod](https://github.com/rcnoob/cs2surf-metamod) | cs2surf-metamod |
| [CS2-KZ/CS2-KZ](https://github.com/CS2-KZ/CS2-KZ) | CS2-KZ (Base) |
| [girlglock/SharpTimer](https://github.com/girlglock/SharpTimer) | SharpTimer (girlglock) |
| [NockyCZ/CS2-Deathmatch](https://github.com/NockyCZ/CS2-Deathmatch) | CS2-Deathmatch |
| [j4asper/AIO-1v1-Plugin-CS2](https://github.com/j4asper/AIO-1v1-Plugin-CS2) | AIO-1v1-Plugin-CS2 |
| [rockCityMath/CS2-Multi-1v1](https://github.com/rockCityMath/CS2-Multi-1v1) | CS2-Multi-1v1 |
| [anthev-stack/CS2JumpStatistics](https://github.com/anthev-stack/CS2JumpStatistics) | CS2JumpStatistics |
| [ssypchenko/cs2-gungame](https://github.com/ssypchenko/cs2-gungame) | cs2-gungame |
| [lhunter3/HNS-Freeze](https://github.com/lhunter3/HNS-Freeze) | HNS-Freeze |
| [oylsister/ZombieSharp](https://github.com/oylsister/ZombieSharp) | ZombieSharp |
| [devinjc213/PropHunt](https://github.com/devinjc213/PropHunt) | PropHunt |
| [TomiksOfficial/-CS2-Duels](https://github.com/TomiksOfficial/-CS2-Duels) | CS2-Duels |
| [oqyh/cs2-Knife-Round-GoldKingZ](https://github.com/oqyh/cs2-Knife-Round-GoldKingZ) | cs2-Knife-Round-GoldKingZ |
| [Kandru/cs2-native-mapvote](https://github.com/Kandru/cs2-native-mapvote) | cs2-native-mapvote |
| [ssypchenko/GG1MapChooser](https://github.com/ssypchenko/GG1MapChooser) | GG1MapChooser |
| [Ayrton09/umbrella-multimod-interface-cs2](https://github.com/Ayrton09/umbrella-multimod-interface-cs2) | umbrella-multimod-interface-cs2 |
| [exkludera-cssharp/cs2-scuffed-anticheat](https://github.com/exkludera-cssharp/cs2-scuffed-anticheat) | cs2-scuffed-anticheat |
| [karola3vax/CS2FOW](https://github.com/karola3vax/CS2FOW) | CS2FOW |
| [wiruwiru/CallAdminSystem-CS2](https://github.com/wiruwiru/CallAdminSystem-CS2) | CallAdminSystem-CS2 |
| [1Mack/CS2-CallAdmin](https://github.com/1Mack/CS2-CallAdmin) | CS2-CallAdmin |
| [imp87/discord-relay-report](https://github.com/imp87/discord-relay-report) | discord-relay-report |
| [Tsukasa-Nefren/simplediscordrelay](https://github.com/Tsukasa-Nefren/simplediscordrelay) | simplediscordrelay |
| [NockyCZ/CS2-Discord-Utilities](https://github.com/NockyCZ/CS2-Discord-Utilities) | CS2-Discord-Utilities |
| [asapverneri/CS2-ChatRelay](https://github.com/asapverneri/CS2-ChatRelay) | CS2-ChatRelay |
| [Kandru/cs2-challenges](https://github.com/Kandru/cs2-challenges) | cs2-challenges |
| [dyshay/CS2Skin](https://github.com/dyshay/CS2Skin) | CS2Skin |
| [samyycX/CS2-PlayerModelChanger](https://github.com/samyycX/CS2-PlayerModelChanger) | CS2-PlayerModelChanger |
| [exkludera-cssharp/equipments](https://github.com/exkludera-cssharp/equipments) | equipments |
| [GianniKoch/EndRoundSounds](https://github.com/GianniKoch/EndRoundSounds) | EndRoundSounds |
| [oqyh/cs2-MVP-Sounds-GoldKingZ](https://github.com/oqyh/cs2-MVP-Sounds-GoldKingZ) | cs2-MVP-Sounds-GoldKingZ |
| [CS2-SpawnPorter](https://github.com/CS2-SpawnPorter) | CS2-SpawnPorter |
| [oqyh/cs2-Spawn-Loadout-GoldKingZ](https://github.com/oqyh/cs2-Spawn-Loadout-GoldKingZ) | cs2-Spawn-Loadout-GoldKingZ |
| [Kandru/cs2-map-modifiers](https://github.com/Kandru/cs2-map-modifiers) | cs2-map-modifiers |
| [ZeSpama/cs2-Team-Identity-Manager](https://github.com/ZeSpama/cs2-Team-Identity-Manager) | cs2-Team-Identity-Manager |
| [Kandru/cs2-teambalancer](https://github.com/Kandru/cs2-teambalancer) | cs2-teambalancer |
| [Mesharsky/CS2-Advanced-TeamBalance](https://github.com/Mesharsky/CS2-Advanced-TeamBalance) | CS2-Advanced-TeamBalance |
| [gerod220/Economy](https://github.com/gerod220/Economy) | Economy |
| [Kandru/cs2-cosmetics](https://github.com/Kandru/cs2-cosmetics) | cs2-cosmetics |
| [Quantor97/CS2-RollTheDice-Plugin](https://github.com/Quantor97/CS2-RollTheDice-Plugin) | RollTheDice |
| [HybridMind1337/CS2-Hybrid-DamageInfo](https://github.com/HybridMind1337/CS2-Hybrid-DamageInfo) | CS2-Hybrid-DamageInfo |
| [darkerz7/CS2-GameHUD](https://github.com/darkerz7/CS2-GameHUD) | CS2-GameHUD |
| [sarim-hk/CS2Stats](https://github.com/sarim-hk/CS2Stats) | CS2Stats |
| [NeuTroNBZh/CS2-STATPLAY](https://github.com/NeuTroNBZh/CS2-STATPLAY) | CS2-STATPLAY |
| [imi-tat0r/CS2-CustomVotes](https://github.com/imi-tat0r/CS2-CustomVotes) | CS2-CustomVotes |
| [KingBroo/VoteSystem](https://github.com/KingBroo/VoteSystem) | VoteSystem |
| [Alleyv2/Counterstrikesharp-plugin-MapChooser-for-CS2](https://github.com/Alleyv2/Counterstrikesharp-plugin-MapChooser-for-CS2) | MapChooser |
| [cofyye/CS2-MapManager-COFYYE](https://github.com/cofyye/CS2-MapManager-COFYYE) | CS2-MapManager-COFYYE |
| [CounterStrike2-Plugins-Archive/cs2-advanced-weapon-system](https://github.com/CounterStrike2-Plugins-Archive/cs2-advanced-weapon-system) | cs2-advanced-weapon-system |
| [Ravid-A/cs2-retakes-weapon-allocator](https://github.com/Ravid-A/cs2-retakes-weapon-allocator) | cs2-retakes-weapon-allocator |
| [TPP-cs/Serex-CS2-Practice-Mod](https://github.com/TPP-cs/Serex-CS2-Practice-Mod) | Serex-CS2-Practice-Mod |
| [ProxTricky/CS2PracticeMod](https://github.com/ProxTricky/CS2PracticeMod) | CS2PracticeMod |
| [Phi-S/cs2-practice-mode](https://github.com/Phi-S/cs2-practice-mode) | cs2-practice-mode |
