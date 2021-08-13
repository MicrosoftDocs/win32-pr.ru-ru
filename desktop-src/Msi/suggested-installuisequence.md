---
description: предлагаемые последовательности действий для базовой таблицы инсталуисекуенце в базе данных установщик Windows.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: Предложенные Инсталлуисекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab5c65ed594cf86f86555de235d0ceb0530b9f3e233bfdf5c38d094ca9719a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624336"
---
# <a name="suggested-installuisequence"></a>Предложенные Инсталлуисекуенце



| Действие                                          | Условие                                                                                                  | Последовательность |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| фаталеррордлг                                   |                                                                                                            | –3       |
| усерекситдлг                                     |                                                                                                            | –2       |
| екситдлг                                         |                                                                                                            | –1       |
| [лаунчкондитионс](launchconditions-action.md) |                                                                                                            | 100      |
| препаредлг                                      |                                                                                                            | 140      |
| [аппсеарч](appsearch-action.md)               |                                                                                                            | 400      |
| [ккпсеарч](ccpsearch-action.md)               | НЕ [ **установлено**](installed.md)                                                                         | 500      |
| [рмккпсеарч](rmccpsearch-action.md)           | НЕ [ **установлено**](installed.md)                                                                         | 600      |
| [костинитиализе](costinitialize-action.md)     |                                                                                                            | 800      |
| [филекост](filecost-action.md)                 |                                                                                                            | 900      |
| [костфинализе](costfinalize-action.md)         |                                                                                                            | 1000     |
| велкомедлг                                      | НЕ [ **установлено**](installed.md)                                                                         | 1230     |
| ресумедлг                                       | [**Установлено**](installed.md) И ( [**возобновить**](resume.md) или [**выбрать**](preselected.md))       | 1240     |
| маинтенанцевелкомедлг                           | [**Установлено**](installed.md) И не [**возобновлять**](resume.md) и не [**выделять**](preselected.md) | 1250     |
| прогрессдлг                                     |                                                                                                            | 1280     |
| [ExecuteAction](executeaction-action.md)       |                                                                                                            | 1300     |



 

 

 



