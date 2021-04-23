---
description: Роли устройств для устаревших приложений мультимедиа Windows
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: Роли устройств для устаревших приложений мультимедиа Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a4ad6728659e4c865aed773575268844fe330e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105647759"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a><span data-ttu-id="027ed-103">Роли устройств для устаревших приложений мультимедиа Windows</span><span class="sxs-lookup"><span data-stu-id="027ed-103">Device Roles for Legacy Windows Multimedia Applications</span></span>

> [!Note]  
> <span data-ttu-id="027ed-104">API Ммдевице поддерживает роли устройств.</span><span class="sxs-lookup"><span data-stu-id="027ed-104">The MMDevice API supports device roles.</span></span> <span data-ttu-id="027ed-105">Однако пользовательский интерфейс в Windows Vista не реализует поддержку этой функции.</span><span class="sxs-lookup"><span data-stu-id="027ed-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="027ed-106">Поддержка пользовательского интерфейса для ролей устройств может быть реализована в будущей версии Windows.</span><span class="sxs-lookup"><span data-stu-id="027ed-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="027ed-107">Дополнительные сведения см. [в статье роли устройств в Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="027ed-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="027ed-108">Устаревшие функции Windows мультимедиа **вавеауткскскс** и **вавеинкскскс** не позволяют приложению выбрать [устройство звуковой конечной точки](audio-endpoint-devices.md) , которое пользователь назначил определенной [роли устройства](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="027ed-108">The legacy Windows multimedia **waveOutXxx** and **waveInXxx** functions provide no means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="027ed-109">Однако в Windows Vista основные интерфейсы API аудио можно использовать в сочетании с приложением мультимедиа Windows для выбора устройств на основе роли устройства.</span><span class="sxs-lookup"><span data-stu-id="027ed-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a Windows multimedia application to enable device selection based on device role.</span></span> <span data-ttu-id="027ed-110">Например, с помощью [API ммдевице](mmdevice-api.md)приложение **вавеауткскскс** может определить устройство конечной точки аудио, назначенное роли, определить соответствующее выходное устройство аудио и вызвать функцию **вавеаутопен** , чтобы открыть экземпляр устройства.</span><span class="sxs-lookup"><span data-stu-id="027ed-110">For example, with the help of the [MMDevice API](mmdevice-api.md), a **waveOutXxx** application can identify the audio endpoint device that is assigned to a role, identify the corresponding waveform output device, and call the **waveOutOpen** function to open an instance of the device.</span></span> <span data-ttu-id="027ed-111">Дополнительные сведения о **вавеауткскскс** и **вавеинкскскс** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="027ed-111">For more information about **waveOutXxx** and **waveInXxx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="027ed-112">В следующем примере кода показано, как получить идентификатор устройства волны для устройства конечной точки отрисовки, назначенного конкретной роли устройства:</span><span class="sxs-lookup"><span data-stu-id="027ed-112">The following code example shows how to obtain the waveform device ID for the rendering endpoint device that is assigned to a particular device role:</span></span>


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



<span data-ttu-id="027ed-113">В предыдущем примере кода функция Жетвавеаутид принимает роль устройства (Еконсоле, Емултимедиа или Екоммуникатионс) в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="027ed-113">In the preceding code example, the GetWaveOutId function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="027ed-114">Второй параметр — это указатель, через который функция записывает идентификатор устройства волны для выходного устройства аудио, назначенного указанной роли.</span><span class="sxs-lookup"><span data-stu-id="027ed-114">The second parameter is a pointer through which the function writes the waveform device ID for the waveform output device that is assigned to the specified role.</span></span> <span data-ttu-id="027ed-115">Затем приложение может вызвать **вавеаутопен** с этим идентификатором, чтобы открыть устройство.</span><span class="sxs-lookup"><span data-stu-id="027ed-115">The application can then call **waveOutOpen** with this ID to open the device.</span></span>

<span data-ttu-id="027ed-116">Основной цикл в предыдущем примере кода содержит два вызова функции **вавеаутмессаже** .</span><span class="sxs-lookup"><span data-stu-id="027ed-116">The main loop in the preceding code example contains two calls to the **waveOutMessage** function.</span></span> <span data-ttu-id="027ed-117">Первый вызов отправляет \_ сообщение КУЕРИФУНКТИОНИНСТАНЦЕИДСИЗЕ DRV для получения размера (в байтах) [строки идентификатора конечной точки](endpoint-id-strings.md) устройства волны, идентифицируемого параметром *вавеаутид* .</span><span class="sxs-lookup"><span data-stu-id="027ed-117">The first call sends a DRV\_QUERYFUNCTIONINSTANCEIDSIZE message to retrieve the size, in bytes, of the [endpoint ID string](endpoint-id-strings.md) of the waveform device that is identified by the *waveOutId* parameter.</span></span> <span data-ttu-id="027ed-118">(Строка идентификатора конечной точки определяет устройство аудио конечной точки, которое зависит от абстракции устройства волны.) Размер, сообщаемый этим вызовом, включает пробел для завершающего нуль-символа в конце строки.</span><span class="sxs-lookup"><span data-stu-id="027ed-118">(The endpoint ID string identifies the audio endpoint device that underlies the waveform device abstraction.) The size reported by this call includes the space for the terminating null character at the end of the string.</span></span> <span data-ttu-id="027ed-119">Программа может использовать сведения о размере для выделения буфера, который достаточно велик для размещения всей строки идентификатора конечной точки.</span><span class="sxs-lookup"><span data-stu-id="027ed-119">The program can use the size information to allocate a buffer that is large enough to contain the entire endpoint ID string.</span></span>

<span data-ttu-id="027ed-120">Второй вызов **вавеаутмессаже** ОТПРАВЛЯЕТ сообщение DRV куерифунктионинстанцеид, \_ чтобы получить строку идентификатора устройства для выходного устройства звуковой волны.</span><span class="sxs-lookup"><span data-stu-id="027ed-120">The second call to **waveOutMessage** sends a DRV\_QUERYFUNCTIONINSTANCEID message to retrieve the device ID string of the waveform output device.</span></span> <span data-ttu-id="027ed-121">В примере кода эта строка сравнивается со строкой идентификатора устройства устройства конечной точки аудио с указанной ролью устройства.</span><span class="sxs-lookup"><span data-stu-id="027ed-121">The example code compares this string to the device ID string of the audio endpoint device with the specified device role.</span></span> <span data-ttu-id="027ed-122">Если строки совпадают, функция записывает идентификатор устройства волны в расположение, на которое указывает параметр *пвавеаутид*.</span><span class="sxs-lookup"><span data-stu-id="027ed-122">If the strings match, then the function writes the waveform device ID to the location pointed to by parameter *pWaveOutId*.</span></span> <span data-ttu-id="027ed-123">Вызывающий объект может использовать этот идентификатор для открытия устройства вывода аудио с заданной ролью устройства.</span><span class="sxs-lookup"><span data-stu-id="027ed-123">The caller can use this ID to open the waveform output device that has the specified device role.</span></span>

<span data-ttu-id="027ed-124">Windows Vista поддерживает \_ сообщения КУЕРИФУНКТИОНИНСТАНЦЕИД DRV куерифунктионинстанцеидсизе и DRV \_ .</span><span class="sxs-lookup"><span data-stu-id="027ed-124">Windows Vista supports the DRV\_QUERYFUNCTIONINSTANCEIDSIZE and DRV\_QUERYFUNCTIONINSTANCEID messages.</span></span> <span data-ttu-id="027ed-125">Они не поддерживаются в более ранних версиях Windows, включая Windows Server 2003, Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="027ed-125">They are not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.</span></span>

<span data-ttu-id="027ed-126">Функция в предыдущем примере кода получает идентификатор устройства волны для устройства отрисовки, но при наличии нескольких изменений его можно адаптировать, чтобы получить идентификатор устройства для записи.</span><span class="sxs-lookup"><span data-stu-id="027ed-126">The function in the preceding code example obtains the waveform device ID for a rendering device, but, with a few modifications, it can be adapted to obtain the waveform device ID for a capture device.</span></span> <span data-ttu-id="027ed-127">Затем приложение может вызвать **вавеинопен** с этим идентификатором, чтобы открыть устройство.</span><span class="sxs-lookup"><span data-stu-id="027ed-127">The application can then call **waveInOpen** with this ID to open the device.</span></span> <span data-ttu-id="027ed-128">Чтобы изменить приведенный выше пример кода, чтобы получить идентификатор устройства с звуковой точкой для устройства записи звука, назначенного определенной роли, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="027ed-128">To change the preceding code example to get the waveform device ID for the audio-capture endpoint device that is assigned to a particular role, do the following:</span></span>

-   <span data-ttu-id="027ed-129">Замените все вызовы функций **вавеауткскскс** в предыдущем примере соответствующими вызовами функций **вавеинкскскс** .</span><span class="sxs-lookup"><span data-stu-id="027ed-129">Replace all of the **waveOutXxx** function calls in the preceding example with the corresponding **waveInXxx** function calls.</span></span>
-   <span data-ttu-id="027ed-130">Измените тип маркера ХВАВЕАУТ на ХВАВЕИН.</span><span class="sxs-lookup"><span data-stu-id="027ed-130">Change handle type HWAVEOUT to HWAVEIN.</span></span>
-   <span data-ttu-id="027ed-131">Замените константу перечисления [**Ероле**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) Ерендер на екаптуре.</span><span class="sxs-lookup"><span data-stu-id="027ed-131">Replace [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration constant eRender with eCapture.</span></span>

<span data-ttu-id="027ed-132">В Windows Vista функции **вавеаутопен** и **вавеинопен** всегда назначают звуковые потоки, которые они создают, в сеанс по умолчанию — сеанс конкретного процесса, определяемый идентификатором GUID GUID значения \_ null.</span><span class="sxs-lookup"><span data-stu-id="027ed-132">In Windows Vista, the **waveOutOpen** and **waveInOpen** functions always assign the audio streams that they create to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="027ed-133">См. также</span><span class="sxs-lookup"><span data-stu-id="027ed-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="027ed-134">Взаимодействие с устаревшими API аудио</span><span class="sxs-lookup"><span data-stu-id="027ed-134">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



