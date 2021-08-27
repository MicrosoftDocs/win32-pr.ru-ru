---
description: Перечисление и освобождение служб
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: Перечисление и освобождение служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6472851fbf5f7f84a499d2e9e04804279d397f31452d9617a8868e05cb8ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086614"
---
# <a name="enumerating-and-freeing-services"></a>Перечисление и освобождение служб

Приложение ELS вызывает функцию [**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) для определения служб, доступных в операционной системе. Функцию можно использовать для перечисления всех доступных служб ELS или для фильтрации служб на основе условий поиска, предоставляемых приложением. Когда службы больше не нужны, приложение вызывает [**маппингфрисервицес**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).

## <a name="get-all-supported-services"></a>Получить все поддерживаемые службы

В этом примере кода показано использование [**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) и [**маппингфрисервицес**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) для перечисления и последующего освобождения всех доступных служб в операционной системе. Для этого приложение передает **значение NULL** для параметра *поптионс* объекта **маппингжетсервицес**.


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    // Get all installed ELS services.
    Result = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="get-specific-services"></a>Получение конкретных служб

В следующем примере показано использование [**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) и [**маппингфрисервицес**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) для перечисления и последующего освобождения всех служб категории "распознавание языка". Дополнительные сведения об этой категории служб см. в разделе [**Microsoft распознавание языка**](microsoft-language-detection.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);

    // Use the Language Auto-Detection category to enumerate
    // all language detection services.
    EnumOptions.pszCategory = L"Language Detection";

    // Execute the enumeration:
    Result = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование расширенных лингвистических служб](using-extended-linguistic-services.md)
</dt> <dt>

[**маппингфрисервицес**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



