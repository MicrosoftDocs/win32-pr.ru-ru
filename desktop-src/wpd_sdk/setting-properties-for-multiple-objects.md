---
description: Задание свойств для нескольких объектов
ms.assetid: 0686ba54-4782-42a4-8fdb-2325fc8d8bc2
title: Задание свойств для нескольких объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e951662d9920cb22db0a417f1af94f3eb7eb4d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712567"
---
# <a name="setting-properties-for-multiple-objects"></a><span data-ttu-id="0d3f2-103">Задание свойств для нескольких объектов</span><span class="sxs-lookup"><span data-stu-id="0d3f2-103">Setting Properties for Multiple Objects</span></span>

<span data-ttu-id="0d3f2-104">Некоторые драйверы устройств поддерживают задание свойств для нескольких объектов в одном вызове функции — это называется групповой записью.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-104">Some device drivers support setting properties for multiple objects in a single function call—this is referred to as a bulk write.</span></span> <span data-ttu-id="0d3f2-105">Приложение может выполнять неполную запись с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-105">Your application can perform a bulk write using the interfaces described in the following table.</span></span>



| <span data-ttu-id="0d3f2-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="0d3f2-106">Interface</span></span>                                                                                      | <span data-ttu-id="0d3f2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0d3f2-107">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="0d3f2-108">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="0d3f2-109">Предоставляет доступ к методам, относящимся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-109">Provides access to the content-specific methods.</span></span>             |
| [<span data-ttu-id="0d3f2-110">**Интерфейс Ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="0d3f2-111">Предоставляет доступ к методам, относящимся к конкретному свойству.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-111">Provides access to the property-specific methods.</span></span>            |
| [<span data-ttu-id="0d3f2-112">**Интерфейс Ипортабледевицепропертиесбулк**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-112">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="0d3f2-113">Поддерживает операцию записи в неполное время.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-113">Supports the bulk write operation.</span></span>                           |
| [<span data-ttu-id="0d3f2-114">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="0d3f2-115">Используется для хранения идентификаторов объектов для групповой операции.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-115">Used to store the object identifiers for the bulk operation.</span></span> |
| [<span data-ttu-id="0d3f2-116">**Интерфейс Ипортабледевицевалуесколлектион**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-116">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="0d3f2-117">Используется для задания свойств, которые необходимо записать.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-117">Used to identify the properties to be written.</span></span>               |



 

<span data-ttu-id="0d3f2-118">`WriteContentPropertiesBulk`Функция в модуле контентпропертиес. cpp примера приложения демонстрирует операцию записи в неполное время.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-118">The `WriteContentPropertiesBulk` function in the sample application's ContentProperties.cpp module demonstrates a bulk write operation.</span></span>

<span data-ttu-id="0d3f2-119">Первая задача, выполняемая в этом примере, определяет, поддерживает ли данный драйвер операции с массовыми операциями.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-119">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="0d3f2-120">Это достигается путем вызова QueryInterface для объекта **ипортабледевицепропертиес** и проверки существования **ипортабледевицепропертиесбулк**.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-120">This is accomplished by calling QueryInterface on an **IPortableDeviceProperties** object and checking for the existence of **IPortableDevicePropertiesBulk**.</span></span>


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



<span data-ttu-id="0d3f2-121">Следующая задача влечет за собой создание объекта **ипортабледевицевалуесколлектион** .</span><span class="sxs-lookup"><span data-stu-id="0d3f2-121">The next task entails creating an **IPortableDeviceValuesCollection** object.</span></span> <span data-ttu-id="0d3f2-122">Это объект, содержащий значения свойств, которые будут записаны образцом.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-122">This is the object that contains the property values that the sample will write.</span></span>


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



<span data-ttu-id="0d3f2-123">После этого в примере создается экземпляр [**интерфейса ипортабледевицепропертиесбулккаллбакк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="0d3f2-123">After this, the sample creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="0d3f2-124">Приложение будет использовать методы этого интерфейса для отслеживания хода выполнения асинхронной операции с массовыми операциями записи.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-124">The application will use the methods in this interface to track the progress of the asynchronous bulk-write operation.</span></span>


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



<span data-ttu-id="0d3f2-125">Следующей функцией, которую вызывает пример приложения, является `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` вспомогательная функция.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-125">The next function that the sample application calls is the `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` helper function.</span></span> <span data-ttu-id="0d3f2-126">Эта функция рекурсивно перечисляет все объекты на заданном устройстве и возвращает [**интерфейс ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , содержащий идентификатор для каждого найденного объекта.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-126">This function recursively enumerates all objects on a given device and returns an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="0d3f2-127">Эта функция определена в модуле Контентенумератион. cpp.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-127">This function is defined in the module ContentEnumeration.cpp.</span></span>


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



<span data-ttu-id="0d3f2-128">Объект **ипортабледевицепропвариантколлектион** содержит коллекцию индексированных значений **пропвариант** для одного и того же объекта VarType.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-128">The **IPortableDevicePropVariantCollection** object holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="0d3f2-129">В этом случае эти значения содержат заданный идентификатор объекта для каждого объекта, найденного на устройстве.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-129">In this case, these values contain a given object identifier for each object found on the device.</span></span>

<span data-ttu-id="0d3f2-130">Идентификаторы объектов и их соответствующие свойства имени хранятся в объекте [**ипортабледевицевалуесколлектион**](iportabledevicevalues.md) .</span><span class="sxs-lookup"><span data-stu-id="0d3f2-130">The object identifiers and their respective name properties are stored in an [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) object.</span></span> <span data-ttu-id="0d3f2-131">Свойства имени организованы таким образом, чтобы первому объекту было присвоено свойство Name "NewName0", второму объекту присваивается свойство Name "NewName1" и т. д.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-131">The name properties are organized so that the first object is assigned a name property of "NewName0", the second object is assigned a name property of "NewName1", and so on.</span></span>

<span data-ttu-id="0d3f2-132">В следующем фрагменте из примера показано, как объект **ипортабледевицевалуесколлектион** был инициализирован с помощью идентификаторов объектов и новых строк имени.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-132">The following excerpt from the sample demonstrates how the **IPortableDeviceValuesCollection** object was initialized with object identifiers and new name strings.</span></span>


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



<span data-ttu-id="0d3f2-133">Когда образец создает объект **ипортабледевицевалуесколлектион** , содержащий пары "идентификатор объекта" и "имя", он может начать асинхронную операцию.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-133">Once the sample creates the **IPortableDeviceValuesCollection** object that contains the object identifier and name pairs, it can begin the asynchronous operation.</span></span>

<span data-ttu-id="0d3f2-134">Асинхронная операция записи начинается, когда в примере вызывается метод [**ипортабледевицепропертиесбулк:: куеуесетвалуесбйобжектлист**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) .</span><span class="sxs-lookup"><span data-stu-id="0d3f2-134">The asynchronous write operation begins when the sample calls the [**IPortableDevicePropertiesBulk::QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) method.</span></span> <span data-ttu-id="0d3f2-135">Этот метод уведомляет драйвер о начале выполнения групповой операции.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-135">This method notifies the driver that a bulk operation is about to begin.</span></span> <span data-ttu-id="0d3f2-136">После этого в примере вызывается метод [**ипортабледевицебулк:: Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) для фактической записи новых значений имени.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-136">After this, the sample calls the [**IPortableDeviceBulk::Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) method to begin actually writing the new name values.</span></span>


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



<span data-ttu-id="0d3f2-137">Обратите внимание, что пример ожидает бесконечно долгое время для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-137">Note that the sample waits an infinitely long period of time for the operation to complete.</span></span> <span data-ttu-id="0d3f2-138">Если это рабочее приложение, необходимо изменить код.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-138">If this were a production application, the code would need to be modified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d3f2-139">См. также</span><span class="sxs-lookup"><span data-stu-id="0d3f2-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d3f2-140">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="0d3f2-141">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="0d3f2-142">**Интерфейс Ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-142">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="0d3f2-143">**Интерфейс Ипортабледевицепропертиесбулк**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-143">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="0d3f2-144">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="0d3f2-145">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-145">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



