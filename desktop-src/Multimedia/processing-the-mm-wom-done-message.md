---
title: Обработка сообщения MM_WOM_DONE
description: Обработка сообщения о \_ \_ завершении вом mm
ms.assetid: 215167d0-3020-453d-b6b3-cee5803836c9
keywords:
- звуковая волна, сообщения
- вспомогательный звук, сообщения
- волна аудио, MM_WOM_DONE сообщение
- Вспомогательное аудио, MM_WOM_DONE сообщение
- Сообщение MM_WOM_DONE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e909777c115b6b10500e081a08bde6cfe24b00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486788"
---
# <a name="processing-the-mm_wom_done-message"></a>Обработка сообщения о \_ \_ завершении вом mm

В следующем примере показано, как обработать сообщение [**о \_ \_ завершении вом mm**](mm-wom-done.md) . В этом примере предполагается, что приложение не воспроизводит несколько блоков данных, поэтому выходное устройство можно закрыть после воспроизведения одного блока данных.


```C++
// WndProc--Main window procedure. 
LRESULT FAR PASCAL WndProc(HWND hWnd, UINT msg, WPARAM wParam, 
    LPARAM lParam) 
{ 
switch (msg) 
{ 
    case MM_WOM_DONE: 
 
    // A waveform-audio data block has been played and 
    // can now be freed. 
    waveOutUnprepareHeader((HWAVEOUT) wParam, 
        (LPWAVEHDR) lParam, sizeof(WAVEHDR) ); 
    
    // Free hData memory. 
    
    waveOutClose((HWAVEOUT) wParam); 
    break; 
    } 
    return DefWindowProc(hWnd, msg, wParam, lParam); 
} 
```



 

 




