---
description: Функции времени, включаемые во время выполнения C, используют \_ тип t для представления количества секунд, истекших с полуночи 1 января 1970. В следующем примере значение времени t преобразуется \_ в файловый момент с помощью функции Int32x32To64.
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: Преобразование значения time_t в файловый момент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fc7161e55bb235690f5c7d5fe0f4cd575bd7c902d5357606290def0509f6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764515"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a>Преобразование значения времени \_ t в файловый момент

Функции времени, включаемые во время выполнения C, используют \_ тип t для представления количества секунд, истекших с полуночи 1 января 1970. В следующем примере значение времени t преобразуется \_ в файловый момент с помощью функции [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) .


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



После получения времени файла это значение можно преобразовать в системное время с помощью функции [**филетиметосистемтиме**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) .

 

 
