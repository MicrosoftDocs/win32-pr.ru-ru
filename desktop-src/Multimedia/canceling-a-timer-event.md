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
# <a name="canceling-a-timer-event"></a><span data-ttu-id="2cd0c-109">Отмена события таймера</span><span class="sxs-lookup"><span data-stu-id="2cd0c-109">Canceling a Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="2cd0c-110">В этом разделе описывается устаревшая функция.</span><span class="sxs-lookup"><span data-stu-id="2cd0c-110">This topic describes an obsolete function.</span></span> <span data-ttu-id="2cd0c-111">Новые приложения должны использовать функцию [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) для создания таймеров.</span><span class="sxs-lookup"><span data-stu-id="2cd0c-111">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="2cd0c-112">Для каждого периодического таймера, создающего вызов [**тимесетевент**](/previous-versions//dd757634(v=vs.85)), приложение должно отменить таймер, вызвав функцию [**тимекиллевент**](/previous-versions//dd757630(v=vs.85)) , прежде чем освободить память, содержащую функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="2cd0c-112">For every periodic timer creating by calling [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), the application must cancel the timer by calling the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function before it frees the memory that contains the callback function.</span></span> <span data-ttu-id="2cd0c-113">Для отмены события таймера может быть вызвана Следующая функция.</span><span class="sxs-lookup"><span data-stu-id="2cd0c-113">To cancel a timer event, it might call the following function.</span></span>


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a><span data-ttu-id="2cd0c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="2cd0c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cd0c-115">Использование таймеров мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2cd0c-115">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 