---
description: Свойства устройства
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Свойства устройства (API-интерфейсы Core Audio)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655626"
---
# <a name="device-properties-core-audio-apis"></a><span data-ttu-id="c168b-103">Свойства устройства (API-интерфейсы Core Audio)</span><span class="sxs-lookup"><span data-stu-id="c168b-103">Device Properties (Core Audio APIs)</span></span>

<span data-ttu-id="c168b-104">В процессе перечисления [устройств конечных точек звука](audio-endpoint-devices.md)клиентское приложение может опрашивать объекты конечной точки для их свойств устройства.</span><span class="sxs-lookup"><span data-stu-id="c168b-104">During the process of enumerating [audio endpoint devices](audio-endpoint-devices.md), a client application can interrogate the endpoint objects for their device properties.</span></span> <span data-ttu-id="c168b-105">Свойства устройства предоставляются в реализации интерфейса **ИПРОПЕРТИСТОРЕ** API ммдевице.</span><span class="sxs-lookup"><span data-stu-id="c168b-105">The device properties are exposed in MMDevice API's implementation of the **IPropertyStore** interface.</span></span> <span data-ttu-id="c168b-106">При наличии ссылки на интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) объекта конечной точки клиент может получить ссылку на хранилище свойств объекта конечной точки, вызвав метод [**Иммдевице:: опенпропертисторе**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) .</span><span class="sxs-lookup"><span data-stu-id="c168b-106">Given a reference to the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an endpoint object, a client can obtain a reference to the endpoint object's property store by calling the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method.</span></span>

<span data-ttu-id="c168b-107">Объект-хранилище свойств предоставляет интерфейс **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="c168b-107">The property-store object exposes an **IPropertyStore** interface.</span></span> <span data-ttu-id="c168b-108">Два основных метода в этом интерфейсе — **ипропертисторе:: GetValue**, который получает значение свойства устройства, и **Ипропертисторе:: SetValue**, который задает значение свойства устройства.</span><span class="sxs-lookup"><span data-stu-id="c168b-108">The two primary methods in this interface are **IPropertyStore::GetValue**, which gets a device property value, and **IPropertyStore::SetValue**, which sets a device property value.</span></span> <span data-ttu-id="c168b-109">Дополнительные сведения о **ипропертисторе** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c168b-109">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="c168b-110">Реализация Ммдевице API хранилища свойств отличается от объекта стандартного хранилища свойств оболочки.</span><span class="sxs-lookup"><span data-stu-id="c168b-110">The MMDevice API's implementation of the property store is different from the standard shell property store object.</span></span> <span data-ttu-id="c168b-111">Чтобы изменить значение свойства, клиентское приложение должно вызвать метод **ипропертисторе:: SetValue** .</span><span class="sxs-lookup"><span data-stu-id="c168b-111">To change a property value, the client application must call the **IPropertyStore::SetValue** method.</span></span> <span data-ttu-id="c168b-112">Во время этого вызова новые значения задаются и записываются в реестр.</span><span class="sxs-lookup"><span data-stu-id="c168b-112">During this call, the new values are set and written in the registry.</span></span> <span data-ttu-id="c168b-113">Поэтому приложению не нужно вызывать метод **ипропертисторе:: Commit** после вызова **SetValue** .</span><span class="sxs-lookup"><span data-stu-id="c168b-113">Therefore, the application does not need to call the **IPropertyStore::Commit** method after the **SetValue** call.</span></span> <span data-ttu-id="c168b-114">Дескриптор реестра закрывается только в том случае, если клиент освобождает указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c168b-114">The handle to the registry is closed only when the client releases the interface pointer.</span></span>

<span data-ttu-id="c168b-115">Как правило, клиентские приложения сторонних производителей вызывают метод **GetValue** , но не метод **SetValue** .</span><span class="sxs-lookup"><span data-stu-id="c168b-115">Typically, third-party client applications call the **GetValue** method but not the **SetValue** method.</span></span> <span data-ttu-id="c168b-116">Диспетчер конечных точек задает основные свойства устройства для конечных узлов.</span><span class="sxs-lookup"><span data-stu-id="c168b-116">The endpoint manager sets the basic device properties for endpoints.</span></span> <span data-ttu-id="c168b-117">Диспетчер конечных точек — это компонент Windows Vista, который отвечает за обнаружение наличия устройств конечных точек звука.</span><span class="sxs-lookup"><span data-stu-id="c168b-117">The endpoint manager is the Windows Vista component that is responsible for detecting the presence of audio endpoint devices.</span></span>

<span data-ttu-id="c168b-118">Каждый \_ идентификатор свойства PKEY XXX в следующем списке является константой типа **PROPERTYKEY** , которая определена в файле заголовка функтиондисковерикэйс \_ девпкэй. h.</span><span class="sxs-lookup"><span data-stu-id="c168b-118">Each PKEY\_Xxx property identifier in the following list is a constant of type **PROPERTYKEY** that is defined in header file Functiondiscoverykeys\_devpkey.h.</span></span> <span data-ttu-id="c168b-119">Все устройства конечных точек аудио имеют три свойства устройства.</span><span class="sxs-lookup"><span data-stu-id="c168b-119">All audio endpoint devices have these three device properties.</span></span>



| <span data-ttu-id="c168b-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="c168b-120">Property</span></span>                                                                         | <span data-ttu-id="c168b-121">Описание</span><span class="sxs-lookup"><span data-stu-id="c168b-121">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c168b-122">**PKEY \_ девицеинтерфаце \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="c168b-122">**PKEY\_DeviceInterface\_FriendlyName**</span></span>](pkey-deviceinterface-friendlyname.md) | <span data-ttu-id="c168b-123">Понятное имя звукового адаптера, к которому подключено устройство конечной точки (например, "XYZ Audio Adapter").</span><span class="sxs-lookup"><span data-stu-id="c168b-123">The friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span> <span data-ttu-id="c168b-124">**Пропвариант** Member **VT** имеет значение VT \_ LPWSTR, а Member **пвсзвал** указывает на строку расширенных символов, заканчивающуюся символом NULL, которая содержит понятное имя.</span><span class="sxs-lookup"><span data-stu-id="c168b-124">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span> |
| [<span data-ttu-id="c168b-125">**\_Девицедеск устройства \_ PKEY**</span><span class="sxs-lookup"><span data-stu-id="c168b-125">**PKEY\_Device\_DeviceDesc**</span></span>](pkey-device-devicedesc.md)                       | <span data-ttu-id="c168b-126">Описание устройства конечной точки (например, "динамики").</span><span class="sxs-lookup"><span data-stu-id="c168b-126">The device description of the endpoint device (for example, "Speakers").</span></span> <span data-ttu-id="c168b-127">**Пропвариант** Member **VT** имеет значение VT \_ LPWSTR, а Member **пвсзвал** указывает на строку расширенных символов, заканчивающуюся символом NULL, содержащую описание устройства.</span><span class="sxs-lookup"><span data-stu-id="c168b-127">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the device description.</span></span>                                       |
| [<span data-ttu-id="c168b-128">**PKEY \_ устройство \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="c168b-128">**PKEY\_Device\_FriendlyName**</span></span>](pkey-device-friendlyname.md)                   | <span data-ttu-id="c168b-129">Понятное имя устройства конечной точки (например, "динамики (аудио-адаптер XYZ)").</span><span class="sxs-lookup"><span data-stu-id="c168b-129">The friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span> <span data-ttu-id="c168b-130">**Пропвариант** Member **VT** имеет значение VT \_ LPWSTR, а Member **пвсзвал** указывает на строку расширенных символов, заканчивающуюся символом NULL, которая содержит понятное имя.</span><span class="sxs-lookup"><span data-stu-id="c168b-130">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span>                             |



 

<span data-ttu-id="c168b-131">Некоторые устройства конечных точек звука могут иметь дополнительные свойства, которые не отображаются в приведенном выше списке.</span><span class="sxs-lookup"><span data-stu-id="c168b-131">Some audio endpoint devices might have additional properties that do not appear in the preceding list.</span></span> <span data-ttu-id="c168b-132">Дополнительные сведения о дополнительных свойствах см. в разделе [свойства конечной точки аудио](audio-endpoint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c168b-132">For more information about additional properties, see [Audio Endpoint Properties](audio-endpoint-properties.md).</span></span> <span data-ttu-id="c168b-133">Дополнительные сведения о **PROPERTYKEY** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c168b-133">For more information about **PROPERTYKEY**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="c168b-134">В следующем примере кода выводятся отображаемые имена всех устройств конечной точки отрисовки звука в системе:</span><span class="sxs-lookup"><span data-stu-id="c168b-134">The following code example prints the display names of all audio-rendering endpoint devices in the system:</span></span>


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



<span data-ttu-id="c168b-135">Макрос FAILed в предыдущем примере кода определен в файле заголовка Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="c168b-135">The FAILED macro in the preceding code example is defined in header file Winerror.h.</span></span>

<span data-ttu-id="c168b-136">В приведенном выше примере кода тело цикла **for** в функции принтендпоинтнамес вызывает метод [**Иммдевице:: GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) , чтобы получить [строку идентификатора конечной](endpoint-id-strings.md) точки для устройства аудио конечных точек, представленного экземпляром интерфейса **иммдевице** .</span><span class="sxs-lookup"><span data-stu-id="c168b-136">In the preceding code example, the **for**-loop body in the PrintEndpointNames function calls the [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method to obtain the [endpoint ID string](endpoint-id-strings.md) for the audio endpoint device that is represented by the **IMMDevice** interface instance.</span></span> <span data-ttu-id="c168b-137">Строка уникально идентифицирует устройство по отношению ко всем другим устройствам конечных точек звука в системе.</span><span class="sxs-lookup"><span data-stu-id="c168b-137">The string uniquely identifies the device with respect to all of the other audio endpoint devices in the system.</span></span> <span data-ttu-id="c168b-138">Клиент может использовать строку идентификатора конечной точки для создания экземпляра устройства конечной точки аудио в более позднее время или в другом процессе, вызвав метод [**иммдевицеенумератор::-Device**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="c168b-138">A client can use the endpoint ID string to create an instance of the audio endpoint device at a later time or in a different process by calling the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="c168b-139">Клиенты должны считать содержимое строки идентификатора конечной точки непрозрачной.</span><span class="sxs-lookup"><span data-stu-id="c168b-139">Clients should treat the contents of the endpoint ID string as opaque.</span></span> <span data-ttu-id="c168b-140">То есть клиенты не должны пытаться проанализировать содержимое строки для получения сведений об устройстве.</span><span class="sxs-lookup"><span data-stu-id="c168b-140">That is, clients should not attempt to parse the contents of the string to obtain information about the device.</span></span> <span data-ttu-id="c168b-141">Причина в том, что формат строки не определен и может изменяться от одной реализации API Ммдевице к следующему.</span><span class="sxs-lookup"><span data-stu-id="c168b-141">The reason is that the string format is undefined and might change from one implementation of the MMDevice API to the next.</span></span>

<span data-ttu-id="c168b-142">Понятные имена устройств и строки ИДЕНТИФИКАТОРов конечных точек, полученные функцией Принтендпоинтнамес в предыдущем примере кода, идентичны понятным именам устройств и строкам ИДЕНТИФИКАТОРов конечных точек, предоставляемым DirectSound во время перечисления устройств.</span><span class="sxs-lookup"><span data-stu-id="c168b-142">The friendly device names and endpoint ID strings that are obtained by the PrintEndpointNames function in the preceding code example are identical to the friendly device names and endpoint ID strings that are provided by DirectSound during device enumeration.</span></span> <span data-ttu-id="c168b-143">Дополнительные сведения см. в статье [события аудио для устаревших аудио приложений](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="c168b-143">For more information, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

<span data-ttu-id="c168b-144">В предыдущем примере кода функция Принтендпоинтнамес вызывает функцию **CoCreateInstance** , чтобы создать перечислитель для устройств конечных точек аудио в системе.</span><span class="sxs-lookup"><span data-stu-id="c168b-144">In the preceding code example, the PrintEndpointNames function calls the **CoCreateInstance** function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="c168b-145">Если вызывающая программа ранее не вызывала  функцию CoInitialize или **CoInitializeEx** для инициализации библиотеки COM, вызов **CoCreateInstance** завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c168b-145">Unless the calling program previously called either the **CoInitialize** or **CoInitializeEx** function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="c168b-146">Дополнительные сведения о **CoCreateInstance**, **CoInitialize** и **CoInitializeEx** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c168b-146">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="c168b-147">Дополнительные сведения об интерфейсах **иммдевицеенумератор**, **иммдевицеколлектион** и **ИММДЕВИЦЕ** см. в разделе [API ммдевице](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="c168b-147">For more information about the **IMMDeviceEnumerator**, **IMMDeviceCollection**, and **IMMDevice** interfaces, see [MMDevice API](mmdevice-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c168b-148">См. также</span><span class="sxs-lookup"><span data-stu-id="c168b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c168b-149">Устройства конечных точек звука</span><span class="sxs-lookup"><span data-stu-id="c168b-149">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 



