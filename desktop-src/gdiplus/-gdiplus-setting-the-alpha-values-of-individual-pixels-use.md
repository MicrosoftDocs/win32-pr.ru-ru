---
description: В разделе Использование матрицы цветов для установки альфа-значений в изображениях показан неразрушающий метод изменения альфа-значений изображения.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Установка альфа-значений отдельных пикселов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cd45bf32284ffc9a8cef13f368cff59e1e8a74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541455"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a><span data-ttu-id="29b5a-103">Установка альфа-значений отдельных пикселов</span><span class="sxs-lookup"><span data-stu-id="29b5a-103">Setting the Alpha Values of Individual Pixels</span></span>

<span data-ttu-id="29b5a-104">В разделе [Использование матрицы цветов для установки альфа-значений в изображениях](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) показан неразрушающий метод изменения альфа-значений изображения.</span><span class="sxs-lookup"><span data-stu-id="29b5a-104">The topic [Using a Color Matrix to Set Alpha Values in Images](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) shows a nondestructive method for changing the alpha values of an image.</span></span> <span data-ttu-id="29b5a-105">Пример в этом разделе отображает изображение полупрозрачным образом, но данные пикселей в точечном рисунке не изменяются.</span><span class="sxs-lookup"><span data-stu-id="29b5a-105">The example in that topic renders an image semitransparently, but the pixel data in the bitmap is not changed.</span></span> <span data-ttu-id="29b5a-106">Альфа-значения изменяются только во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="29b5a-106">The alpha values are altered only during rendering.</span></span>

<span data-ttu-id="29b5a-107">В следующем примере показано, как изменить альфа-значения отдельных пикселов.</span><span class="sxs-lookup"><span data-stu-id="29b5a-107">The following example shows how to change the alpha values of individual pixels.</span></span> <span data-ttu-id="29b5a-108">Код в примере фактически изменяет альфа-информацию в объекте [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="29b5a-108">The code in the example actually changes the alpha information in a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="29b5a-109">Этот подход намного медленнее, чем использование матрицы цветов и объекта [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , но позволяет управлять отдельными пикселями в точечном рисунке.</span><span class="sxs-lookup"><span data-stu-id="29b5a-109">The approach is much slower than using a color matrix and an [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object but gives you control over the individual pixels in the bitmap.</span></span>


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



<span data-ttu-id="29b5a-110">На следующем рисунке показан полученный рисунок.</span><span class="sxs-lookup"><span data-stu-id="29b5a-110">The following illustration shows the resulting image.</span></span>

![Иллюстрация, показывающая, что изображение становится более непрозрачным слева направо, над черным прямоугольником](images/image3.png)

<span data-ttu-id="29b5a-112">В предыдущем примере кода используются вложенные циклы для изменения альфа-значения каждого пикселя в точечном рисунке.</span><span class="sxs-lookup"><span data-stu-id="29b5a-112">The preceding code example uses nested loops to change the alpha value of each pixel in the bitmap.</span></span> <span data-ttu-id="29b5a-113">Для каждого пикселя [**Bitmap::**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) SetPixel получает существующий цвет, [**Color:: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) создает временный цвет, содержащий новое альфа-значение, а затем [**Bitmap::**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) /задает новый цвет.</span><span class="sxs-lookup"><span data-stu-id="29b5a-113">For each pixel, [**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) gets the existing color, [**Color::SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) creates a temporary color that contains the new alpha value, and then [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) sets the new color.</span></span> <span data-ttu-id="29b5a-114">Альфа-значение задается на основе столбца точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="29b5a-114">The alpha value is set based on the column of the bitmap.</span></span> <span data-ttu-id="29b5a-115">В первом столбце альфа-каналу присвоено значение 0.</span><span class="sxs-lookup"><span data-stu-id="29b5a-115">In the first column, alpha is set to 0.</span></span> <span data-ttu-id="29b5a-116">В последнем столбце альфа-каналу присвоено значение 255.</span><span class="sxs-lookup"><span data-stu-id="29b5a-116">In the last column, alpha is set to 255.</span></span> <span data-ttu-id="29b5a-117">Таким образом, полученный образ поступает от полностью прозрачного (на левом краю) до полностью непрозрачного (на правом краю).</span><span class="sxs-lookup"><span data-stu-id="29b5a-117">So the resulting image goes from fully transparent (on the left edge) to fully opaque (on the right edge).</span></span>

<span data-ttu-id="29b5a-118">[**Bitmap::**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) [**SetPixel и Bitmap::**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) , позволяющие управлять отдельными значениями пикселей.</span><span class="sxs-lookup"><span data-stu-id="29b5a-118">[**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) and [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) give you control of the individual pixel values.</span></span> <span data-ttu-id="29b5a-119">Однако использование **Bitmap::** **SetPixel и Bitmap::** не так быстро, как использование класса [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) и структуры [**КолорМатрикс**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .</span><span class="sxs-lookup"><span data-stu-id="29b5a-119">However, using **Bitmap::GetPixel** and **Bitmap::SetPixel** is not nearly as fast as using the [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class and the [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>

 

 



