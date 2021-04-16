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
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a>Получение идентификаторов функциональных объектов для устройства

Как указано в разделе [Получение списка функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md) , портативные устройства Windows могут поддерживать одну или несколько функциональных категорий. Любая заданная Функциональная категория может поддерживать один или несколько функциональных объектов. Например, Категория хранилища может поддерживать три объекта функционального хранилища, каждый из которых идентифицируется строкой уникального идентификатора. Первый объект хранилища может затем идентифицироваться строкой "Storage1", вторым по строке "Storage2", а третья — строкой "Storage3".

Функция Листфунктионалобжектс в модуле Девицекапабилитиес. cpp демонстрирует извлечение типов содержимого для функциональных категорий, поддерживаемых выбранным устройством.

Приложение может извлекать функциональные категории, поддерживаемые устройством, с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                                                      | Описание                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Интерфейс Ипортабледевицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Предоставляет доступ к методам получения функциональной категории. |
| [**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) | Используется для перечисления и хранения данных функциональной категории.         |



 

Код, обнаруженный в функции Листфунктионалобжектс, почти идентичен коду, обнаруженному в функции Листфунктионалкатегориес. (См. раздел [Получение функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md) .) Единственное отличие заключается в вызове метода [**ипортабледевицекапабилитиес:: жетфунктионалобжектс**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) , который находится в цикле, который проходит по функциональным категориям.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 



