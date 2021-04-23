---
title: Форматирование записи звука
description: Форматирование записи звука
ms.assetid: 3bbe34a6-8fd6-4780-b5af-fcf3d34ef701
keywords:
- макрос Капсетаудиоформат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f53553804aab401a9c2a4ada5dc9ee39170269
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779130"
---
# <a name="formatting-audio-capture"></a><span data-ttu-id="15906-104">Форматирование записи звука</span><span class="sxs-lookup"><span data-stu-id="15906-104">Formatting Audio Capture</span></span>

<span data-ttu-id="15906-105">В следующем примере используется [**капсетаудиоформат**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) для задания формата аудио для 8-разрядного PCM, стерео.</span><span class="sxs-lookup"><span data-stu-id="15906-105">The following example uses [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) to set the audio format to 11-kHz PCM 8-bit, stereo.</span></span>


```C++
WAVEFORMATEX wfex;

wfex.wFormatTag = WAVE_FORMAT_PCM;
wfex.nChannels = 2;                // Use stereo
wfex.nSamplesPerSec = 11025;
wfex.nAvgBytesPerSec = 22050;
wfex.nBlockAlign = 2;
wfex.wBitsPerSample = 8;
wfex.cbSize = 0;

capSetAudioFormat(hWndC, &wfex, sizeof(WAVEFORMATEX)); 
 
```



## <a name="related-topics"></a><span data-ttu-id="15906-106">См. также</span><span class="sxs-lookup"><span data-stu-id="15906-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15906-107">Использование видеозаписи</span><span class="sxs-lookup"><span data-stu-id="15906-107">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




