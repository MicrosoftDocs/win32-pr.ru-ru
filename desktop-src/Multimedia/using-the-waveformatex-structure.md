---
title: Использование структуры ВАВЕФОРМАТЕКС
description: Использование структуры ВАВЕФОРМАТЕКС
ms.assetid: 9b668e1e-cb5f-4065-802b-23974925eacf
keywords:
- звуковая волна, структура ВАВЕФОРМАТЕКС
- Вспомогательная звуковая, ВАВЕФОРМАТЕКСная структура
- Структура ВАВЕФОРМАТЕКС
- Звуковые данные PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3831d9760580f294573a4bc1bec3aef1d42cf345b2d714a897b22940a89a0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136058"
---
# <a name="using-the-waveformatex-structure"></a>Использование структуры ВАВЕФОРМАТЕКС

Для звуковых данных PCM, не имеющих более двух каналов, с 8-разрядными или 16-разрядными примерами, используйте структуру [**вавеформатекс**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) для указания формата данных.

В следующем примере показано, как настроить структуру **вавеформатекс** для 11,025 Килохертз (кГц) 8-разрядный моно и для 16-разрядного стерео с 44,1 кГц. После настройки **вавеформатекс** в примере вызывается функция исформатсуппортед, чтобы убедиться, что устройство вывода PCM формата выходных данных поддерживает формат. Исходный код для Исформатсуппортед показан в примере [определения поддержки нестандартного формата](determining-nonstandard-format-support.md).


```C++
UINT wReturn; 
WAVEFORMATEX pcmWaveFormat; 
 
// Set up WAVEFORMATEX for 11 kHz 8-bit mono. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 1; 
pcmWaveFormat.nSamplesPerSec = 11025L; 
pcmWaveFormat.nAvgBytesPerSec = 11025L; 
pcmWaveFormat.nBlockAlign = 1; 
pcmWaveFormat.wBitsPerSample = 8; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono is supported.", 
       "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono NOT supported.", 
       "", MB_ICONINFORMATION); 
else 
     MessageBox(hMainWnd, "Error opening waveform device.", 
       "Error", MB_ICONEXCLAMATION); 
 
// Set up WAVEFORMATEX for 44.1 kHz 16-bit stereo. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 2; 
pcmWaveFormat.nSamplesPerSec = 44100L; 
pcmWaveFormat.nAvgBytesPerSec = 176400L; 
pcmWaveFormat.nBlockAlign = 4; 
pcmWaveFormat.wBitsPerSample = 16; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in the system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo is supported.", 
      "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo NOT supported.", 
      "", MB_ICONINFORMATION); 
else 
    MessageBox(hMainWnd, "Error opening waveform device.", 
      "Error", MB_ICONEXCLAMATION); 

```



 

 