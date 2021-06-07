---
description: Классы устранения неполадок событий службы WMI создаются событиями в службе WMI, такими как создание пула потоков.
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: Классы устранения неполадок событий службы WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e811ac5b276e5562f73b5b432d5f3255af5bab7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443065"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>Классы устранения неполадок событий службы WMI

Классы устранения неполадок событий службы WMI создаются событиями в службе WMI, такими как создание пула потоков.

Вы можете подписываться на абстрактный базовый класс уведомлений [**MSFT \_ вмиессевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) , чтобы получить все производные события, перечисленные в следующей таблице.



|   Событие                                                                                        |   Описание                                                                                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**MSFT \_ вмиессевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | Родительский класс для всех самособытий подсистемы событий (ESS) инструментарий управления Windows (WMI) (WMI). |
| [**MSFT \_ вмирегистернотификатионевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | Представляет создание приемника событий для уведомления для запроса события.                       |
| [**MSFT \_ вмиканцелнотификатионсинк**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | создается при отмене приемника событий.                                                           |
| [**MSFT \_ вмисреадпулевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | предоставляет уведомления о событиях потоков в подсистеме событий WMI (ESS).                           |
| [**MSFT \_ вмисреадпулкреатед**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | Предоставляет уведомление при создании потока в подсистеме событий WMI (ESS).                   |
| [**MSFT \_ вмисреадпулделетед**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | Предоставляет уведомление при удалении потока в подсистеме событий WMI (ESS).                   |
| [**MSFT \_ вмифилтеревент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | Родительский класс для всех событий фильтра для постоянного потребителя событий.                                        |
| [**MSFT \_ вмифилтерактиватед**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilteractivated)                     | Определяет успешную активацию постоянного фильтра подписки потребителя событий.                |
| [**MSFT \_ вмифилтердеактиватед**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterdeactivated)                 | Определяет успешную деактивацию фильтра постоянной подписки потребителя.                    |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Устранение неполадок WMI](wmi-troubleshooting.md)
</dt> <dt>

Устранение неполадок инструментария WMI
</dt> <dt>

[Мониторинг событий](monitoring-events.md)
</dt> <dt>

[Получение события WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
