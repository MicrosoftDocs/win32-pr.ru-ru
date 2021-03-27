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
# <a name="creating-and-saving-a-multiple-frame-image"></a><span data-ttu-id="f2791-103">Создание и сохранение многокадрового изображения</span><span class="sxs-lookup"><span data-stu-id="f2791-103">Creating and Saving a Multiple-Frame Image</span></span>

<span data-ttu-id="f2791-104">В некоторых форматах файлов можно сохранить несколько изображений (кадров) в одном файле.</span><span class="sxs-lookup"><span data-stu-id="f2791-104">With certain file formats, you can save multiple images (frames) to a single file.</span></span> <span data-ttu-id="f2791-105">Например, можно сохранить несколько страниц в одном TIFF-файле.</span><span class="sxs-lookup"><span data-stu-id="f2791-105">For example, you can save several pages to a single TIFF file.</span></span> <span data-ttu-id="f2791-106">Чтобы сохранить первую страницу, вызовите метод [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) класса [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="f2791-106">To save the first page, call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="f2791-107">Чтобы сохранить последующие страницы, вызовите метод [савеадд](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) класса **Image** .</span><span class="sxs-lookup"><span data-stu-id="f2791-107">To save subsequent pages, call the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **Image** class.</span></span>

> [!Note]  
> <span data-ttu-id="f2791-108">[Савеадд](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) нельзя использовать для добавления кадров в анимированный GIF-файл.</span><span class="sxs-lookup"><span data-stu-id="f2791-108">You cannot use [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) to add frames to an animated gif file.</span></span>

 

<span data-ttu-id="f2791-109">Следующее консольное приложение создает TIFF-файл с четырьмя страницами.</span><span class="sxs-lookup"><span data-stu-id="f2791-109">The following console application creates a TIFF file with four pages.</span></span> <span data-ttu-id="f2791-110">Изображения, которые становятся страницами TIFF-файла, берутся из четырех дисковых файлов: Shapes.bmp, Cereal.gif, Iron.jpg и House.png.</span><span class="sxs-lookup"><span data-stu-id="f2791-110">The images that become the pages of the TIFF file come from four disk files: Shapes.bmp, Cereal.gif, Iron.jpg, and House.png.</span></span> <span data-ttu-id="f2791-111">Код сначала формирует четыре объекта [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) : **Multi**, **Page2**, **Page3** и **Page4**.</span><span class="sxs-lookup"><span data-stu-id="f2791-111">The code first constructs four [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects: **multi**, **page2**, **page3**, and **page4**.</span></span> <span data-ttu-id="f2791-112">Сначала **Multi** содержит только изображение из Shapes.bmp, но в конечном итоге содержит все четыре изображения.</span><span class="sxs-lookup"><span data-stu-id="f2791-112">At first, **multi** contains only the image from Shapes.bmp, but eventually it contains all four images.</span></span> <span data-ttu-id="f2791-113">Когда отдельные страницы добавляются в объект с **несколькими**  **изображениями** , они также добавляются в файл на диске в формате Multi. tif.</span><span class="sxs-lookup"><span data-stu-id="f2791-113">As the individual pages are added to the **multi**  **Image** object, they are also added to the disk file Multiframe.tif.</span></span>

<span data-ttu-id="f2791-114">Обратите внимание, что код вызывает метод [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (не [савеадд](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) для сохранения первой страницы.</span><span class="sxs-lookup"><span data-stu-id="f2791-114">Note that the code calls [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (not [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) to save the first page.</span></span> <span data-ttu-id="f2791-115">Первым аргументом, передаваемым методу Save, является имя дискового файла, который в конечном итоге будет содержать несколько кадров.</span><span class="sxs-lookup"><span data-stu-id="f2791-115">The first argument passed to the Save method is the name of the disk file that will eventually contain several frames.</span></span> <span data-ttu-id="f2791-116">Второй аргумент, передаваемый методу Save, указывает кодировщик, который будет использоваться для преобразования данных в объекте с **несколькими**  [**изображениями**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) в формат (в данном случае это TIFF), необходимый для файла на диске.</span><span class="sxs-lookup"><span data-stu-id="f2791-116">The second argument passed to the Save method specifies the encoder that will be used to convert the data in the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object to the format (in this case TIFF) required by the disk file.</span></span> <span data-ttu-id="f2791-117">Тот же кодировщик используется автоматически всеми последовательными вызовами метода Савеадд объекта **Image** .  </span><span class="sxs-lookup"><span data-stu-id="f2791-117">That same encoder is used automatically by all subsequent calls to the SaveAdd method of the **multi**  **Image** object.</span></span>

<span data-ttu-id="f2791-118">Третьим аргументом, передаваемым методу [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) , является адрес объекта [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) .</span><span class="sxs-lookup"><span data-stu-id="f2791-118">The third argument passed to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method is the address of an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object.</span></span> <span data-ttu-id="f2791-119">Объект **EncoderParameters** содержит массив, содержащий один объект [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="f2791-119">The **EncoderParameters** object has an array that contains a single [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="f2791-120">Члену **GUID** этого объекта **EncoderParameter** присваивается значение енкодерсавефлаг.</span><span class="sxs-lookup"><span data-stu-id="f2791-120">The **Guid** member of that **EncoderParameter** object is set to EncoderSaveFlag.</span></span> <span data-ttu-id="f2791-121">Элемент **value** объекта **EncoderParameter** указывает на **ulong** , которая содержит значение енкодервалуемултифраме.</span><span class="sxs-lookup"><span data-stu-id="f2791-121">The **Value** member of the **EncoderParameter** object points to a **ULONG** that contains the value EncoderValueMultiFrame.</span></span>

<span data-ttu-id="f2791-122">Код сохраняет вторую, третью и четвертую страницы, вызывая метод [савеадд](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) объекта **Multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="f2791-122">The code saves the second, third, and fourth pages by calling the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="f2791-123">Первым аргументом, передаваемым в метод Савеадд, является адрес объекта **Image** .</span><span class="sxs-lookup"><span data-stu-id="f2791-123">The first argument passed to the SaveAdd method is the address of an **Image** object.</span></span> <span data-ttu-id="f2791-124">Изображение в этом объекте **изображения** добавляется к объекту с **несколькими**  **изображениями** и добавляется в файл на диске с расширением. tif.</span><span class="sxs-lookup"><span data-stu-id="f2791-124">The image in that **Image** object is added to the **multi**  **Image** object and is also added to the Multiframe.tif disk file.</span></span> <span data-ttu-id="f2791-125">Вторым аргументом, передаваемым методу Савеадд, является адрес того же объекта [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) , который использовался методом [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) .</span><span class="sxs-lookup"><span data-stu-id="f2791-125">The second argument passed to the SaveAdd method is the address of the same [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that was used by the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method.</span></span> <span data-ttu-id="f2791-126">Разница заключается в том, что **ulong** , на которую указывает элемент **value** , теперь содержит значение енкодервалуефрамедименсионпаже.</span><span class="sxs-lookup"><span data-stu-id="f2791-126">The difference is that the **ULONG** pointed to by the **Value** member now contains the value EncoderValueFrameDimensionPage.</span></span>

<span data-ttu-id="f2791-127">Функция Main зависит от вспомогательной функции Жетенкодерклсид, которая показана в статье [Получение идентификатора класса для кодировщика](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="f2791-127">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
