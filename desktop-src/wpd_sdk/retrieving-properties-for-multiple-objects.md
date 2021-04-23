---
description: Получение свойств для нескольких объектов
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Получение свойств для нескольких объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c069f6a28b923339f66f8423f211eff4704ef6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712683"
---
# <a name="retrieving-properties-for-multiple-objects"></a><span data-ttu-id="e8600-103">Получение свойств для нескольких объектов</span><span class="sxs-lookup"><span data-stu-id="e8600-103">Retrieving Properties for Multiple Objects</span></span>

<span data-ttu-id="e8600-104">Некоторые драйверы устройств поддерживают извлечение свойств для нескольких объектов в одном вызове функции. Это называется массовым извлечением.</span><span class="sxs-lookup"><span data-stu-id="e8600-104">Some device drivers support the retrieval of properties for multiple objects in a single function call; this is referred to as a bulk retrieval.</span></span> <span data-ttu-id="e8600-105">Существует два типа операций извлечения: первый тип извлекает свойства для списка объектов, а второй тип извлекает свойства для всех объектов заданного формата.</span><span class="sxs-lookup"><span data-stu-id="e8600-105">There are two types of bulk retrieval operations: the first type retrieves properties for a list of objects, and the second type retrieves properties for all objects of a given format.</span></span> <span data-ttu-id="e8600-106">В примере, описанном в этом разделе, показан первый из них.</span><span class="sxs-lookup"><span data-stu-id="e8600-106">The example described in this section demonstrates the former.</span></span>

<span data-ttu-id="e8600-107">Приложение может выполнять групповое извлечение с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e8600-107">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="e8600-108">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="e8600-108">Interface</span></span>                                                                                      | <span data-ttu-id="e8600-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e8600-109">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="e8600-110">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="e8600-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="e8600-111">Предоставляет доступ к методам, относящимся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="e8600-111">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="e8600-112">**Интерфейс Ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="e8600-112">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="e8600-113">Используется для задания извлекаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="e8600-113">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="e8600-114">**Интерфейс Ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="e8600-114">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="e8600-115">Используется для определения того, поддерживает ли данный драйвер групповые операции.</span><span class="sxs-lookup"><span data-stu-id="e8600-115">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="e8600-116">**Интерфейс Ипортабледевицепропертиесбулк**</span><span class="sxs-lookup"><span data-stu-id="e8600-116">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="e8600-117">Поддерживает операцию извлечения с массовым набором.</span><span class="sxs-lookup"><span data-stu-id="e8600-117">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="e8600-118">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="e8600-118">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="e8600-119">Используется для хранения идентификаторов объектов для групповой операции.</span><span class="sxs-lookup"><span data-stu-id="e8600-119">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="e8600-120">Функция Реадконтентпропертиесбулк в модуле Контентпропертиес. cpp примера приложения демонстрирует операцию получения небольшого объема.</span><span class="sxs-lookup"><span data-stu-id="e8600-120">The ReadContentPropertiesBulk function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation.</span></span>

<span data-ttu-id="e8600-121">Первая задача, выполняемая в этом примере, определяет, поддерживает ли данный драйвер операции с массовыми операциями.</span><span class="sxs-lookup"><span data-stu-id="e8600-121">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="e8600-122">Это достигается путем вызова QueryInterface в интерфейсе Ипортабледевицепропертиес и проверки существования Ипортабледевицепропертиесбулк.</span><span class="sxs-lookup"><span data-stu-id="e8600-122">This is accomplished by calling QueryInterface on the IPortableDeviceProperties interface and checking for the existence of IPortableDevicePropertiesBulk.</span></span>


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



<span data-ttu-id="e8600-123">Если драйвер поддерживает групповые операции, следующим шагом является создание экземпляра [**интерфейса ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) и указание ключей, соответствующих свойствам, которые будет извлекать приложение.</span><span class="sxs-lookup"><span data-stu-id="e8600-123">If the driver supports bulk operations, the next step is to create an instance of the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and to specify the keys that correspond to the properties that the application will retrieve.</span></span> <span data-ttu-id="e8600-124">Описание этого процесса см. в разделе [Получение свойств для одного объекта](retrieving-properties-for-a-single-object.md) .</span><span class="sxs-lookup"><span data-stu-id="e8600-124">For a description of this process, see the [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md) topic.</span></span>

<span data-ttu-id="e8600-125">После указания соответствующих ключей пример приложения создает экземпляр [**интерфейса ипортабледевицепропертиесбулккаллбакк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="e8600-125">After the appropriate keys are specified, the sample application creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="e8600-126">Приложение будет использовать методы этого интерфейса для отслеживания хода выполнения асинхронной операции извлечения с массовым извлечением.</span><span class="sxs-lookup"><span data-stu-id="e8600-126">The application will use the methods in this interface to track the progress of the asynchronous bulk-retrieval operation.</span></span>


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



<span data-ttu-id="e8600-127">Следующей функцией, которую вызывает пример приложения, является вспомогательная функция Креатеипортабледевицепропвариантколлектионвисаллобжектидс.</span><span class="sxs-lookup"><span data-stu-id="e8600-127">The next function that the sample application calls is the CreateIPortableDevicePropVariantCollectionWithAllObjectIDs helper function.</span></span> <span data-ttu-id="e8600-128">Эта функция создает список всех доступных идентификаторов объектов, например для целей.</span><span class="sxs-lookup"><span data-stu-id="e8600-128">This function creates a list of all available object identifiers for example purposes.</span></span> <span data-ttu-id="e8600-129">(В реальном приложении список идентификаторов будет ограничен определенным набором объектов.</span><span class="sxs-lookup"><span data-stu-id="e8600-129">(A real-world application would limit the list of identifiers to a particular set of objects.</span></span> <span data-ttu-id="e8600-130">Например, приложение может создать список идентификаторов для всех объектов, находящихся в данном представлении папки.</span><span class="sxs-lookup"><span data-stu-id="e8600-130">For instance, an application may create a list of identifiers for all of the objects currently in a given folder view.)</span></span>

<span data-ttu-id="e8600-131">Как отмечалось выше, вспомогательная функция рекурсивно перечисляет все объекты на заданном устройстве.</span><span class="sxs-lookup"><span data-stu-id="e8600-131">As noted above, the helper function recursively enumerates all objects on a given device.</span></span> <span data-ttu-id="e8600-132">Он возвращает этот список в [**интерфейсе ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , который содержит идентификатор для каждого найденного объекта.</span><span class="sxs-lookup"><span data-stu-id="e8600-132">It returns this list in an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="e8600-133">Вспомогательная функция определяется в модуле Контентенумератион. cpp.</span><span class="sxs-lookup"><span data-stu-id="e8600-133">The helper function is defined in the module ContentEnumeration.cpp.</span></span>


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



<span data-ttu-id="e8600-134">После выполнения предыдущих действий пример приложения инициирует асинхронное получение свойства.</span><span class="sxs-lookup"><span data-stu-id="e8600-134">Once the previous steps are accomplished, the sample application initiates the asynchronous property retrieval.</span></span> <span data-ttu-id="e8600-135">Это достигается путем выполнения следующих действий.</span><span class="sxs-lookup"><span data-stu-id="e8600-135">This is accomplished by doing the following:</span></span>

1.  <span data-ttu-id="e8600-136">Вызов Ипортабледевицепропертиесбулк:: Куеуежетвалуесбйобжектлист, который помещает запрос в очередь на получение набора свойств.</span><span class="sxs-lookup"><span data-stu-id="e8600-136">Calling IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, which queues a request for the bulk property retrieval.</span></span> <span data-ttu-id="e8600-137">(Обратите внимание, что хотя запрос помещается в очередь, он не запускается.)</span><span class="sxs-lookup"><span data-stu-id="e8600-137">(Note that although the request is queued, it is not started.)</span></span>
2.  <span data-ttu-id="e8600-138">Вызов Ипортабледевицепропертиесбулк:: Start для инициации запроса в очереди.</span><span class="sxs-lookup"><span data-stu-id="e8600-138">Calling IPortableDevicePropertiesBulk::Start to initiate the queued request.</span></span>

<span data-ttu-id="e8600-139">Эти шаги показаны в следующем фрагменте кода из примера приложения.</span><span class="sxs-lookup"><span data-stu-id="e8600-139">These steps are demonstrated in the following code excerpt from the sample application.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e8600-140">См. также</span><span class="sxs-lookup"><span data-stu-id="e8600-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8600-141">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="e8600-141">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="e8600-142">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="e8600-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="e8600-143">**Интерфейс Ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="e8600-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="e8600-144">**Интерфейс Ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="e8600-144">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="e8600-145">**Интерфейс Ипортабледевицепропертиесбулк**</span><span class="sxs-lookup"><span data-stu-id="e8600-145">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="e8600-146">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="e8600-146">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="e8600-147">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="e8600-147">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



