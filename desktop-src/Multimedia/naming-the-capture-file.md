---
title: Присвоение имени файлу записи
description: Присвоение имени файлу записи
ms.assetid: fae2fd6a-4c2f-432f-a714-9faae6daeafe
keywords:
- макрос Капфилесеткаптурефиле
- макрос Капфилеаллок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c07653b854b4af476c22566aac5e9ecf27cb78b3dac5b317aab4b8f3f23a19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373319"
---
# <a name="naming-the-capture-file"></a>Присвоение имени файлу записи

В следующем примере используется макрос [**капфилесеткаптурефиле**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) , чтобы указать альтернативное имя файла (MYCAP.AVI) для файла записи и макроса [**капфилеаллок**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) , чтобы предварительно выделить файл размером 5 МБ.


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 




