---
title: Получение свойств объекта WPD
description: Получение свойств объекта
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3c6eba4435b23ef5c637feaca7c2d4ab6b160e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081240"
---
# <a name="retrieving-wpd-object-properties"></a><span data-ttu-id="c6705-103">Получение свойств объекта WPD</span><span class="sxs-lookup"><span data-stu-id="c6705-103">Retrieving WPD object properties</span></span>

<span data-ttu-id="c6705-104">Службы часто содержат дочерние объекты, принадлежащие одному из форматов, поддерживаемых каждой службой.</span><span class="sxs-lookup"><span data-stu-id="c6705-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="c6705-105">Например, служба контактов может поддерживать несколько контактных объектов из формата абстрактного контакта.</span><span class="sxs-lookup"><span data-stu-id="c6705-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="c6705-106">Каждый объект Contact описывается связанными свойствами (имя контактного лица, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="c6705-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="c6705-107">Приложение Впдсервицеаписампле содержит код, демонстрирующий, как приложение может извлекать свойства объекта содержимого, поддерживаемые данной службой контактов.</span><span class="sxs-lookup"><span data-stu-id="c6705-107">The WpdServiceApiSample application includes code that demonstrates how an application can retrieve the content-object properties supported by a given Contacts service.</span></span> <span data-ttu-id="c6705-108">В этом образце используются следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="c6705-108">This sample uses the following interfaces.</span></span>



|                                                                      |                                                                                              |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6705-109">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="c6705-109">Interface</span></span>                                                            | <span data-ttu-id="c6705-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c6705-110">Description</span></span>                                                                                  |
| [<span data-ttu-id="c6705-111">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="c6705-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="c6705-112">Извлекает интерфейс **IPortableDeviceContent2** для доступа к поддерживаемым методам службы.</span><span class="sxs-lookup"><span data-stu-id="c6705-112">Retrieves the **IPortableDeviceContent2** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="c6705-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="c6705-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="c6705-114">Предоставляет доступ к методам, относящимся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="c6705-114">Provides access to the content-specific methods.</span></span>                                             |
| [<span data-ttu-id="c6705-115">**ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="c6705-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | <span data-ttu-id="c6705-116">Возвращает значения свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="c6705-116">Retrieves the object property values.</span></span>                                                        |
| [<span data-ttu-id="c6705-117">**ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="c6705-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)               | <span data-ttu-id="c6705-118">Содержит значения свойств, которые были считаны для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="c6705-118">Holds the property values that were read for that object.</span></span>                                    |
| [<span data-ttu-id="c6705-119">**ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="c6705-119">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md) | <span data-ttu-id="c6705-120">Содержит параметры для данного метода.</span><span class="sxs-lookup"><span data-stu-id="c6705-120">Contains the parameters for a given method.</span></span>                                                  |



 

<span data-ttu-id="c6705-121">Когда пользователь выбирает параметр "7" в командной строке, приложение вызывает метод **реадконтентпропертиес** , который находится в модуле контентпропертиес. cpp.</span><span class="sxs-lookup"><span data-stu-id="c6705-121">When the user chooses option "7" at the command line, the application invokes the **ReadContentProperties** method that is found in the ContentProperties.cpp module.</span></span>

<span data-ttu-id="c6705-122">Этот метод получает следующие четыре свойства для указанного объекта Contact.</span><span class="sxs-lookup"><span data-stu-id="c6705-122">This method retrieves the following four properties for the specified contact object.</span></span>



|                              |                                                                                                                                                                                                                  |                                 |                                     |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| <span data-ttu-id="c6705-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="c6705-123">Property</span></span>                     | <span data-ttu-id="c6705-124">Описание</span><span class="sxs-lookup"><span data-stu-id="c6705-124">Description</span></span>                                                                                                                                                                                                      | <span data-ttu-id="c6705-125">PROPERTYKEY служб устройств</span><span class="sxs-lookup"><span data-stu-id="c6705-125">Device Services PROPERTYKEY</span></span>     | <span data-ttu-id="c6705-126">Эквивалентный \_ PROPERTYKEY WPD</span><span class="sxs-lookup"><span data-stu-id="c6705-126">Equivalent WPD\_PROPERTYKEY</span></span>         |
| <span data-ttu-id="c6705-127">Идентификатор родительского объекта</span><span class="sxs-lookup"><span data-stu-id="c6705-127">Parent-object identifier</span></span>     | <span data-ttu-id="c6705-128">Строка, указывающая идентификатор родителя данного объекта.</span><span class="sxs-lookup"><span data-stu-id="c6705-128">A string that specifies the identifier for the given object's parent.</span></span>                                                                                                                                            | <span data-ttu-id="c6705-129">PKEY \_ женерикобж \_ ParentID</span><span class="sxs-lookup"><span data-stu-id="c6705-129">PKEY\_GenericObj\_ParentID</span></span>      | <span data-ttu-id="c6705-130">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c6705-130">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="c6705-131">Имя объекта</span><span class="sxs-lookup"><span data-stu-id="c6705-131">Object name</span></span>                  | <span data-ttu-id="c6705-132">Строка, указывающая имя данного объекта</span><span class="sxs-lookup"><span data-stu-id="c6705-132">A string that specifies the name of the given object</span></span>                                                                                                                                                             | <span data-ttu-id="c6705-133">\_Имя PKEY женерикобж \_</span><span class="sxs-lookup"><span data-stu-id="c6705-133">PKEY\_GenericObj\_Name</span></span>          | <span data-ttu-id="c6705-134">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c6705-134">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="c6705-135">Постоянный уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="c6705-135">Persistent unique identifier</span></span> | <span data-ttu-id="c6705-136">Строка, указывающая уникальный идентификатор для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="c6705-136">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="c6705-137">Этот идентификатор сохраняется в сеансах в отличие от идентификатора объекта.</span><span class="sxs-lookup"><span data-stu-id="c6705-137">This identifier is persistent across sessions, unlike the object identifier.</span></span> <span data-ttu-id="c6705-138">Для служб это должно быть строковое представление идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="c6705-138">For services, this needs to be a string-representation of a GUID.</span></span> | <span data-ttu-id="c6705-139">PKEY \_ женерикобж \_ персистентуид</span><span class="sxs-lookup"><span data-stu-id="c6705-139">PKEY\_GenericObj\_PersistentUID</span></span> | <span data-ttu-id="c6705-140">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c6705-140">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="c6705-141">Формат объекта</span><span class="sxs-lookup"><span data-stu-id="c6705-141">Object format</span></span>                | <span data-ttu-id="c6705-142">Глобальный уникальный идентификатор (GUID), указывающий формат файла, соответствующего заданному объекту.</span><span class="sxs-lookup"><span data-stu-id="c6705-142">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object</span></span>                                                                                                        | <span data-ttu-id="c6705-143">PKEY \_ женерикобж \_ обжектформат</span><span class="sxs-lookup"><span data-stu-id="c6705-143">PKEY\_GenericObj\_ObjectFormat</span></span>  | <span data-ttu-id="c6705-144">\_Формат объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c6705-144">WPD\_OBJECT\_FORMAT</span></span>                 |



 

-   <span data-ttu-id="c6705-145">Идентификатор родителя</span><span class="sxs-lookup"><span data-stu-id="c6705-145">Parent ID</span></span>
-   <span data-ttu-id="c6705-146">Имя</span><span class="sxs-lookup"><span data-stu-id="c6705-146">Name</span></span>
-   <span data-ttu-id="c6705-147">персистентуид</span><span class="sxs-lookup"><span data-stu-id="c6705-147">PersistentUID</span></span>
-   <span data-ttu-id="c6705-148">Формат</span><span class="sxs-lookup"><span data-stu-id="c6705-148">Format</span></span>

<span data-ttu-id="c6705-149">Обратите внимание, что перед получением свойств содержимого пример приложения открывает службу контактов на подключенном устройстве.</span><span class="sxs-lookup"><span data-stu-id="c6705-149">Note that prior to retrieving the content properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="c6705-150">В следующем коде для метода **реадконтентпропертиес** показано, как приложение использует интерфейс [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) для получения интерфейса [**ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) .</span><span class="sxs-lookup"><span data-stu-id="c6705-150">The following code for the **ReadContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="c6705-151">Передавая ПРОПЕРТИКЭЙС запрошенных свойств в метод [**ипортабледевицепропертиес::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) , **реадконтентпропертиес** извлекает запрошенные значения, а затем отображает их в окне консоли.</span><span class="sxs-lookup"><span data-stu-id="c6705-151">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **ReadContentProperties** retrieves the requested values, and then displays them to the console window.</span></span>


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting property reading\n");
    }

    // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pService->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
        }
    }

    // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
    // to access the property-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pContent->Properties(&pProperties);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
        }
    }

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
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
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
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

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="c6705-152">См. также</span><span class="sxs-lookup"><span data-stu-id="c6705-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6705-153">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="c6705-153">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="c6705-154">**ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="c6705-154">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="c6705-155">впдсервицесаписампле</span><span class="sxs-lookup"><span data-stu-id="c6705-155">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



