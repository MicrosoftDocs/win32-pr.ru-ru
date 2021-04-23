---
title: Преобразование JPEG-изображения без потерь
description: При сжатии изображения JPEG некоторые сведения в нем теряются.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ea7011f25a97a228c44bdb87ba09ca8b284ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984432"
---
# <a name="lossless-transform-of-a-jpeg-image"></a><span data-ttu-id="d7f78-103">Преобразование JPEG-изображения без потерь</span><span class="sxs-lookup"><span data-stu-id="d7f78-103">Lossless transform of a JPEG image</span></span>

<span data-ttu-id="d7f78-104">При сжатии изображения JPEG некоторые сведения в нем теряются.</span><span class="sxs-lookup"><span data-stu-id="d7f78-104">When you compress a JPEG image, some of the information in the image is lost.</span></span> <span data-ttu-id="d7f78-105">Если открыть файл JPEG, изменить изображение и сохранить его в другом JPEG-файле, качество будет уменьшено.</span><span class="sxs-lookup"><span data-stu-id="d7f78-105">If you open a JPEG file, alter the image, and save it to another JPEG file, the quality will decrease.</span></span> <span data-ttu-id="d7f78-106">Если повторить этот процесс много раз, вы увидите значительное снижение качества изображения.</span><span class="sxs-lookup"><span data-stu-id="d7f78-106">If you repeat that process many times, you will see a substantial degradation in the image quality.</span></span>

<span data-ttu-id="d7f78-107">Так как JPEG является одним из наиболее популярных форматов изображений в Интернете, и, так как пользователям часто приходится изменять изображения JPEG, GDI+ предоставляет следующие преобразования, которые можно выполнять с изображениями в формате JPEG без потери информации:</span><span class="sxs-lookup"><span data-stu-id="d7f78-107">Because JPEG is one of the most popular image formats on the Web, and because people often like to modify JPEG images, GDI+ provides the following transformations that can be performed on JPEG images without loss of information:</span></span>

-   <span data-ttu-id="d7f78-108">Поворот на 90 градусов</span><span class="sxs-lookup"><span data-stu-id="d7f78-108">Rotate 90 degrees</span></span>
-   <span data-ttu-id="d7f78-109">Поворот на 180 градусов</span><span class="sxs-lookup"><span data-stu-id="d7f78-109">Rotate 180 degrees</span></span>
-   <span data-ttu-id="d7f78-110">Поворот на 270 градусов</span><span class="sxs-lookup"><span data-stu-id="d7f78-110">Rotate 270 degrees</span></span>
-   <span data-ttu-id="d7f78-111">Отразить по горизонтали</span><span class="sxs-lookup"><span data-stu-id="d7f78-111">Flip horizontally</span></span>
-   <span data-ttu-id="d7f78-112">Отразить по вертикали</span><span class="sxs-lookup"><span data-stu-id="d7f78-112">Flip vertically</span></span>

<span data-ttu-id="d7f78-113">При вызове метода [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) объекта [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) можно применить один из преобразований, показанных в приведенном выше списке.</span><span class="sxs-lookup"><span data-stu-id="d7f78-113">You can apply one of the transformations shown in the preceding list when you call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="d7f78-114">Если выполняются следующие условия, преобразование будет продолжено без потери информации:</span><span class="sxs-lookup"><span data-stu-id="d7f78-114">If the following conditions are met, then the transformation will proceed without loss of information:</span></span>

-   <span data-ttu-id="d7f78-115">Файл, используемый для создания объекта [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) , — это JPEG-файл.</span><span class="sxs-lookup"><span data-stu-id="d7f78-115">The file used to construct the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object is a JPEG file.</span></span>
-   <span data-ttu-id="d7f78-116">Ширина и высота изображения являются кратными 16.</span><span class="sxs-lookup"><span data-stu-id="d7f78-116">The width and height of the image are both multiples of 16.</span></span>

<span data-ttu-id="d7f78-117">Если ширина и высота изображения не кратны 16, то GDI+ будет лучше сохранять качество изображения при применении одного из поворотов или преобразований, показанных в приведенном выше списке.</span><span class="sxs-lookup"><span data-stu-id="d7f78-117">If the width and height of the image are not both multiples of 16, GDI+ will do its best to preserve the image quality when you apply one of the rotation or flipping transformations shown in the preceding list.</span></span>

<span data-ttu-id="d7f78-118">Чтобы преобразовать изображение JPEG, инициализируйте объект [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) и передайте адрес этого объекта методу [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) класса [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="d7f78-118">To transform a JPEG image, initialize an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object and pass the address of that object to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="d7f78-119">Инициализируйте объект **EncoderParameters** , чтобы он был массивом, состоящим из одного объекта [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="d7f78-119">Initialize the **EncoderParameters** object so that it has an array that consists of one [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="d7f78-120">Инициализируйте этот один объект **EncoderParameter** , чтобы его **значение** -член указывало на переменную **ulong** , содержащую один из следующих элементов перечисления [**енкодервалуе**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :</span><span class="sxs-lookup"><span data-stu-id="d7f78-120">Initialize that one **EncoderParameter** object so that its **Value** member points to a **ULONG** variable that holds one of the following elements of the [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>

-   <span data-ttu-id="d7f78-121">EncoderValueTransformRotate90,</span><span class="sxs-lookup"><span data-stu-id="d7f78-121">EncoderValueTransformRotate90,</span></span>
-   <span data-ttu-id="d7f78-122">EncoderValueTransformRotate180,</span><span class="sxs-lookup"><span data-stu-id="d7f78-122">EncoderValueTransformRotate180,</span></span>
-   <span data-ttu-id="d7f78-123">EncoderValueTransformRotate270,</span><span class="sxs-lookup"><span data-stu-id="d7f78-123">EncoderValueTransformRotate270,</span></span>
-   <span data-ttu-id="d7f78-124">Енкодервалуетрансформфлифоризонтал,</span><span class="sxs-lookup"><span data-stu-id="d7f78-124">EncoderValueTransformFlipHorizontal,</span></span>
-   <span data-ttu-id="d7f78-125">енкодервалуетрансформфлипвертикал</span><span class="sxs-lookup"><span data-stu-id="d7f78-125">EncoderValueTransformFlipVertical</span></span>

<span data-ttu-id="d7f78-126">Задайте для элемента **GUID** объекта [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) значение енкодертрансформатион.</span><span class="sxs-lookup"><span data-stu-id="d7f78-126">Set the **Guid** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object to EncoderTransformation.</span></span>

<span data-ttu-id="d7f78-127">Следующее консольное приложение создает объект [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) из файла JPEG, а затем сохраняет его в новый файл.</span><span class="sxs-lookup"><span data-stu-id="d7f78-127">The following console application creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then saves the image to a new file.</span></span> <span data-ttu-id="d7f78-128">Во время процесса сохранения изображение поворачивается на 90 градусов.</span><span class="sxs-lookup"><span data-stu-id="d7f78-128">During the save process, the image is rotated 90 degrees.</span></span> <span data-ttu-id="d7f78-129">Если ширина и высота изображения являются кратными 16, процесс поворота и сохранения изображения не приводит к утрате информации.</span><span class="sxs-lookup"><span data-stu-id="d7f78-129">If the width and height of the image are both multiples of 16, the process of rotating and saving the image causes no loss of information.</span></span>

<span data-ttu-id="d7f78-130">Функция Main зависит от вспомогательной функции Жетенкодерклсид, которая показана в статье [Получение идентификатора класса для кодировщика](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="d7f78-130">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
