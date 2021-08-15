---
description: После начала сеанса трассировки событий можно использовать Трацесетинформатион, чтобы дать системе инструкцию вернуть дополнительные данные трассировки событий.
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: Извлечение дополнительных данных трассировки событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae65e516a63154fb76d3d558e02e9533e58e119e977f851c2404f0a218ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393902"
---
# <a name="retrieving-additional-event-tracing-data"></a>Извлечение дополнительных данных трассировки событий

После начала сеанса трассировки событий можно использовать [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) , чтобы дать системе инструкцию вернуть дополнительные данные трассировки событий. Дополнительные сведения будут помещены в раздел расширенных данных соответствующей трассировки событий.

В следующей процедуре описывается использование функции [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) для получения дополнительных данных из сеанса трассировки событий.

**Получение дополнительных данных трассировки событий**

1.  Начните сеанс с помощью вызова [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea).

    Дополнительные сведения см. в разделе [Настройка и запуск сеанса трассировки событий](configuring-and-starting-an-event-tracing-session.md).

2.  Вызовите [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) , чтобы задать дополнительные данные трассировки событий.

    Используйте перечисление [**\_ \_ класса сведений о событиях**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) в параметре *классинформатион* , чтобы описать дополнительные сведения, которые необходимо получить. В следующем примере показано, как вызвать [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), используя обработчик сеанса, возвращенный из вызова [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea), и значение **трацепровидербинаритраккинг** из **\_ \_ класса info**.

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  Кроме того, можно использовать [**трацекуеринформатион**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) для получения сведений о текущих параметрах сеанса трассировки событий.

    Как и [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**трацекуеринформатион**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) использует перечисление [**\_ \_ класса сведений о событиях**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) , чтобы описать, какие сведения нужно получить из системы.

 

 
