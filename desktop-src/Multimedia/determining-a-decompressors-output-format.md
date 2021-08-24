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
ms.openlocfilehash: 9cc17db0d7aa015c955825840fb70d12714be3c0a44a69bf5abc59290ebc633c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497424"
---
# <a name="determining-a-decompressors-output-format"></a>Определение формата вывода декомпрессора

В следующем примере определяется размер буфера, необходимый для данных, указывающих формат распаковки, с помощью макроса [**икдекомпрессжетформатсизе**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) , выделяется буфер соответствующего размера с помощью функции [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) и извлекаются сведения о формате распаковки с помощью макроса [**икдекомпрессжетформат**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



В следующем примере показано, как приложение может использовать макрос [**икдекомпресскуери**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) , чтобы определить, может ли декомпрессор работать с форматами входных и выходных данных.


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



В следующем фрагменте кода показано, как получить сведения о палитре с помощью макроса [**икдекомпрессжетпалетте**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 