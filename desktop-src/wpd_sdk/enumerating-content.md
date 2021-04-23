---
description: Перечисление содержимого
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: Перечисление содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662385"
---
# <a name="enumerating-content"></a><span data-ttu-id="d988e-103">Перечисление содержимого</span><span class="sxs-lookup"><span data-stu-id="d988e-103">Enumerating Content</span></span>

<span data-ttu-id="d988e-104">Содержимое устройства (будь то содержимое, которое является папкой, телефонной книгой, видео или изображением по-прежнему) называется объектом в API WPD.</span><span class="sxs-lookup"><span data-stu-id="d988e-104">The content on a device (whether that content is a folder, a phone book, a video, or a still image) is called an object in the WPD API.</span></span> <span data-ttu-id="d988e-105">На эти объекты ссылаются идентификаторы объектов, описанные в свойствах.</span><span class="sxs-lookup"><span data-stu-id="d988e-105">These objects are referenced by object identifiers and described by properties.</span></span> <span data-ttu-id="d988e-106">Вы можете перечислить объекты на устройстве, вызвав методы в [**интерфейсе ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), [**интерфейсе ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)и [**интерфейсе иенумпортабледевицеобжектидс**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span><span class="sxs-lookup"><span data-stu-id="d988e-106">You can enumerate the objects on a device by calling methods in the [**IPortableDevice interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), the [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent), and the [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span>

<span data-ttu-id="d988e-107">Пример приложения демонстрирует перечисление содержимого в функции Енумератеаллконтент, которая находится в модуле Контентенумератион. cpp.</span><span class="sxs-lookup"><span data-stu-id="d988e-107">The sample application demonstrates content enumeration in the EnumerateAllContent function that is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="d988e-108">Эта функция, в свою очередь, вызывает функцию Рекурсивинумерате, которая просматривает иерархию объектов, найденных на выбранном устройстве, и возвращает идентификатор объекта для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="d988e-108">This function, in turn, calls a RecursiveEnumerate function that walks the hierarchy of objects found on the selected device and returns an object identifier for each object.</span></span>

<span data-ttu-id="d988e-109">Как уже отмечалось, функция Рекурсивинумерате извлекает идентификатор объекта для каждого объекта, найденного на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d988e-109">As noted, the RecursiveEnumerate function retrieves an object identifier for each object found on the device.</span></span> <span data-ttu-id="d988e-110">Идентификатор объекта является строковым значением.</span><span class="sxs-lookup"><span data-stu-id="d988e-110">The object identifier is a string value.</span></span> <span data-ttu-id="d988e-111">Когда приложение получает этот идентификатор, оно может получить более описательные сведения об объекте (например, имя объекта, идентификатор родителя объекта и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d988e-111">Once your application retrieves this identifier, it can obtain more descriptive object information (such as the object's name, the identifier for the object's parent, and so on).</span></span> <span data-ttu-id="d988e-112">Эти описательные сведения называются свойствами объекта (или метаданными).</span><span class="sxs-lookup"><span data-stu-id="d988e-112">This descriptive information is referred to as object properties (or metadata).</span></span> <span data-ttu-id="d988e-113">Приложение может извлекать эти свойства путем вызова членов [**интерфейса ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).</span><span class="sxs-lookup"><span data-stu-id="d988e-113">Your application can retrieve these properties by calling members of the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).</span></span>

<span data-ttu-id="d988e-114">Функция Енумератеаллконтент начинается с получения указателя на [**интерфейс ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span><span class="sxs-lookup"><span data-stu-id="d988e-114">The EnumerateAllContent function begins by retrieving a pointer to an [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span></span> <span data-ttu-id="d988e-115">Он извлекает этот указатель, вызывая метод [**ипортабледевице:: Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .</span><span class="sxs-lookup"><span data-stu-id="d988e-115">It retrieves this pointer by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="d988e-116">После получения указателя на интерфейс Ипортабледевицеконтент функция Енумератеаллконтент вызывает функцию Рекурсивинумерате, которая просматривает иерархию объектов, найденных на данном устройстве, и возвращает идентификатор объекта для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="d988e-116">Once it retrieves the pointer to the IPortableDeviceContent interface, the EnumerateAllContent function calls the RecursiveEnumerate function, which walks the hierarchy of objects found on the given device and returns an object identifier for each.</span></span>

<span data-ttu-id="d988e-117">Функция Рекурсивинумерате начинается с получения указателя на [**интерфейс иенумпортабледевицеобжектидс**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span><span class="sxs-lookup"><span data-stu-id="d988e-117">The RecursiveEnumerate function begins by retrieving a pointer to an [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span> <span data-ttu-id="d988e-118">Этот интерфейс предоставляет методы, используемые приложением для перемещения по списку объектов, найденных на данном устройстве.</span><span class="sxs-lookup"><span data-stu-id="d988e-118">This interface exposes the methods that an application uses to navigate the list of objects found on a given device.</span></span>

<span data-ttu-id="d988e-119">В этом примере функция Рекурсивинумерате вызывает метод [**иенумпортабледевицеобжектидс:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) для прохода по списку объектов.</span><span class="sxs-lookup"><span data-stu-id="d988e-119">In this sample, the RecursiveEnumerate function calls the [**IEnumPortableDeviceObjectIDs::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method to traverse the list of objects.</span></span>

<span data-ttu-id="d988e-120">Каждый вызов метода [**иенумпортабледевицеобжектс:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) запрашивает пакет из 10 идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="d988e-120">Each call to the [**IEnumPortableDeviceObjects::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method requests a batch of 10 identifiers.</span></span> <span data-ttu-id="d988e-121">(Это значение указывается ЧИСЛОм \_ ОБЪЕКТЫ \_ для \_ запроса константы, которая указывается в качестве первого аргумента.)</span><span class="sxs-lookup"><span data-stu-id="d988e-121">(This value is specified by the NUM\_OBJECTS\_TO\_REQUEST constant that is supplied as the first argument.)</span></span>


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
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
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
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



## <a name="related-topics"></a><span data-ttu-id="d988e-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d988e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d988e-123">**Интерфейс Иенумпортабледевицеобжектидс**</span><span class="sxs-lookup"><span data-stu-id="d988e-123">**IEnumPortableDeviceObjectIDs Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="d988e-124">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="d988e-124">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="d988e-125">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="d988e-125">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="d988e-126">**Интерфейс Ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="d988e-126">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="d988e-127">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="d988e-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



