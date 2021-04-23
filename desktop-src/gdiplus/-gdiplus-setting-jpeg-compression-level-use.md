---
description: Чтобы указать уровень сжатия при сохранении изображения JPEG, инициализируйте объект EncoderParameters и передайте адрес этого объекта методу Save класса Image.
ms.assetid: b8365c00-2223-4aff-9fb2-422976af4c31
title: Задание уровня сжатия JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07d2e82dfb21e121609d5e09e5c31e2242ec652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809629"
---
# <a name="setting-jpeg-compression-level"></a><span data-ttu-id="ea0c3-103">Задание уровня сжатия JPEG</span><span class="sxs-lookup"><span data-stu-id="ea0c3-103">Setting JPEG Compression Level</span></span>

<span data-ttu-id="ea0c3-104">Чтобы указать уровень сжатия при сохранении изображения JPEG, инициализируйте объект [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) и передайте адрес этого объекта методу [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) класса [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="ea0c3-104">To specify the compression level when you save a JPEG image, initialize an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object and pass the address of that object to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="ea0c3-105">Инициализируйте объект **EncoderParameters** , чтобы он был массивом, состоящим из одного объекта [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="ea0c3-105">Initialize the **EncoderParameters** object so that it has an array consisting of one [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="ea0c3-106">Инициализируйте этот один объект **EncoderParameter** , чтобы его **значение** указывало на значение **ulong** от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-106">Initialize that one **EncoderParameter** object so that its **Value** member points to a **ULONG** value from 0 through 100.</span></span> <span data-ttu-id="ea0c3-107">Задайте для элемента **GUID** объекта **EncoderParameter** значение енкодеркуалити.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-107">Set the **Guid** member of the **EncoderParameter** object to EncoderQuality.</span></span>

<span data-ttu-id="ea0c3-108">Следующее консольное приложение сохраняет три изображения JPEG, каждое из которых имеет разный уровень качества.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-108">The following console application saves three JPEG images, each with a different quality level.</span></span> <span data-ttu-id="ea0c3-109">Уровень качества 0 соответствует максимальному сжатию, а уровень качества 100 — минимальному сжатию.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-109">A quality level of 0 corresponds to the greatest compression, and a quality level of 100 corresponds to the least compression.</span></span>

<span data-ttu-id="ea0c3-110">Функция Main зависит от вспомогательной функции Жетенкодерклсид, которая показана в статье [Получение идентификатора класса для кодировщика](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md):</span><span class="sxs-lookup"><span data-stu-id="ea0c3-110">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md):</span></span>


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
   ULONG             quality;
   Status            stat;

   // Get an image from the disk.
   Image* image = new Image(L"Shapes.bmp");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will let this value vary from 0 to 100.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderQuality;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Save the image as a JPEG with quality level 0.
   quality = 0;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes001.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes001.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes001.jpg");

   // Save the image as a JPEG with quality level 50.
   quality = 50;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes050.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes050.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes050.jpg");

      // Save the image as a JPEG with quality level 100.
   quality = 100;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes100.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes100.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes100.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
