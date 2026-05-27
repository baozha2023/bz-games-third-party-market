# bz-games 第三方市场

为 [bz-games](https://github.com/baozha2023/bz-games) 游戏平台收录第三方开源游戏的索引仓库。本仓库中的游戏均为 GitHub 上的开源项目，通过 `gameManifest` 字段自动适配平台，无需游戏自带 `game.json`。

## 如何添加新游戏

1. Fork 本仓库
2. 在 `market.json` 的 `games` 数组中新增一个游戏条目
3. 下载游戏 ZIP 包，计算 SHA256 和文件大小：

   ```powershell
   # 下载
   Invoke-WebRequest -Uri "下载URL" -OutFile "game.zip"
   # 计算 SHA256
   Get-FileHash -Algorithm SHA256 game.zip
   # 查看大小（字节）
   (Get-Item game.zip).Length
   ```

4. 填写完整的 `gameManifest`，确保 `entry` 字段指向正确的入口文件
5. 提交 Pull Request

## market.json 格式说明

`market.json` 字段填写规范、`gameManifest` 配置说明及回退机制详见 [bz-games-market/README.md](https://github.com/baozha2023/bz-games-market/blob/master/README.md)。

## 版权说明

本仓库中所有游戏版权归原作者所有，本仓库仅提供下载索引和平台适配配置。

## 已有游戏

| 游戏名称 | 作者 | 仓库地址 |
|---------|------|---------|
| Floppy Bird | Nebez | [nebez/floppybird](https://github.com/nebez/floppybird) |
| 2048 | Gabriele Cirulli | [gabrielecirulli/2048](https://github.com/gabrielecirulli/2048) |
| Hextris | Garrett Finucane & Logan Engstrom | [Hextris/hextris](https://github.com/Hextris/hextris) |
| A Dark Room | Doublespeak Games | [doublespeakgames/adarkroom](https://github.com/doublespeakgames/adarkroom) |
| T-Rex Runner | Wayou | [wayou/t-rex-runner](https://github.com/wayou/t-rex-runner) |
| Astray | Rye Terrell | [wwwtyro/Astray](https://github.com/wwwtyro/Astray) |
| HexGL | Thibaut Despoulain | [BKcore/HexGL](https://github.com/BKcore/HexGL) |
| Beatrix | congusbongus | [cxong/Beatrix](https://github.com/cxong/Beatrix) |
| shapez.io | tobspr Games | [tobspr-games/shapez.io](https://github.com/tobspr-games/shapez.io) |
