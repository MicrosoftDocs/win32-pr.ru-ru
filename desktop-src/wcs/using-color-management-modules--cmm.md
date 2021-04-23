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
ms.openlocfilehash: 518558305639f0699358f22fb3544698741cfedf
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/02/2021
ms.locfileid: "105719851"
---
# <a name="using-color-management-modules-cmm"></a><span data-ttu-id="f5487-110">Использование модулей управления цветом (CMM)</span><span class="sxs-lookup"><span data-stu-id="f5487-110">Using Color Management Modules (CMM)</span></span>

<span data-ttu-id="f5487-111">Модули управления цветом (Кммс) — это модули кода WCS, которые используют информацию в профилях устройств для выполнения преобразования цветов и сопоставления цветов.</span><span class="sxs-lookup"><span data-stu-id="f5487-111">Color Management Modules (CMMs) are modules of WCS code that use the information in device profiles to perform color conversion and color mapping.</span></span> <span data-ttu-id="f5487-112">Разработчикам приложений не следует реализовывать Кммс.</span><span class="sxs-lookup"><span data-stu-id="f5487-112">Application developers should not have to implement CMMs.</span></span> <span data-ttu-id="f5487-113">Корпорация Майкрософт предоставляет CMM по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f5487-113">Microsoft provides the default CMM.</span></span> <span data-ttu-id="f5487-114">Однако при написании программного обеспечения, требующего использования специализированных цветов и алгоритмов сопоставления цветов, вы можете создать его.</span><span class="sxs-lookup"><span data-stu-id="f5487-114">However, if you do write software that requires the use of specialized color conversion and color mapping algorithms, you may create one.</span></span>

> [!Note]  
> <span data-ttu-id="f5487-115">Точки входа в CMM *не* являются функциями API и не должны вызываться приложениями.</span><span class="sxs-lookup"><span data-stu-id="f5487-115">CMM entry points are *not* API functions and should not be called by applications.</span></span>

 

<span data-ttu-id="f5487-116">При установке Кммс программа установки регистрирует их в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="f5487-116">When CMMs are installed, the installation program registers them in the Windows registry.</span></span> <span data-ttu-id="f5487-117">Приложения могут перечислить зарегистрированные Кммс и выбрать один из них с помощью функции [**селекткмм**](/windows/win32/api/icm/nf-icm-selectcmm) .</span><span class="sxs-lookup"><span data-stu-id="f5487-117">Applications can enumerate the registered CMMs and select one using the [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) function.</span></span> <span data-ttu-id="f5487-118">В следующем примере приложения показано, как перечислить все зарегистрированные Кммс.</span><span class="sxs-lookup"><span data-stu-id="f5487-118">The following sample application demonstrates how to enumerate all registered CMMs.</span></span>


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
                 gszICMatcher, &amp;hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&amp;hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &amp;dwMaxName, &amp;dwMaxValue,
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
                   &amp;cjCMM,NULL,&amp;dwType,
                   chCMMFile,&amp;cjCMMFile) == ERROR_SUCCESS)
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



 

 




