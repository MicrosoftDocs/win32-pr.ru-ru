---
title: Запись данных
description: Запись данных
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- макрос Капкаптуресекуенце
- макрос Капфилесавеас
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764ff00dedcc044ed5234f8b647b08eaded35ce191bcb56e05cb35f47450677b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941302"
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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 




