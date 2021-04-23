---
description: Роли устройств для приложений DirectShow
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: Роли устройств для приложений DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df8b43ddd56870b65fc9ec1e3bb600e8e6b79528
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495822"
---
# <a name="device-roles-for-directshow-applications"></a><span data-ttu-id="d10c6-103">Роли устройств для приложений DirectShow</span><span class="sxs-lookup"><span data-stu-id="d10c6-103">Device Roles for DirectShow Applications</span></span>

> [!Note]  
> <span data-ttu-id="d10c6-104">[API ммдевице](mmdevice-api.md) поддерживает роли устройств.</span><span class="sxs-lookup"><span data-stu-id="d10c6-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="d10c6-105">Однако пользовательский интерфейс в Windows Vista не реализует поддержку этой функции.</span><span class="sxs-lookup"><span data-stu-id="d10c6-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="d10c6-106">Поддержка пользовательского интерфейса для ролей устройств может быть реализована в будущей версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d10c6-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="d10c6-107">Дополнительные сведения см. [в статье роли устройств в Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="d10c6-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="d10c6-108">API DirectShow не предоставляет приложению возможность выбрать [устройство аудио конечных точек](audio-endpoint-devices.md) , назначенное определенной [роли устройства](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="d10c6-108">The DirectShow API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that is assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="d10c6-109">Однако в Windows Vista основные API-интерфейсы аудиоподсистемы можно использовать в сочетании с приложением DirectShow для выбора устройств на основе роли устройства.</span><span class="sxs-lookup"><span data-stu-id="d10c6-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectShow application to enable device selection based on device role.</span></span> <span data-ttu-id="d10c6-110">С помощью основных API-интерфейсов аудио приложение может:</span><span class="sxs-lookup"><span data-stu-id="d10c6-110">With the help of the core audio APIs, the application can:</span></span>

-   <span data-ttu-id="d10c6-111">Определяет устройство аудио конечной точки, назначенное пользователю для конкретной роли устройства.</span><span class="sxs-lookup"><span data-stu-id="d10c6-111">Identify the audio endpoint device that the user has assigned to a particular device role.</span></span>
-   <span data-ttu-id="d10c6-112">Создайте фильтр рендеринга звука DirectShow с интерфейсом [**ибасефилтер**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) , который инкапсулирует устройство конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="d10c6-112">Create a DirectShow audio rendering filter with an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface that encapsulates the audio endpoint device.</span></span>
-   <span data-ttu-id="d10c6-113">Создайте граф DirectShow, включающий фильтр.</span><span class="sxs-lookup"><span data-stu-id="d10c6-113">Build a DirectShow graph that incorporates the filter.</span></span>

<span data-ttu-id="d10c6-114">Дополнительные сведения о DirectShow и [**ибасефилтер**](/windows/desktop/api/strmif/nn-strmif-ibasefilter)см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d10c6-114">For more information about DirectShow and [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), see the Windows SDK documentation.</span></span>

<span data-ttu-id="d10c6-115">В следующем примере кода показано, как создать фильтр рендеринга звука DirectShow, который инкапсулирует устройство конечной точки отрисовки, назначенное конкретной роли устройства:</span><span class="sxs-lookup"><span data-stu-id="d10c6-115">The following code example shows how to create a DirectShow audio rendering filter that encapsulates the rendering endpoint device that is assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// Create a DirectShow audio rendering filter that
// encapsulates the audio endpoint device that is currently
// assigned to the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

// This application's audio session GUID
const GUID guidAudioSessionId = {
    0xb13ff52e, 0xa5cf, 0x4fca,
    {0x9f, 0xc3, 0x42, 0x26, 0x5b, 0x0b, 0x14, 0xfb}
};

HRESULT CreateAudioRenderer(ERole role, IBaseFilter** ppAudioRenderer)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    if (ppAudioRenderer == NULL)
    {
        return E_POINTER;
    }

    // Activate the IBaseFilter interface on the
    // audio renderer with the specified role.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator,
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    DIRECTX_AUDIO_ACTIVATION_PARAMS  daap;
    daap.cbDirectXAudioActivationParams = sizeof(daap);
    daap.guidAudioSession = guidAudioSessionId;
    daap.dwAudioStreamFlags = AUDCLNT_STREAMFLAGS_CROSSPROCESS;

    PROPVARIANT  var;
    PropVariantInit(&var);

    var.vt = VT_BLOB;
    var.blob.cbSize = sizeof(daap);
    var.blob.pBlobData = (BYTE*)&daap;

    hr = pDevice->Activate(__uuidof(IBaseFilter),
                           CLSCTX_ALL, &var,
                           (void**)ppAudioRenderer);
    EXIT_ON_ERROR(hr)

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    return hr;
}
```



<span data-ttu-id="d10c6-116">В предыдущем примере кода функция Креатеаудиорендерер принимает роль устройства (Еконсоле, Емултимедиа или Екоммуникатионс) в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="d10c6-116">In the preceding code example, the CreateAudioRenderer function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="d10c6-117">Второй параметр — это указатель, через который функция записывает адрес экземпляра интерфейса [**ибасефилтер**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="d10c6-117">The second parameter is a pointer through which the function writes the address of an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface instance.</span></span> <span data-ttu-id="d10c6-118">Кроме того, в примере показано, как использовать метод [**иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) , чтобы назначить аудиопоток в экземпляре **ибасефилтер** для межпроцессного аудио-сеанса с идентификатором GUID сеанса конкретного приложения (заданным константой **гуидаудиосессионид** ).</span><span class="sxs-lookup"><span data-stu-id="d10c6-118">In addition, the example shows how to use the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to assign the audio stream in the **IBaseFilter** instance to a cross-process audio session with an application-specific session GUID (specified by the **guidAudioSessionId** constant).</span></span> <span data-ttu-id="d10c6-119">Третий параметр в вызове **активации** указывает на структуру, содержащую идентификатор GUID сеанса и флаг перекрестной обработки.</span><span class="sxs-lookup"><span data-stu-id="d10c6-119">The third parameter in the **Activate** call points to a structure that contains the session GUID and cross-process flag.</span></span> <span data-ttu-id="d10c6-120">Если пользователь запускает несколько экземпляров приложения, звуковые потоки из всех экземпляров используют один и тот же идентификатор GUID сеанса и, таким же, принадлежат одному сеансу.</span><span class="sxs-lookup"><span data-stu-id="d10c6-120">If the user runs multiple instances of the application, then the audio streams from all the instances use the same session GUID and thus belong to the same session.</span></span>

<span data-ttu-id="d10c6-121">Кроме того, вызывающий объект может указать **значение NULL** в качестве третьего параметра в вызове [**активации**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) , чтобы назначить поток сеансу по умолчанию в качестве сеанса, зависящего от процесса, с идентификатором GUID GUID сеанса \_ null.</span><span class="sxs-lookup"><span data-stu-id="d10c6-121">Alternatively, the caller can specify **NULL** as the third parameter in the [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) call to assign the stream to the default session as the process-specific session with session GUID value GUID\_NULL.</span></span> <span data-ttu-id="d10c6-122">Дополнительные сведения см. в разделе **иммдевице:: Activate**.</span><span class="sxs-lookup"><span data-stu-id="d10c6-122">For more information, see **IMMDevice::Activate**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d10c6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d10c6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d10c6-124">Взаимодействие с устаревшими API аудио</span><span class="sxs-lookup"><span data-stu-id="d10c6-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
