---
title: Получение и Настройка разрешения таймера
description: Получение и Настройка разрешения таймера
ms.assetid: 237a6770-89b9-4922-b9e9-0e0bf3e0c9b6
keywords:
- Таймеры мультимедиа, разрешение
- таймеры, разрешение
- Минимальное разрешение таймера
- Максимальное разрешение таймера
- Таймеры мультимедиа, максимальное разрешение
- таймеры, максимальное разрешение
- Таймеры мультимедиа, минимальное разрешение
- таймеры, минимальное разрешение
- Функция Тимежетдевкапс
- Функция Тимебегинпериод
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5feca59e6fb4c528d6042b00eb7aa23263245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681426"
---
# <a name="obtaining-and-setting-timer-resolution"></a>Получение и Настройка разрешения таймера

В следующем примере вызывается функция [**тимежетдевкапс**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) , чтобы определить минимальное и максимальное разрешения таймера, поддерживаемые службами таймера. Прежде чем настроит все события таймера, в примере устанавливается минимальное разрешение таймера с помощью функции [**тимебегинпериод**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) .


```C++
#define TARGET_RESOLUTION 1         // 1-millisecond target resolution

TIMECAPS tc;
UINT     wTimerRes;

if (timeGetDevCaps(&tc, sizeof(TIMECAPS)) != TIMERR_NOERROR) 
{
    // Error; application can't continue.
}

wTimerRes = min(max(tc.wPeriodMin, TARGET_RESOLUTION), tc.wPeriodMax);
timeBeginPeriod(wTimerRes); 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование таймеров мультимедиа](using-multimedia-timers.md)
</dt> </dl>

 

 




