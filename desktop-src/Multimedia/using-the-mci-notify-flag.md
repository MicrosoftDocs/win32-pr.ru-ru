---
title: Использование флага MCI_NOTIFY
description: Использование \_ флага уведомления MCI
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- Флаг MCI_NOTIFY
- Команда MCI_PLAY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0e7269ee7d80dd47372d9210fbdbc1332b3a88a96e2a17d6719c9945ab30aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136142"
---
# <a name="using-the-mci_notify-flag"></a>Использование \_ флага уведомления MCI

В следующем примере показано \_ использование флага уведомления MCI с командой [**MCI \_ Play**](mci-play.md) . Дескриптор процедуры окна, которая будет обрабатывать сообщение [**\_ мЦинотифи mm**](mm-mcinotify.md) , указывается в *HWND*.


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




