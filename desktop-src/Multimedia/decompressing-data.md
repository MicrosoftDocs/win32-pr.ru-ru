---
title: Распаковка данных
description: Распаковка данных
ms.assetid: 1faf0238-7bef-4363-9bbc-44737600c946
keywords:
- Диспетчер сжатия видео (ВКМ), распаковка данных
- ВКМ (диспетчер сжатия видео), распаковка данных
- Макрос Икдекомпрессбегин
- Функция Икдекомпресс
- Макрос Икдекомпрессенд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b44ea375bb1f2b5c41a361ca7f31387439b610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776340"
---
# <a name="decompressing-data"></a><span data-ttu-id="acc0e-108">Распаковка данных</span><span class="sxs-lookup"><span data-stu-id="acc0e-108">Decompressing Data</span></span>

<span data-ttu-id="acc0e-109">В следующем примере показано, как приложение может инициализировать декомпрессор с помощью макроса [**икдекомпрессбегин**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) , распаковать последовательность кадров с помощью функции [**икдекомпресс**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) и завершить распаковку с помощью макроса [**икдекомпрессенд**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .</span><span class="sxs-lookup"><span data-stu-id="acc0e-109">The following example shows how an application can initialize a decompressor using the [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) macro, decompress a frame sequence using the [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) function, and terminate decompression using the [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) macro.</span></span>


```C++
LPBITMAPINFOHEADER lbpiIn, lpbiOut; 
LPVOID             lpIn, lpOut; 
LONG               lNumFrames, lFrameNum; 
 
// Assume lpbiIn and lpbiOut are initialized to the input and output 
// format and lpIn and lpOut are pointing to the buffers. 
if (ICDecompressBegin(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    for (lFrameNum = 0; lFrameNum < lNumFrames, lFrameNum++)
    { 
        if (ICDecompress(hIC, 0, lpbiIn, lpIn, lpbiOut, 
            lpOut) == ICERR_OK) 
        { 
            // Frame decompressed OK so we can process it as required. 
        } 
        else 
        { 
            // Handle the decompression error that occurred. 
        } 
    } 
    ICDecompressEnd(hIC); 
} 
else 
{ 
    // Handle the error identifying an unsupported format. 
} 
 
```



 

 




