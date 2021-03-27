---
description: После начала сеанса трассировки событий можно использовать Трацесетинформатион, чтобы дать системе инструкцию вернуть дополнительные данные трассировки событий.
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: Извлечение дополнительных данных трассировки событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef864de40b924e0210603646d5ba5430d5d9b643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991308"
---
# <a name="retrieving-additional-event-tracing-data"></a><span data-ttu-id="33b03-103">Извлечение дополнительных данных трассировки событий</span><span class="sxs-lookup"><span data-stu-id="33b03-103">Retrieving Additional Event Tracing Data</span></span>

<span data-ttu-id="33b03-104">После начала сеанса трассировки событий можно использовать [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) , чтобы дать системе инструкцию вернуть дополнительные данные трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="33b03-104">Once you have begun an event tracing session, you can use [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to instruct the system to return additional event tracing data.</span></span> <span data-ttu-id="33b03-105">Дополнительные сведения будут помещены в раздел расширенных данных соответствующей трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="33b03-105">The additional information will be placed in the extended data section of the relevant event trace.</span></span>

<span data-ttu-id="33b03-106">В следующей процедуре описывается использование функции [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) для получения дополнительных данных из сеанса трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="33b03-106">The following procedure describes how to use the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function to retrieve additional data from an event tracing session.</span></span>

<span data-ttu-id="33b03-107">**Получение дополнительных данных трассировки событий**</span><span class="sxs-lookup"><span data-stu-id="33b03-107">**To retrieve additional event tracing data**</span></span>

1.  <span data-ttu-id="33b03-108">Начните сеанс с помощью вызова [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span><span class="sxs-lookup"><span data-stu-id="33b03-108">Start your session with a call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span></span>

    <span data-ttu-id="33b03-109">Дополнительные сведения см. в разделе [Настройка и запуск сеанса трассировки событий](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="33b03-109">For more information, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

2.  <span data-ttu-id="33b03-110">Вызовите [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) , чтобы задать дополнительные данные трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="33b03-110">Call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to set additional event tracing data.</span></span>

    <span data-ttu-id="33b03-111">Используйте перечисление [**\_ \_ класса сведений о событиях**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) в параметре *классинформатион* , чтобы описать дополнительные сведения, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="33b03-111">use the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration in the *ClassInformation* parameter to describe the additional information you wish to retrieve.</span></span> <span data-ttu-id="33b03-112">В следующем примере показано, как вызвать [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), используя обработчик сеанса, возвращенный из вызова [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea), и значение **трацепровидербинаритраккинг** из **\_ \_ класса info**.</span><span class="sxs-lookup"><span data-stu-id="33b03-112">The following example describes how to call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), using the session handle returned from the call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and the **TraceProviderBinaryTracking** value from **EVENT\_INFO\_CLASS**.</span></span>

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  <span data-ttu-id="33b03-113">Кроме того, можно использовать [**трацекуеринформатион**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) для получения сведений о текущих параметрах сеанса трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="33b03-113">Alternately, you can use [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) to retrieve information about the current event tracing session settings.</span></span>

    <span data-ttu-id="33b03-114">Как и [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**трацекуеринформатион**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) использует перечисление [**\_ \_ класса сведений о событиях**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) , чтобы описать, какие сведения нужно получить из системы.</span><span class="sxs-lookup"><span data-stu-id="33b03-114">Like [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) uses the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration to describe what information to retrieve from the system.</span></span>

 

 
