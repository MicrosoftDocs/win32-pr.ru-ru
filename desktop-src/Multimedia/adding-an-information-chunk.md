---
title: Добавление информационного блока
description: Добавление информационного блока
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- макрос Капфилесетинфочунк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420181fd0da326ebf3ccc6f921e55161c2005d17c3f8713cd104481147b40f1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145137"
---
# <a name="adding-an-information-chunk"></a>Добавление информационного блока

Если необходимо включить в приложение другие сведения, помимо аудио и видео, можно создать фрагменты информации и вставить их в файл записи. Информационные блоки могут содержать несколько типов информации, включая сведения об авторских правах, идентификации источника видео или сведения о внешнем времени. В следующем примере хранятся сведения о внешнем времени — SMPTE (общество инженеров и телевизоров движения) в информационном фрагменте и добавляется в файл записи с помощью макроса [**капфилесетинфочунк**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .


```C++
//  This example assumes the application controls 
//  the video source for preroll and postroll. 
CAPINFOCHUNK cic;
// . 
// . 
// . 
cic.fccInfoID = infotypeSMPTE_TIME;
cic.lpData = "00:20:30:12"; 
cic.cbData = strlen (cic.lpData) + 1;
capFileSetInfoChunk (hwndC, &cic); 
 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 




