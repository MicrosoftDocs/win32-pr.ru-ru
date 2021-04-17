---
description: Перечисление и освобождение служб
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: Перечисление и освобождение служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859abe590ccaf2f71df676d5989778d5b391be57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684249"
---
# <a name="enumerating-and-freeing-services"></a><span data-ttu-id="90c2d-103">Перечисление и освобождение служб</span><span class="sxs-lookup"><span data-stu-id="90c2d-103">Enumerating and Freeing Services</span></span>

<span data-ttu-id="90c2d-104">Приложение ELS вызывает функцию [**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) для определения служб, доступных в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="90c2d-104">The ELS application calls the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function to determine the services that are available on the operating system.</span></span> <span data-ttu-id="90c2d-105">Функцию можно использовать для перечисления всех доступных служб ELS или для фильтрации служб на основе условий поиска, предоставляемых приложением.</span><span class="sxs-lookup"><span data-stu-id="90c2d-105">The function can be used either to enumerate all available ELS services, or to filter the services based on application-provided search criteria.</span></span> <span data-ttu-id="90c2d-106">Когда службы больше не нужны, приложение вызывает [**маппингфрисервицес**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span><span class="sxs-lookup"><span data-stu-id="90c2d-106">When services are no longer needed, the application calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span></span>

## <a name="get-all-supported-services"></a><span data-ttu-id="90c2d-107">Получить все поддерживаемые службы</span><span class="sxs-lookup"><span data-stu-id="90c2d-107">Get All Supported Services</span></span>

<span data-ttu-id="90c2d-108">В этом примере кода показано использование [**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) и [**маппингфрисервицес**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) для перечисления и последующего освобождения всех доступных служб в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="90c2d-108">This code example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all available services on the operating system.</span></span> <span data-ttu-id="90c2d-109">Для этого приложение передает **значение NULL** для параметра *поптионс* объекта **маппингжетсервицес**.</span><span class="sxs-lookup"><span data-stu-id="90c2d-109">To do this, the application passes **NULL** for the *pOptions* parameter of **MappingGetServices**.</span></span>


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



## <a name="get-specific-services"></a><span data-ttu-id="90c2d-110">Получение конкретных служб</span><span class="sxs-lookup"><span data-stu-id="90c2d-110">Get Specific Services</span></span>

<span data-ttu-id="90c2d-111">В следующем примере показано использование [**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) и [**маппингфрисервицес**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) для перечисления и последующего освобождения всех служб категории "распознавание языка".</span><span class="sxs-lookup"><span data-stu-id="90c2d-111">The next example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all services of category "Language Detection".</span></span> <span data-ttu-id="90c2d-112">Дополнительные сведения об этой категории служб см. в разделе [**Microsoft распознавание языка**](microsoft-language-detection.md).</span><span class="sxs-lookup"><span data-stu-id="90c2d-112">For more information about this service category, see [**Microsoft Language Detection**](microsoft-language-detection.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="90c2d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="90c2d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90c2d-114">Использование расширенных лингвистических служб</span><span class="sxs-lookup"><span data-stu-id="90c2d-114">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="90c2d-115">**маппингфрисервицес**</span><span class="sxs-lookup"><span data-stu-id="90c2d-115">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[<span data-ttu-id="90c2d-116">**маппингжетсервицес**</span><span class="sxs-lookup"><span data-stu-id="90c2d-116">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



