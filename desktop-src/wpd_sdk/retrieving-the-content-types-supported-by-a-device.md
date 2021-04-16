---
description: Получение типов содержимого, поддерживаемых устройством
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Получение типов содержимого, поддерживаемых устройством
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e1b37160065be3130fca687f5f3277d9108a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712479"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a><span data-ttu-id="ac9b5-103">Получение типов содержимого, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="ac9b5-103">Retrieving the Content Types Supported by a Device</span></span>

<span data-ttu-id="ac9b5-104">Как указано в разделе [Получение списка функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md) , портативные устройства Windows могут поддерживать одну или несколько функциональных категорий.</span><span class="sxs-lookup"><span data-stu-id="ac9b5-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="ac9b5-105">Любая заданная Функциональная категория может поддерживать один или несколько типов содержимого.</span><span class="sxs-lookup"><span data-stu-id="ac9b5-105">Any given functional category may support one or more content types.</span></span> <span data-ttu-id="ac9b5-106">Например, Категория хранилища может поддерживать типы содержимого папок, аудио и изображений.</span><span class="sxs-lookup"><span data-stu-id="ac9b5-106">For example, the storage category may support content types of folder, audio, and image.</span></span>

<span data-ttu-id="ac9b5-107">Описание типов содержимого, поддерживаемых WPD, см. в разделе [**\_ тип содержимого WPD \_ \_ ALL**](wpd-content-type-all.md) .</span><span class="sxs-lookup"><span data-stu-id="ac9b5-107">For a description of the content types supported by WPD, see the [**WPD\_CONTENT\_TYPE\_ALL**](wpd-content-type-all.md) topic.</span></span>

<span data-ttu-id="ac9b5-108">Функция Листсуппортедконтенттипес в модуле Девицекапабилитиес. cpp демонстрирует извлечение типов содержимого для функциональных категорий, поддерживаемых выбранным устройством.</span><span class="sxs-lookup"><span data-stu-id="ac9b5-108">The ListSupportedContentTypes function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="ac9b5-109">Приложение может извлекать функциональные категории, поддерживаемые устройством, с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ac9b5-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="ac9b5-110">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac9b5-110">Interface</span></span>                                                                                      | <span data-ttu-id="ac9b5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ac9b5-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="ac9b5-112">**Интерфейс Ипортабледевицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="ac9b5-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="ac9b5-113">Предоставляет доступ к методам получения функциональной категории.</span><span class="sxs-lookup"><span data-stu-id="ac9b5-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="ac9b5-114">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="ac9b5-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="ac9b5-115">Используется для перечисления и хранения данных функциональной категории.</span><span class="sxs-lookup"><span data-stu-id="ac9b5-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="ac9b5-116">Код, обнаруженный в функции Листсуппортедконтенттипес, почти идентичен коду, обнаруженному в функции Листфунктионалкатегориес.</span><span class="sxs-lookup"><span data-stu-id="ac9b5-116">The code found in the ListSupportedContentTypes function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="ac9b5-117">(См. раздел [Получение функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md) .) Единственное отличие заключается в вызове метода [**ипортабледевицекапабилитиес:: жетсуппортедконтенттипес**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) , который находится в цикле, который проходит по функциональным категориям.</span><span class="sxs-lookup"><span data-stu-id="ac9b5-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) method, which appears within the loop that iterates through the functional categories.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories   = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}

// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get all functional categories supported by the device.
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name and supported content types.
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.

            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the content types supported for this category
                CComPtr<IPortableDevicePropVariantCollection> pContentTypes;
                hr = pCapabilities->GetSupportedContentTypes(*pv.puuid, &pContentTypes);
                if (SUCCEEDED(hr))
                {
                    printf("Supported Content Types: ");
                    DisplayContentTypes(pContentTypes);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get supported content types from the device, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="ac9b5-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ac9b5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac9b5-119">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="ac9b5-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="ac9b5-120">**Интерфейс Ипортабледевицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="ac9b5-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="ac9b5-121">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="ac9b5-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="ac9b5-122">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="ac9b5-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



