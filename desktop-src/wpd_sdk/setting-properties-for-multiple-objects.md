---
description: Задание свойств для нескольких объектов
ms.assetid: 0686ba54-4782-42a4-8fdb-2325fc8d8bc2
title: Задание свойств для нескольких объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14517e26843265d8273785657e98b691c155821c10f57b92d53e374c20d34ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842686"
---
# <a name="setting-properties-for-multiple-objects"></a>Задание свойств для нескольких объектов

Некоторые драйверы устройств поддерживают задание свойств для нескольких объектов в одном вызове функции — это называется групповой записью. Приложение может выполнять неполную запись с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                                                      | Описание                                                  |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Предоставляет доступ к методам, относящимся к содержимому.             |
| [**Интерфейс Ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Предоставляет доступ к методам, относящимся к конкретному свойству.            |
| [**Интерфейс Ипортабледевицепропертиесбулк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Поддерживает операцию записи в неполное время.                           |
| [**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) | Используется для хранения идентификаторов объектов для групповой операции. |
| [**Интерфейс Ипортабледевицевалуесколлектион**](iportabledevicevaluescollection.md)           | Используется для задания свойств, которые необходимо записать.               |



 

`WriteContentPropertiesBulk`Функция в модуле контентпропертиес. cpp примера приложения демонстрирует операцию записи в неполное время.

Первая задача, выполняемая в этом примере, определяет, поддерживает ли данный драйвер операции с массовыми операциями. Это достигается путем вызова QueryInterface для объекта **ипортабледевицепропертиес** и проверки существования **ипортабледевицепропертиесбулк**.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
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



Следующая задача влечет за собой создание объекта **ипортабледевицевалуесколлектион** . Это объект, содержащий значения свойств, которые будут записаны образцом.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDeviceValuesCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDeviceValuesCollection,
                          (VOID**) &pPropertiesToWrite);
    if (FAILED(hr))
    {
        printf("! Failed to CoCreate IPortableDeviceValuesCollection for bulk property values, hr = 0x%lx\n", hr);
    }
}
```



После этого в примере создается экземпляр [**интерфейса ипортабледевицепропертиесбулккаллбакк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk). Приложение будет использовать методы этого интерфейса для отслеживания хода выполнения асинхронной операции с массовыми операциями записи.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    pCallback = new CSetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CSetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



Следующей функцией, которую вызывает пример приложения, является `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` вспомогательная функция. Эта функция рекурсивно перечисляет все объекты на заданном устройстве и возвращает [**интерфейс ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , содержащий идентификатор для каждого найденного объекта. Эта функция определена в модуле Контентенумератион. cpp.


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



Объект **ипортабледевицепропвариантколлектион** содержит коллекцию индексированных значений **пропвариант** для одного и того же объекта VarType. В этом случае эти значения содержат заданный идентификатор объекта для каждого объекта, найденного на устройстве.

Идентификаторы объектов и их соответствующие свойства имени хранятся в объекте [**ипортабледевицевалуесколлектион**](iportabledevicevalues.md) . Свойства имени организованы таким образом, чтобы первому объекту было присвоено свойство Name "NewName0", второму объекту присваивается свойство Name "NewName1" и т. д.

В следующем фрагменте из примера показано, как объект **ипортабледевицевалуесколлектион** был инициализирован с помощью идентификаторов объектов и новых строк имени.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = pObjectIDs->GetCount(&cObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of objectIDs from IPortableDevicePropVariantCollection, hr = 0x%lx\n", hr);
    }
}


if (SUCCEEDED(hr))
{
    for(DWORD dwIndex = 0; (dwIndex < cObjectIDs) && (hr == S_OK); dwIndex++)
    {
        CComPtr<IPortableDeviceValues>  pValues;
        PROPVARIANT                     pv = {0};

        PropVariantInit(&pv);
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pValues);
        if (FAILED(hr))
        {
            printf("! Failed to CoCreate CLSID_PortableDeviceValues, hr = 0x%lx\n", hr);
        }

        // Get the Object ID whose properties we will set
        if (hr == S_OK)
        {
            hr = pObjectIDs->GetAt(dwIndex, &pv);
            if (FAILED(hr))
            {
                printf("! Failed to get next Object ID from list, hr = 0x%lx\n", hr);
            }
        }

        // Save them into the IPortableDeviceValues so the driver knows which object this proeprty set belongs to
        if (hr == S_OK)
        {
            hr = pValues->SetStringValue(WPD_OBJECT_ID, pv.pwszVal);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID, hr = 0x%lx\n", hr);
            }
        }

        // Set the new values.  In this sample, we attempt to set the name property.
        if (hr == S_OK)
        {
            CAtlStringW strValue;
            strValue.Format(L"NewName%d", dwIndex);

            hr = pValues->SetStringValue(WPD_OBJECT_NAME, strValue.GetString());
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_NAME, hr = 0x%lx\n", hr);
            }
        }

        // Add this property set to the collection
        if (hr == S_OK)
        {
            hr = pPropertiesToWrite->Add(pValues);
            if (FAILED(hr))
            {
                printf("! Failed to add values to collection, hr = 0x%lx\n", hr);
            }
        }
        PropVariantClear(&pv);
    }
}
```



Когда образец создает объект **ипортабледевицевалуесколлектион** , содержащий пары "идентификатор объекта" и "имя", он может начать асинхронную операцию.

Асинхронная операция записи начинается, когда в примере вызывается метод [**ипортабледевицепропертиесбулк:: куеуесетвалуесбйобжектлист**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) . Этот метод уведомляет драйвер о начале выполнения групповой операции. После этого в примере вызывается метод [**ипортабледевицебулк:: Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) для фактической записи новых значений имени.


```C++
   HRESULT                                       hr                = S_OK;
   GUID                                          guidContext       = GUID_NULL;
   CSetBulkValuesCallback*                       pCallback         = NULL;
   CComPtr<IPortableDeviceProperties>            pProperties;
   CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
   CComPtr<IPortableDeviceValues>                pObjectProperties;
   CComPtr<IPortableDeviceContent>               pContent;
   CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
   CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
   DWORD                                         cObjectIDs        = 0;
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueSetValuesByObjectList(pPropertiesToWrite,
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
           printf("! QueueSetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



Обратите внимание, что пример ожидает бесконечно долгое время для завершения операции. Если это рабочее приложение, необходимо изменить код.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Интерфейс Ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Интерфейс Ипортабледевицепропертиесбулк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 



