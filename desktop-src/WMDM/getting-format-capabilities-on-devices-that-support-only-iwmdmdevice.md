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
# <a name="getting-format-capabilities-through-iwmdmdevice"></a>Получение возможностей форматирования через Ивмдмдевице

Рекомендуемый метод для запроса устройства в качестве его возможностей воспроизведения — [**IWMDMDevice3:: жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Однако если устройство не поддерживает этот метод, приложение может вызвать [**ивмдмдевице:: жетформатсуппорт**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) , чтобы извлечь массив поддерживаемых звуковых форматов в виде структур [**\_ вавеформатекс**](-waveformatex.md) и форматов MIME в виде строк с устройства.

В следующих шагах показано, как приложение может использовать этот метод для запроса поддерживаемых форматов на устройстве:

1.  Вызовите **жетформатсуппорт** , чтобы получить массивы как для аудио, так и для форматов MIME.
2.  Пройдите по полученным аудио форматам и изучите каждую структуру [**\_ вавеформатекс**](-waveformatex.md) , чтобы попытаться найти приемлемый звуковой формат.
3.  Пройдите по полученным строкам формата MIME (при необходимости), чтобы найти допустимый тип файла. Пакет SDK не определяет константы для форматов MIME. следует использовать стандартные отраслевые значения (которые можно найти на веб-сайте iana.org). Устройство должно перечислять определенные типы MIME, которые он поддерживает.

Следующий код C++ демонстрирует извлечение возможностей форматирования с устройства с помощью **жетформатсуппорт**.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Обнаружение возможностей форматирования устройств**](discovering-device-format-capabilities.md)
</dt> <dt>

[**Получение возможностей форматирования на устройствах, поддерживающих IWMDMDevice3**](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




