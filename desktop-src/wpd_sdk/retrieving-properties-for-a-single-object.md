---
description: Получение свойств для одного объекта
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Получение свойств для одного объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5851b31256659c2ca036bac504a53fa51a20ee14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712480"
---
# <a name="retrieving-properties-for-a-single-object"></a><span data-ttu-id="20b39-103">Получение свойств для одного объекта</span><span class="sxs-lookup"><span data-stu-id="20b39-103">Retrieving Properties for a Single Object</span></span>

<span data-ttu-id="20b39-104">После того как приложение извлекает идентификатор объекта (см. раздел " [Перечисление содержимого](enumerating-content.md) ") для данного объекта, он может получить описательные сведения об этом объекте, вызвав методы в [**интерфейсе ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) и [**интерфейсе ипортабледевицекэйколлектион**](iportabledevicekeycollection.md).</span><span class="sxs-lookup"><span data-stu-id="20b39-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can retrieve descriptive information about that object by calling methods in the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) and the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md).</span></span>

<span data-ttu-id="20b39-105">Метод [**ипортабледевицепропертиес::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) GetObject извлекает список указанных свойств для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="20b39-105">The [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method retrieves a list of specified properties for a given object.</span></span> <span data-ttu-id="20b39-106">(Приложение может также вызвать метод GetObjects и указать значение **null** для параметра PKEY, чтобы получить все свойства для данного объекта, однако производительность этого метода может значительно замедлиться при получении всех свойств.)</span><span class="sxs-lookup"><span data-stu-id="20b39-106">(Your application could also call the GetValues method and specify a **NULL** value for the pKeys parameter to retrieve all properties for a given object; however, the performance of this method may be significantly slower when retrieving all properties.)</span></span>

<span data-ttu-id="20b39-107">Однако перед тем, как приложение вызовет методы GetObject, необходимо задать свойства для извлечения, задав соответствующие ключи в [**объекте ипортабледевицекэйколлектион**](iportabledevicekeycollection.md).</span><span class="sxs-lookup"><span data-stu-id="20b39-107">Before your application calls GetValues, however, it needs to identify the properties to retrieve by setting corresponding keys in an [**IPortableDeviceKeyCollection object**](iportabledevicekeycollection.md).</span></span> <span data-ttu-id="20b39-108">Приложение определит интересующие вас свойства, вызвав метод [**ипортабледевицекэйколлектион:: Add**](iportabledevicekeycollection-add.md) и УКАЗАВ значение PROPERTYKEY, идентифицирующее каждое свойство, которое оно будет извлекать.</span><span class="sxs-lookup"><span data-stu-id="20b39-108">Your application will identify the properties of interest by calling the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method and supplying a PROPERTYKEY value that identifies each property that it will retrieve.</span></span>

<span data-ttu-id="20b39-109">Функция Реадконтентпропертиес в модуле Контентпропертиес. cpp примера приложения демонстрирует, как извлекаются пять свойств для выбранного объекта.</span><span class="sxs-lookup"><span data-stu-id="20b39-109">The ReadContentProperties function in the ContentProperties.cpp module of the sample application demonstrates how the five properties were retrieved for a selected object.</span></span> <span data-ttu-id="20b39-110">В следующей таблице описаны все эти свойства и соответствующие значения РЕФПРОПЕРТИКЭЙ.</span><span class="sxs-lookup"><span data-stu-id="20b39-110">The following table describes each of these properties and their corresponding REFPROPERTYKEY value.</span></span>



| <span data-ttu-id="20b39-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="20b39-111">Property</span></span>                     | <span data-ttu-id="20b39-112">Описание</span><span class="sxs-lookup"><span data-stu-id="20b39-112">Description</span></span>                                                                                                                                      | <span data-ttu-id="20b39-113">PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="20b39-113">PROPERTYKEY</span></span>                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="20b39-114">Идентификатор родительского объекта</span><span class="sxs-lookup"><span data-stu-id="20b39-114">Parent-object identifier</span></span>     | <span data-ttu-id="20b39-115">Строка, указывающая идентификатор родителя данного объекта.</span><span class="sxs-lookup"><span data-stu-id="20b39-115">A string that specifies the identifier for the given object's parent.</span></span>                                                                            | <span data-ttu-id="20b39-116">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="20b39-116">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="20b39-117">Имя объекта</span><span class="sxs-lookup"><span data-stu-id="20b39-117">Object name</span></span>                  | <span data-ttu-id="20b39-118">Строка, указывающая имя данного объекта.</span><span class="sxs-lookup"><span data-stu-id="20b39-118">A string that specifies the name of the given object.</span></span>                                                                                            | <span data-ttu-id="20b39-119">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="20b39-119">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="20b39-120">Постоянный уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="20b39-120">Persistent unique identifier</span></span> | <span data-ttu-id="20b39-121">Строка, указывающая уникальный идентификатор для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="20b39-121">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="20b39-122">(Этот идентификатор сохраняется в сеансах, в отличие от идентификатора объекта.)</span><span class="sxs-lookup"><span data-stu-id="20b39-122">(This identifier is persistent across sessions, unlike the object identifier.)</span></span> | <span data-ttu-id="20b39-123">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="20b39-123">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="20b39-124">Формат объекта</span><span class="sxs-lookup"><span data-stu-id="20b39-124">Object format</span></span>                | <span data-ttu-id="20b39-125">Глобальный уникальный идентификатор (GUID), указывающий формат файла, соответствующего заданному объекту.</span><span class="sxs-lookup"><span data-stu-id="20b39-125">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object.</span></span>                                       | <span data-ttu-id="20b39-126">\_Формат объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="20b39-126">WPD\_OBJECT\_FORMAT</span></span>                 |
| <span data-ttu-id="20b39-127">Тип содержимого объекта</span><span class="sxs-lookup"><span data-stu-id="20b39-127">Object content type</span></span>          | <span data-ttu-id="20b39-128">Идентификатор GUID, указывающий тип содержимого, связанного с данным объектом.</span><span class="sxs-lookup"><span data-stu-id="20b39-128">A GUID that specifies the type of content associated with a given object.</span></span>                                                                        | <span data-ttu-id="20b39-129">\_ \_ тип содержимого объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="20b39-129">WPD\_OBJECT\_CONTENT\_TYPE</span></span>          |



 

<span data-ttu-id="20b39-130">В следующем фрагменте функции Реадконтентпропертиес показано, как в примере приложения использовался [**интерфейс ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) и метод [**Ипортабледевицекэйколлектион:: Add**](iportabledevicekeycollection-add.md) для определения получаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="20b39-130">The following excerpt from the ReadContentProperties function demonstrates how the sample application used the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method to identify the properties it would retrieve.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPropertiesToRead));
if (SUCCEEDED(hr))
{
    // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="20b39-131">После того как пример приложения настроил соответствующие ключи, он вызывает метод [**ипортабледевицепропертиес::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) GetObject, чтобы получить указанные значения для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="20b39-131">Once the sample application set the appropriate keys, it called the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method to retrieve the specified values for the given object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                pPropertiesToRead,   // The properties we want to read
                                &pObjectProperties); // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="20b39-132">См. также</span><span class="sxs-lookup"><span data-stu-id="20b39-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20b39-133">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="20b39-133">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="20b39-134">**Интерфейс Ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="20b39-134">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="20b39-135">**Интерфейс Ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="20b39-135">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="20b39-136">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="20b39-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



