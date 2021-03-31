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
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a>Получение функциональных категорий, поддерживаемых устройством

Портативные устройства Windows могут поддерживать одну или несколько функциональных категорий. Эти категории описаны в следующей таблице.



| Категория                    | Описание                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| Запись звука               | Устройство можно использовать для записи звука.                                              |
| Сведения о подготовке к просмотру       | Устройство предоставляет данные, описывающие файлы мультимедиа, которые могут быть отображены. |
| Служба коротких сообщений (SMS) | Устройство поддерживает текстовые сообщения.                                                  |
| Запись образа продолжается         | Устройство можно использовать для записи образов по-прежнему.                                      |
| Память                     | Устройство можно использовать для хранения файлов.                                               |



 

Функция Листфунктионалкатегориес в модуле Девицекапабилитиес. cpp демонстрирует получение функциональных категорий для выбранного устройства.

Приложение может извлекать функциональные категории, поддерживаемые устройством, с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                                                      | Описание                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Интерфейс Ипортабледевицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Предоставляет доступ к методам получения функциональной категории. |
| [**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) | Используется для перечисления и хранения данных функциональной категории.         |



 

Первая задача, выполняемая примером приложения, — это извлечение объекта [**ипортабледевицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , который используется для получения функциональных категорий на выбранном устройстве.


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



Извлеченные категории хранятся в объекте [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) .

Следующим шагом является перечисление и отображение поддерживаемых категорий. Первым этапом выполнения примера приложения является получение числа поддерживаемых категорий. Затем этот счетчик используется для прохода по объекту [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , содержащему поддерживаемые категории.


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

 

 



