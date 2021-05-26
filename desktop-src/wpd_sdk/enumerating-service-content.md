---
description: Перечисление содержимого службы
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Перечисление содержимого службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b701bdab867e96bc9658e2624ea18aa65dfc33
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424254"
---
# <a name="enumerating-service-content"></a><span data-ttu-id="d57f6-103">Перечисление содержимого службы</span><span class="sxs-lookup"><span data-stu-id="d57f6-103">Enumerating Service Content</span></span>

<span data-ttu-id="d57f6-104">После открытия службы приложение может начать выполнять операции, связанные с обслуживанием.</span><span class="sxs-lookup"><span data-stu-id="d57f6-104">After your application opens a service, it can begin performing service-related operations.</span></span> <span data-ttu-id="d57f6-105">В случае с приложением Впдсервицесаписампле одной из этих операций является перечисление содержимого для данной службы контактов.</span><span class="sxs-lookup"><span data-stu-id="d57f6-105">In the case of the WpdServicesApiSample application, one of these operations is the enumeration of content for a given Contacts service.</span></span> <span data-ttu-id="d57f6-106">В следующей таблице описаны используемые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="d57f6-106">The following table describes the interfaces used.</span></span>



| <span data-ttu-id="d57f6-107">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="d57f6-107">Interface</span></span>                                                            | <span data-ttu-id="d57f6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d57f6-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d57f6-109">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="d57f6-109">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="d57f6-110">Используется для получения интерфейса IPortableDeviceContent2 для доступа к содержимому службы.</span><span class="sxs-lookup"><span data-stu-id="d57f6-110">Used to retrieve the IPortableDeviceContent2 interface to access content on the service.</span></span>         |
| [<span data-ttu-id="d57f6-111">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="d57f6-111">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="d57f6-112">Используется для получения интерфейса Иенумпортабледевицеобжектидс для перечисления объектов в службе.</span><span class="sxs-lookup"><span data-stu-id="d57f6-112">Used to retrieve the IEnumPortableDeviceObjectIDs interface to enumerate objects on the service.</span></span> |
| [<span data-ttu-id="d57f6-113">**иенумпортабледевицеобжектидс**</span><span class="sxs-lookup"><span data-stu-id="d57f6-113">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | <span data-ttu-id="d57f6-114">Используется для перечисления объектов в службе.</span><span class="sxs-lookup"><span data-stu-id="d57f6-114">Used to enumerate objects on the service.</span></span>                                                        |



 

<span data-ttu-id="d57f6-115">Код перечисления содержимого находится в модуле Контентенумератион. cpp.</span><span class="sxs-lookup"><span data-stu-id="d57f6-115">The content enumeration code is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="d57f6-116">Этот код находится в методах **енумератеаллконтент** и **рекурсивинумерате** .</span><span class="sxs-lookup"><span data-stu-id="d57f6-116">This code resides in the **EnumerateAllContent** and the **RecursiveEnumerate** methods.</span></span> <span data-ttu-id="d57f6-117">Первый метод вызывает второй.</span><span class="sxs-lookup"><span data-stu-id="d57f6-117">The former method calls the latter.</span></span>

<span data-ttu-id="d57f6-118">Метод **енумератеконтент** принимает указатель на объект [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) в качестве одного параметра.</span><span class="sxs-lookup"><span data-stu-id="d57f6-118">The **EnumerateContent** method takes a pointer to an [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) object as its one parameter.</span></span> <span data-ttu-id="d57f6-119">Этот объект соответствует службе, открытой ранее приложением при вызове метода [**ипортабледевицесервице:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) .</span><span class="sxs-lookup"><span data-stu-id="d57f6-119">This object corresponds to a service that the application opened earlier when it called the [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) method.</span></span>

<span data-ttu-id="d57f6-120">Метод **енумератеконтент** создает объект [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) и передает этот объект в метод [**ипортабледевицесервице:: Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) .</span><span class="sxs-lookup"><span data-stu-id="d57f6-120">The **EnumerateContent** method creates an [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) object and passes this object to the [**IPortableDeviceService::Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) method.</span></span> <span data-ttu-id="d57f6-121">Этот метод, в свою очередь, получает содержимое на корневом уровне службы, а затем рекурсивно начинает получать содержимое, найденное под корнем.</span><span class="sxs-lookup"><span data-stu-id="d57f6-121">This method, in turn, retrieves the content at the root level of the service, and then recursively begins to retrieve content found beneath the root.</span></span>

<span data-ttu-id="d57f6-122">Следующий код соответствует методу **енумератеконтент** .</span><span class="sxs-lookup"><span data-stu-id="d57f6-122">The following code corresponds to the **EnumerateContent** method.</span></span>


```C++
// Enumerate all content on the service starting with the
// "DEVICE" object
void EnumerateAllContent(
    IPortableDeviceService* pService)
{
    HRESULT                          hr = S_OK;
    CComPtr<IPortableDeviceContent2> pContent;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    hr = pService->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="d57f6-123">Следующий код соответствует методу **рекурсивинумерате** .</span><span class="sxs-lookup"><span data-stu-id="d57f6-123">The following code corresponds to the **RecursiveEnumerate** method.</span></span> <span data-ttu-id="d57f6-124">Метод Рекурсивинумерате создает интерфейс **иенумпортабледевицеобжектидс** для заданного родительского объекта и вызывает **Иенумпортабледевицеобжектидс:: Next**, получая пакет непосредственных дочерних объектов.</span><span class="sxs-lookup"><span data-stu-id="d57f6-124">The RecursiveEnumerate method instantiates an **IEnumPortableDeviceObjectIDs** interface for the supplied parent object, and calls **IEnumPortableDeviceObjectIDs::Next**, retrieving a batch of immediate child objects.</span></span> <span data-ttu-id="d57f6-125">Для каждого дочернего объекта Рекурсивинумерате вызывается снова, чтобы вернуть дочерние объекты-потомки и т. д.</span><span class="sxs-lookup"><span data-stu-id="d57f6-125">For each child object, RecursiveEnumerate is called again to return its descendent child objects, and so on.</span></span>


```C++
// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                   pszObjectID,
    IPortableDeviceContent2* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent2, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="d57f6-126">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d57f6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d57f6-127">**иенумпортабледевицеобжектидс**</span><span class="sxs-lookup"><span data-stu-id="d57f6-127">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="d57f6-128">**Интерфейс IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="d57f6-128">**IPortableDeviceContent2 Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="d57f6-129">**Интерфейс Ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="d57f6-129">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="d57f6-130">Открытие службы</span><span class="sxs-lookup"><span data-stu-id="d57f6-130">Opening a Service</span></span>](opening-a-service.md)
</dt> <dt>

[<span data-ttu-id="d57f6-131">впдсервицесаписампле</span><span class="sxs-lookup"><span data-stu-id="d57f6-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



