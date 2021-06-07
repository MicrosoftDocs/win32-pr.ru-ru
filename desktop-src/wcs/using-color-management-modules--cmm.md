---
title: Использование модулей управления цветом (CMM)
description: Модули управления цветом (Кммс) — это модули кода WCS, которые используют информацию в профилях устройств для выполнения преобразования цветов и сопоставления цветов.
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- Цветовая система Windows (WCS), модуль управления цветом (CMM)
- WCS (цветовая система Windows), модуль управления цветом (CMM)
- Управление цветом изображений, модуль управления цветом (CMM)
- Управление цветом, модуль управления цветом (CMM)
- цвета, модуль управления цветом (CMM)
- Модуль управления цветом (CMM)
- CMM (модуль управления цветом)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b12a087bfc972ffcbd7f9fb083a9d73d669f134
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386903"
---
# <a name="using-color-management-modules-cmm"></a>Использование модулей управления цветом (CMM)

Модули управления цветом (Кммс) — это модули кода WCS, которые используют информацию в профилях устройств для выполнения преобразования цветов и сопоставления цветов. Разработчикам приложений не следует реализовывать Кммс. Корпорация Майкрософт предоставляет CMM по умолчанию. Однако при написании программного обеспечения, требующего использования специализированных цветов и алгоритмов сопоставления цветов, вы можете создать его.

> [!Note]  
> Точки входа в CMM *не* являются функциями API и не должны вызываться приложениями.

 

При установке Кммс программа установки регистрирует их в реестре Windows. Приложения могут перечислить зарегистрированные Кммс и выбрать один из них с помощью функции [**селекткмм**](/windows/win32/api/icm/nf-icm-selectcmm) . В следующем примере приложения показано, как перечислить все зарегистрированные Кммс.


```C++
#include <stdio.h>
#include <stdlib.h>
#include <stddef.h>
#include <string.h>
#include <mbstring.h>
#include <windows.h>
#include <icm.h>

#ifdef WINDOWS_98
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\ICM\\ICMatchers");
#else
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ICMatchers");
#endif

_CRTAPI1 main (int argc, char *argv[])
{
    DWORD dwNumCMM = 0;

    HANDLE hkCMM;
    DWORD dwErr = RegCreateKey(HKEY_LOCAL_MACHINE,
                 gszICMatcher, &hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &dwMaxName, &dwMaxValue,
                                NULL, NULL);
    TCHAR chCMM[dwMaxName];
    ULONG cjCMM = sizeof(chCMM)/sizeof(chCMM[0]);
    DWORD dwType;
    TCHAR chCMMFile[dwMaxValue];
    ULONG cjCMMFile = sizeof(chCMMFile)/sizeof(chCMMFile[0]);

    if (dwErr != ERROR_SUCCESS)
    {
        printf("Could not open ICMatcher registry key: %d\n", dwErr);
    }

    if (dwErr == ERROR_SUCCESS)
    {
        while (RegEnumValue(
                   hkCMM,dwNumCMM,chCMM,
                   &cjCMM,NULL,&dwType,
                   chCMMFile,&cjCMMFile) == ERROR_SUCCESS)
        {
            if (dwType == REG_SZ)
            {
                printf("%d: %-80s - %-80s\n",dwNumCMM,chCMM,chCMMFile);
            }
            else
            {
                printf("%d: error\n");
            }

            dwNumCMM++;
            cjCMM = sizeof(chCMM);
            cjCMMFile = sizeof(chCMMFile);
        }
    }

    RegCloseKey(hkCMM);
}
```



 

 




