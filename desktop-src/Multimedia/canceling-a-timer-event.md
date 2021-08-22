---
title: Отмена события таймера
description: Отмена события таймера
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- Таймеры мультимедиа, события
- таймеры, события
- Функция Тимекиллевент
- Отмена событий таймера
- Таймеры мультимедиа, отмена событий
- таймеры, отмена событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4e9a92a02dca8ffd4723685fc96cdb0f82fc34a0fa2e3481a71a51997c316
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691797"
---
# <a name="canceling-a-timer-event"></a>Отмена события таймера

> [!Note]  
> В этом разделе описывается устаревшая функция. Новые приложения должны использовать функцию [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) для создания таймеров.

 

Для каждого периодического таймера, создающего вызов [**тимесетевент**](/previous-versions//dd757634(v=vs.85)), приложение должно отменить таймер, вызвав функцию [**тимекиллевент**](/previous-versions//dd757630(v=vs.85)) , прежде чем освободить память, содержащую функцию обратного вызова. Для отмены события таймера может быть вызвана Следующая функция.


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование таймеров мультимедиа](using-multimedia-timers.md)
</dt> </dl>

 

 