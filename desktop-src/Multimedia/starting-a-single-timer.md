---
title: Запуск одного события таймера
description: Запуск одного события таймера
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- Таймеры мультимедиа, события
- таймеры, события
- Таймеры мультимедиа, начальные события
- таймеры, события запуска
- Функция Тимесетевент
- Запуск событий таймера
- события с одним таймером
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc3a4c69aefe8df3310c8ff974ef7592b435eabccd661bdbeb1ebbf85dc3c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037174"
---
# <a name="starting-a-single-timer-event"></a>Запуск одного события таймера

> [!Note]  
> В этом разделе описывается устаревшая функция. Новые приложения должны использовать функцию [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) для создания таймеров.

 

Чтобы запустить одно событие таймера, вызовите функцию [**тимесетевент**](/previous-versions//dd757634(v=vs.85)) , указав период времени перед обратным вызовом, разрешение, адрес функции обратного вызова (см. [**тимепрок**](/previous-versions//dd757631(v=vs.85))) и данные пользователя, которые необходимо передать функцией обратного вызова. Приложение может использовать функцию, подобную приведенной ниже, для запуска одного события таймера.


```C++
UINT SetTimerCallback(NPSEQ npSeq,  // sequencer data
    UINT msInterval)                // event interval
{ 
    npSeq->wTimerID = timeSetEvent(
        msInterval,                    // delay
        wTimerRes,                     // resolution (global variable)
        OneShotCallback,               // callback function
        (DWORD)npSeq,                  // user data
        TIME_ONESHOT );                // single timer event
    if(! npSeq->wTimerID)
        return ERR_TIMER;
    else
        return ERR_NOERROR;
} 

```



Пример функции обратного вызова Онешоткаллбакк см. в разделе [написание функции обратного вызова таймера](writing-a-timer-callback-function.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование таймеров мультимедиа](using-multimedia-timers.md)
</dt> </dl>

 

 