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
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a><span data-ttu-id="7f505-103">Использование матрицы цветов для настройки альфа-компонентов в изображениях</span><span class="sxs-lookup"><span data-stu-id="7f505-103">Using a Color Matrix to Set Alpha Values in Images</span></span>

<span data-ttu-id="7f505-104">Класс [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) (который наследует от класса [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ) и класс [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) предоставляют функциональные возможности для получения и установки значений пикселей.</span><span class="sxs-lookup"><span data-stu-id="7f505-104">The [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class (which inherits from the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class) and the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class provide functionality for getting and setting pixel values.</span></span> <span data-ttu-id="7f505-105">Можно использовать класс **ImageAttributes** , чтобы изменить альфа-значения для всего изображения, или можно вызвать метод [**Bitmap:: SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) класса **Bitmap** , чтобы изменить отдельные значения пикселей.</span><span class="sxs-lookup"><span data-stu-id="7f505-105">You can use the **ImageAttributes** class to modify the alpha values for an entire image, or you can call the [**Bitmap::SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) method of the **Bitmap** class to modify individual pixel values.</span></span> <span data-ttu-id="7f505-106">Дополнительные сведения об установке отдельных значений пикселей см. в разделе [Установка альфа-значений отдельных пикселов](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).</span><span class="sxs-lookup"><span data-stu-id="7f505-106">For more information on setting individual pixel values, see [Setting the Alpha Values of Individual Pixels](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).</span></span>

<span data-ttu-id="7f505-107">В следующем примере рисуется широкая черная линия, а затем отображается непрозрачное изображение, охватывающее часть этой строки.</span><span class="sxs-lookup"><span data-stu-id="7f505-107">The following example draws a wide black line and then displays an opaque image that covers part of that line.</span></span>


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



<span data-ttu-id="7f505-108">На следующем рисунке показан полученный рисунок, который рисуется в (30, 0).</span><span class="sxs-lookup"><span data-stu-id="7f505-108">The following illustration shows the resulting image, which is drawn at (30, 0).</span></span> <span data-ttu-id="7f505-109">Обратите внимание, что широкая черная линия не отображается сквозь изображение.</span><span class="sxs-lookup"><span data-stu-id="7f505-109">Note that the wide black line doesn't show through the image.</span></span>

![Иллюстрация, демонстрирующая непрозрачное изображение, пересекающее тонкий, широкий и черный прямоугольники](images/image1.png)

<span data-ttu-id="7f505-111">Класс [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) имеет множество свойств, которые можно использовать для изменения изображений во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="7f505-111">The [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class has many properties that you can use to modify images during rendering.</span></span> <span data-ttu-id="7f505-112">В следующем примере объект **ImageAttributes** используется для установки всех альфа-значений в 80 процентов от того, что они имели.</span><span class="sxs-lookup"><span data-stu-id="7f505-112">In the following example, an **ImageAttributes** object is used to set all the alpha values to 80 percent of what they were.</span></span> <span data-ttu-id="7f505-113">Это делается путем инициализации матрицы цветов и установки значения масштабирования альфа в матрице в 0,8.</span><span class="sxs-lookup"><span data-stu-id="7f505-113">This is done by initializing a color matrix and setting the alpha scaling value in the matrix to 0.8.</span></span> <span data-ttu-id="7f505-114">Адрес матрицы цветов передается методу [**ImageAttributes:: сетколорматрикс**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) объекта **ImageAttributes** , а адрес объекта **ImageAttributes** передается методу [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта.</span><span class="sxs-lookup"><span data-stu-id="7f505-114">The address of the color matrix is passed to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object, and the address of the **ImageAttributes** object is passed to the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


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



<span data-ttu-id="7f505-115">Во время отрисовки альфа-значения в точечном рисунке преобразуются в 80 процентов от того, что они имели.</span><span class="sxs-lookup"><span data-stu-id="7f505-115">During rendering, the alpha values in the bitmap are converted to 80 percent of what they were.</span></span> <span data-ttu-id="7f505-116">В результате получается изображение, которое смешивается с фоном.</span><span class="sxs-lookup"><span data-stu-id="7f505-116">This results in an image that is blended with the background.</span></span> <span data-ttu-id="7f505-117">Как показано на рисунке ниже, точечный рисунок выглядит прозрачным. можно увидеть сплошную черную линию.</span><span class="sxs-lookup"><span data-stu-id="7f505-117">As the following illustration shows, the bitmap image looks transparent; you can see the solid black line through it.</span></span>

![Иллюстрация, похожая на предыдущую, но изображение является прозрачным для SEM](images/image2.png)

<span data-ttu-id="7f505-119">Когда изображение находится над белой частью фона, изображение смешивается с белым цветом.</span><span class="sxs-lookup"><span data-stu-id="7f505-119">Where the image is over the white portion of the background, the image has been blended with the color white.</span></span> <span data-ttu-id="7f505-120">Когда изображение пересекает черную линию, изображение смешивается с черным цветом.</span><span class="sxs-lookup"><span data-stu-id="7f505-120">Where the image crosses the black line, the image is blended with the color black.</span></span>

 

 



