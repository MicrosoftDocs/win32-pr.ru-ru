---
description: Время прерываний — это время, прошедшее с момента последнего запуска системы (в 100-наносекундных интервалах).
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Время прерываний
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0da8fa92fc51cdceef6f0052dda7a2cd27d7b21b24d11bd8ec7b1ea4aff18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885514"
---
# <a name="interrupt-time"></a>Время прерываний

*Время прерываний* — это время, прошедшее с момента последнего запуска системы (в 100-наносекундных интервалах). Отсчет времени прерывания начинается с нуля при запуске системы и увеличивается в каждом прерывании такта по длине такта. Точная длина такта часов зависит от базового оборудования и может различаться между системами.

в отличие от [системного времени](system-time.md), счетчик времени прерывания не подлежит корректировке пользователями или службой времени Windows, что делает ее лучшим выбором для измерения коротких длительностей. Приложения, для которых требуется более высокая точность, чем количество времени прерывания, должны использовать [таймер высокого разрешения](../winmsg/about-timers.md). Используйте функцию [**куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) , чтобы получить частоту таймера высокого разрешения и функцию [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) для получения значения счетчика.

Для получения счетчика времени прерывания можно использовать функции [**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**куеринтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)и [**куерюнбиасединтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) . Несмещенное время прерываний означает, что учитывается только время, когда система находится в рабочем состоянии, поэтому счетчик времени прерывания не является "смещенным" по времени, которое система тратит на спящий режим или спящий режим.

**Windows server 2008, Windows Vista, Windows Server 2003 и Windows XP/2000:** функция [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) доступна начиная с Windows 7 и Windows Server 2008 R2.

Разрешение таймера, заданное функциями [**тимебегинпериод**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) и [**тиминдпериод**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) , влияет на разрешение функций [**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) и [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) . Однако увеличение разрешения таймера не рекомендуется, так как оно может снизить общую производительность системы и увеличить энергопотребление, предотвращая переход процессора в состояние энергосбережения. Вместо этого приложения должны использовать таймер высокого разрешения.

> [!Note]  
> функции [**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**куеринтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)и [**куерюнбиасединтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) выдают разные результаты для сборок отладки ("checked") Windows, так как количество и такты времени прерывания преобразуются примерно в 49 дней. Это помогает выявить ошибки, которые могут не произойти, пока система не будет работать в течение длительного времени. Проверенная сборка доступна подписчикам MSDN через веб-сайт [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) .

 

В следующем примере показано, как получить счетчик времени прерывания путем вызова функций [**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**куеринтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)и [**куерюнбиасединтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) . ссылка на библиотеку OneCore. lib при создании консольного приложения, вызывающего эти функции.


```C++
#include "stdafx.h"
#include <windows.h>
#include <realtimeapiset.h>

void InterruptTimeTest()
{
    ULONGLONG InterruptTime;
    ULONGLONG PreciseInterruptTime;
    ULONGLONG UnbiasedInterruptTime;
    ULONGLONG PreciseUnbiasedInterruptTime;

        // The interrupt time that QueryInterruptTime reports is based on the 
        // latest tick of the system clock timer. The system clock timer is 
        // the hardware timer that periodically generates interrupts for the 
        // system clock. The uniform period between system clock timer 
        // interrupts is referred to as a system clock tick, and is typically 
        // in the range of 0.5 milliseconds to 15.625 milliseconds, depending 
        // on the hardware platform. The interrupt time value retrieved by 
        // QueryInterruptTime is accurate within a system clock tick.

    QueryInterruptTime(&InterruptTime);
    printf("Interrupt time: %.7f seconds\n", 
            (double)InterruptTime/(double)10000000);

        // Precise interrupt time is more precise than the interrupt time that
        // QueryInterruptTime reports because the functions that report  
        // precise interrupt time read the timer hardware directly.

    QueryInterruptTimePrecise(&PreciseInterruptTime);
    printf("Precise interrupt time: %.7f seconds\n", 
            (double)PreciseInterruptTime/(double)10000000);

        // Unbiased interrupt time means that only time that the system is in 
        // the working state is counted. Therefore, the interrupt-time count 
        // is not biased by time the system spends in sleep or hibernation.

    QueryUnbiasedInterruptTime(&UnbiasedInterruptTime);
    printf("Unbiased interrupt time: %.7f seconds\n", 
            (double)UnbiasedInterruptTime/(double)10000000);

        // QueryUnbiasedInterruptTimePrecise gets an interrupt-time count
        // that is both unbiased and precise, as defined in the comments
        // included earlier in this example.

    QueryUnbiasedInterruptTimePrecise(&PreciseUnbiasedInterruptTime);
    printf("Precise unbiased interrupt time: %.7f seconds\n", 
            (double)PreciseUnbiasedInterruptTime/(double)10000000);

}

int main(void)
{
    void InterruptTimeTime();

    InterruptTimeTest();
    return(0);
}
```



Чтобы получить время, прошедшее с учетом времени в спящем режиме или спящем режиме, используйте функцию [**жеттикккаунт**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) или [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) или используйте счетчик производительности системного времени. Этот счетчик производительности можно получить из данных о производительности в разделе реестра **hKey \_ Performance \_ Data**. Возвращаемое значение является 8-байтовым значением. Дополнительные сведения см. в статье [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[**куеринтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[**куерюнбиасединтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[**тимебегинпериод**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[**тиминдпериод**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
