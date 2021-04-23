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
ms.openlocfilehash: 1534cf660c2f2423dc526c3d29f8eca06878fc0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487605"
---
# <a name="using-the-waveformatex-structure"></a><span data-ttu-id="54c40-107">Использование структуры ВАВЕФОРМАТЕКС</span><span class="sxs-lookup"><span data-stu-id="54c40-107">Using the WAVEFORMATEX Structure</span></span>

<span data-ttu-id="54c40-108">Для звуковых данных PCM, не имеющих более двух каналов, с 8-разрядными или 16-разрядными примерами, используйте структуру [**вавеформатекс**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) для указания формата данных.</span><span class="sxs-lookup"><span data-stu-id="54c40-108">For PCM audio data on no more than two channels and with 8-bit or 16-bit samples, use the [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to specify the data format.</span></span>

<span data-ttu-id="54c40-109">В следующем примере показано, как настроить структуру **вавеформатекс** для 11,025 Килохертз (кГц) 8-разрядный моно и для 16-разрядного стерео с 44,1 кГц.</span><span class="sxs-lookup"><span data-stu-id="54c40-109">The following example shows how to set up a **WAVEFORMATEX** structure for 11.025 kilohertz (kHz) 8-bit mono and for 44.1 kHz 16-bit stereo.</span></span> <span data-ttu-id="54c40-110">После настройки **вавеформатекс** в примере вызывается функция исформатсуппортед, чтобы убедиться, что устройство вывода PCM формата выходных данных поддерживает формат.</span><span class="sxs-lookup"><span data-stu-id="54c40-110">After setting up **WAVEFORMATEX**, the example calls the IsFormatSupported function to verify that the PCM waveform output device supports the format.</span></span> <span data-ttu-id="54c40-111">Исходный код для Исформатсуппортед показан в примере [определения поддержки нестандартного формата](determining-nonstandard-format-support.md).</span><span class="sxs-lookup"><span data-stu-id="54c40-111">The source code for IsFormatSupported is shown in an example in [Determining Nonstandard Format Support](determining-nonstandard-format-support.md).</span></span>


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



 

 