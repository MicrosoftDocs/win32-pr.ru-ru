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
# <a name="drawing-positioning-and-cloning-images"></a>Отрисовка, позиционирование и клонирование изображений

Класс [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) можно использовать для загрузки и вывода растровых изображений (точечных рисунков) и векторных изображений (метафайлов). Для вывода изображения требуется [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и объект **изображения** . Объект **Graphics** предоставляет метод [**Graphics::D равимаже**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) , который получает адрес объекта **изображения** в качестве аргумента.

В следующем примере объект [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла Climber.jpg а затем отображается изображение. Конечная точка для верхнего левого угла изображения (10, 10) задается во втором и третьем параметрах метода [**Graphics::D равимаже**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) .


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



Приведенный выше код, а также определенный файл Climber.jpg, выдают следующие выходные данные.

![снимок экрана окна, содержащего фотографию](images/aboutgdip03-art04.png)

Объекты [**изображений**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) можно создавать из различных форматов графических файлов: BMP, GIF, JPEG, EXIF, PNG, TIFF, WMF, EMF и Icon.

В следующем примере создаются объекты [**изображений**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) из различных типов файлов, а затем отображаются изображения.


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



Класс [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) предоставляет метод [**Image:: Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) , который можно использовать для создания копии существующего **изображения**, [**метафайла**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)или [**растрового**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) объекта. Метод [clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) перегружен в классе **Bitmap** , а один из вариантов имеет параметр исходного прямоугольника, который можно использовать для указания части исходного изображения, которую требуется скопировать. В следующем примере создается объект **Bitmap** путем клонирования верхней половины существующего объекта **Bitmap** . Затем отображаются оба изображения.


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



Приведенный выше код, а также определенный файл Spiral.png, выдают следующие выходные данные.

![Иллюстрация изображения, за которым следует верхняя половина изображения Оригнал](images/aboutgdip03-art05.png)

 

 
