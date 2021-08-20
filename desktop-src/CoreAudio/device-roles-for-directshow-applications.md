---
description: роли устройств для DirectShow приложений
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: роли устройств для DirectShow приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e22a86e5537f11b6b4153753841a2682b5ac77a043a3fa74538714a2540377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957363"
---
# <a name="device-roles-for-directshow-applications"></a>роли устройств для DirectShow приложений

> [!Note]  
> [API ммдевице](mmdevice-api.md) поддерживает роли устройств. однако пользовательский интерфейс в Windows Vista не реализует поддержку этой функции. Поддержка пользовательского интерфейса для ролей устройств может быть реализована в следующей версии Windows. дополнительные сведения см. [в статье роли устройств в Windows Vista](device-roles-in-windows-vista.md).

 

DirectShow API не позволяет приложению выбрать [устройство звуковой конечной точки](audio-endpoint-devices.md) , назначенное определенной [роли устройства](device-roles.md). однако в Windows Vista основные api-интерфейсы аудиоподсистемы можно использовать в сочетании с приложением DirectShow для включения выбора устройств на основе роли устройства. С помощью основных API-интерфейсов аудио приложение может:

-   Определяет устройство аудио конечной точки, назначенное пользователю для конкретной роли устройства.
-   создание DirectShow фильтра рендеринга звука с помощью интерфейса [**ибасефилтер**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) , который инкапсулирует устройство конечной точки аудио.
-   создание DirectShow графа, включающего фильтр.

дополнительные сведения о DirectShow и [**ибасефилтер**](/windows/desktop/api/strmif/nn-strmif-ibasefilter)см. в документации по Windows SDK.

в следующем примере кода показано, как создать DirectShow фильтр рендеринга звука, который инкапсулирует устройство конечной точки отрисовки, назначенное конкретной роли устройства:


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



В предыдущем примере кода функция Креатеаудиорендерер принимает роль устройства (Еконсоле, Емултимедиа или Екоммуникатионс) в качестве входного параметра. Второй параметр — это указатель, через который функция записывает адрес экземпляра интерфейса [**ибасефилтер**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) . Кроме того, в примере показано, как использовать метод [**иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) , чтобы назначить аудиопоток в экземпляре **ибасефилтер** для межпроцессного аудио-сеанса с идентификатором GUID сеанса конкретного приложения (заданным константой **гуидаудиосессионид** ). Третий параметр в вызове **активации** указывает на структуру, содержащую идентификатор GUID сеанса и флаг перекрестной обработки. Если пользователь запускает несколько экземпляров приложения, звуковые потоки из всех экземпляров используют один и тот же идентификатор GUID сеанса и, таким же, принадлежат одному сеансу.

Кроме того, вызывающий объект может указать **значение NULL** в качестве третьего параметра в вызове [**активации**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) , чтобы назначить поток сеансу по умолчанию в качестве сеанса, зависящего от процесса, с идентификатором GUID GUID сеанса \_ null. Дополнительные сведения см. в разделе **иммдевице:: Activate**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Взаимодействие с устаревшими API аудио](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
