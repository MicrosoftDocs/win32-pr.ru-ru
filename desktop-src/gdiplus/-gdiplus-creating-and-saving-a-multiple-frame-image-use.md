---
description: В некоторых форматах файлов можно сохранить несколько изображений (кадров) в одном файле.
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: Создание и сохранение многокадрового изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532a8fc8f8fc7e8742651f3d3853e001d493609b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156202"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a>Создание и сохранение многокадрового изображения

В некоторых форматах файлов можно сохранить несколько изображений (кадров) в одном файле. Например, можно сохранить несколько страниц в одном TIFF-файле. Чтобы сохранить первую страницу, вызовите метод [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) класса [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Чтобы сохранить последующие страницы, вызовите метод [савеадд](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) класса **Image** .

> [!Note]  
> [Савеадд](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) нельзя использовать для добавления кадров в анимированный GIF-файл.

 

Следующее консольное приложение создает TIFF-файл с четырьмя страницами. Изображения, которые становятся страницами TIFF-файла, берутся из четырех дисковых файлов: Shapes.bmp, Cereal.gif, Iron.jpg и House.png. Код сначала формирует четыре объекта [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) : **Multi**, **Page2**, **Page3** и **Page4**. Сначала **Multi** содержит только изображение из Shapes.bmp, но в конечном итоге содержит все четыре изображения. Когда отдельные страницы добавляются в объект с **несколькими**  **изображениями** , они также добавляются в файл на диске в формате Multi. tif.

Обратите внимание, что код вызывает метод [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (не [савеадд](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) для сохранения первой страницы. Первым аргументом, передаваемым методу Save, является имя дискового файла, который в конечном итоге будет содержать несколько кадров. Второй аргумент, передаваемый методу Save, указывает кодировщик, который будет использоваться для преобразования данных в объекте с **несколькими**  [**изображениями**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) в формат (в данном случае это TIFF), необходимый для файла на диске. Тот же кодировщик используется автоматически всеми последовательными вызовами метода Савеадд объекта **Image** .  

Третьим аргументом, передаваемым методу [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) , является адрес объекта [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) . Объект **EncoderParameters** содержит массив, содержащий один объект [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Члену **GUID** этого объекта **EncoderParameter** присваивается значение енкодерсавефлаг. Элемент **value** объекта **EncoderParameter** указывает на **ulong** , которая содержит значение енкодервалуемултифраме.

Код сохраняет вторую, третью и четвертую страницы, вызывая метод [савеадд](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) объекта **Multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Первым аргументом, передаваемым в метод Савеадд, является адрес объекта **Image** . Изображение в этом объекте **изображения** добавляется к объекту с **несколькими**  **изображениями** и добавляется в файл на диске с расширением. tif. Вторым аргументом, передаваемым методу Савеадд, является адрес того же объекта [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) , который использовался методом [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) . Разница заключается в том, что **ulong** , на которую указывает элемент **value** , теперь содержит значение енкодервалуефрамедименсионпаже.

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

   EncoderParameters encoderParameters;
   ULONG             parameterValue;
   Status            stat;

   // An EncoderParameters object has an array of
   // EncoderParameter objects. In this case, there is only
   // one EncoderParameter object in the array.
   encoderParameters.Count = 1;

   // Initialize the one EncoderParameter object.
   encoderParameters.Parameter[0].Guid = EncoderSaveFlag;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;
   encoderParameters.Parameter[0].Value = &parameterValue;

   // Get the CLSID of the TIFF encoder.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/tiff", &encoderClsid);

   // Create four image objects.
   Image* multi = new Image(L"Shapes.bmp");
   Image* page2 = new Image(L"Cereal.gif");
   Image* page3 = new Image(L"Iron.jpg");
   Image* page4 = new Image(L"House.png");

   // Save the first page (frame).
   parameterValue = EncoderValueMultiFrame;
   stat = multi->Save(L"MultiFrame.tif", &encoderClsid, &encoderParameters);
   if(stat == Ok)
      printf("Page 1 saved successfully.\n");

   // Save the second page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page2, &encoderParameters);
   if(stat == Ok)
      printf("Page 2 saved successfully.\n");

   // Save the third page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page3, &encoderParameters);
   if(stat == Ok)
      printf("Page 3 saved successfully.\n");

   // Save the fourth page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page4, &encoderParameters);
   if(stat == Ok)
      printf("Page 4 saved successfully.\n");

   // Close the multiframe file.
   parameterValue = EncoderValueFlush;
   stat = multi->SaveAdd(&encoderParameters);
   if(stat == Ok)
      printf("File closed successfully.\n");

   delete multi;
   delete page2;
   delete page3;
   delete page4;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
