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
# <a name="processing-the-mm_wom_done-message"></a><span data-ttu-id="d0b76-108">Обработка сообщения о \_ \_ завершении вом mm</span><span class="sxs-lookup"><span data-stu-id="d0b76-108">Processing the MM\_WOM\_DONE Message</span></span>

<span data-ttu-id="d0b76-109">В следующем примере показано, как обработать сообщение [**о \_ \_ завершении вом mm**](mm-wom-done.md) .</span><span class="sxs-lookup"><span data-stu-id="d0b76-109">The following example shows how to process the [**MM\_WOM\_DONE**](mm-wom-done.md) message.</span></span> <span data-ttu-id="d0b76-110">В этом примере предполагается, что приложение не воспроизводит несколько блоков данных, поэтому выходное устройство можно закрыть после воспроизведения одного блока данных.</span><span class="sxs-lookup"><span data-stu-id="d0b76-110">This example assumes the application does not play multiple data blocks, so it can close the output device after playing a single data block.</span></span>


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



 

 




