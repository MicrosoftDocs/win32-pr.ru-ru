---
description: Класс Bitmap (который наследует от класса Image) и класс ImageAttributes предоставляют функциональные возможности для получения и установки значений пикселей.
ms.assetid: e3d67431-6098-4b2a-8910-5695a8473216
title: Использование матрицы цветов для настройки альфа-компонентов в изображениях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81180b1f09b11e37b322e37106dab1879a00bbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541439"
---
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a>Использование матрицы цветов для настройки альфа-компонентов в изображениях

Класс [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) (который наследует от класса [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ) и класс [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) предоставляют функциональные возможности для получения и установки значений пикселей. Можно использовать класс **ImageAttributes** , чтобы изменить альфа-значения для всего изображения, или можно вызвать метод [**Bitmap:: SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) класса **Bitmap** , чтобы изменить отдельные значения пикселей. Дополнительные сведения об установке отдельных значений пикселей см. в разделе [Установка альфа-значений отдельных пикселов](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).

В следующем примере рисуется широкая черная линия, а затем отображается непрозрачное изображение, охватывающее часть этой строки.


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



На следующем рисунке показан полученный рисунок, который рисуется в (30, 0). Обратите внимание, что широкая черная линия не отображается сквозь изображение.

![Иллюстрация, демонстрирующая непрозрачное изображение, пересекающее тонкий, широкий и черный прямоугольники](images/image1.png)

Класс [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) имеет множество свойств, которые можно использовать для изменения изображений во время подготовки к просмотру. В следующем примере объект **ImageAttributes** используется для установки всех альфа-значений в 80 процентов от того, что они имели. Это делается путем инициализации матрицы цветов и установки значения масштабирования альфа в матрице в 0,8. Адрес матрицы цветов передается методу [**ImageAttributes:: сетколорматрикс**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) объекта **ImageAttributes** , а адрес объекта **ImageAttributes** передается методу [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта.


```
// Create a Bitmap object and load it with the texture image.
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// Initialize the color matrix.
// Notice the value 0.8 in row 4, column 4.
ColorMatrix colorMatrix = {1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.8f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
// Create an ImageAttributes object and set its color matrix.
ImageAttributes imageAtt;
imageAtt.SetColorMatrix(&colorMatrix, ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw the semitransparent bitmap image.
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
graphics.DrawImage(
   &bitmap, 
   Rect(30, 0, iWidth, iHeight),  // Destination rectangle
   0,                             // Source rectangle X 
   0,                             // Source rectangle Y
   iWidth,                        // Source rectangle width
   iHeight,                       // Source rectangle height
   UnitPixel, 
   &imageAtt);
```



Во время отрисовки альфа-значения в точечном рисунке преобразуются в 80 процентов от того, что они имели. В результате получается изображение, которое смешивается с фоном. Как показано на рисунке ниже, точечный рисунок выглядит прозрачным. можно увидеть сплошную черную линию.

![Иллюстрация, похожая на предыдущую, но изображение является прозрачным для SEM](images/image2.png)

Когда изображение находится над белой частью фона, изображение смешивается с белым цветом. Когда изображение пересекает черную линию, изображение смешивается с черным цветом.

 

 



