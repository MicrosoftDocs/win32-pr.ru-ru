---
title: Получение сведений об упаковщиках и декомпрессорах
description: Получение сведений об упаковщиках и декомпрессорах
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- Диспетчер сжатия видео (ВКМ), получение сведений об компрессорах
- ВКМ (диспетчер сжатия видео), получение сведений об компрессорах
- Функция Икжетинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874793233ef0aec4de5b372573fb8dcd79f5d875
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410731"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a>Получение сведений об упаковщиках и декомпрессорах

В следующем примере функция [**икжетинфо**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) используется для получения сведений об упаковщике или декомпрессоре.


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



В следующем примере для получения значений по умолчанию используются макросы [**икжетдефаулткэйфрамерате**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) и [**икжетдефаулткуалити**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) .


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



В следующем примере используются макросы [**иккуерябаут**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) и [**икабаут**](/windows/desktop/api/Vfw/nf-vfw-icabout) для вывода диалогового окна о программе для сжатия или распаковки, если диалоговое окно существует.


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




