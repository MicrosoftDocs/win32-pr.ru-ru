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
# <a name="enumerating-content"></a>Перечисление содержимого

Содержимое устройства (будь то содержимое, которое является папкой, телефонной книгой, видео или изображением по-прежнему) называется объектом в API WPD. На эти объекты ссылаются идентификаторы объектов, описанные в свойствах. Вы можете перечислить объекты на устройстве, вызвав методы в [**интерфейсе ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), [**интерфейсе ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)и [**интерфейсе иенумпортабледевицеобжектидс**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).

Пример приложения демонстрирует перечисление содержимого в функции Енумератеаллконтент, которая находится в модуле Контентенумератион. cpp. Эта функция, в свою очередь, вызывает функцию Рекурсивинумерате, которая просматривает иерархию объектов, найденных на выбранном устройстве, и возвращает идентификатор объекта для каждого объекта.

Как уже отмечалось, функция Рекурсивинумерате извлекает идентификатор объекта для каждого объекта, найденного на устройстве. Идентификатор объекта является строковым значением. Когда приложение получает этот идентификатор, оно может получить более описательные сведения об объекте (например, имя объекта, идентификатор родителя объекта и т. д.). Эти описательные сведения называются свойствами объекта (или метаданными). Приложение может извлекать эти свойства путем вызова членов [**интерфейса ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).

Функция Енумератеаллконтент начинается с получения указателя на [**интерфейс ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent). Он извлекает этот указатель, вызывая метод [**ипортабледевице:: Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .


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



После получения указателя на интерфейс Ипортабледевицеконтент функция Енумератеаллконтент вызывает функцию Рекурсивинумерате, которая просматривает иерархию объектов, найденных на данном устройстве, и возвращает идентификатор объекта для каждого из них.

Функция Рекурсивинумерате начинается с получения указателя на [**интерфейс иенумпортабледевицеобжектидс**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids). Этот интерфейс предоставляет методы, используемые приложением для перемещения по списку объектов, найденных на данном устройстве.

В этом примере функция Рекурсивинумерате вызывает метод [**иенумпортабледевицеобжектидс:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) для прохода по списку объектов.

Каждый вызов метода [**иенумпортабледевицеобжектс:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) запрашивает пакет из 10 идентификаторов. (Это значение указывается ЧИСЛОм \_ ОБЪЕКТЫ \_ для \_ запроса константы, которая указывается в качестве первого аргумента.)


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Иенумпортабледевицеобжектидс**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Интерфейс Ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 



