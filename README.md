# BingWallpaper

[![total / day](https://img.shields.io/badge/dynamic/json?url=https://data.jsdelivr.com/v1/package/gh/star2000/count@2/stats/day&label=total&query=total&suffix=+/+day&style=flat-square)](https://github.com/star2000/count)
[![total / week](https://img.shields.io/badge/dynamic/json?url=https://data.jsdelivr.com/v1/package/gh/star2000/count@2/stats/week&label=total&query=total&suffix=+/+week&style=flat-square)](https://github.com/star2000/count)
[![total / month](https://img.shields.io/badge/dynamic/json?url=https://data.jsdelivr.com/v1/package/gh/star2000/count@2/stats/month&label=total&query=total&suffix=+/+month&style=flat-square)](https://github.com/star2000/count)
[![total / year](https://img.shields.io/badge/dynamic/json?url=https://data.jsdelivr.com/v1/package/gh/star2000/count@2/stats/year&label=total&query=total&suffix=+/+year&style=flat-square)](https://github.com/star2000/count)

Windows Daily Bing Wallpaper

Automatically triggered at 0:00 GMT

Automatic delay if not powered on or connected to the Internet

Minimum version supported are Win7, Win2008 

## How to use

Run the commands in a Privileged (Admin) Powershell

### Install

```ps1
powershell [Net.ServicePointManager]::SecurityProtocol = [Net.ServicePointManager]::SecurityProtocol -bor 3072; (New-Object Net.WebClient).DownloadString('https://github.com/GiaSen/BingWallpaper/raw/master/install.ps1') | iex
```

### Uninstall

```ps1
powershell [Net.ServicePointManager]::SecurityProtocol = [Net.ServicePointManager]::SecurityProtocol -bor 3072; (New-Object Net.WebClient).DownloadString('https://github.com/GiaSen/BingWallpaper/raw/master/uninstall.ps1') | iex
```

## Environment variables

Change behavior through environment variables
```bat
setx "环境变量名" "环境变量值"
```

Manual execution, or run from task scheduler
```bat
schtasks /Run /TN "\star2000\BingWallpaper"
```

- Save path
  - Environment variable name: `WallpaperPath`
  - Default: None (do not save)
  - Optional value: any path with write permission
  - Note: Do not start with `.jpg` At the end, the filename defaults to `%Y-%m-%d.jpg`（YYYY-MM-DD.jpg），see [UNIX time format](https://docs.microsoft.com/zh-cn/powershell/module/microsoft.powershell.utility/get-date#notes)
- Resolution
  - Environment variable name: `WallpaperResolution`
  - Default: `1920x1080`
  - Optional values:
    - `UHD` (Original image resolution, generally above 4k)
    - `1920x1200`
    - `1920x1080`
    - `1366x768`
    - `1280x768`
    - `1024x768`
    - `800x600`
    - `800x480`
    - `768x1280`
    - `720x1280`
    - `640x480`
    - `480x800`
    - `400x240`
    - `320x240`
    - `240x320`
- International Edition
  - Environment variable name: `WallpaperEnSearch`
  - Defaults: `0` (Domestic version)
  - Optional values: `0`, `1`
- Older wallpaper (max 7 days ago)
  - Environment variable name: `WallpaperDaysAgo`
  - Defaults: `0` (Today)
  - Optional values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`

## [Donate to star2000, original developer, alipay](https://blog.star2000.work/images/alipay.png)
