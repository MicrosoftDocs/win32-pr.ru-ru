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
ms.openlocfilehash: c6aca93f23ed74a4a4974633d8345f2e897535e156ccc03f46eb0da92a2d2fdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037864"
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



 

 




