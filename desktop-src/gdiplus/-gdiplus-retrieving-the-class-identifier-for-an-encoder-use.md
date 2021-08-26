---
description: Функция Жетенкодерклсид в следующем примере получает тип MIME кодировщика и возвращает идентификатор класса (CLSID) этого кодировщика.
ms.assetid: f78dac7c-4bc1-4614-8a26-d99d5619399a
title: Получение идентификатора класса для кодировщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a40c31c7ad997ed3e7525ff247019f6a41c681b9523dc523105bd5ba6c7ca6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014714"
---
# <a name="retrieving-the-class-identifier-for-an-encoder"></a>Получение идентификатора класса для кодировщика

Функция Жетенкодерклсид в следующем примере получает тип MIME кодировщика и возвращает идентификатор класса (**CLSID**) этого кодировщика. типы MIME кодировщиков, встроенных в Windows GDI+, выглядят следующим образом:

-   image/bmp
-   image/jpeg
-   image/gif
-   image/tiff
-   image/png

Функция вызывает [**жетимажеенкодерс**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) для получения массива объектов [**имажекодеЦинфо**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) . Если один из объектов **имажекодеЦинфо** в этом массиве представляет запрошенный кодировщик, функция возвращает индекс объекта **ИмажекодеЦинфо** и копирует **CLSID** в переменную, на которую указывает **пклсид**. Если функция завершается с ошибкой, возвращается значение – 1.


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



Следующее консольное приложение вызывает функцию Жетенкодерклсид для определения **идентификатора CLSID** кодировщика PNG:


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



При запуске предыдущего консольного приложения вы получаете выходные данные, аналогичные приведенным ниже.


```
An ImageCodecInfo object representing the PNG encoder
was found at position 4 in the array.
The CLSID of the PNG encoder is {557CF406-1A04-11D3-9A73-0000F81EF32E}.
```



 

 
