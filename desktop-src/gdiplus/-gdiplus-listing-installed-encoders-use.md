---
description: Интерфейс GDI+ предоставляет функцию Жетимажеенкодерс, позволяющую определить, какие кодировщики изображений доступны на компьютере.
ms.assetid: a261cf61-b853-4208-984b-0d5040eb1667
title: Список установленных кодировщиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f310e9d366cdacde019373724f2b9feb3b94aef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985156"
---
# <a name="listing-installed-encoders"></a><span data-ttu-id="b2bd0-103">Список установленных кодировщиков</span><span class="sxs-lookup"><span data-stu-id="b2bd0-103">Listing Installed Encoders</span></span>

<span data-ttu-id="b2bd0-104">Интерфейс GDI+ предоставляет функцию [**жетимажеенкодерс**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) , позволяющую определить, какие кодировщики изображений доступны на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b2bd0-104">GDI+ provides the [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) function so that you can determine which image encoders are available on your computer.</span></span> <span data-ttu-id="b2bd0-105">**Жетимажеенкодерс** возвращает массив объектов [**имажекодеЦинфо**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="b2bd0-105">**GetImageEncoders** returns an array of [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) objects.</span></span> <span data-ttu-id="b2bd0-106">Перед вызовом **жетимажеенкодерс** необходимо выделить буфер, достаточно большой для получения этого массива.</span><span class="sxs-lookup"><span data-stu-id="b2bd0-106">Before you call **GetImageEncoders**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="b2bd0-107">Чтобы определить размер требуемого буфера, можно вызвать [**жетимажеенкодерссизе**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize) .</span><span class="sxs-lookup"><span data-stu-id="b2bd0-107">You can call [**GetImageEncodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="b2bd0-108">В следующем консольном приложении перечислены доступные кодировщики изображений:</span><span class="sxs-lookup"><span data-stu-id="b2bd0-108">The following console application lists the available image encoders:</span></span>


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



<span data-ttu-id="b2bd0-109">При запуске предыдущего консольного приложения выходные данные будут выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b2bd0-109">When you run the preceding console application, the output will be similar to the following:</span></span>


```
image/bmp
image/jpeg
image/gif
image/tiff
image/png
```



 

 
