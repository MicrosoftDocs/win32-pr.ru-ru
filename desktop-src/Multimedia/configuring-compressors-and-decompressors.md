---
title: Настройка сжатия и декомпрессоров
description: Настройка сжатия и декомпрессоров
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- Диспетчер сжатия видео (ВКМ), Настройка компрессоров
- ВКМ (диспетчер сжатия видео), Настройка компрессоров
- Макрос Иккуериконфигуре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a9ac7eb56c0870d7a08d8ed9fd221a2626bb6be83cc4683cd86c4bfa907db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144927"
---
# <a name="configuring-compressors-and-decompressors"></a>Настройка сжатия и декомпрессоров

В следующем примере с помощью макроса [**иккуериконфигуре**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) показано, как проверить, поддерживает ли упаковщик диалоговое окно Конфигурация, и отображать его, если оно есть.


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



В следующем примере показано, как получить данные о состоянии с помощью макроса [**икжетстате**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



В следующем примере показано, как восстановить данные о состоянии с помощью макроса [**иксетстате**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) . Данные состояния, восстанавливаемые приложениями, не должны содержать изменений данных о состоянии, полученных из драйвера.


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




