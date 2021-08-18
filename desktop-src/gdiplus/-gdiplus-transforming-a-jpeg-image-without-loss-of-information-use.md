---
title: Преобразование JPEG-изображения без потерь
description: При сжатии изображения JPEG некоторые сведения в нем теряются.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67152084f95220db3fe7afecfa4be07b366a92b31eb713ec192a2805ecb42ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977294"
---
# <a name="lossless-transform-of-a-jpeg-image"></a>Преобразование JPEG-изображения без потерь

При сжатии изображения JPEG некоторые сведения в нем теряются. Если открыть файл JPEG, изменить изображение и сохранить его в другом JPEG-файле, качество будет уменьшено. Если повторить этот процесс много раз, вы увидите значительное снижение качества изображения.

так как jpeg является одним из наиболее популярных форматов изображений в интернете, и, так как пользователям часто приходится изменять изображения jpeg, GDI+ предоставляет следующие преобразования, которые можно выполнять с изображениями в формате jpeg без потери информации:

-   Повернуть на 90 градусов
-   Поворот на 180 градусов
-   Поворот на 270 градусов
-   Отразить по горизонтали
-   Отразить по вертикали

При вызове метода [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) объекта [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) можно применить один из преобразований, показанных в приведенном выше списке. Если выполняются следующие условия, преобразование будет продолжено без потери информации:

-   Файл, используемый для создания объекта [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) , — это JPEG-файл.
-   Ширина и высота изображения являются кратными 16.

если ширина и высота изображения не кратны 16, GDI+ будет лучше сохранить качество изображения при применении одного из поворотов или преобразований, показанных в приведенном выше списке.

Чтобы преобразовать изображение JPEG, инициализируйте объект [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) и передайте адрес этого объекта методу [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) класса [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Инициализируйте объект **EncoderParameters** , чтобы он был массивом, состоящим из одного объекта [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Инициализируйте этот один объект **EncoderParameter** , чтобы его **значение** -член указывало на переменную **ulong** , содержащую один из следующих элементов перечисления [**енкодервалуе**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :

-   EncoderValueTransformRotate90,
-   EncoderValueTransformRotate180,
-   EncoderValueTransformRotate270,
-   Енкодервалуетрансформфлифоризонтал,
-   енкодервалуетрансформфлипвертикал

Задайте для элемента **GUID** объекта [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) значение енкодертрансформатион.

Следующее консольное приложение создает объект [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) из файла JPEG, а затем сохраняет его в новый файл. Во время процесса сохранения изображение поворачивается на 90 градусов. Если ширина и высота изображения являются кратными 16, процесс поворота и сохранения изображения не приводит к утрате информации.

Функция Main зависит от вспомогательной функции Жетенкодерклсид, которая показана в статье [Получение идентификатора класса для кодировщика](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID             encoderClsid;
   EncoderParameters encoderParameters;
   ULONG             transformation;
   UINT              width;
   UINT              height;
   Status            stat;

   // Get a JPEG image from the disk.
   Image* image = new Image(L"Shapes.jpg");

   // Determine whether the width and height of the image 
   // are multiples of 16.
   width = image->GetWidth();
   height = image->GetHeight();

   printf("The width of the image is %u", width);
   if(width / 16.0 - width / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   printf("The height of the image is %u", height);
   if(height / 16.0 - height / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will set that value to EncoderValueTransformRotate90.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderTransformation;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Rotate and save the image.
   transformation = EncoderValueTransformRotate90;
   encoderParameters.Parameter[0].Value = &transformation;
   stat = image->Save(L"ShapesR90.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"ShapesR90.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"ShapesR90.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
