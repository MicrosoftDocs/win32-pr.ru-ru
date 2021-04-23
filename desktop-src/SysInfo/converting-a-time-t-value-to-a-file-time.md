---
description: Функции времени, включаемые во время выполнения C, используют \_ тип t для представления количества секунд, истекших с полуночи 1 января 1970. В следующем примере значение времени t преобразуется \_ в файловый момент с помощью функции Int32x32To64.
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: Преобразование значения time_t в файловый момент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee866efaed716fb12d2501337236afdb7cf641b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664716"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a><span data-ttu-id="95302-104">Преобразование значения времени \_ t в файловый момент</span><span class="sxs-lookup"><span data-stu-id="95302-104">Converting a time\_t Value to a File Time</span></span>

<span data-ttu-id="95302-105">Функции времени, включаемые во время выполнения C, используют \_ тип t для представления количества секунд, истекших с полуночи 1 января 1970.</span><span class="sxs-lookup"><span data-stu-id="95302-105">The time functions included in the C run-time use the time\_t type to represent the number of seconds elapsed since midnight, January 1, 1970.</span></span> <span data-ttu-id="95302-106">В следующем примере значение времени t преобразуется \_ в файловый момент с помощью функции [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) .</span><span class="sxs-lookup"><span data-stu-id="95302-106">The following example converts a time\_t value to a file time, using the [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) function.</span></span>


```C++
#include <windows.h>
#include <time.h>

void TimetToFileTime( time_t t, LPFILETIME pft )
{
    LONGLONG ll = Int32x32To64(t, 10000000) + 116444736000000000;
    pft->dwLowDateTime = (DWORD) ll;
    pft->dwHighDateTime = ll >>32;
}
```



<span data-ttu-id="95302-107">После получения времени файла это значение можно преобразовать в системное время с помощью функции [**филетиметосистемтиме**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) .</span><span class="sxs-lookup"><span data-stu-id="95302-107">After you have obtained a file time, you can convert this value to system time using the [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) function.</span></span>

 

 
