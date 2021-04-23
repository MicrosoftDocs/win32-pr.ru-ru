---
description: Класс Image можно использовать для загрузки и вывода растровых изображений (точечных рисунков) и векторных изображений (метафайлов).
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: Отрисовка, позиционирование и клонирование изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa265a8f75cbfcaf0ff614ded4466482e5b986b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264066"
---
# <a name="drawing-positioning-and-cloning-images"></a><span data-ttu-id="e8837-103">Отрисовка, позиционирование и клонирование изображений</span><span class="sxs-lookup"><span data-stu-id="e8837-103">Drawing, Positioning, and Cloning Images</span></span>

<span data-ttu-id="e8837-104">Класс [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) можно использовать для загрузки и вывода растровых изображений (точечных рисунков) и векторных изображений (метафайлов).</span><span class="sxs-lookup"><span data-stu-id="e8837-104">You can use the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class to load and display raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="e8837-105">Для вывода изображения требуется [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и объект **изображения** .</span><span class="sxs-lookup"><span data-stu-id="e8837-105">To display an image, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and an **Image** object.</span></span> <span data-ttu-id="e8837-106">Объект **Graphics** предоставляет метод [**Graphics::D равимаже**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) , который получает адрес объекта **изображения** в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="e8837-106">The **Graphics** object provides the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method, which receives the address of the **Image** object as an argument.</span></span>

<span data-ttu-id="e8837-107">В следующем примере объект [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла Climber.jpg а затем отображается изображение.</span><span class="sxs-lookup"><span data-stu-id="e8837-107">The following example constructs an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Climber.jpg and then displays the image.</span></span> <span data-ttu-id="e8837-108">Конечная точка для верхнего левого угла изображения (10, 10) задается во втором и третьем параметрах метода [**Graphics::D равимаже**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="e8837-108">The destination point for the upper-left corner of the image, (10, 10), is specified in the second and third parameters of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method.</span></span>


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



<span data-ttu-id="e8837-109">Приведенный выше код, а также определенный файл Climber.jpg, выдают следующие выходные данные.</span><span class="sxs-lookup"><span data-stu-id="e8837-109">The preceding code, along with a particular file, Climber.jpg, produced the following output.</span></span>

![снимок экрана окна, содержащего фотографию](images/aboutgdip03-art04.png)

<span data-ttu-id="e8837-111">Объекты [**изображений**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) можно создавать из различных форматов графических файлов: BMP, GIF, JPEG, EXIF, PNG, TIFF, WMF, EMF и Icon.</span><span class="sxs-lookup"><span data-stu-id="e8837-111">You can construct [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of graphics file formats: BMP, GIF, JPEG, Exif, PNG, TIFF, WMF, EMF, and ICON.</span></span>

<span data-ttu-id="e8837-112">В следующем примере создаются объекты [**изображений**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) из различных типов файлов, а затем отображаются изображения.</span><span class="sxs-lookup"><span data-stu-id="e8837-112">The following example constructs [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of file types and then displays the images.</span></span>


```
Image myBMP(L"SpaceCadet.bmp");
Image myEMF(L"Metafile1.emf");
Image myGIF(L"Soda.gif");
Image myJPEG(L"Mango.jpg");
Image myPNG(L"Flowers.png");
Image myTIFF(L"MS.tif");

myGraphics.DrawImage(&myBMP, 10, 10);
myGraphics.DrawImage(&myEMF, 220, 10);
myGraphics.DrawImage(&myGIF, 320, 10);
myGraphics.DrawImage(&myJPEG, 380, 10);
myGraphics.DrawImage(&myPNG, 150, 200);
myGraphics.DrawImage(&myTIFF, 300, 200);
```



<span data-ttu-id="e8837-113">Класс [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) предоставляет метод [**Image:: Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) , который можно использовать для создания копии существующего **изображения**, [**метафайла**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)или [**растрового**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) объекта.</span><span class="sxs-lookup"><span data-stu-id="e8837-113">The [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class provides a [**Image::Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) method that you can use to make a copy of an existing **Image**, [**Metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile), or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="e8837-114">Метод [clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) перегружен в классе **Bitmap** , а один из вариантов имеет параметр исходного прямоугольника, который можно использовать для указания части исходного изображения, которую требуется скопировать.</span><span class="sxs-lookup"><span data-stu-id="e8837-114">The [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) method is overloaded in the **Bitmap** class, and one of the variations has a source-rectangle parameter that you can use to specify the portion of the original image that you want to copy.</span></span> <span data-ttu-id="e8837-115">В следующем примере создается объект **Bitmap** путем клонирования верхней половины существующего объекта **Bitmap** .</span><span class="sxs-lookup"><span data-stu-id="e8837-115">The following example creates a **Bitmap** object by cloning the top half of an existing **Bitmap** object.</span></span> <span data-ttu-id="e8837-116">Затем отображаются оба изображения.</span><span class="sxs-lookup"><span data-stu-id="e8837-116">Then both images are displayed.</span></span>


```
Bitmap* originalBitmap = new Bitmap(L"Spiral.png");
RectF sourceRect(
   0.0f,
   0.0f, 
   (REAL)(originalBitmap->GetWidth()), 
   (REAL)(originalBitmap->GetHeight())/2.0f);

Bitmap* secondBitmap = originalBitmap->Clone(sourceRect, PixelFormatDontCare);

myGraphics.DrawImage(originalBitmap, 10, 10);
myGraphics.DrawImage(secondBitmap, 100, 10);
```



<span data-ttu-id="e8837-117">Приведенный выше код, а также определенный файл Spiral.png, выдают следующие выходные данные.</span><span class="sxs-lookup"><span data-stu-id="e8837-117">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![Иллюстрация изображения, за которым следует верхняя половина изображения Оригнал](images/aboutgdip03-art05.png)

 

 
