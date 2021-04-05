---
title: Определение формата выходных данных программы сжатия
description: Определение формата выходных данных программы сжатия
ms.assetid: 910bd77f-4c65-4ea2-bab2-96f42a2b6cf1
keywords:
- Диспетчер сжатия видео (ВКМ), формат вывода
- ВКМ (диспетчер сжатия видео), формат вывода
- Макрос Иккомпрессжетформат
- Макрос Иккомпресскуери
- Макрос Иккомпрессжетсизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4356870598dc08ad84c4073be5ffa3c2ddbd5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133866"
---
# <a name="determining-a-compressors-output-format"></a>Определение формата выходных данных программы сжатия

В следующем примере макрос размера [**иккомпрессжетформат**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) используется для определения размера буфера, необходимого для данных, указывающих на формат сжатия, выделяет буфер соответствующего размера с помощью функции [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) и получает сведения о формате сжатия с помощью макроса **иккомпрессжетформат** .


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// *lpbiIn must be initialized to the input format. 
 
dwFormatSize = ICCompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICCompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



В следующем примере используется макрос [**иккомпресскуери**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) , чтобы определить, может ли программа сжатия работать с входными и выходными форматами.


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// Both *lpbiIn and *lpbiOut must be initialized to the respective
// formats.
 

if (ICCompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
 
    // Format is supported; use the compressor. 
 
}
 
 
```



В следующем примере используется макрос [**иккомпрессжетсизе**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) для определения размера буфера и выделяется буфер этого размера с помощью [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).


```C++
// Find the worst-case buffer size. 
dwCompressBufferSize = ICCompressGetSize(hIC, lpbiIn, lpbiOut); 
 
// Allocate a buffer and get lpOutput to point to it. 
h = GlobalAlloc(GHND, dwCompressBufferSize); 
lpOutput = (LPVOID)GlobalLock(h);
 
 
```



 

 