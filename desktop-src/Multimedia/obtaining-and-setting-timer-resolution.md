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
# <a name="obtaining-and-setting-timer-resolution"></a><span data-ttu-id="38887-113">Получение и Настройка разрешения таймера</span><span class="sxs-lookup"><span data-stu-id="38887-113">Obtaining and Setting Timer Resolution</span></span>

<span data-ttu-id="38887-114">В следующем примере вызывается функция [**тимежетдевкапс**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) , чтобы определить минимальное и максимальное разрешения таймера, поддерживаемые службами таймера.</span><span class="sxs-lookup"><span data-stu-id="38887-114">The following example calls the [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) function to determine the minimum and maximum timer resolutions supported by the timer services.</span></span> <span data-ttu-id="38887-115">Прежде чем настроит все события таймера, в примере устанавливается минимальное разрешение таймера с помощью функции [**тимебегинпериод**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) .</span><span class="sxs-lookup"><span data-stu-id="38887-115">Before it sets up any timer events, the example establishes the minimum timer resolution by using the [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="38887-116">См. также</span><span class="sxs-lookup"><span data-stu-id="38887-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38887-117">Использование таймеров мультимедиа</span><span class="sxs-lookup"><span data-stu-id="38887-117">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 




