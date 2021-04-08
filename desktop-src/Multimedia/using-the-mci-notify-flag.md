---
title: Использование флага MCI_NOTIFY
description: Использование \_ флага уведомления MCI
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- Флаг MCI_NOTIFY
- Команда MCI_PLAY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472613d2e6efcd6b30c88ed64dfa7875b4742527
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887923"
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



 

 




