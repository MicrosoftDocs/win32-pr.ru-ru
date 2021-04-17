---
description: Получение свойств для нескольких объектов по формату объектов
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Получение свойств для нескольких объектов по формату объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497847"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a><span data-ttu-id="f6a9a-103">Получение свойств для нескольких объектов по формату объектов</span><span class="sxs-lookup"><span data-stu-id="f6a9a-103">Retrieving Properties for Multiple Objects by Object Format</span></span>

<span data-ttu-id="f6a9a-104">Помимо полного извлечения свойств для коллекции идентификаторов объектов, приложение может также выполнять полное извлечение свойств для всех объектов определенного типа.</span><span class="sxs-lookup"><span data-stu-id="f6a9a-104">In addition to a bulk retrieval of properties for a collection of object identifiers, an application can also perform a bulk retrieval of properties for all objects of a particular type.</span></span> <span data-ttu-id="f6a9a-105">Как и в предыдущем примере, для полного извлечения для данного типа требуется, чтобы драйвер устройства поддерживал операции полного извлечения.</span><span class="sxs-lookup"><span data-stu-id="f6a9a-105">As in the previous example, bulk retrieval for a given type requires that the device driver support bulk retrievals.</span></span>

<span data-ttu-id="f6a9a-106">Приложение может выполнять групповое извлечение с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f6a9a-106">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="f6a9a-107">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f6a9a-107">Interface</span></span>                                                                                      | <span data-ttu-id="f6a9a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f6a9a-108">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="f6a9a-109">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="f6a9a-110">Предоставляет доступ к методам, относящимся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="f6a9a-110">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="f6a9a-111">**Интерфейс Ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-111">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="f6a9a-112">Используется для задания извлекаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="f6a9a-112">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="f6a9a-113">**Интерфейс Ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-113">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="f6a9a-114">Используется для определения того, поддерживает ли данный драйвер групповые операции.</span><span class="sxs-lookup"><span data-stu-id="f6a9a-114">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="f6a9a-115">**Интерфейс Ипортабледевицепропертиесбулк**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-115">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="f6a9a-116">Поддерживает операцию извлечения с массовым набором.</span><span class="sxs-lookup"><span data-stu-id="f6a9a-116">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="f6a9a-117">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-117">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="f6a9a-118">Используется для хранения идентификаторов объектов для групповой операции.</span><span class="sxs-lookup"><span data-stu-id="f6a9a-118">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="f6a9a-119">Функция Реадконтентпропертиесбулкфилтерингформат в модуле Контентпропертиес. cpp примера приложения демонстрирует операцию множественного извлечения для объектов определенного типа или формата.</span><span class="sxs-lookup"><span data-stu-id="f6a9a-119">The ReadContentPropertiesBulkFilteringFormat function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation for objects of a particular type or format.</span></span>

<span data-ttu-id="f6a9a-120">Код, обнаруженный в функции Реадконтентпропертиесбулкфилтерингформат, почти идентичен коду, обнаруженному в функции Реадконтентпропертиесбулк.</span><span class="sxs-lookup"><span data-stu-id="f6a9a-120">The code found in the ReadContentPropertiesBulkFilteringFormat function is almost identical to the code found in the ReadContentPropertiesBulk function.</span></span> <span data-ttu-id="f6a9a-121">(Полное описание этой функции см. в разделе [Получение свойств для нескольких объектов](retrieving-properties-for-multiple-objects.md) .)</span><span class="sxs-lookup"><span data-stu-id="f6a9a-121">(See the [Retrieving Properties for Multiple Objects](retrieving-properties-for-multiple-objects.md) topic for a complete description of this function.)</span></span>

<span data-ttu-id="f6a9a-122">Одно основное различие возникает при постановке операции в очередь.</span><span class="sxs-lookup"><span data-stu-id="f6a9a-122">The one primary difference occurs when the operation is queued.</span></span> <span data-ttu-id="f6a9a-123">При фильтрации по типу или формату вызывается метод [**ипортабледевицепропертиесбулк:: куеуежетвалуесбйобжектформат**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) , а не метод [**Ипортабледевицепропертиесбулк:: QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) .</span><span class="sxs-lookup"><span data-stu-id="f6a9a-123">When filtering by type or format, the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) method is called instead of the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) method.</span></span>


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a><span data-ttu-id="f6a9a-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f6a9a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6a9a-125">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="f6a9a-126">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="f6a9a-127">**Интерфейс Ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-127">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="f6a9a-128">**Интерфейс Ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-128">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="f6a9a-129">**Интерфейс Ипортабледевицепропертиесбулк**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-129">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="f6a9a-130">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-130">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="f6a9a-131">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="f6a9a-131">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



