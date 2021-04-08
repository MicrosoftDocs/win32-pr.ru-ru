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
# <a name="capturing-data"></a><span data-ttu-id="d40be-105">Запись данных</span><span class="sxs-lookup"><span data-stu-id="d40be-105">Capturing Data</span></span>

<span data-ttu-id="d40be-106">В следующем примере используется макрос [**капкаптуресекуенце**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) для запуска видеозаписи и макроса [**капфилесавеас**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) для копирования записанных данных из файла записи в файл NEWFILE.AVI.</span><span class="sxs-lookup"><span data-stu-id="d40be-106">The following example uses the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro to start video capture and the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro to copy the captured data from the capture file to the file NEWFILE.AVI.</span></span>


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a><span data-ttu-id="d40be-107">См. также</span><span class="sxs-lookup"><span data-stu-id="d40be-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d40be-108">Использование видеозаписи</span><span class="sxs-lookup"><span data-stu-id="d40be-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




