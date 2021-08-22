---
title: Форматирование записи звука
description: Форматирование записи звука
ms.assetid: 3bbe34a6-8fd6-4780-b5af-fcf3d34ef701
keywords:
- макрос Капсетаудиоформат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36acf1f98bcb6ea5d6786264406c28da78e909e3e57c5d796eac080139229f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496384"
---
# <a name="formatting-audio-capture"></a>Форматирование записи звука

В следующем примере используется [**капсетаудиоформат**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) для задания формата аудио для 8-разрядного PCM, стерео.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 




