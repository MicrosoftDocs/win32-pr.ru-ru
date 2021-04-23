---
description: Функция Жетенкодерклсид в следующем примере получает тип MIME кодировщика и возвращает идентификатор класса (CLSID) этого кодировщика.
ms.assetid: f78dac7c-4bc1-4614-8a26-d99d5619399a
title: Получение идентификатора класса для кодировщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03193bfa9f2e86e92f66a649280828f12d4807c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985133"
---
# <a name="retrieving-the-class-identifier-for-an-encoder"></a><span data-ttu-id="a07f9-103">Получение идентификатора класса для кодировщика</span><span class="sxs-lookup"><span data-stu-id="a07f9-103">Retrieving the Class Identifier for an Encoder</span></span>

<span data-ttu-id="a07f9-104">Функция Жетенкодерклсид в следующем примере получает тип MIME кодировщика и возвращает идентификатор класса (**CLSID**) этого кодировщика.</span><span class="sxs-lookup"><span data-stu-id="a07f9-104">The function GetEncoderClsid in the following example receives the MIME type of an encoder and returns the class identifier (**CLSID**) of that encoder.</span></span> <span data-ttu-id="a07f9-105">Ниже приведены типы MIME кодировщиков, встроенных в Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="a07f9-105">The MIME types of the encoders built into Windows GDI+ are as follows:</span></span>

-   <span data-ttu-id="a07f9-106">image/bmp</span><span class="sxs-lookup"><span data-stu-id="a07f9-106">image/bmp</span></span>
-   <span data-ttu-id="a07f9-107">image/jpeg</span><span class="sxs-lookup"><span data-stu-id="a07f9-107">image/jpeg</span></span>
-   <span data-ttu-id="a07f9-108">image/gif</span><span class="sxs-lookup"><span data-stu-id="a07f9-108">image/gif</span></span>
-   <span data-ttu-id="a07f9-109">image/tiff</span><span class="sxs-lookup"><span data-stu-id="a07f9-109">image/tiff</span></span>
-   <span data-ttu-id="a07f9-110">image/png</span><span class="sxs-lookup"><span data-stu-id="a07f9-110">image/png</span></span>

<span data-ttu-id="a07f9-111">Функция вызывает [**жетимажеенкодерс**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) для получения массива объектов [**имажекодеЦинфо**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="a07f9-111">The function calls [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) to get an array of [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) objects.</span></span> <span data-ttu-id="a07f9-112">Если один из объектов **имажекодеЦинфо** в этом массиве представляет запрошенный кодировщик, функция возвращает индекс объекта **ИмажекодеЦинфо** и копирует **CLSID** в переменную, на которую указывает **пклсид**.</span><span class="sxs-lookup"><span data-stu-id="a07f9-112">If one of the **ImageCodecInfo** objects in that array represents the requested encoder, the function returns the index of the **ImageCodecInfo** object and copies the **CLSID** into the variable pointed to by **pClsid**.</span></span> <span data-ttu-id="a07f9-113">Если функция завершается с ошибкой, возвращается значение – 1.</span><span class="sxs-lookup"><span data-stu-id="a07f9-113">If the function fails, it returns –1.</span></span>


```
int GetEncoderClsid(const WCHAR* format, CLSID* pClsid)
{
   UINT  num = 0;          // number of image encoders
   UINT  size = 0;         // size of the image encoder array in bytes

   ImageCodecInfo* pImageCodecInfo = NULL;

   GetImageEncodersSize(&num, &size);
   if(size == 0)
      return -1;  // Failure

   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));
   if(pImageCodecInfo == NULL)
      return -1;  // Failure

   GetImageEncoders(num, size, pImageCodecInfo);

   for(UINT j = 0; j < num; ++j)
   {
      if( wcscmp(pImageCodecInfo[j].MimeType, format) == 0 )
      {
         *pClsid = pImageCodecInfo[j].Clsid;
         free(pImageCodecInfo);
         return j;  // Success
      }    
   }

   free(pImageCodecInfo);
   return -1;  // Failure
}
```



<span data-ttu-id="a07f9-114">Следующее консольное приложение вызывает функцию Жетенкодерклсид для определения **идентификатора CLSID** кодировщика PNG:</span><span class="sxs-lookup"><span data-stu-id="a07f9-114">The following console application calls the GetEncoderClsid function to determine the **CLSID** of the PNG encoder:</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

#include "GdiplusHelperFunctions.h"

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID  encoderClsid;
   INT    result;
   WCHAR  strGuid[39];

   result = GetEncoderClsid(L"image/png", &encoderClsid);

   if(result < 0)
   {
      printf("The PNG encoder is not installed.\n");
   }
   else
   {
      StringFromGUID2(encoderClsid, strGuid, 39);
      printf("An ImageCodecInfo object representing the PNG encoder\n");
      printf("was found at position %d in the array.\n", result);
      wprintf(L"The CLSID of the PNG encoder is %s.\n", strGuid);
   }

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="a07f9-115">При запуске предыдущего консольного приложения вы получаете выходные данные, аналогичные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="a07f9-115">When you run the preceding console application, you get an output similar to the following:</span></span>


```
An ImageCodecInfo object representing the PNG encoder
was found at position 4 in the array.
The CLSID of the PNG encoder is {557CF406-1A04-11D3-9A73-0000F81EF32E}.
```



 

 
