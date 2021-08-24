---
description: Получение свойств для нескольких объектов
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Получение свойств для нескольких объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1ad9ec397daa90c149fe950c1fc4777c407e3f5f3a359f46cf8bef56e18b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083518"
---
# <a name="retrieving-properties-for-multiple-objects"></a>Получение свойств для нескольких объектов

Некоторые драйверы устройств поддерживают извлечение свойств для нескольких объектов в одном вызове функции. Это называется массовым извлечением. Существует два типа операций извлечения: первый тип извлекает свойства для списка объектов, а второй тип извлекает свойства для всех объектов заданного формата. В примере, описанном в этом разделе, показан первый из них.

Приложение может выполнять групповое извлечение с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                                                      | Описание                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Предоставляет доступ к методам, относящимся к содержимому.                   |
| [**Интерфейс Ипортабледевицекэйколлектион**](iportabledevicekeycollection.md)                 | Используется для задания извлекаемых свойств.                   |
| [**Интерфейс Ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Используется для определения того, поддерживает ли данный драйвер групповые операции. |
| [**Интерфейс Ипортабледевицепропертиесбулк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Поддерживает операцию извлечения с массовым набором.                             |
| [**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) | Используется для хранения идентификаторов объектов для групповой операции.       |



 

Функция Реадконтентпропертиесбулк в модуле Контентпропертиес. cpp примера приложения демонстрирует операцию получения небольшого объема.

Первая задача, выполняемая в этом примере, определяет, поддерживает ли данный драйвер операции с массовыми операциями. Это достигается путем вызова QueryInterface в интерфейсе Ипортабледевицепропертиес и проверки существования Ипортабледевицепропертиесбулк.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CGetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceKeyCollection>         pPropertiesToRead;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;


if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pProperties->QueryInterface(IID_PPV_ARGS(&pPropertiesBulk));
    if (FAILED(hr))
    {
        printf("This driver does not support BULK property operations.\n");
    }
}
```



Если драйвер поддерживает групповые операции, следующим шагом является создание экземпляра [**интерфейса ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) и указание ключей, соответствующих свойствам, которые будет извлекать приложение. Описание этого процесса см. в разделе [Получение свойств для одного объекта](retrieving-properties-for-a-single-object.md) .

После указания соответствующих ключей пример приложения создает экземпляр [**интерфейса ипортабледевицепропертиесбулккаллбакк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk). Приложение будет использовать методы этого интерфейса для отслеживания хода выполнения асинхронной операции извлечения с массовым извлечением.


```C++
if (SUCCEEDED(hr))
{
    pCallback = new CGetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CGetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



Следующей функцией, которую вызывает пример приложения, является вспомогательная функция Креатеипортабледевицепропвариантколлектионвисаллобжектидс. Эта функция создает список всех доступных идентификаторов объектов, например для целей. (В реальном приложении список идентификаторов будет ограничен определенным набором объектов. Например, приложение может создать список идентификаторов для всех объектов, находящихся в данном представлении папки.

Как отмечалось выше, вспомогательная функция рекурсивно перечисляет все объекты на заданном устройстве. Он возвращает этот список в [**интерфейсе ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , который содержит идентификатор для каждого найденного объекта. Вспомогательная функция определяется в модуле Контентенумератион. cpp.


```C++
// 7) Call our helper function CreateIPortableDevicePropVariantCollectionWithAllObjectIDs
// to enumerate and create an IPortableDevicePropVariantCollection with the object
// identifiers needed to perform the bulk operation on.
if (SUCCEEDED(hr))
{
    hr = CreateIPortableDevicePropVariantCollectionWithAllObjectIDs(pDevice,
                                                                    pContent,
                                                                    &pObjectIDs);
}
```



После выполнения предыдущих действий пример приложения инициирует асинхронное получение свойства. Это достигается путем выполнения следующих действий.

1.  Вызов Ипортабледевицепропертиесбулк:: Куеуежетвалуесбйобжектлист, который помещает запрос в очередь на получение набора свойств. (Обратите внимание, что хотя запрос помещается в очередь, он не запускается.)
2.  Вызов Ипортабледевицепропертиесбулк:: Start для инициации запроса в очереди.

Эти шаги показаны в следующем фрагменте кода из примера приложения.


```C++
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueGetValuesByObjectList(pObjectIDs,
                                                        pPropertiesToRead,
                                                        pCallback,
                                                        &guidContext);


       if(SUCCEEDED(hr))
       {
           // Cleanup any previously created global event handles.
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               CloseHandle(g_hBulkPropertyOperationEvent);
               g_hBulkPropertyOperationEvent = NULL;
           }

           // In order to create a simpler to follow example we create and wait infinitly
           // for the bulk property operation to complete and ignore any errors.
           // Production code should be written in a more robust manner.
           // Create the global event handle to wait on for the bulk operation
           // to complete.
           g_hBulkPropertyOperationEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               // Call Start() to actually being the Asynchronous bulk operation.
               hr = pPropertiesBulk->Start(guidContext);
               if(FAILED(hr))
               {
                   printf("! Failed to start property operation, hr = 0x%lx\n", hr);
               }
           }
           else
           {
               printf("! Failed to create the global event handle to wait on for the bulk operation. Aborting operation.\n");
           }
       }
       else
       {
           printf("! QueueGetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Интерфейс Ипортабледевицекэйколлектион**](iportabledevicekeycollection.md)
</dt> <dt>

[**Интерфейс Ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Интерфейс Ипортабледевицепропертиесбулк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 



