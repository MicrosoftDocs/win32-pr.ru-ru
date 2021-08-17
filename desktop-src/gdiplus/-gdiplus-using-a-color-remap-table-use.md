---
description: Повторное сопоставление — это процесс преобразования цветов в изображении в соответствии с таблицей преобразования цветов. Таблица преобразования цветов — это массив структур Колормап. Каждая структура Колормап в массиве имеет элемент Олдколор и элемент Невколор.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Использование таблицы преобразования цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00f36c493bbdc696fa672b2899d4d7c6d3231a9e40c0e4162b5113d78a67164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036302"
---
# <a name="using-a-color-remap-table"></a>Использование таблицы преобразования цветов

Повторное сопоставление — это процесс преобразования цветов в изображении в соответствии с таблицей преобразования цветов. Таблица преобразования цветов — это массив структур [**колормап**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) . Каждая структура **колормап** в массиве имеет элемент **Олдколор** и элемент **невколор** .

когда GDI+ рисует изображение, каждый пиксель изображения сравнивается с массивом старых цветов. Если цвет пикселя совпадает со старым цветом, его цвет изменяется на соответствующий новый цвет. Цвета изменяются только для отрисовки — цветовые значения самого изображения (хранящегося в объекте [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) или [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) ) не изменяются.

Чтобы нарисовать повторно сопоставленное изображение, инициализируйте массив структур [**колормап**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) . Передайте адрес этого массива методу [**ImageAttributes:: сетремаптабле**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) объекта [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , а затем передайте адрес объекта **ImageAttributes** методу [методов DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

В следующем примере объект [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла RemapInput.bmp. Код создает таблицу преобразования цветов, состоящую из одной структуры [**колормап**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) . Элемент **олдколор** структуры **колормап** красным, а элемент **невколор** — синим. Изображение рисуется один раз без повторного сопоставления и повторного сопоставления. В процессе повторного сопоставления все красные пиксели меняются на синие.


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



На следующем рисунке показано исходное изображение слева и повторно назначенное изображение справа.

![Иллюстрация, демонстрирующая две версии многоцветного изображения; Красная область первой версии является синей во второй версии](images/colortrans7.png)

 

 



