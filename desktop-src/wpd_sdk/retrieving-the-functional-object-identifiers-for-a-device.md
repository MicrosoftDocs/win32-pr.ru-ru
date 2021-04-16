---
description: Получение идентификаторов функциональных объектов для устройства
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Получение идентификаторов функциональных объектов для устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a753324e24a6b78625a78b4128380288b6672f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712292"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a><span data-ttu-id="87f43-103">Получение идентификаторов функциональных объектов для устройства</span><span class="sxs-lookup"><span data-stu-id="87f43-103">Retrieving the Functional Object Identifiers for a Device</span></span>

<span data-ttu-id="87f43-104">Как указано в разделе [Получение списка функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md) , портативные устройства Windows могут поддерживать одну или несколько функциональных категорий.</span><span class="sxs-lookup"><span data-stu-id="87f43-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="87f43-105">Любая заданная Функциональная категория может поддерживать один или несколько функциональных объектов.</span><span class="sxs-lookup"><span data-stu-id="87f43-105">Any given functional category may support one or more functional objects.</span></span> <span data-ttu-id="87f43-106">Например, Категория хранилища может поддерживать три объекта функционального хранилища, каждый из которых идентифицируется строкой уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="87f43-106">For example, the storage category may support three functional storage objects, each of which is identified by a unique identifier string.</span></span> <span data-ttu-id="87f43-107">Первый объект хранилища может затем идентифицироваться строкой "Storage1", вторым по строке "Storage2", а третья — строкой "Storage3".</span><span class="sxs-lookup"><span data-stu-id="87f43-107">The first storage object may then be identified by the string "Storage1", the second by the string "Storage2", and the third by the string "Storage3".</span></span>

<span data-ttu-id="87f43-108">Функция Листфунктионалобжектс в модуле Девицекапабилитиес. cpp демонстрирует извлечение типов содержимого для функциональных категорий, поддерживаемых выбранным устройством.</span><span class="sxs-lookup"><span data-stu-id="87f43-108">The ListFunctionalObjects function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="87f43-109">Приложение может извлекать функциональные категории, поддерживаемые устройством, с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="87f43-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="87f43-110">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="87f43-110">Interface</span></span>                                                                                      | <span data-ttu-id="87f43-111">Описание</span><span class="sxs-lookup"><span data-stu-id="87f43-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="87f43-112">**Интерфейс Ипортабледевицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="87f43-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="87f43-113">Предоставляет доступ к методам получения функциональной категории.</span><span class="sxs-lookup"><span data-stu-id="87f43-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="87f43-114">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="87f43-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="87f43-115">Используется для перечисления и хранения данных функциональной категории.</span><span class="sxs-lookup"><span data-stu-id="87f43-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="87f43-116">Код, обнаруженный в функции Листфунктионалобжектс, почти идентичен коду, обнаруженному в функции Листфунктионалкатегориес.</span><span class="sxs-lookup"><span data-stu-id="87f43-116">The code found in the ListFunctionalObjects function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="87f43-117">(См. раздел [Получение функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md) .) Единственное отличие заключается в вызове метода [**ипортабледевицекапабилитиес:: жетфунктионалобжектс**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) , который находится в цикле, который проходит по функциональным категориям.</span><span class="sxs-lookup"><span data-stu-id="87f43-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method, which appears within the loop that iterates through the functional categories.</span></span>


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

// Loop through each functional category and get the list of
// functional object identifiers associated with a particular
// category.
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

                // Display the object identifiers for all
                // functional objects within this category
                CComPtr<IPortableDevicePropVariantCollection> pFunctionalObjectIds;
                hr = pCapabilities->GetFunctionalObjects(*pv.puuid, &pFunctionalObjectIds);
                if (SUCCEEDED(hr))
                {
                    printf("Functional Objects: ");
                    DisplayFunctionalObjectIDs(pFunctionalObjectIds);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
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



## <a name="related-topics"></a><span data-ttu-id="87f43-118">См. также</span><span class="sxs-lookup"><span data-stu-id="87f43-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87f43-119">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="87f43-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="87f43-120">**Интерфейс Ипортабледевицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="87f43-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="87f43-121">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="87f43-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="87f43-122">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="87f43-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



