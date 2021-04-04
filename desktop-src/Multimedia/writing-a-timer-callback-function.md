---
title: Написание функции обратного вызова таймера
description: Написание функции обратного вызова таймера
ms.assetid: 85260b6b-42de-43f4-83b7-94edbf660006
keywords:
- Таймеры мультимедиа, функции обратного вызова
- таймеры, функции обратного вызова
- Написание функций обратного вызова таймера
- Таймеры мультимедиа, написание функций обратного вызова
- таймеры, написание функций обратного вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609cf2dda455897fb6cae0f3c48252016ba54cb9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987418"
---
# <a name="writing-a-timer-callback-function"></a><span data-ttu-id="9b272-108">Написание функции обратного вызова таймера</span><span class="sxs-lookup"><span data-stu-id="9b272-108">Writing a Timer Callback Function</span></span>

> [!Note]  
> <span data-ttu-id="9b272-109">В этом разделе описывается устаревшая функция.</span><span class="sxs-lookup"><span data-stu-id="9b272-109">This topic describes an obsolete function.</span></span> <span data-ttu-id="9b272-110">Новые приложения должны использовать функцию [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) для создания таймеров.</span><span class="sxs-lookup"><span data-stu-id="9b272-110">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="9b272-111">Следующая функция обратного вызова, Онешоттимер, делает недействительным идентификатор для одного события таймера и вызывает подпрограммы таймера для выполнения задач, связанных с конкретным приложением.</span><span class="sxs-lookup"><span data-stu-id="9b272-111">The following callback function, OneShotTimer, invalidates the identifier for the single timer event and calls a timer routine to handle the application-specific tasks.</span></span> <span data-ttu-id="9b272-112">Дополнительные сведения см. в разделе [**тимепрок**](/previous-versions//dd757631(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9b272-112">For more information, see [**TimeProc**](/previous-versions//dd757631(v=vs.85)).</span></span>


```C++
void CALLBACK OneShotTimer(UINT wTimerID, UINT msg, 
    DWORD dwUser, DWORD dw1, DWORD dw2) 
{ 
    NPSEQ npSeq;             // pointer to sequencer data 
    npSeq = (NPSEQ)dwUser;
    npSeq->wTimerID = 0;     // invalidate timer ID (no longer in use)
    TimerRoutine(npSeq);     // handle tasks 
} 
```



## <a name="related-topics"></a><span data-ttu-id="9b272-113">См. также</span><span class="sxs-lookup"><span data-stu-id="9b272-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b272-114">Использование таймеров мультимедиа</span><span class="sxs-lookup"><span data-stu-id="9b272-114">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 