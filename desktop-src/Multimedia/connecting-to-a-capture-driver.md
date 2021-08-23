---
title: Подключение к драйверу записи
description: Подключение к драйверу записи
ms.assetid: ce83329f-de5a-4428-bc0d-be5f3d35ff1a
keywords:
- макрос Капдривердисконнект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34e606c439143400f1ea1845db37e7faf93009350254c173c4003400c3996f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144867"
---
# <a name="connecting-to-a-capture-driver"></a>Подключение к драйверу записи

В следующем примере показано, как подключить окно Capture с помощью обработчика *хвндк* к драйверу мсвидео, а затем отключать их с помощью макроса [**капдривердисконнект**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) :


```C++
fOK = SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0, 0L); 
// 
// Or, use the macro to connect to the MSVIDEO driver: 
// fOK = capDriverConnect(hWndC, 0); 
// 
// Place code to set up and capture video here. 
// 
capDriverDisconnect (hWndC); 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 




