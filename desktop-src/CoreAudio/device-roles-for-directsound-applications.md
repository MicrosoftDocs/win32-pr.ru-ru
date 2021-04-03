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
# <a name="device-roles-for-directsound-applications"></a>Роли устройств для приложений DirectSound

> [!Note]  
> [API ммдевице](mmdevice-api.md) поддерживает роли устройств. Однако пользовательский интерфейс в Windows Vista не реализует поддержку этой функции. Поддержка пользовательского интерфейса для ролей устройств может быть реализована в будущей версии Windows. Дополнительные сведения см. [в статье роли устройств в Windows Vista](device-roles-in-windows-vista.md).

 

API DirectSound не предоставляет приложению возможность выбрать [устройство звуковой конечной точки](audio-endpoint-devices.md) , которое пользователь назначил определенной [роли устройства](device-roles.md). Однако в Windows Vista базовые API аудио можно использовать в сочетании с приложением DirectSound для выбора устройств на основе роли устройства. С помощью основных API-интерфейсов аудио приложение может определить устройство аудио конечной точки, назначенное определенной роли, получить GUID DirectSound для устройства конечной точки и вызвать функцию **директсаундкреате** или **директсаундкаптурекреате** , чтобы создать экземпляр интерфейса **идиректсаунд** или **идиректсаундкаптуре** , инкапсулирующий устройство конечной точки. Дополнительные сведения о DirectSound см. в документации по Windows SDK.

В следующем примере кода показано, как получить идентификатор GUID устройства DirectSound для устройства отрисовки или записи, которое в настоящее время назначено конкретной роли устройства:


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



В предыдущем примере кода функция Жетдиректсаундгуид принимает направление потока данных (Ерендер или Екаптуре) и роль устройства (Еконсоле, Емултимедиа или Екоммуникатионс) в качестве входных параметров. Третий параметр — это указатель, через который функция записывает GUID устройства, которое приложение может передать в качестве входного параметра в функцию **директсаундкреате** или **директсаундкаптурекреате** .

В предыдущем примере кода идентификатор GUID устройства DirectSound получается следующим образом:

-   Создание экземпляра интерфейса [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , представляющего устройство аудио конечной точки с указанным направлением потока данных и ролью устройства.
-   Открытие хранилища свойств устройства конечной точки аудио.
-   Получение свойства [**\_ Аудиоендпоинт \_ GUID PKEY**](pkey-audioendpoint-guid.md) из хранилища свойств. Значение свойства представляет собой строковое представление идентификатора GUID устройства DirectSound для устройства конечной точки аудио.
-   Вызов функции [**клсидфромстринг**](https://www.bing.com/search?q=**CLSIDFromString**) для преобразования строкового представления GUID устройства в структуру GUID. Дополнительные сведения о **клсидфромстринг** см. в документации по Windows SDK.

После получения GUID устройства из функции Жетдиректсаундгуид приложение может вызвать **директсаундкреате** или **директсаундкаптурекреате** с этим идентификатором GUID, чтобы создать устройство DirectSound для подготовки или записи, которое инкапсулирует устройство конечной точки аудио. Когда DirectSound создает устройство таким образом, он всегда назначает звуковой поток устройства сеансу по умолчанию — для конкретного процесса, определяемого значением GUID идентификатора GUID сеанса, значение \_ null.

Если приложению требуется DirectSound для назначения потока для межпроцессного аудио-сеанса или сеанса с идентификатором GUID сеанса, отличного от **null** , он должен вызвать метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) для создания объекта **идиректсаунд** или **идиректсаундкаптуре** вместо использования метода, показанного в предыдущем примере кода. Пример кода, демонстрирующий использование метода **Activate** для указания межпроцессного аудио-сеанса или идентификатора GUID сеанса, отличного от **null** , см. в разделе [роли устройств для приложений DirectShow](device-roles-for-directshow-applications.md). В примере кода в этом разделе показано, как создать фильтр DirectShow, но с незначительными изменениями код можно адаптировать для создания устройства DirectSound.

Функция Жетдиректсаундгуид в предыдущем примере кода вызывает функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать перечислитель для устройств конечных точек аудио в системе. Если вызывающая программа ранее не вызывала [](/windows/desktop/api/objbase/nf-objbase-coinitialize) функцию CoInitialize или [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM, вызов **CoCreateInstance** завершится ошибкой. Дополнительные сведения о **CoCreateInstance**, **CoInitialize** и **CoInitializeEx** см. в документации по Windows SDK.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Взаимодействие с устаревшими API аудио](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
