---
title: Добавление информационного блока
description: Добавление информационного блока
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- макрос Капфилесетинфочунк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb99fb29e4b1882b4f257c428315f42ee3a360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258559"
---
# <a name="adding-an-information-chunk"></a><span data-ttu-id="7257b-104">Добавление информационного блока</span><span class="sxs-lookup"><span data-stu-id="7257b-104">Adding an Information Chunk</span></span>

<span data-ttu-id="7257b-105">Если необходимо включить в приложение другие сведения, помимо аудио и видео, можно создать фрагменты информации и вставить их в файл записи.</span><span class="sxs-lookup"><span data-stu-id="7257b-105">If you need to include other information in your application in addition to audio and video, you can create information chunks and insert them into a capture file.</span></span> <span data-ttu-id="7257b-106">Информационные блоки могут содержать несколько типов информации, включая сведения об авторских правах, идентификации источника видео или сведения о внешнем времени.</span><span class="sxs-lookup"><span data-stu-id="7257b-106">Information chunks can contain several types of information, including the details of a copyright notice, identification of the video source, or external timing information.</span></span> <span data-ttu-id="7257b-107">В следующем примере хранятся сведения о внешнем времени — SMPTE (общество инженеров и телевизоров движения) в информационном фрагменте и добавляется в файл записи с помощью макроса [**капфилесетинфочунк**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="7257b-107">The following example stores external timing information a SMPTE (Society of Motion Picture and Television Engineers) timecode in an information chunk and adds the chunk to a capture file using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7257b-108">См. также</span><span class="sxs-lookup"><span data-stu-id="7257b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7257b-109">Использование видеозаписи</span><span class="sxs-lookup"><span data-stu-id="7257b-109">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




