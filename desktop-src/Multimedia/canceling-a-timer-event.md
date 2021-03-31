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
ms.openlocfilehash: 1380b2868596e0177e806f5df5217bb839abe61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069967"
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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование таймеров мультимедиа](using-multimedia-timers.md)
</dt> </dl>

 

 