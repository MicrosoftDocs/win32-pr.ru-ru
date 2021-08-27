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
ms.openlocfilehash: b023a8f82fa92aa78a2a2dcf47a8f6c9447f943ac0f68440c6d7aff3123fc84e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038444"
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



 

 




