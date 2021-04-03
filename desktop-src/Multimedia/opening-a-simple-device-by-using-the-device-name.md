---
title: Открытие простого устройства с помощью имени устройства
description: Открытие простого устройства с помощью имени устройства
ms.assetid: 9e116499-2094-40e1-b2bc-3e3b8281a472
keywords:
- Функция МЦисендкомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f84a852a18da3edb4431308259bacf38623bce3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987394"
---
# <a name="opening-a-simple-device-by-using-the-device-name"></a>Открытие простого устройства с помощью имени устройства

В следующем примере показано, как открыть устройство воспроизведения компакт-дисков, указав имя устройства с помощью функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) .


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;
 
// Opens a CD audio device by specifying the device name.

mciOpenParms.lpstrDeviceType = "cdaudio";

if (dwReturn = mciSendCommand(NULL, MCI_OPEN, MCI_OPEN_TYPE,
    (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 