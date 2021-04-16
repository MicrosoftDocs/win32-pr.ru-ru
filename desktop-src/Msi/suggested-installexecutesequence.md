---
description: Предлагаемые последовательности действий для базовой таблицы Инсталлексекутесекуенце в базе данных установщик Windows.
ms.assetid: 7f337f37-1528-4b7e-a628-f9d235510a6f
title: Предложенные Инсталлексекутесекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c25f2db56ef3ad7296bddf4088ad32191f57df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547191"
---
# <a name="suggested-installexecutesequence"></a>Предложенные Инсталлексекутесекуенце



| Действие                                                          | Условие                          | Последовательность |
|-----------------------------------------------------------------|------------------------------------|----------|
| [лаунчкондитионс](launchconditions-action.md)                 |                                    | 100      |
| [аппсеарч](appsearch-action.md)                               |                                    | 400      |
| [ккпсеарч](ccpsearch-action.md)                               | НЕ [ **установлено**](installed.md) | 500      |
| [рмккпсеарч](rmccpsearch-action.md)                           | НЕ [ **установлено**](installed.md) | 600      |
| [валидатепродуктид](validateproductid-action.md)               |                                    | 700      |
| [костинитиализе](costinitialize-action.md)                     |                                    | 800      |
| [филекост](filecost-action.md)                                 |                                    | 900      |
| [костфинализе](costfinalize-action.md)                         |                                    | 1000     |
| [сетодбкфолдерс](setodbcfolders-action.md)                     |                                    | 1100     |
| [инсталлвалидате](installvalidate-action.md)                   |                                    | 1400     |
| [инсталлинитиализе](installinitialize-action.md)               |                                    | 1500     |
| [аллокатерегистриспаце](allocateregistryspace-action.md)       | НЕ [ **установлено**](installed.md) | 1550     |
| [процесскомпонентс](processcomponents-action.md)               |                                    | 1600     |
| [унпублишкомпонентс](unpublishcomponents-action.md)           |                                    | 1700     |
| [унпублишфеатурес](unpublishfeatures-action.md)               |                                    | 1800     |
| [стопсервицес](stopservices-action.md)                         | [**VersionNT**](versionnt.md)     | 1900     |
| [делетесервицес](deleteservices-action.md)                     | [**VersionNT**](versionnt.md)     | 2000     |
| [унрегистеркомплус](unregistercomplus-action.md)               |                                    | 2100     |
| [селфунрегмодулес](selfunregmodules-action.md)                 |                                    | 2200     |
| [унрегистертипелибрариес](unregistertypelibraries-action.md)   |                                    | 2300     |
| [ремовеодбк](removeodbc-action.md)                             |                                    | 2400     |
| [унрегистерфонтс](unregisterfonts-action.md)                   |                                    | 2500     |
| [ремоверегистривалуес](removeregistryvalues-action.md)         |                                    | 2600     |
| [унрегистерклассинфо](unregisterclassinfo-action.md)           |                                    | 2700     |
| [унрегистерекстенсионинфо](unregisterextensioninfo-action.md)   |                                    | 2800     |
| [унрегистерпрогидинфо](unregisterprogidinfo-action.md)         |                                    | 2900     |
| [унрегистермимеинфо](unregistermimeinfo-action.md)             |                                    | 3000     |
| [ремовеинивалуес](removeinivalues-action.md)                   |                                    | 3100     |
| [ремовешорткутс](removeshortcuts-action.md)                   |                                    | 3200     |
| [ремовинвиронментстрингс](removeenvironmentstrings-action.md) |                                    | 3300     |
| [ремоведупликатефилес](removeduplicatefiles-action.md)         |                                    | 3400     |
| [ремовефилес](removefiles-action.md)                           |                                    | 3500     |
| [ремовефолдерс](removefolders-action.md)                       |                                    | 3600     |
| [креатефолдерс](createfolders-action.md)                       |                                    | 3700     |
| [мовефилес](movefiles-action.md)                               |                                    | 3800     |
| [инсталлфилес](installfiles-action.md)                         |                                    | 4000     |
| [патчфилес](patchfiles-action.md)                             |                                    | 4090     |
| [дупликатефилес](duplicatefiles-action.md)                     |                                    | 4210     |
| [BindImage](bindimage-action.md)                               |                                    | 4300     |
| [креатешорткутс](createshortcuts-action.md)                   |                                    | 4500     |
| [регистерклассинфо](registerclassinfo-action.md)               |                                    | 4600     |
| [регистерекстенсионинфо](registerextensioninfo-action.md)       |                                    | 4700     |
| [регистерпрогидинфо](registerprogidinfo-action.md)             |                                    | 4800     |
| [регистермимеинфо](registermimeinfo-action.md)                 |                                    | 4900     |
| [вритерегистривалуес](writeregistryvalues-action.md)           |                                    | 5000     |
| [вритеинивалуес](writeinivalues-action.md)                     |                                    | 5100     |
| [вритинвиронментстрингс](writeenvironmentstrings-action.md)   |                                    | 5200     |
| [регистерфонтс](registerfonts-action.md)                       |                                    | 5300     |
| [инсталлодбк](installodbc-action.md)                           |                                    | 5400     |
| [регистертипелибрариес](registertypelibraries-action.md)       |                                    | 5500     |
| [селфрегмодулес](selfregmodules-action.md)                     |                                    | 5600     |
| [регистеркомплус](registercomplus-action.md)                   |                                    | 5700     |
| [инсталлсервицес](installservices-action.md)                   | [**VersionNT**](versionnt.md)     | 5800     |
| [стартсервицес](startservices-action.md)                       | [**VersionNT**](versionnt.md)     | 5900     |
| [RegisterUser](registeruser-action.md)                         |                                    | 6000     |
| [регистерпродукт](registerproduct-action.md)                   |                                    | 6100     |
| [публишкомпонентс](publishcomponents-action.md)               |                                    | 6200     |
| [публишфеатурес](publishfeatures-action.md)                   |                                    | 6300     |
| [публишпродукт](publishproduct-action.md)                     |                                    | 6400     |
| [Функции InstallFinalize](installfinalize-action.md)                   |                                    | 6600     |



 

 

 



