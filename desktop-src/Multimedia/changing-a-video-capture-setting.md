---
title: Изменение параметра видеозаписи
description: Изменение параметра видеозаписи
ms.assetid: a5fe7e1e-084d-4102-91d4-ffe5d1d0e5c8
keywords:
- макрос Капкаптурежетсетуп
- макрос Капкаптуресетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b3f2629325c67bcad1fed26a9fed4d053372392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411354"
---
# <a name="changing-a-video-capture-setting"></a>Изменение параметра видеозаписи

В следующем примере используются макросы [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) и [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) для изменения скорости записи со значения по умолчанию (15 кадров в секунду) на 10 кадров в секунду.


```C++
CAPTUREPARMS CaptureParms;
float FramesPerSec = 10.0;

capCaptureGetSetup(hWndC, &CaptureParms, sizeof(CAPTUREPARMS));

CaptureParms.dwRequestMicroSecPerFrame = (DWORD) (1.0e6 / 
    FramesPerSec);
capCaptureSetSetup(hWndC, &CaptureParms, sizeof (CAPTUREPARMS)); 
 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 




