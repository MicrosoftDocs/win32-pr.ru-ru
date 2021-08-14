---
title: Задание формата времени
description: Задание формата времени
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- Сообщение команды MCI_SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eb5a9194f3f2598cd8f88fbefb3ea741f51eb9c25210deb6db69c54259e189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370892"
---
# <a name="setting-the-time-format"></a>Задание формата времени

Чтобы задать формат времени для открытого устройства, используйте команду [**MCI \_ Set**](mci-set.md) с помощью команды MCI [**\_ Set \_ пармс**](mci-set-parms.md) Structure. Задайте для элемента **двтимеформат** одну из следующих констант.



| Константа                   | Формат времени                                          |
|----------------------------|------------------------------------------------------|
| \_ \_ байты формата MCI         | Байты (в \[ файлах формата PCM с модуляцией кода \] ) |
| \_ \_ миллисекунды формата MCI  | Миллисекунды                                         |
| формат MCI, \_ \_ MSF           | Минуты в секунду на кадр                                  |
| \_примеры формата \_ MCI       | Примеры                                              |
| \_Формат MCI \_ SMPTE \_ 24     | SMPTE, 24 кадра                                      |
| \_Формат MCI \_ SMPTE \_ 25     | SMPTE, 25 кадров                                      |
| \_Формат MCI \_ SMPTE \_ 30     | SMPTE, 30 кадров                                      |
| \_Формат MCI \_ SMPTE \_ 30DROP | SMPTE, 30 кадров                                 |
| \_Формат MCI \_ тмсф          | Записано/мин в секунду на кадр                            |
| MCI \_ Seq \_ Формат \_ сонгптр  | Указатель песни MIDI                                    |



 

В следующем примере в качестве формата времени задается миллисекунда на устройстве, указанном переменной Вдевицеид с помощью функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) .


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 