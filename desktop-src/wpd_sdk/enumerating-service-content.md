---
description: Перечисление содержимого службы
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Перечисление содержимого службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9846565b7cdc4b0a4475cb99806b671452dcbe134e40d4b1e3d70df249c510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083568"
---
# <a name="enumerating-service-content"></a>Перечисление содержимого службы

После открытия службы приложение может начать выполнять операции, связанные с обслуживанием. В случае с приложением Впдсервицесаписампле одной из этих операций является перечисление содержимого для данной службы контактов. В следующей таблице описаны используемые интерфейсы.



| Интерфейс                                                            | Описание                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Используется для получения интерфейса IPortableDeviceContent2 для доступа к содержимому службы.         |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Используется для получения интерфейса Иенумпортабледевицеобжектидс для перечисления объектов в службе. |
| [**иенумпортабледевицеобжектидс**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | Используется для перечисления объектов в службе.                                                        |



 

Код перечисления содержимого находится в модуле Контентенумератион. cpp. Этот код находится в методах **енумератеаллконтент** и **рекурсивинумерате** . Первый метод вызывает второй.

Метод **енумератеконтент** принимает указатель на объект [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) в качестве одного параметра. Этот объект соответствует службе, открытой ранее приложением при вызове метода [**ипортабледевицесервице:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) .

Метод **енумератеконтент** создает объект [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) и передает этот объект в метод [**ипортабледевицесервице:: Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) . Этот метод, в свою очередь, получает содержимое на корневом уровне службы, а затем рекурсивно начинает получать содержимое, найденное под корнем.

Следующий код соответствует методу **енумератеконтент** .


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



Следующий код соответствует методу **рекурсивинумерате** . Метод Рекурсивинумерате создает интерфейс **иенумпортабледевицеобжектидс** для заданного родительского объекта и вызывает **Иенумпортабледевицеобжектидс:: Next**, получая пакет непосредственных дочерних объектов. Для каждого дочернего объекта Рекурсивинумерате вызывается снова, чтобы вернуть дочерние объекты-потомки и т. д.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**иенумпортабледевицеобжектидс**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**Интерфейс IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**Интерфейс Ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[Открытие службы](opening-a-service.md)
</dt> <dt>

[впдсервицесаписампле](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



