---
description: Получение функциональных категорий, поддерживаемых устройством
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Получение функциональных категорий, поддерживаемых устройством
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514c6255fa089dc235b5edd8a25b5ef581aee84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911360"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a><span data-ttu-id="8ded8-103">Получение функциональных категорий, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="8ded8-103">Retrieving the Functional Categories Supported by a Device</span></span>

<span data-ttu-id="8ded8-104">Портативные устройства Windows могут поддерживать одну или несколько функциональных категорий.</span><span class="sxs-lookup"><span data-stu-id="8ded8-104">Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="8ded8-105">Эти категории описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8ded8-105">These categories are described in the following table.</span></span>



| <span data-ttu-id="8ded8-106">Категория</span><span class="sxs-lookup"><span data-stu-id="8ded8-106">Category</span></span>                    | <span data-ttu-id="8ded8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8ded8-107">Description</span></span>                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ded8-108">Запись звука</span><span class="sxs-lookup"><span data-stu-id="8ded8-108">Audio capture</span></span>               | <span data-ttu-id="8ded8-109">Устройство можно использовать для записи звука.</span><span class="sxs-lookup"><span data-stu-id="8ded8-109">The device can be used to record audio.</span></span>                                              |
| <span data-ttu-id="8ded8-110">Сведения о подготовке к просмотру</span><span class="sxs-lookup"><span data-stu-id="8ded8-110">Rendering information</span></span>       | <span data-ttu-id="8ded8-111">Устройство предоставляет данные, описывающие файлы мультимедиа, которые могут быть отображены.</span><span class="sxs-lookup"><span data-stu-id="8ded8-111">The device provides data describing the media files that it is capable of rendering.</span></span> |
| <span data-ttu-id="8ded8-112">Служба коротких сообщений (SMS)</span><span class="sxs-lookup"><span data-stu-id="8ded8-112">Short message service (SMS)</span></span> | <span data-ttu-id="8ded8-113">Устройство поддерживает текстовые сообщения.</span><span class="sxs-lookup"><span data-stu-id="8ded8-113">The device supports text messaging.</span></span>                                                  |
| <span data-ttu-id="8ded8-114">Запись образа продолжается</span><span class="sxs-lookup"><span data-stu-id="8ded8-114">Still image capture</span></span>         | <span data-ttu-id="8ded8-115">Устройство можно использовать для записи образов по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="8ded8-115">The device can be used to capture still images.</span></span>                                      |
| <span data-ttu-id="8ded8-116">Память</span><span class="sxs-lookup"><span data-stu-id="8ded8-116">Storage</span></span>                     | <span data-ttu-id="8ded8-117">Устройство можно использовать для хранения файлов.</span><span class="sxs-lookup"><span data-stu-id="8ded8-117">The device can be used to store files.</span></span>                                               |



 

<span data-ttu-id="8ded8-118">Функция Листфунктионалкатегориес в модуле Девицекапабилитиес. cpp демонстрирует получение функциональных категорий для выбранного устройства.</span><span class="sxs-lookup"><span data-stu-id="8ded8-118">The ListFunctionalCategories function in the DeviceCapabilities.cpp module demonstrates the retrieval of functional categories for a selected device.</span></span>

<span data-ttu-id="8ded8-119">Приложение может извлекать функциональные категории, поддерживаемые устройством, с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8ded8-119">Your application can retrieve the functional categories supported by a device by using the interfaces described in the following table.</span></span>



| <span data-ttu-id="8ded8-120">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="8ded8-120">Interface</span></span>                                                                                      | <span data-ttu-id="8ded8-121">Описание</span><span class="sxs-lookup"><span data-stu-id="8ded8-121">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="8ded8-122">**Интерфейс Ипортабледевицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="8ded8-122">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="8ded8-123">Предоставляет доступ к методам получения функциональной категории.</span><span class="sxs-lookup"><span data-stu-id="8ded8-123">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="8ded8-124">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="8ded8-124">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="8ded8-125">Используется для перечисления и хранения данных функциональной категории.</span><span class="sxs-lookup"><span data-stu-id="8ded8-125">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="8ded8-126">Первая задача, выполняемая примером приложения, — это извлечение объекта [**ипортабледевицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , который используется для получения функциональных категорий на выбранном устройстве.</span><span class="sxs-lookup"><span data-stu-id="8ded8-126">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the functional categories on the selected device.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

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
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="8ded8-127">Извлеченные категории хранятся в объекте [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="8ded8-127">The retrieved categories are stored in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="8ded8-128">Следующим шагом является перечисление и отображение поддерживаемых категорий.</span><span class="sxs-lookup"><span data-stu-id="8ded8-128">The next step is the enumeration and display of the supported categories.</span></span> <span data-ttu-id="8ded8-129">Первым этапом выполнения примера приложения является получение числа поддерживаемых категорий.</span><span class="sxs-lookup"><span data-stu-id="8ded8-129">The first step that the sample application accomplishes is to retrieve the count of supported categories.</span></span> <span data-ttu-id="8ded8-130">Затем этот счетчик используется для прохода по объекту [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , содержащему поддерживаемые категории.</span><span class="sxs-lookup"><span data-stu-id="8ded8-130">It then uses this count to iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that contains the supported categories.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
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

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="8ded8-131">См. также</span><span class="sxs-lookup"><span data-stu-id="8ded8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ded8-132">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="8ded8-132">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="8ded8-133">**Интерфейс Ипортабледевицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="8ded8-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="8ded8-134">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="8ded8-134">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="8ded8-135">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="8ded8-135">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



