---
description: Роли устройств для приложений DirectSound
ms.assetid: 7d82d67f-aad8-4e5b-ac65-87d75774e613
title: Роли устройств для приложений DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3829817f8b00c7288aceb8d0b6d418d5793ae580
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990331"
---
# <a name="device-roles-for-directsound-applications"></a><span data-ttu-id="8409e-103">Роли устройств для приложений DirectSound</span><span class="sxs-lookup"><span data-stu-id="8409e-103">Device Roles for DirectSound Applications</span></span>

> [!Note]  
> <span data-ttu-id="8409e-104">[API ммдевице](mmdevice-api.md) поддерживает роли устройств.</span><span class="sxs-lookup"><span data-stu-id="8409e-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="8409e-105">Однако пользовательский интерфейс в Windows Vista не реализует поддержку этой функции.</span><span class="sxs-lookup"><span data-stu-id="8409e-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="8409e-106">Поддержка пользовательского интерфейса для ролей устройств может быть реализована в будущей версии Windows.</span><span class="sxs-lookup"><span data-stu-id="8409e-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="8409e-107">Дополнительные сведения см. [в статье роли устройств в Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="8409e-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="8409e-108">API DirectSound не предоставляет приложению возможность выбрать [устройство звуковой конечной точки](audio-endpoint-devices.md) , которое пользователь назначил определенной [роли устройства](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="8409e-108">The DirectSound API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="8409e-109">Однако в Windows Vista базовые API аудио можно использовать в сочетании с приложением DirectSound для выбора устройств на основе роли устройства.</span><span class="sxs-lookup"><span data-stu-id="8409e-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectSound application to enable device selection based on device role.</span></span> <span data-ttu-id="8409e-110">С помощью основных API-интерфейсов аудио приложение может определить устройство аудио конечной точки, назначенное определенной роли, получить GUID DirectSound для устройства конечной точки и вызвать функцию **директсаундкреате** или **директсаундкаптурекреате** , чтобы создать экземпляр интерфейса **идиректсаунд** или **идиректсаундкаптуре** , инкапсулирующий устройство конечной точки.</span><span class="sxs-lookup"><span data-stu-id="8409e-110">With the help of the core audio APIs, the application can identify the audio endpoint device that is assigned to a particular role, get the DirectSound device GUID for the endpoint device, and call the **DirectSoundCreate** or **DirectSoundCaptureCreate** function to create an **IDirectSound** or **IDirectSoundCapture** interface instance that encapsulates the endpoint device.</span></span> <span data-ttu-id="8409e-111">Дополнительные сведения о DirectSound см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8409e-111">For more information about DirectSound, see the Windows SDK documentation.</span></span>

<span data-ttu-id="8409e-112">В следующем примере кода показано, как получить идентификатор GUID устройства DirectSound для устройства отрисовки или записи, которое в настоящее время назначено конкретной роли устройства:</span><span class="sxs-lookup"><span data-stu-id="8409e-112">The following code example shows how to obtain the DirectSound device GUID for the rendering or capture device that is currently assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// Get the DirectSound or DirectSoundCapture device GUID for
// an audio endpoint device. If flow = eRender, the function
// gets the DirectSound device GUID for the rendering device
// with the specified device role. If flow = eCapture, the
// function gets the DirectSoundCapture device GUID for the
// capture device with the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetDirectSoundGuid(EDataFlow flow, ERole role, GUID* pDevGuid)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    if (pDevGuid == NULL)
    {
        return E_POINTER;
    }

    // Get a device enumerator for the audio endpoint
    // devices in the system.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the endpoint device with the specified dataflow
    // direction (eRender or eCapture) and device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    EXIT_ON_ERROR(hr)

    // Get the DirectSound or DirectSoundCapture device GUID
    // (in WCHAR string format) for the endpoint device.
    hr = pProps->GetValue(PKEY_AudioEndpoint_GUID, &var);
    EXIT_ON_ERROR(hr)

    // Convert the WCHAR string to a GUID structure.
    hr = CLSIDFromString(var.pwszVal, pDevGuid);
    EXIT_ON_ERROR(hr)

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    SAFE_RELEASE(pProps);
    return hr;
}
```



<span data-ttu-id="8409e-113">В предыдущем примере кода функция Жетдиректсаундгуид принимает направление потока данных (Ерендер или Екаптуре) и роль устройства (Еконсоле, Емултимедиа или Екоммуникатионс) в качестве входных параметров.</span><span class="sxs-lookup"><span data-stu-id="8409e-113">In the preceding code example, the GetDirectSoundGuid function accepts a data-flow direction (eRender or eCapture) and a device role (eConsole, eMultimedia, or eCommunications) as input parameters.</span></span> <span data-ttu-id="8409e-114">Третий параметр — это указатель, через который функция записывает GUID устройства, которое приложение может передать в качестве входного параметра в функцию **директсаундкреате** или **директсаундкаптурекреате** .</span><span class="sxs-lookup"><span data-stu-id="8409e-114">The third parameter is a pointer through which the function writes a device GUID that the application can supply as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span>

<span data-ttu-id="8409e-115">В предыдущем примере кода идентификатор GUID устройства DirectSound получается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8409e-115">The preceding code example obtains the DirectSound device GUID by:</span></span>

-   <span data-ttu-id="8409e-116">Создание экземпляра интерфейса [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , представляющего устройство аудио конечной точки с указанным направлением потока данных и ролью устройства.</span><span class="sxs-lookup"><span data-stu-id="8409e-116">Creating an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface instance that represents the audio endpoint device that has the specified data-flow direction and device role.</span></span>
-   <span data-ttu-id="8409e-117">Открытие хранилища свойств устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="8409e-117">Opening the property store of the audio endpoint device.</span></span>
-   <span data-ttu-id="8409e-118">Получение свойства [**\_ Аудиоендпоинт \_ GUID PKEY**](pkey-audioendpoint-guid.md) из хранилища свойств.</span><span class="sxs-lookup"><span data-stu-id="8409e-118">Getting the [**PKEY\_AudioEndpoint\_GUID**](pkey-audioendpoint-guid.md) property from the property store.</span></span> <span data-ttu-id="8409e-119">Значение свойства представляет собой строковое представление идентификатора GUID устройства DirectSound для устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="8409e-119">The property value is a string representation of the DirectSound device GUID for the audio endpoint device.</span></span>
-   <span data-ttu-id="8409e-120">Вызов функции [**клсидфромстринг**](https://www.bing.com/search?q=**CLSIDFromString**) для преобразования строкового представления GUID устройства в структуру GUID.</span><span class="sxs-lookup"><span data-stu-id="8409e-120">Calling the [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) function to convert the string representation of the device GUID to a GUID structure.</span></span> <span data-ttu-id="8409e-121">Дополнительные сведения о **клсидфромстринг** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8409e-121">For more information about **CLSIDFromString**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="8409e-122">После получения GUID устройства из функции Жетдиректсаундгуид приложение может вызвать **директсаундкреате** или **директсаундкаптурекреате** с этим идентификатором GUID, чтобы создать устройство DirectSound для подготовки или записи, которое инкапсулирует устройство конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="8409e-122">After obtaining a device GUID from the GetDirectSoundGuid function, the application can call **DirectSoundCreate** or **DirectSoundCaptureCreate** with this GUID to create the DirectSound rendering or capture device that encapsulates the audio endpoint device.</span></span> <span data-ttu-id="8409e-123">Когда DirectSound создает устройство таким образом, он всегда назначает звуковой поток устройства сеансу по умолчанию — для конкретного процесса, определяемого значением GUID идентификатора GUID сеанса, значение \_ null.</span><span class="sxs-lookup"><span data-stu-id="8409e-123">When DirectSound creates a device in this way, it always assigns the device's audio stream to the default session—the process-specific audio session that is identified by the session GUID value GUID\_NULL.</span></span>

<span data-ttu-id="8409e-124">Если приложению требуется DirectSound для назначения потока для межпроцессного аудио-сеанса или сеанса с идентификатором GUID сеанса, отличного от **null** , он должен вызвать метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) для создания объекта **идиректсаунд** или **идиректсаундкаптуре** вместо использования метода, показанного в предыдущем примере кода.</span><span class="sxs-lookup"><span data-stu-id="8409e-124">If the application requires DirectSound to assign the stream to a cross-process audio session or to a session with a non-**NULL** session GUID, it should call the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to create an **IDirectSound** or **IDirectSoundCapture** object instead of using the technique shown in the preceding code example.</span></span> <span data-ttu-id="8409e-125">Пример кода, демонстрирующий использование метода **Activate** для указания межпроцессного аудио-сеанса или идентификатора GUID сеанса, отличного от **null** , см. в разделе [роли устройств для приложений DirectShow](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="8409e-125">For a code example that shows how to use the **Activate** method to specify a cross-process audio session or a non-**NULL** session GUID for a stream, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="8409e-126">В примере кода в этом разделе показано, как создать фильтр DirectShow, но с незначительными изменениями код можно адаптировать для создания устройства DirectSound.</span><span class="sxs-lookup"><span data-stu-id="8409e-126">The code example in that section shows how to create a DirectShow filter, but, with minor modifications, the code can be adapted to create a DirectSound device.</span></span>

<span data-ttu-id="8409e-127">Функция Жетдиректсаундгуид в предыдущем примере кода вызывает функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать перечислитель для устройств конечных точек аудио в системе.</span><span class="sxs-lookup"><span data-stu-id="8409e-127">The GetDirectSoundGuid function in the preceding code example calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="8409e-128">Если вызывающая программа ранее не вызывала [](/windows/desktop/api/objbase/nf-objbase-coinitialize) функцию CoInitialize или [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM, вызов **CoCreateInstance** завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8409e-128">Unless the calling program previously called either the [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="8409e-129">Дополнительные сведения о **CoCreateInstance**, **CoInitialize** и **CoInitializeEx** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8409e-129">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8409e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="8409e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8409e-131">Взаимодействие с устаревшими API аудио</span><span class="sxs-lookup"><span data-stu-id="8409e-131">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
