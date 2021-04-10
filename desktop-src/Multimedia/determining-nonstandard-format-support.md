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
# <a name="determining-nonstandard-format-support"></a>Определение поддержки нестандартного формата

Чтобы узнать, поддерживает ли устройство определенный формат (стандартный или нестандартный), можно вызвать функцию [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) с \_ \_ флагом запроса Wave Format. В следующем примере этот метод используется для определения того, поддерживает ли устройство аудио-аудио определенного формата.


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



Этот метод определения поддержки нестандартного формата также применяется к устройствам ввода аудио-сигнала. Единственное отличие заключается в том, что функция [**вавеинопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) используется вместо [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) для запроса поддержки формата.

Чтобы определить, поддерживается ли формат данных Wave-Audio любыми устройствами аудио-сигнала в системе, используйте методику, показанную в предыдущем примере, но укажите \_ константу СОПОСТАВИТЕЛЯ волн для параметра *удевицеид* .

 

 