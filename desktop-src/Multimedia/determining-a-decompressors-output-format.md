---
title: Определение формата вывода декомпрессора
description: Определение формата вывода декомпрессора
ms.assetid: afedef5e-a506-40bd-aaad-fd85b0468ed7
keywords:
- Диспетчер сжатия видео (ВКМ), формат вывода
- ВКМ (диспетчер сжатия видео), формат вывода
- Макрос Икдекомпрессжетформатсизе
- Макрос Икдекомпресскуери
- Макрос Икдекомпрессжетпалетте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb4140a4118cb2a36ccd75088556c53c55fdcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133807"
---
# <a name="determining-a-decompressors-output-format"></a><span data-ttu-id="ba655-108">Определение формата вывода декомпрессора</span><span class="sxs-lookup"><span data-stu-id="ba655-108">Determining a Decompressor's Output Format</span></span>

<span data-ttu-id="ba655-109">В следующем примере определяется размер буфера, необходимый для данных, указывающих формат распаковки, с помощью макроса [**икдекомпрессжетформатсизе**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) , выделяется буфер соответствующего размера с помощью функции [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) и извлекаются сведения о формате распаковки с помощью макроса [**икдекомпрессжетформат**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .</span><span class="sxs-lookup"><span data-stu-id="ba655-109">The following example determines the buffer size needed for the data specifying the decompression format using the [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) macro, allocates a buffer of the appropriate size using the [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) function, and retrieves the decompression format information using the [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) macro.</span></span>


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



<span data-ttu-id="ba655-110">В следующем примере показано, как приложение может использовать макрос [**икдекомпресскуери**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) , чтобы определить, может ли декомпрессор работать с форматами входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ba655-110">The following example shows how an application can use the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro to determine if a decompressor can handle the input and output formats.</span></span>


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



<span data-ttu-id="ba655-111">В следующем фрагменте кода показано, как получить сведения о палитре с помощью макроса [**икдекомпрессжетпалетте**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="ba655-111">The following code fragment shows how to get the palette information using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 