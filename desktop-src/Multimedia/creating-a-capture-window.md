---
title: Создание окна записи
description: Создание окна записи
ms.assetid: a727ce14-9b12-4f21-bab4-fa2eb245dce7
keywords:
- Функция Капкреатекаптуревиндов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d44e7701900d090a8d73b226039d468e2da817e9c0f9746fc10eaa13578d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144777"
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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 




