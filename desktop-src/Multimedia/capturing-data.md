---
title: Запись данных
description: Запись данных
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- макрос Капкаптуресекуенце
- макрос Капфилесавеас
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24b2110da9a85faaa991e67efdd1ef48e3d9c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068328"
---
# <a name="capturing-data"></a>Запись данных

В следующем примере используется макрос [**капкаптуресекуенце**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) для запуска видеозаписи и макроса [**капфилесавеас**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) для копирования записанных данных из файла записи в файл NEWFILE.AVI.


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 




