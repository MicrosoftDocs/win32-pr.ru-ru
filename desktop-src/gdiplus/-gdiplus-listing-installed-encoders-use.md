---
description: GDI+ предоставляет функцию жетимажеенкодерс, позволяющую определить, какие кодировщики изображений доступны на компьютере.
ms.assetid: a261cf61-b853-4208-984b-0d5040eb1667
title: Список установленных кодировщиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072b18d226d2ad09bc79cb1d1599ea5c0c62fa695a7aae2ff5969e27031e37b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066885"
---
# <a name="listing-installed-encoders"></a>Список установленных кодировщиков

GDI+ предоставляет функцию [**жетимажеенкодерс**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) , позволяющую определить, какие кодировщики изображений доступны на компьютере. **Жетимажеенкодерс** возвращает массив объектов [**имажекодеЦинфо**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) . Перед вызовом **жетимажеенкодерс** необходимо выделить буфер, достаточно большой для получения этого массива. Чтобы определить размер требуемого буфера, можно вызвать [**жетимажеенкодерссизе**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize) .

В следующем консольном приложении перечислены доступные кодировщики изображений:


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  num;        // number of image encoders
   UINT  size;       // size, in bytes, of the image encoder array

   ImageCodecInfo* pImageCodecInfo;

   // How many encoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageEncodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageEncoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageEncoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfo, is a pointer to that buffer. 
   GetImageEncoders(num, size, pImageCodecInfo);

   // Display the graphics file format (MimeType)
   // for each ImageCodecInfo object.
   for(UINT j = 0; j < num; ++j)
   { 
      wprintf(L"%s\n", pImageCodecInfo[j].MimeType);   
   }

   free(pImageCodecInfo);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



При запуске предыдущего консольного приложения выходные данные будут выглядеть следующим образом:


```
image/bmp
image/jpeg
image/gif
image/tiff
image/png
```



 

 
