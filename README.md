# cs2pkg-port

CS2 插件的 **`.cs2pkg` 格式分发包**,由 [cyqmq](https://github.com/cyqmq) 从原仓库移植/打包,
可直接配合 [cs2-link-manager](https://github.com/cyqmq/cs2-link-manager) 使用:

```bash
cs2lm add --pkg <plugin>.cs2pkg
cs2lm install <plugin>
```

> `.cs2pkg` 是 cs2-link-manager 的标准插件包格式(zip 内含 `cs2pkg.json` + `addons/` 树)。
> 本仓库的包采用**扩展格式**:`cs2pkg.json` 含 `author`/`description`/`license`/`homepage`/`repository`/`dependencies`/`plugins` 字段。
> 多插件包(`ByDexterTR-All`、`CS2-SimpleAdmin`)通过 `plugins` 字段声明目录,`cs2lm add --pkg` 会自动拆成多个仓库条目。

## 作为官方插件源使用(index.json)

本仓库同时作为 **cs2-link-manager 官方插件源**,遵循 [`index.json` v1 规范](https://github.com/cyqmq/cs2-link-manager/blob/main/docs/INDEX.md):

```bash
# 1) 添加插件源
cs2lm source add https://raw.githubusercontent.com/cyqmq/cs2pkg-port/main/index.json

# 2) 一键安装/更新源内全部插件(77 个可独立更新的插件)
cs2lm update --yes

# 3) 只更新某个插件
cs2lm update CS2-SimpleAdmin
```

- `index.json` 位于仓库根目录,每次发 Release 后同步更新。
- 每个条目包含 `version` / `download_url`(Release 资产直链)/ `sha256` / `size` / `author` / `description` / `category`(热门插件),包体下载后自动校验 sha256 与包内 `cs2pkg.json` 身份一致性。
- 索引覆盖 **78 个条目**:46 个 ByDexterTR 单插件 + `CS2-SimpleAdmin`(主插件)+ `CS2-SimpleAdmin_FunCommands` + `CS2-SimpleAdmin_StealthModule` + `cs2-retakes` + **27 个从真实源仓库移植的插件** + **1 个游戏内容包**(CS2-Bot-Improver,见下节)。
- `ByDexterTR-All.cs2pkg` 与 `dist/from-sources/bundles/` 下的多插件包是手工安装用全量包,不进索引(个体插件均可独立更新)。
- 插件与**真实上游源仓库**的对应关系见 [`SOURCES.md`](SOURCES.md)(含仓库实况/兼容性甄别)。

## 来自 ByDexterTR/CS2Plugins

原仓库:https://github.com/ByDexterTR/CS2Plugins (46 个 CounterStrikeSharp 插件)

| 插件 | 原仓库 | 移植版本 | 包文件 |
| --- | --- | --- | --- |
| 1v1Slay | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `1v1Slay.cs2pkg` |
| AdminList | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `AdminList.cs2pkg` |
| Ads | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Ads.cs2pkg` |
| AntiCapsLock | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `AntiCapsLock.cs2pkg` |
| AntiTeamFlash | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `AntiTeamFlash.cs2pkg` |
| BhopDoorFix | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `BhopDoorFix.cs2pkg` |
| BringGoto | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `BringGoto.cs2pkg` |
| Cekilis | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Cekilis.cs2pkg` |
| ChatCleaner | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `ChatCleaner.cs2pkg` |
| Cit | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Cit.cs2pkg` |
| CommandMaker | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `CommandMaker.cs2pkg` |
| CTBan | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `CTBan.cs2pkg` |
| CTKit | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `CTKit.cs2pkg` |
| CTKov | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `CTKov.cs2pkg` |
| CTPerk | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `CTPerk.cs2pkg` |
| CTRev | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `CTRev.cs2pkg` |
| CTSpawnKill | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `CTSpawnKill.cs2pkg` |
| DiscordLogger | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `DiscordLogger.cs2pkg` |
| FortniteArmor | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `FortniteArmor.cs2pkg` |
| FPS | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `FPS.cs2pkg` |
| GoBhop | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `GoBhop.cs2pkg` |
| HideTeammates | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `HideTeammates.cs2pkg` |
| JBDoors | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `JBDoors.cs2pkg` |
| JBLaserWar | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `JBLaserWar.cs2pkg` |
| JBRace | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `JBRace.cs2pkg` |
| JBTeams | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `JBTeams.cs2pkg` |
| Lazer | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Lazer.cs2pkg` |
| MapBlock | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `MapBlock.cs2pkg` |
| Meslekmenu | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Meslekmenu.cs2pkg` |
| PlayerHourCheck | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `PlayerHourCheck.cs2pkg` |
| PlayerRGB | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `PlayerRGB.cs2pkg` |
| Postprocessing | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Postprocessing.cs2pkg` |
| PrivateMessage | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `PrivateMessage.cs2pkg` |
| Redbull | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Redbull.cs2pkg` |
| ScreenText | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `ScreenText.cs2pkg` |
| Sesler | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Sesler.cs2pkg` |
| ShowPlayerClips | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `ShowPlayerClips.cs2pkg` |
| Silahsil | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Silahsil.cs2pkg` |
| Slowmode | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Slowmode.cs2pkg` |
| SpawnkillProtection | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `SpawnkillProtection.cs2pkg` |
| Speedometer | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Speedometer.cs2pkg` |
| Sustum | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Sustum.cs2pkg` |
| TeamShuffle | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `TeamShuffle.cs2pkg` |
| Thirdperson | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `Thirdperson.cs2pkg` |
| VIPCore | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `VIPCore.cs2pkg` |
| WardenMarker | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `WardenMarker.cs2pkg` |
| **ByDexterTR-All** (46 个插件全量包,多插件包) | [ByDexterTR/CS2Plugins](https://github.com/ByDexterTR/CS2Plugins) | 1.0.0 | `ByDexterTR-All.cs2pkg` |

## 来自 awesome-cs2

来源列表:https://github.com/samyycX/awesome-cs2 (以下为已打包为 `.cs2pkg` 的插件)

| 插件 | 原仓库 | 移植版本 | 包文件 |
| --- | --- | --- | --- |
| cs2-retakes | [B3none/cs2-retakes](https://github.com/B3none/cs2-retakes) | 3.1.1 | `cs2-retakes.cs2pkg` |
| CS2-SimpleAdmin(主插件) | [daffyyyy/CS2-SimpleAdmin](https://github.com/daffyyyy/CS2-SimpleAdmin) | 1.9.0 | `CS2-SimpleAdmin.cs2pkg` |
| CS2-SimpleAdmin_FunCommands(子模块) | [daffyyyy/CS2-SimpleAdmin](https://github.com/daffyyyy/CS2-SimpleAdmin) | 1.9.0 | `CS2-SimpleAdmin_FunCommands.cs2pkg` |
| CS2-SimpleAdmin_StealthModule(子模块) | [daffyyyy/CS2-SimpleAdmin](https://github.com/daffyyyy/CS2-SimpleAdmin) | 1.9.0 | `CS2-SimpleAdmin_StealthModule.cs2pkg` |

## 来自真实源仓库(from-sources)

这些插件直接从各自**真实上游源仓库**的 GitHub Release 打包(不再是聚合仓库),版本由 `cs2lm` 从插件 `deps.json` 自动检测(无内嵌版本的插件为 `1.0.0`)。仓库实况与兼容性甄别见 [`SOURCES.md`](SOURCES.md)。

| 插件 | 原仓库 | 移植版本 | 包文件 |
| --- | --- | --- | --- |
| AntiDLL | [KillStr3aK/CS2-AntiDLL](https://github.com/KillStr3aK/CS2-AntiDLL) | 1.0.0 | `AntiDLL.cs2pkg` |
| CS2-Advanced-TeamBalance | [Mesharsky/CS2-Advanced-TeamBalance](https://github.com/Mesharsky/CS2-Advanced-TeamBalance) | 1.0.0 | `CS2-Advanced-TeamBalance.cs2pkg` |
| CS2-CustomVotes | [imi-tat0r/CS2-CustomVotes](https://github.com/imi-tat0r/CS2-CustomVotes) | 1.1.4 | `CS2-CustomVotes.cs2pkg` |
| CS2-GameHUD | [cofyye/CS2-InfoTop-COFYYE](https://github.com/cofyye/CS2-InfoTop-COFYYE)(随 InfoTop 分发包) | 1.0.0 | `CS2-GameHUD.cs2pkg` |
| cs2-Give-Taser | [oqyh/cs2-Plugins-For-Community](https://github.com/oqyh/cs2-Plugins-For-Community) | 1.0.0 | `cs2-Give-Taser.cs2pkg` |
| cs2-Give-Weapons | [oqyh/cs2-Plugins-For-Community](https://github.com/oqyh/cs2-Plugins-For-Community) | 1.0.0 | `cs2-Give-Weapons.cs2pkg` |
| cs2-gungame | [ssypchenko/cs2-gungame](https://github.com/ssypchenko/cs2-gungame) | 1.0.0 | `cs2-gungame.cs2pkg` |
| cs2-Knife-Round-GoldKingZ | [oqyh/cs2-Knife-Round-GoldKingZ](https://github.com/oqyh/cs2-Knife-Round-GoldKingZ) | 1.0.0 | `cs2-Knife-Round-GoldKingZ.cs2pkg` |
| cs2-retakes-weapon-allocator | [Ravid-A/cs2-retakes-weapon-allocator](https://github.com/Ravid-A/cs2-retakes-weapon-allocator) | 1.0.0 | `cs2-retakes-weapon-allocator.cs2pkg` |
| cs2-Spawn-Loadout-GoldKingZ | [oqyh/cs2-Spawn-Loadout-GoldKingZ](https://github.com/oqyh/cs2-Spawn-Loadout-GoldKingZ) | 1.0.0 | `cs2-Spawn-Loadout-GoldKingZ.cs2pkg` |
| CS2-STATPLAY | [NeuTroNBZh/CS2-STATPLAY](https://github.com/NeuTroNBZh/CS2-STATPLAY) | 1.1.2 | `CS2-STATPLAY.cs2pkg` |
| cs2-WeaponPaints | [Nereziel/cs2-WeaponPaints](https://github.com/Nereziel/cs2-WeaponPaints) | 1.0.0 | `cs2-WeaponPaints.cs2pkg` |
| CS2Fixes | [Source2ZE/CS2Fixes](https://github.com/Source2ZE/CS2Fixes) | 1.0.0 | `CS2Fixes.cs2pkg` |
| cs2kz-metamod | [KZGlobalTeam/cs2kz-metamod](https://github.com/KZGlobalTeam/cs2kz-metamod) | 1.0.0 | `cs2kz-metamod.cs2pkg` |
| CS2MenuManager_MenuManager | [cofyye/CS2-MapManager-COFYYE](https://github.com/cofyye/CS2-MapManager-COFYYE)(随 MapManager 分发包) | 1.0.41 | `CS2MenuManager_MenuManager.cs2pkg` |
| CS2Skin | [dyshay/CS2Skin](https://github.com/dyshay/CS2Skin) | 1.0.0 | `CS2Skin.cs2pkg` |
| CS2Stats | [sarim-hk/CS2Stats](https://github.com/sarim-hk/CS2Stats) | 1.0.0 | `CS2Stats.cs2pkg` |
| cs2surf-metamod | [rcnoob/cs2surf-metamod](https://github.com/rcnoob/cs2surf-metamod) | 1.0.0 | `cs2surf-metamod.cs2pkg` |
| CSPracc | [CHR15cs/CS2-Practice-Plugin](https://github.com/CHR15cs/CS2-Practice-Plugin) | 1.0.0.2 | `CSPracc.cs2pkg` |
| GG1MapChooser | [ssypchenko/GG1MapChooser](https://github.com/ssypchenko/GG1MapChooser) | 1.0.0 | `GG1MapChooser.cs2pkg` |
| InfoTop-COFYYE | [cofyye/CS2-InfoTop-COFYYE](https://github.com/cofyye/CS2-InfoTop-COFYYE) | 1.0.0 | `InfoTop-COFYYE.cs2pkg` |
| MapManager-COFYYE | [cofyye/CS2-MapManager-COFYYE](https://github.com/cofyye/CS2-MapManager-COFYYE) | 1.0.0 | `MapManager-COFYYE.cs2pkg` |
| MatchZy | [shobhit-pathak/MatchZy](https://github.com/shobhit-pathak/MatchZy) | 0.9.1 | `MatchZy.cs2pkg` |
| ResourcePrecacher | [CHR15cs/CS2-Practice-Plugin](https://github.com/CHR15cs/CS2-Practice-Plugin)(随 CSPracc 分发包) | 1.0.0.2 | `ResourcePrecacher.cs2pkg` |
| RollTheDice | [Quantor97/CS2-RollTheDice-Plugin](https://github.com/Quantor97/CS2-RollTheDice-Plugin) | 1.0.0 | `RollTheDice.cs2pkg` |
| simplediscordrelay | [Tsukasa-Nefren/simplediscordrelay](https://github.com/Tsukasa-Nefren/simplediscordrelay) | 1.0.0 | `simplediscordrelay.cs2pkg` |
| VoteSystem | [KingBroo/VoteSystem](https://github.com/KingBroo/VoteSystem) | 1.0.0 | `VoteSystem.cs2pkg` |

## 游戏内容包(kind: content)

CS2-Bot-Improver 是一个**全家桶式游戏内容 mod**（Metamod + CounterStrikeSharp 混合框架），通过 `kind: "content"` 格式打包，支持 `roots` 多根目录映射、`requires_frameworks` 框架依赖声明和 `platform` 平台字段。

| 内容包 | 原仓库 | 版本 | 包文件 | 说明 |
| --- | --- | --- | --- | --- |
| CS2-Bot-Improver | [ed0ard/CS2-Bot-Improver](https://github.com/ed0ard/CS2-Bot-Improver) | 1.4.5 | `CS2-Bot-Improver.cs2pkg` | 9 个 CSS 插件 + 3 个 Metamod 插件 + cfg/overrides/backup/gameinfo.gi；需预装 Metamod + CSS 框架 |

## 说明

- 所有包均通过 `cs2lm add --pkg` 验证(可正常注册并生成 manifest)。
- 插件源 `index.json` 经真实 `cs2lm source add` + `cs2lm update` **端到端验证**:全部插件安装成功,sha256 校验、多插件拆分均正常。
- **兼容性**:2026-10-09 版 cs2-link-manager 已修复 `split_css_plugins` 对 `configs/` 目录的假设 bug,并新增版本自动检测;本仓库全部包(含多插件包)已**原生验证通过**。
- `ByDexterTR-All.cs2pkg` 包含 `.Compiled` 中全部 46 个插件的编译产物,一键安装全部插件。
- `CS2-SimpleAdmin.cs2pkg` 是 SimpleAdmin 官方 Release 的完整多插件包(主插件 + FunCommands + StealthModule);索引另提供 `CS2-SimpleAdmin_FunCommands.cs2pkg` 与 `CS2-SimpleAdmin_StealthModule.cs2pkg` 两个单插件包,便于独立安装/更新。
- from-sources 插件从真实源仓库 Release 打包;个别仓库的 Release 同时携带多个插件目录(如 InfoTop 分发包附带 `CS2-GameHUD`、CSPracc 分发包附带 `ResourcePrecacher`),已拆分为独立单插件包。`dist/from-sources/bundles/` 保留了原始多插件包,仅用于手工安装。
- 多插件包在 `cs2lm add --pkg` 时按 `plugins` 字段自动拆分,每个插件独立安装/卸载/更新。
- 插件版权归各自作者所有;本仓库仅做格式转换与分发。

