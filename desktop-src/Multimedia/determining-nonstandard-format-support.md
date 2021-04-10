---
title: Определение поддержки нестандартного формата
description: Определение поддержки нестандартного формата
ms.assetid: a795aa7d-704b-4f03-9815-7a298907bd3d
keywords:
- звуковая волна, нестандартная поддержка формата
- Вспомогательная звуковая, нестандартная поддержка формата
- звуковая волна, поддержка стандартного формата
- Вспомогательное аудио, поддержка стандартного формата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0933a82ca8da53c89e1cb8b7d32b40dc89ae0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069916"
---
# <a name="determining-nonstandard-format-support"></a><span data-ttu-id="17d6f-107">Определение поддержки нестандартного формата</span><span class="sxs-lookup"><span data-stu-id="17d6f-107">Determining Nonstandard Format Support</span></span>

<span data-ttu-id="17d6f-108">Чтобы узнать, поддерживает ли устройство определенный формат (стандартный или нестандартный), можно вызвать функцию [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) с \_ \_ флагом запроса Wave Format.</span><span class="sxs-lookup"><span data-stu-id="17d6f-108">To see whether a device supports a particular format (standard or nonstandard), you can call the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function with the WAVE\_FORMAT\_QUERY flag.</span></span> <span data-ttu-id="17d6f-109">В следующем примере этот метод используется для определения того, поддерживает ли устройство аудио-аудио определенного формата.</span><span class="sxs-lookup"><span data-stu-id="17d6f-109">The following example uses this technique to determine whether a waveform-audio device supports a specified format.</span></span>


```C++
// Determines whether the specified waveform-audio output device 
// supports a specified waveform-audio format. Returns 
// MMSYSERR_NOERROR if the format is supported, WAVEERR_BADFORMAT if 
// the format is not supported, and one of the other MMSYSERR_ error 
// codes if there are other errors encountered in opening the 
// specified waveform-audio device. 
 
MMRESULT IsFormatSupported(LPWAVEFORMATEX pwfx, UINT uDeviceID) 
{ 
    return (waveOutOpen( 
        NULL,                 // ptr can be NULL for query 
        uDeviceID,            // the device identifier 
        pwfx,                 // defines requested format 
        NULL,                 // no callback 
        NULL,                 // no instance data 
        WAVE_FORMAT_QUERY));  // query only, do not open device 
} 
```



<span data-ttu-id="17d6f-110">Этот метод определения поддержки нестандартного формата также применяется к устройствам ввода аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="17d6f-110">This technique for determining nonstandard format support also applies to waveform-audio input devices.</span></span> <span data-ttu-id="17d6f-111">Единственное отличие заключается в том, что функция [**вавеинопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) используется вместо [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) для запроса поддержки формата.</span><span class="sxs-lookup"><span data-stu-id="17d6f-111">The only difference is that the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function is used in place of [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) to query for format support.</span></span>

<span data-ttu-id="17d6f-112">Чтобы определить, поддерживается ли формат данных Wave-Audio любыми устройствами аудио-сигнала в системе, используйте методику, показанную в предыдущем примере, но укажите \_ константу СОПОСТАВИТЕЛЯ волн для параметра *удевицеид* .</span><span class="sxs-lookup"><span data-stu-id="17d6f-112">To determine whether a particular waveform-audio data format is supported by any of the waveform-audio devices in a system, use the technique illustrated in the previous example, but specify the WAVE\_MAPPER constant for the *uDeviceID* parameter.</span></span>

 

 