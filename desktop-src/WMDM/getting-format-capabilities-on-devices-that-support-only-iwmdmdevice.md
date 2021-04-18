---
title: Получение возможностей форматирования через Ивмдмдевице
description: Получение возможностей форматирования на устройствах, поддерживающих только Ивмдмдевице
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Диспетчер устройств Windows Media, возможности устройств
- Диспетчер устройств, возможности устройства
- рекомендации по программированию, возможности устройств
- Классические приложения, возможности устройств
- Создание приложений диспетчер устройств Windows Media, возможности устройств
- запись файлов на устройства, возможности устройств
- Метод Ивмдмдевице
- Диспетчер устройств Windows Media, метод Ивмдмдевице
- Диспетчер устройств, метод Ивмдмдевице
- инструкции по программированию, метод Ивмдмдевице
- Классические приложения, метод Ивмдмдевице
- Создание приложений диспетчер устройств Windows Media, метод Ивмдмдевице
- запись файлов на устройства, метод Ивмдмдевице
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a923919611b40197b1deed30e781042e008ef41
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/27/2019
ms.locfileid: "104335755"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a><span data-ttu-id="78fbb-116">Получение возможностей форматирования через Ивмдмдевице</span><span class="sxs-lookup"><span data-stu-id="78fbb-116">Getting format capabilities through IWMDMDevice</span></span>

<span data-ttu-id="78fbb-117">Рекомендуемый метод для запроса устройства в качестве его возможностей воспроизведения — [**IWMDMDevice3:: жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="78fbb-117">The recommended method for querying a device for its playback capabilities is [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span> <span data-ttu-id="78fbb-118">Однако если устройство не поддерживает этот метод, приложение может вызвать [**ивмдмдевице:: жетформатсуппорт**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) , чтобы извлечь массив поддерживаемых звуковых форматов в виде структур [**\_ вавеформатекс**](-waveformatex.md) и форматов MIME в виде строк с устройства.</span><span class="sxs-lookup"><span data-stu-id="78fbb-118">However, if a device does not support this method, the application instead can call [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) to retrieve an array of supported audio formats as [**\_WAVEFORMATEX**](-waveformatex.md) structures and MIME formats as strings from the device.</span></span>

<span data-ttu-id="78fbb-119">В следующих шагах показано, как приложение может использовать этот метод для запроса поддерживаемых форматов на устройстве:</span><span class="sxs-lookup"><span data-stu-id="78fbb-119">The following steps show how an application can use this method to query a device for supported formats:</span></span>

1.  <span data-ttu-id="78fbb-120">Вызовите **жетформатсуппорт** , чтобы получить массивы как для аудио, так и для форматов MIME.</span><span class="sxs-lookup"><span data-stu-id="78fbb-120">Call **GetFormatSupport** to retrieve arrays of both audio and mime formats.</span></span>
2.  <span data-ttu-id="78fbb-121">Пройдите по полученным аудио форматам и изучите каждую структуру [**\_ вавеформатекс**](-waveformatex.md) , чтобы попытаться найти приемлемый звуковой формат.</span><span class="sxs-lookup"><span data-stu-id="78fbb-121">Loop through the retrieved audio formats and examine each [**\_WAVEFORMATEX**](-waveformatex.md) structure to try to find an acceptable audio format</span></span>
3.  <span data-ttu-id="78fbb-122">Пройдите по полученным строкам формата MIME (при необходимости), чтобы найти допустимый тип файла.</span><span class="sxs-lookup"><span data-stu-id="78fbb-122">Loop through the retrieved MIME format strings (if desired) to find an acceptable file type.</span></span> <span data-ttu-id="78fbb-123">Пакет SDK не определяет константы для форматов MIME. следует использовать стандартные отраслевые значения (которые можно найти на веб-сайте iana.org).</span><span class="sxs-lookup"><span data-stu-id="78fbb-123">The SDK does not define constants for MIME formats; you should use industry standard values (which can be found at the iana.org Web site).</span></span> <span data-ttu-id="78fbb-124">Устройство должно перечислять определенные типы MIME, которые он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="78fbb-124">A device should list the specific MIME types that it supports.</span></span>

<span data-ttu-id="78fbb-125">Следующий код C++ демонстрирует извлечение возможностей форматирования с устройства с помощью **жетформатсуппорт**.</span><span class="sxs-lookup"><span data-stu-id="78fbb-125">The following C++ code demonstrates retrieving format capabilities from a device, using **GetFormatSupport**.</span></span>


```C++
// Function to print out device caps for a device 
// that supports only IWMDMDevice.
void CWMDMController::GetCaps(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get all capabilities for audio and mime support.
    _WAVEFORMATEX* pAudioFormats;
    LPWSTR* pMimeFormats;
    UINT numAudioFormats = 0;
    UINT numMimeFormats = 0;
    hr = pDevice->GetFormatSupport(
        &pAudioFormats,
        &numAudioFormats,
        &pMimeFormats,
        &numMimeFormats);
    if (FAILED(hr)) return;

    // Print out audio format data.
    if (numAudioFormats > 0)
    {
        // TODO: Display a banner for the supported audio-format listing.
    }
    else
    {
        // TODO: Display a message indicating that no audio formats are supported.
    }
    for (int i = 0; i < numAudioFormats; i++)
    {
       // TODO: For each valid audio format, display the max channel, 
       // max samples/second, avg. bytes/sec, block alignment, and 
       // max bits/sample values.
    }

    // Print out MIME formats.
    if (numMimeFormats > 0)
        // TODO: Display a banner to precede the MIME format listing.
    else
        // TODO: Display a banner indicating that no MIME formats are supported.
    for (i = 0; i < numMimeFormats; i++)
    {
        // TODO: Display the specified MIME format.
    }
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="78fbb-126">См. также</span><span class="sxs-lookup"><span data-stu-id="78fbb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78fbb-127">**Обнаружение возможностей форматирования устройств**</span><span class="sxs-lookup"><span data-stu-id="78fbb-127">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> <dt>

[<span data-ttu-id="78fbb-128">**Получение возможностей форматирования на устройствах, поддерживающих IWMDMDevice3**</span><span class="sxs-lookup"><span data-stu-id="78fbb-128">**Getting Format Capabilities on Devices That Support IWMDMDevice3**</span></span>](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




