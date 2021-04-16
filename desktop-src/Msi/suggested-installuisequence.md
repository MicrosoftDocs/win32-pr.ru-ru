---
description: Предлагаемые последовательности действий для базовой таблицы Инсталуисекуенце в базе данных установщик Windows.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: Предложенные Инсталлуисекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650847"
---
# <a name="suggested-installuisequence"></a>Предложенные Инсталлуисекуенце



| Действие                                          | Условие                                                                                                  | Последовательность |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| фаталеррордлг                                   |                                                                                                            | –3       |
| усерекситдлг                                     |                                                                                                            | -2       |
| екситдлг                                         |                                                                                                            | -1       |
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



 

 

 



