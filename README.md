---
id: hydrocore.setups.readme
title: "HydroCore setups — описания установок"
type: reference
status: draft
authority: contract
visibility: internal
version: "0.1"
updated: "2026-11-26"
---

# HydroCore setups

Сабмодуль `setups` верхнеуровневого репозитория HydroCore. Здесь лежат описания
конкретных установок в формате `InstallationSetup` (SW-0014).

## Файлы

| Файл | Установка |
| --- | --- |
| `installation-066-kazan-tsm.yaml` | №066, Казань, ЦСМ; 61 устройство, 39 связей |

Контракт формата: `specs/installation-setup-format.md` в корневом репозитории HydroCore.
Источник пилотного файла: `FlowPlant-Configuration`, ветка `_066_Казань_ЦСМ`,
commit `31996c3`, `setup.json` (конверсия без потерь, включая массивы комментариев).

Backend загружает такой файл через `--config <setup.yaml>`: `SetupLoader` проверяет
контракт, `SetupConverter` строит runtime-конфиг, `SetupGraphConverter` — граф связей.
