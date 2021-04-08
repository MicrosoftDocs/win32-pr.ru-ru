---
title: Создание окна записи
description: Создание окна записи
ms.assetid: a727ce14-9b12-4f21-bab4-fa2eb245dce7
keywords:
- Функция Капкреатекаптуревиндов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28375da063839d3120ca60bdabd5ca997fa31b02
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067841"
---
# <a name="creating-a-capture-window"></a>Создание окна записи

В следующем примере создается окно записи с помощью функции [**капкреатекаптуревиндов**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) .


```C++
hWndC = capCreateCaptureWindow (
    TEXT("My Capture Window"),   // window name if pop-up 
    WS_CHILD | WS_VISIBLE,       // window style 
    0, 0, 160, 120,              // window position and dimensions
    (HWND) hwndParent, 
    (int) nID /* child ID */); 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 




