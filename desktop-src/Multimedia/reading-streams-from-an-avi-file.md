---
title: чтение Потоки из файла AVI
description: чтение Потоки из файла AVI
ms.assetid: fa17cac4-bc6f-48ef-8960-286386b43c82
keywords:
- Функция Авистреаминфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d42c4682c1875fffbea079ab9ef55d954f15d3e9d49c2da1309504da68aa92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371519"
---
# <a name="reading-streams-from-an-avi-file"></a>чтение Потоки из файла AVI

Следующая подпрограммы получает потоковую информацию из файла AVI и определяет тип потока из структуры [**авистреаминфо**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) , возвращаемой функцией [**авистреаминфо**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) .


```C++
// StreamTypes - opens the streams in an AVI file and determines 
// stream types. 
// 
// Global variables 
// gcpavi - count of streams in an AVI file 
// gapavi[] = array of stream-interface pointers 
 
void StreamTypes(HWND hwnd) 
{ 
    AVISTREAMINFO     avis; 
    LONG    r, lHeight = 0; 
    WORD    w; 
    int     i; 
    RECT    rc; 
 
// Walk through all streams. 
    for (i = 0; i < gcpavi; i++) { 
        AVIStreamInfo(gapavi[i], &avis, sizeof(avis)); 
 
        if (avis.fccType == streamtypeVIDEO) { 
 
        // Place video-processing functions here. 
 
        } 
        else if (avis.fccType == streamtypeAUDIO) { 
 
        // Place audio-processing functions here. 
 
        } 
        else if (avis.fccType == streamtypeTEXT) { 
 
        // Place text-processing functions here. 
 
        } 
    } 
} 
 
```



 

 




