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
# <a name="writing-a-timer-callback-function"></a>Написание функции обратного вызова таймера

> [!Note]  
> В этом разделе описывается устаревшая функция. Новые приложения должны использовать функцию [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) для создания таймеров.

 

Следующая функция обратного вызова, Онешоттимер, делает недействительным идентификатор для одного события таймера и вызывает подпрограммы таймера для выполнения задач, связанных с конкретным приложением. Дополнительные сведения см. в разделе [**тимепрок**](/previous-versions//dd757631(v=vs.85)).


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование таймеров мультимедиа](using-multimedia-timers.md)
</dt> </dl>

 

 