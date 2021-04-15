---
description: Время прерываний — это время, прошедшее с момента последнего запуска системы (в 100-наносекундных интервалах).
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Время прерываний
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6018d97ab0eecd1182c02b734357ca13fbe12632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662545"
---
# <a name="interrupt-time"></a><span data-ttu-id="ebf5c-103">Время прерываний</span><span class="sxs-lookup"><span data-stu-id="ebf5c-103">Interrupt Time</span></span>

<span data-ttu-id="ebf5c-104">*Время прерываний* — это время, прошедшее с момента последнего запуска системы (в 100-наносекундных интервалах).</span><span class="sxs-lookup"><span data-stu-id="ebf5c-104">*Interrupt time* is the amount of time since the system was last started, in 100-nanosecond intervals.</span></span> <span data-ttu-id="ebf5c-105">Отсчет времени прерывания начинается с нуля при запуске системы и увеличивается в каждом прерывании такта по длине такта.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-105">The interrupt-time count begins at zero when the system starts and is incremented at each clock interrupt by the length of a clock tick.</span></span> <span data-ttu-id="ebf5c-106">Точная длина такта часов зависит от базового оборудования и может различаться между системами.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-106">The exact length of a clock tick depends on underlying hardware and can vary between systems.</span></span>

<span data-ttu-id="ebf5c-107">В отличие от [системного времени](system-time.md), счетчик времени прерывания не подлежит корректировке пользователями или службой времени Windows, что делает ее лучшим выбором для измерения коротких длительностей.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-107">Unlike [system time](system-time.md), the interrupt-time count is not subject to adjustments by users or the Windows time service, making it a better choice for measuring short durations.</span></span> <span data-ttu-id="ebf5c-108">Приложения, для которых требуется более высокая точность, чем количество времени прерывания, должны использовать [таймер высокого разрешения](../winmsg/about-timers.md).</span><span class="sxs-lookup"><span data-stu-id="ebf5c-108">Applications that require greater precision than the interrupt-time count should use a [high-resolution timer](../winmsg/about-timers.md).</span></span> <span data-ttu-id="ebf5c-109">Используйте функцию [**куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) , чтобы получить частоту таймера высокого разрешения и функцию [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) для получения значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-109">Use the [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) function to retrieve the frequency of the high-resolution timer and the [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) function to retrieve the counter's value.</span></span>

<span data-ttu-id="ebf5c-110">Для получения счетчика времени прерывания можно использовать функции [**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**куеринтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)и [**куерюнбиасединтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) .</span><span class="sxs-lookup"><span data-stu-id="ebf5c-110">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions can be used to retrieve the interrupt-time count.</span></span> <span data-ttu-id="ebf5c-111">Несмещенное время прерываний означает, что учитывается только время, когда система находится в рабочем состоянии, поэтому счетчик времени прерывания не является "смещенным" по времени, которое система тратит на спящий режим или спящий режим.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-111">Unbiased interrupt-time means that only time that the system is in the working state is counted—therefore, the interrupt-time count is not "biased" by time the system spends in sleep or hibernation.</span></span>

<span data-ttu-id="ebf5c-112">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP/2000:** Функция [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) доступна начиная с Windows 7 и windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-112">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:** The [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) function is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="ebf5c-113">Разрешение таймера, заданное функциями [**тимебегинпериод**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) и [**тиминдпериод**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) , влияет на разрешение функций [**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) и [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) .</span><span class="sxs-lookup"><span data-stu-id="ebf5c-113">The timer resolution set by the [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) functions affects the resolution of the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) and [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) functions.</span></span> <span data-ttu-id="ebf5c-114">Однако увеличение разрешения таймера не рекомендуется, так как оно может снизить общую производительность системы и увеличить энергопотребление, предотвращая переход процессора в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-114">However, increasing the timer resolution is not recommended because it can reduce overall system performance and increase power consumption by preventing the processor from entering power-saving states.</span></span> <span data-ttu-id="ebf5c-115">Вместо этого приложения должны использовать таймер высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-115">Instead, applications should use a high-resolution timer.</span></span>

> [!Note]  
> <span data-ttu-id="ebf5c-116">Функции [**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**куеринтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)и [**куерюнбиасединтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) выдают разные результаты для отладочных сборок Windows, так как количество времени прерывания и число тактов увеличивается на 49 дней.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-116">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days.</span></span> <span data-ttu-id="ebf5c-117">Это помогает выявить ошибки, которые могут не произойти, пока система не будет работать в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-117">This helps to identify bugs that might not occur until the system has been running for a long time.</span></span> <span data-ttu-id="ebf5c-118">Проверенная сборка доступна подписчикам MSDN через веб-сайт [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ebf5c-118">The checked build is available to MSDN subscribers through the [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) Web site.</span></span>

 

<span data-ttu-id="ebf5c-119">В следующем примере показано, как получить счетчик времени прерывания путем вызова функций [**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**куеринтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)и [**куерюнбиасединтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) .</span><span class="sxs-lookup"><span data-stu-id="ebf5c-119">The following example shows how to retrieve the interrupt-time count by calling the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions.</span></span> <span data-ttu-id="ebf5c-120">Ссылка на библиотеку OneCore. lib при создании консольного приложения, вызывающего эти функции.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-120">Link to the OneCore.lib library when you build a console application that calls these functions.</span></span>


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



<span data-ttu-id="ebf5c-121">Чтобы получить время, прошедшее с учетом времени в спящем режиме или спящем режиме, используйте функцию [**жеттикккаунт**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) или [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) или используйте счетчик производительности системного времени.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-121">To retrieve elapsed time that accounts for sleep or hibernation, use the [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) or [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) function, or use the System Up Time performance counter.</span></span> <span data-ttu-id="ebf5c-122">Этот счетчик производительности можно получить из данных о производительности в разделе реестра **hKey \_ Performance \_ Data**.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-122">This performance counter can be retrieved from the performance data in the registry key **HKEY\_PERFORMANCE\_DATA**.</span></span> <span data-ttu-id="ebf5c-123">Возвращаемое значение является 8-байтовым значением.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-123">The value returned is an 8-byte value.</span></span> <span data-ttu-id="ebf5c-124">Дополнительные сведения см. в статье [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="ebf5c-124">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebf5c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ebf5c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebf5c-126">**куеринтеррупттиме**</span><span class="sxs-lookup"><span data-stu-id="ebf5c-126">**QueryInterruptTime**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[<span data-ttu-id="ebf5c-127">**куеринтеррупттимепреЦисе**</span><span class="sxs-lookup"><span data-stu-id="ebf5c-127">**QueryInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="ebf5c-128">**куерюнбиасединтеррупттиме**</span><span class="sxs-lookup"><span data-stu-id="ebf5c-128">**QueryUnbiasedInterruptTime**</span></span>](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[<span data-ttu-id="ebf5c-129">**куерюнбиасединтеррупттимепреЦисе**</span><span class="sxs-lookup"><span data-stu-id="ebf5c-129">**QueryUnbiasedInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="ebf5c-130">**тимебегинпериод**</span><span class="sxs-lookup"><span data-stu-id="ebf5c-130">**timeBeginPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[<span data-ttu-id="ebf5c-131">**тиминдпериод**</span><span class="sxs-lookup"><span data-stu-id="ebf5c-131">**timeEndPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
