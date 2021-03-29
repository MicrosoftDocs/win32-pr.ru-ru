---
title: Рисование данных
description: Рисование данных
ms.assetid: cc4f383d-54d4-4027-ad6a-da19bb07c17f
keywords:
- Диспетчер сжатия видео (ВКМ), рисование
- ВКМ (диспетчер сжатия видео), рисование
- Функция Икдрав
- Макрос Икдравстарт
- Макрос Икдравстоп
- Макрос Икдравфлуш
- Макрос Икдравенд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f598ef47bbbf6b8f53c7fb2639c9ddff1390ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067729"
---
# <a name="drawing-data"></a>Рисование данных

В следующем примере используется функция [**икдрав**](/windows/desktop/api/Vfw/nf-vfw-icdraw) и макросы [**икдравстарт**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart), [**икдравстоп**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop), [**икдравфлуш**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush)и [**икдравенд**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) для рисования данных на экране.


```C++
DWORD    dwNumBuffers; 
 
// Find out how many buffers need filling before drawing starts.

ICGetBuffersWanted(hIC, &dwNumBuffers); 
for (dw = 0; dw < dwNumBuffers; dw++)
{ 
    ICDraw(hIC, 0, lpFormat, lpData, cbData, dw); // fill the pipeline
    
    // Point lpFormat and lpData to next format and buffer.
    
} 
ICDrawStart(hIC);  // starts the clock 
dw = 0; 
while (fPlaying) 
{ 
    ICDraw(hIC, 0, lpFormat, lpData, chData, dw); // fill more buffers 
    
    // Point lpFormat and lpData to next format and buffer,
    // update dw.
} 
 
ICDrawStop(hIC);   // stops drawing and decompressing when done 
ICDrawFlush(hIC);  // flushes any existing buffers 
ICDrawEnd(hIC);    // ends decompression 
 
```



 

 




