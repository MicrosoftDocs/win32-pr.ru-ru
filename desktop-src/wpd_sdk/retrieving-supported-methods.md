---
description: Получение поддерживаемых методов службы
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Получение поддерживаемых методов службы
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6029af655a8835a4eee887d919c534856062ff13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911120"
---
# <a name="retrieving-supported-service-methods"></a><span data-ttu-id="0f76b-103">Получение поддерживаемых методов службы</span><span class="sxs-lookup"><span data-stu-id="0f76b-103">Retrieving Supported Service Methods</span></span>

<span data-ttu-id="0f76b-104">Методы службы инкапсулируют функциональные возможности, определяемые и реализуемые каждой службой.</span><span class="sxs-lookup"><span data-stu-id="0f76b-104">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="0f76b-105">Они относятся к каждому типу служб и представляются уникальными идентификаторами GUID.</span><span class="sxs-lookup"><span data-stu-id="0f76b-105">They are specific to each type of service type and are represented by a unique GUID.</span></span>

<span data-ttu-id="0f76b-106">Например, служба Contacts определяет метод **бегинсинк** , который вызывается приложениями для подготовки устройства к синхронизации объектов Contact, и метод **ендсинк** для уведомления устройства о завершении синхронизации.</span><span class="sxs-lookup"><span data-stu-id="0f76b-106">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span>

<span data-ttu-id="0f76b-107">Приложения могут программно запрашивать Поддерживаемые методы и получать доступ к этим методам и их атрибутам с помощью интерфейса [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="0f76b-107">Applications can programmatically query the supported methods and access these methods and their attributes by using the [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span>

<span data-ttu-id="0f76b-108">Методы службы не следует путать с командами WPD.</span><span class="sxs-lookup"><span data-stu-id="0f76b-108">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="0f76b-109">Команды WPD являются частью стандартного интерфейса драйвера устройства WPD (DDI) и являются механизмом обмена данными между приложением WPD и драйвером.</span><span class="sxs-lookup"><span data-stu-id="0f76b-109">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="0f76b-110">Команды являются предопределенными, сгруппированные по категориям, например \_ категории WPD \_ Common, и представляются структурой PROPERTYKEY.</span><span class="sxs-lookup"><span data-stu-id="0f76b-110">Commands are predefined, grouped by categories, for example, WPD\_CATEGORY\_COMMON, and are represented by a PROPERTYKEY structure.</span></span> <span data-ttu-id="0f76b-111">Дополнительные сведения см. в разделе [**команды**](commands.md) .</span><span class="sxs-lookup"><span data-stu-id="0f76b-111">For more information, see the [**Commands**](commands.md) topic.</span></span>

<span data-ttu-id="0f76b-112">Приложение Впдсервицесаписампле содержит код, демонстрирующий, как приложение может извлекать методы, поддерживаемые данной службой контактов, с помощью интерфейсов, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0f76b-112">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the methods supported by a given Contacts service by using the interfaces in the following table.</span></span>



|                                                                                      |                                                                                                                |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f76b-113">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="0f76b-113">Interface</span></span>                                                                            | <span data-ttu-id="0f76b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="0f76b-114">Description</span></span>                                                                                                    |
| [<span data-ttu-id="0f76b-115">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="0f76b-115">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="0f76b-116">Используется для получения интерфейса **ипортабледевицесервицекапабилитиес** для доступа к поддерживаемым методам службы.</span><span class="sxs-lookup"><span data-stu-id="0f76b-116">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="0f76b-117">**ипортабледевицесервицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="0f76b-117">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="0f76b-118">Предоставляет доступ к поддерживаемым методам, атрибутам методов и параметрам методов.</span><span class="sxs-lookup"><span data-stu-id="0f76b-118">Provides access to the supported methods, method attributes and method parameters.</span></span>                             |
| [<span data-ttu-id="0f76b-119">**ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="0f76b-119">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="0f76b-120">Содержит список поддерживаемых методов.</span><span class="sxs-lookup"><span data-stu-id="0f76b-120">Contains the list of supported methods.</span></span>                                                                        |
| [<span data-ttu-id="0f76b-121">**ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="0f76b-121">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="0f76b-122">Содержит атрибуты для метода и для параметров данного метода.</span><span class="sxs-lookup"><span data-stu-id="0f76b-122">Contains the attributes for a method and for a given method's parameters.</span></span>                                      |
| [<span data-ttu-id="0f76b-123">**ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="0f76b-123">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="0f76b-124">Содержит параметры для данного метода.</span><span class="sxs-lookup"><span data-stu-id="0f76b-124">Contains the parameters for a given method.</span></span>                                                                    |



 

<span data-ttu-id="0f76b-125">Когда пользователь выбирает параметр "5" в командной строке, приложение вызывает метод **листсуппортедмесодс** , который находится в модуле сервицемесодс. cpp.</span><span class="sxs-lookup"><span data-stu-id="0f76b-125">When the user chooses option "5" at the command line, the application invokes the **ListSupportedMethods** method that is found in the ServiceMethods.cpp module.</span></span>

<span data-ttu-id="0f76b-126">Обратите внимание, что перед получением списка событий пример приложения открывает службу контактов на подключенном устройстве.</span><span class="sxs-lookup"><span data-stu-id="0f76b-126">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="0f76b-127">В WPD метод описывается его именем, правами доступа, параметрами и связанными данными.</span><span class="sxs-lookup"><span data-stu-id="0f76b-127">In WPD, a method is described by its name, access rights, parameters, and related data.</span></span> <span data-ttu-id="0f76b-128">Пример приложения отображает понятное имя, например "Кустоммесод", или GUID.</span><span class="sxs-lookup"><span data-stu-id="0f76b-128">The sample application displays a user-friendly name, for example, "CustomMethod", or a GUID.</span></span> <span data-ttu-id="0f76b-129">За именем метода или идентификатором GUID следует доступ к данным ("чтение и запись"), имя любого связанного формата и данные параметра.</span><span class="sxs-lookup"><span data-stu-id="0f76b-129">The method name or GUID is followed by access data ("Read/Write"), the name of any associated format, and the parameter data.</span></span> <span data-ttu-id="0f76b-130">Эти данные включают имя параметра, использование, VARTYPE и форму.</span><span class="sxs-lookup"><span data-stu-id="0f76b-130">This data includes the parameter name, usage, VARTYPE, and form.</span></span>

<span data-ttu-id="0f76b-131">Пять методов в модуле Сервицемесодс. cpp поддерживают извлечение методов (и связанных данных) для заданной службы Contacts: **листсуппортедмесодс**, **дисплаймесод**, **дисплаймесодакцесс**, **DisplayFormat** и **дисплаймесодпараметерс**.</span><span class="sxs-lookup"><span data-stu-id="0f76b-131">Five methods in the ServiceMethods.cpp module support the retrieval of methods (and related data) for the given Contacts service: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters**.</span></span> <span data-ttu-id="0f76b-132">Метод **листсуппортедмесодс** извлекает количество поддерживаемых методов и идентификатор GUID для каждого; Затем он вызывает метод **дисплаймесод** .</span><span class="sxs-lookup"><span data-stu-id="0f76b-132">The **ListSupportedMethods** method retrieves a count of supported methods and the GUID identifier for each; it then calls the **DisplayMethod** method.</span></span> <span data-ttu-id="0f76b-133">Метод **дисплаймесод** вызывает метод [**Ипортабледевицесервицекапапбилитиес:: жетмесодаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) для получения параметров данного метода, параметров и т. д.</span><span class="sxs-lookup"><span data-stu-id="0f76b-133">The **DisplayMethod** method calls the [**IPortableDeviceServiceCapapbilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve the given method's options, parameters, and so on.</span></span> <span data-ttu-id="0f76b-134">После того как **дисплаймесод** извлекает данные метода, он отображает имя (или GUID), ограничения доступа, связанный формат (если он есть) и описания параметров.</span><span class="sxs-lookup"><span data-stu-id="0f76b-134">After the **DisplayMethod** retrieves the method data, it renders the name (or GUID), the access restrictions, the associated format (if any), and the parameter descriptions.</span></span> <span data-ttu-id="0f76b-135">**Дисплаймесодакцесс**, **DisplayFormat** и **дисплаймесодпараметерс** — это вспомогательные функции, которые отображают соответствующие поля данных.</span><span class="sxs-lookup"><span data-stu-id="0f76b-135">The **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** are helper functions that render their respective fields of data.</span></span>

<span data-ttu-id="0f76b-136">Метод **листсуппортедмесодс** вызывает метод [**Ипортабледевицесервице:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) для получения интерфейса [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="0f76b-136">The **ListSupportedMethods** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="0f76b-137">Используя этот интерфейс, он получает Поддерживаемые методы, вызывая метод [**ипортабледевицесервицекапабилитиес:: жетсуппортедмесодс**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) .</span><span class="sxs-lookup"><span data-stu-id="0f76b-137">Using this interface, it retrieves the supported methods by calling the [**IPortableDeviceServiceCapabilities::GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="0f76b-138">Метод **жетсуппортедмесодс** извлекает идентификаторы GUID для каждого метода, поддерживаемого службой, и копирует этот идентификатор GUID в объект [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="0f76b-138">The **GetSupportedMethods** method retrieves the GUIDs for each method supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="0f76b-139">В следующем коде используется метод **листсуппортедмесодс** .</span><span class="sxs-lookup"><span data-stu-id="0f76b-139">The following code uses the **ListSupportedMethods** method.</span></span>


```C++
// List all supported methods on the service
void ListSupportedMethods(IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumMethods    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all methods supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedMethods(&pMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get supported methods from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported methods found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pMethods->GetCount(&dwNumMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported methods, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Methods Found on the service\n\n", dwNumMethods);

    // Loop through each method and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumMethods; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pMethods->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a method.  It is assumed that
                // methods are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayMethod(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }    
}
```



<span data-ttu-id="0f76b-140">После того как метод **листсуппортедмесодс** извлекает идентификатор GUID для каждого события, поддерживаемого данной службой, он вызывает метод **дисплаймесод** для получения атрибутов, зависящих от метода.</span><span class="sxs-lookup"><span data-stu-id="0f76b-140">After the **ListSupportedMethods** method retrieves the GUID for each event supported by the given service, it invokes the **DisplayMethod** method to retrieve the method-specific attributes.</span></span> <span data-ttu-id="0f76b-141">К этим атрибутам относятся: понятное для скрипта имя, необходимые ограничения доступа, любой связанный формат и список параметров.</span><span class="sxs-lookup"><span data-stu-id="0f76b-141">These attributes include: the method's script-friendly name , required access restrictions, any associated format, and list of parameters.</span></span>

<span data-ttu-id="0f76b-142">Метод **дисплаймесод** вызывает метод [**Ипортабледевицесервицекапабилитиес:: жетмесодаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) для получения коллекции атрибутов для данного метода.</span><span class="sxs-lookup"><span data-stu-id="0f76b-142">The **DisplayMethod** method invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve a collection of attributes for the given method.</span></span> <span data-ttu-id="0f76b-143">Затем он вызывает метод [**ипортабледевицевалуес:: GetStringValue**](iportabledevicevalues-getstringvalue.md) для получения имени метода.</span><span class="sxs-lookup"><span data-stu-id="0f76b-143">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method to retrieve the method's name.</span></span> <span data-ttu-id="0f76b-144">**Дисплаймесод** вызывает [**Ипортабледевицевалуес:: жетунсигнединтежервалуе**](iportabledevicevalues-getunsignedintegervalue.md) для получения доступа рестрктионс.</span><span class="sxs-lookup"><span data-stu-id="0f76b-144">The **DisplayMethod** calls the [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) to retrieve the access restrctions.</span></span> <span data-ttu-id="0f76b-145">После этого он вызывает [**ипортабледевицевалуес:: жетгуидвалуе**](iportabledevicevalues-getguidvalue.md) для получения любого связанного формата.</span><span class="sxs-lookup"><span data-stu-id="0f76b-145">After this, it calls [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) to retrieve any associated format.</span></span> <span data-ttu-id="0f76b-146">И, наконец, **дисплаймесод** вызывает метод [**Ипортабледевицевалуес:: жетипортабледевицекэйколлектионвалуе**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) для получения данных параметра.</span><span class="sxs-lookup"><span data-stu-id="0f76b-146">And, finally, the **DisplayMethod** calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the parameter data.</span></span> <span data-ttu-id="0f76b-147">Он передает данные, возвращаемые этими методами, в вспомогательные функции **дисплаймесодакцесс**, **DisplayFormat** и **дисплаймесодпараметерс** , которые отображают сведения для данного метода.</span><span class="sxs-lookup"><span data-stu-id="0f76b-147">It passes the data returned by these methods to the **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** helper functions, which render the information for the given method.</span></span>

<span data-ttu-id="0f76b-148">В следующем коде используется метод **дисплаймесод** .</span><span class="sxs-lookup"><span data-stu-id="0f76b-148">The following code uses the **DisplayMethod** method.</span></span>


```C++
// Display basic information about a method
void DisplayMethod(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the method attributes which describe the method
    HRESULT hr = pCapabilities->GetMethodAttributes(Method, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the method attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR   pszMethodName  = NULL;
        DWORD   dwMethodAccess = WPD_COMMAND_ACCESS_READ;
        GUID    guidFormat     = GUID_NULL;

        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the method if available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_METHOD_ATTRIBUTE_NAME, &pszMethodName);
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszMethodName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Method));
        }       

        // Display the method access if available, otherwise default to WPD_COMMAND_ACCESS_READ access
        hr = pAttributes->GetUnsignedIntegerValue(WPD_METHOD_ATTRIBUTE_ACCESS, &dwMethodAccess);
        if (FAILED(hr))
        {
            dwMethodAccess = WPD_COMMAND_ACCESS_READ;
            hr = S_OK;
        }
        printf("\n\tAccess: ");
        DisplayMethodAccess(dwMethodAccess);

        // Display the associated format if specified.
        // Methods that have an associated format may only be supported for that format.
        // Methods that don't have associated formats generally apply to the entire service.
        hr = pAttributes->GetGuidValue(WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("\n\tAssociated Format: ");
            DisplayFormat(pCapabilities, guidFormat);
        }

        // Display the method parameters, if available
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_METHOD_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayMethodParameters(pCapabilities, Method, pParameters);
        }
        
        CoTaskMemFree(pszMethodName);
        pszMethodName = NULL;

    }
}
```



<span data-ttu-id="0f76b-149">Вспомогательная функция **дисплаймесодакцесс** получает значение типа DWORD, которое содержит параметры доступа метода.</span><span class="sxs-lookup"><span data-stu-id="0f76b-149">The **DisplayMethodAccess** helper function receives a DWORD value that contains the method's access options.</span></span> <span data-ttu-id="0f76b-150">Он сравнивает это значение с командой WPD, доступное для \_ команды, \_ \_ Read и WPD, \_ \_ \_ чтобы определить права доступа метода.</span><span class="sxs-lookup"><span data-stu-id="0f76b-150">It compares this value to WPD\_COMMAND\_ACCESS\_READ and WPD\_COMMAND\_ACCESS\_READWRITE to determine the method's access privilege.</span></span> <span data-ttu-id="0f76b-151">Используя результат, он отображает строку, указывающую ограничение доступа для данного метода.</span><span class="sxs-lookup"><span data-stu-id="0f76b-151">Using the result, it renders a string indicating the access restriction for the given method.</span></span>

<span data-ttu-id="0f76b-152">В следующем коде используется вспомогательная функция **дисплаймесодакцесс** .</span><span class="sxs-lookup"><span data-stu-id="0f76b-152">The following code uses the **DisplayMethodAccess** helper function.</span></span>


```C++
void DisplayMethodAccess(
    DWORD   dwAccess)
{
    switch(static_cast<WPD_COMMAND_ACCESS_TYPES>(dwAccess))
    {
        case WPD_COMMAND_ACCESS_READ:
            printf("Read");
            break;
            
        case WPD_COMMAND_ACCESS_READWRITE:
            printf("Read/Write");
            break;

        default:
            printf("Unknown Access");
            break;
    }
}
```



<span data-ttu-id="0f76b-153">Вспомогательная функция **дисплаймесод** получает объект [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) и идентификатор GUID метода в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="0f76b-153">The **DisplayMethod** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object and the method's GUID as parameters.</span></span> <span data-ttu-id="0f76b-154">Используя объект **ипортабледевицесервицекапабилитиес** , он вызывает метод [**Ипортабледевицесервицекапабилитиес:: жетмесодаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) для получения атрибутов метода и их отображения в окне консоли приложения.</span><span class="sxs-lookup"><span data-stu-id="0f76b-154">Using the **IPortableDeviceServiceCapabilities** object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method to retrieve the method attributes and render them in the application's console window.</span></span>

<span data-ttu-id="0f76b-155">Вспомогательная функция **дисплаймесодпараметерс** получает объект [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) , GUID метода и объект ипортабледевицекэйколлектион, содержащий параметры метода.</span><span class="sxs-lookup"><span data-stu-id="0f76b-155">The **DisplayMethodParameters** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object, the method's GUID, and an IPortableDeviceKeyCollection object containing the method parameters.</span></span> <span data-ttu-id="0f76b-156">Используя объект [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) , он вызывает метод [**Ипортабледевицесервицекапабилитиес:: жетмесодпараметераттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) для получения имени параметра, использования, VarType и формы.</span><span class="sxs-lookup"><span data-stu-id="0f76b-156">Using the [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) method to retrieve the parameter's name, usage, VARTYPE, and form.</span></span> <span data-ttu-id="0f76b-157">Эта информация отображается в окне консоли приложения.</span><span class="sxs-lookup"><span data-stu-id="0f76b-157">It renders this information in the application's console window.</span></span>

<span data-ttu-id="0f76b-158">В следующем коде используется вспомогательная функция **дисплаймесодпараметерс** .</span><span class="sxs-lookup"><span data-stu-id="0f76b-158">The following code uses the **DisplayMethodParameters** helper function.</span></span>


```C++
// Display the method parameters.
void DisplayMethodParameters(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method,
    IPortableDeviceKeyCollection*       pParameters)
{
    DWORD   dwNumParameters = 0;

    // Get the number of parameters for this event.
    HRESULT hr = pParameters->GetCount(&dwNumParameters);
    if (FAILED(hr))
    {
        printf("! Failed to get number of parameters, hr = 0x%lx\n",hr);
    }

    printf("\n\t%d Method Parameters:\n", dwNumParameters);

    // Loop through each parameter and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumParameters; dwIndex++)
        {
            PROPERTYKEY parameter;
            hr = pParameters->GetAt(dwIndex, &parameter);

            if (SUCCEEDED(hr))
            {
                CComPtr<IPortableDeviceValues> pAttributes;

                // Display the parameter's Name, Usage, Vartype, and Form
                hr = pCapabilities->GetMethodParameterAttributes(Method, parameter, &pAttributes);
                if (FAILED(hr))
                {
                    printf("! Failed to get the method parameter attributes, hr = 0x%lx\n",hr);
                }

                if (SUCCEEDED(hr))
                {
                    PWSTR   pszParameterName    = NULL;
                    DWORD   dwAttributeVarType  = 0;
                    DWORD   dwAttributeForm     = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                    DWORD   dwAttributeUsage    = (DWORD)-1;

                    hr = pAttributes->GetStringValue(WPD_PARAMETER_ATTRIBUTE_NAME, &pszParameterName);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tName: %ws\n", pszParameterName);
                    }
                    else
                    {
                        printf("! Failed to get the method parameter name, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_USAGE value, if specified. 
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_USAGE, &dwAttributeUsage);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tUsage: ");
                        DisplayParameterUsage(dwAttributeUsage);
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter usage, hr = 0x%lx\n",hr);
                    }

                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_VARTYPE, &dwAttributeVarType);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tVARTYPE: ");
                        DisplayVarType(static_cast<VARTYPE>(dwAttributeVarType));
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter VARTYPE, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_FORM value.
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_FORM, &dwAttributeForm);
                    if (FAILED(hr))
                    {
                        // If the read fails, assume WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED
                        dwAttributeForm = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                        hr = S_OK;
                    }

                    printf("\t\tForm: ");
                    DisplayParameterForm(dwAttributeForm);
                    printf("\n");

                    CoTaskMemFree(pszParameterName);
                    pszParameterName = NULL;
                }
                
                printf("\n");
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="0f76b-159">См. также</span><span class="sxs-lookup"><span data-stu-id="0f76b-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f76b-160">**ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="0f76b-160">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="0f76b-161">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="0f76b-161">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="0f76b-162">**ипортабледевицесервицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="0f76b-162">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="0f76b-163">**ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="0f76b-163">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="0f76b-164">впдсервицесаписампле</span><span class="sxs-lookup"><span data-stu-id="0f76b-164">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



