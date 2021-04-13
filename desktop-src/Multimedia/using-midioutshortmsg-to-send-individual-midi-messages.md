---
title: Использование Мидиаутшортмсг для отправки отдельных сообщений MIDI
description: Использование Мидиаутшортмсг для отправки отдельных сообщений MIDI
ms.assetid: 7a8f7c6c-28ac-4aa6-9073-969fc8e59f4e
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), отправка сообщений
- MIDI (цифровой интерфейс музыкального инструмента), отправка сообщений
- Отправка сообщений MIDI
- Цифровой интерфейс MIDI, функция Мидиаутшортмсг
- MIDI (цифровой интерфейс музыкального инструмента), функция Мидиаутшортмсг
- Функция Мидиаутшортмсг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b0ce924f9aebce67f515fc0714fdc855cbe33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487649"
---
# <a name="using-midioutshortmsg-to-send-individual-midi-messages"></a>Использование Мидиаутшортмсг для отправки отдельных сообщений MIDI

В следующем примере функция [**мидиаутшортмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) используется для отправки УКАЗАННОГО события MIDI на заданное устройство вывода MIDI:


```C++
UINT sendMIDIEvent(HMIDIOUT hmo, BYTE bStatus, BYTE bData1, 
    BYTE bData2) 
{ 
    union { 
        DWORD dwData; 
        BYTE bData[4]; 
    } u; 
 
    // Construct the MIDI message. 
 
    u.bData[0] = bStatus;  // MIDI status byte 
    u.bData[1] = bData1;   // first MIDI data byte 
    u.bData[2] = bData2;   // second MIDI data byte 
    u.bData[3] = 0; 
 
    // Send the message. 
    return midiOutShortMsg(hmo, u.dwData); 
} 
```



> [!Note]  
> Драйверы вывода MIDI не требуются для проверки данных перед их отправкой на порт вывода. Приложения должны обеспечивать отправку только допустимых данных.

 

 

 