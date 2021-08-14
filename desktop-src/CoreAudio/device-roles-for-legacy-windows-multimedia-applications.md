---
description: роли устройств для устаревших Windows мультимедийных приложений
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: роли устройств для устаревших Windows мультимедийных приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b0c1c8b61da896ca8877a913ba14d5013de71ac6fd7c14bcdebfe21c4ffcb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406924"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a>роли устройств для устаревших Windows мультимедийных приложений

> [!Note]  
> API Ммдевице поддерживает роли устройств. однако пользовательский интерфейс в Windows Vista не реализует поддержку этой функции. Поддержка пользовательского интерфейса для ролей устройств может быть реализована в следующей версии Windows. дополнительные сведения см. [в статье роли устройств в Windows Vista](device-roles-in-windows-vista.md).

 

устаревшие функции Windows мультимедиа **вавеауткскскс** и **вавеинкскскс** не позволяют приложению выбрать [устройство звуковой конечной точки](audio-endpoint-devices.md) , которое пользователь назначил определенной [роли устройства](device-roles.md). однако в Windows Vista основные api-интерфейсы аудиоподсистемы можно использовать в сочетании с приложением мультимедиа Windows для включения выбора устройств на основе роли устройства. Например, с помощью [API ммдевице](mmdevice-api.md)приложение **вавеауткскскс** может определить устройство конечной точки аудио, назначенное роли, определить соответствующее выходное устройство аудио и вызвать функцию **вавеаутопен** , чтобы открыть экземпляр устройства. дополнительные сведения о **вавеауткскскс** и **вавеинкскскс** см. в документации по Windows SDK.

В следующем примере кода показано, как получить идентификатор устройства волны для устройства конечной точки отрисовки, назначенного конкретной роли устройства:


```C++
//-----------------------------------------------------------
// This function gets the waveOut ID of the audio endpoint
// device that is currently assigned to the specified device
// role. The caller can use the waveOut ID to open the
// waveOut device that corresponds to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetWaveOutId(ERole role, int *pWaveOutId)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    WCHAR *pstrEndpointIdKey = NULL;
    WCHAR *pstrEndpointId = NULL;

    if (pWaveOutId == NULL)
    {
        return E_POINTER;
    }

    // Create an audio endpoint device enumerator.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the audio endpoint device that the user has
    // assigned to the specified device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    // Get the endpoint ID string of the audio endpoint device.
    hr = pDevice->GetId(&pstrEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Get the size of the endpoint ID string.
    size_t  cbEndpointIdKey;

    hr = StringCbLength(pstrEndpointIdKey,
                        STRSAFE_MAX_CCH * sizeof(WCHAR),
                        &cbEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Include terminating null in string size.
    cbEndpointIdKey += sizeof(WCHAR);

    // Allocate a buffer for a second string of the same size.
    pstrEndpointId = (WCHAR*)CoTaskMemAlloc(cbEndpointIdKey);
    if (pstrEndpointId == NULL)
    {
        EXIT_ON_ERROR(hr = E_OUTOFMEMORY)
    }

    // Each for-loop iteration below compares the endpoint ID
    // string of the audio endpoint device to the endpoint ID
    // string of an enumerated waveOut device. If the strings
    // match, then we've found the waveOut device that is
    // assigned to the specified device role.
    int waveOutId;
    int cWaveOutDevices = waveOutGetNumDevs();

    for (waveOutId = 0; waveOutId < cWaveOutDevices; waveOutId++)
    {
        MMRESULT mmr;
        size_t cbEndpointId;

        // Get the size (including the terminating null) of
        // the endpoint ID string of the waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEIDSIZE,
                             (DWORD_PTR)&cbEndpointId, NULL);
        if (mmr != MMSYSERR_NOERROR ||
            cbEndpointIdKey != cbEndpointId)  // do sizes match?
        {
            continue;  // not a matching device
        }

        // Get the endpoint ID string for this waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEID,
                             (DWORD_PTR)pstrEndpointId,
                             cbEndpointId);
        if (mmr != MMSYSERR_NOERROR)
        {
            continue;
        }

        // Check whether the endpoint ID string of this waveOut
        // device matches that of the audio endpoint device.
        if (lstrcmpi(pstrEndpointId, pstrEndpointIdKey) == 0)
        {
            *pWaveOutId = waveOutId;  // found match
            hr = S_OK;
            break;
        }
    }

    if (waveOutId == cWaveOutDevices)
    {
        // We reached the end of the for-loop above without
        // finding a waveOut device with a matching endpoint
        // ID string. This behavior is quite unexpected.
        hr = E_UNEXPECTED;
    }

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    CoTaskMemFree(pstrEndpointIdKey);  // NULL pointer okay
    CoTaskMemFree(pstrEndpointId);
    return hr;
}
```



В предыдущем примере кода функция Жетвавеаутид принимает роль устройства (Еконсоле, Емултимедиа или Екоммуникатионс) в качестве входного параметра. Второй параметр — это указатель, через который функция записывает идентификатор устройства волны для выходного устройства аудио, назначенного указанной роли. Затем приложение может вызвать **вавеаутопен** с этим идентификатором, чтобы открыть устройство.

Основной цикл в предыдущем примере кода содержит два вызова функции **вавеаутмессаже** . Первый вызов отправляет \_ сообщение КУЕРИФУНКТИОНИНСТАНЦЕИДСИЗЕ DRV для получения размера (в байтах) [строки идентификатора конечной точки](endpoint-id-strings.md) устройства волны, идентифицируемого параметром *вавеаутид* . (Строка идентификатора конечной точки определяет устройство аудио конечной точки, которое зависит от абстракции устройства волны.) Размер, сообщаемый этим вызовом, включает пробел для завершающего нуль-символа в конце строки. Программа может использовать сведения о размере для выделения буфера, который достаточно велик для размещения всей строки идентификатора конечной точки.

Второй вызов **вавеаутмессаже** ОТПРАВЛЯЕТ сообщение DRV куерифунктионинстанцеид, \_ чтобы получить строку идентификатора устройства для выходного устройства звуковой волны. В примере кода эта строка сравнивается со строкой идентификатора устройства устройства конечной точки аудио с указанной ролью устройства. Если строки совпадают, функция записывает идентификатор устройства волны в расположение, на которое указывает параметр *пвавеаутид*. Вызывающий объект может использовать этот идентификатор для открытия устройства вывода аудио с заданной ролью устройства.

Windows Vista поддерживает сообщения DRV \_ куерифунктионинстанцеидсизе и DRV \_ куерифунктионинстанцеид. они не поддерживаются в более ранних версиях Windows, включая Windows Server 2003, Windows XP и Windows 2000.

Функция в предыдущем примере кода получает идентификатор устройства волны для устройства отрисовки, но при наличии нескольких изменений его можно адаптировать, чтобы получить идентификатор устройства для записи. Затем приложение может вызвать **вавеинопен** с этим идентификатором, чтобы открыть устройство. Чтобы изменить приведенный выше пример кода, чтобы получить идентификатор устройства с звуковой точкой для устройства записи звука, назначенного определенной роли, выполните следующие действия.

-   Замените все вызовы функций **вавеауткскскс** в предыдущем примере соответствующими вызовами функций **вавеинкскскс** .
-   Измените тип маркера ХВАВЕАУТ на ХВАВЕИН.
-   Замените константу перечисления [**Ероле**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) Ерендер на екаптуре.

в Windows Vista функции **вавеаутопен** и **вавеинопен** всегда назначают звуковые потоки, которые они создают, в сеанс по умолчанию — сеанс конкретного процесса, определяемый идентификатором guid guid для сеанса \_ NULL.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Взаимодействие с устаревшими API аудио](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



