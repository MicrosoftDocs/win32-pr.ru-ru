---
description: Повторное сопоставление — это процесс преобразования цветов в изображении в соответствии с таблицей преобразования цветов. Таблица преобразования цветов — это массив структур Колормап. Каждая структура Колормап в массиве имеет элемент Олдколор и элемент Невколор.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Использование таблицы преобразования цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1c07bc0a67a02ea07aeaa3931e661af5665e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144860"
---
# <a name="using-a-color-remap-table"></a><span data-ttu-id="f9a5c-105">Использование таблицы преобразования цветов</span><span class="sxs-lookup"><span data-stu-id="f9a5c-105">Using a Color Remap Table</span></span>

<span data-ttu-id="f9a5c-106">Повторное сопоставление — это процесс преобразования цветов в изображении в соответствии с таблицей преобразования цветов.</span><span class="sxs-lookup"><span data-stu-id="f9a5c-106">Remapping is the process of converting the colors in an image according to a color remap table.</span></span> <span data-ttu-id="f9a5c-107">Таблица преобразования цветов — это массив структур [**колормап**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="f9a5c-107">The color remap table is an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="f9a5c-108">Каждая структура **колормап** в массиве имеет элемент **Олдколор** и элемент **невколор** .</span><span class="sxs-lookup"><span data-stu-id="f9a5c-108">Each **ColorMap** structure in the array has an **oldColor** member and a **newColor** member.</span></span>

<span data-ttu-id="f9a5c-109">Когда GDI+ рисует изображение, каждый пиксель изображения сравнивается с массивом старых цветов.</span><span class="sxs-lookup"><span data-stu-id="f9a5c-109">When GDI+ draws an image, each pixel of the image is compared to the array of old colors.</span></span> <span data-ttu-id="f9a5c-110">Если цвет пикселя совпадает со старым цветом, его цвет изменяется на соответствующий новый цвет.</span><span class="sxs-lookup"><span data-stu-id="f9a5c-110">If a pixel's color matches an old color, its color is changed to the corresponding new color.</span></span> <span data-ttu-id="f9a5c-111">Цвета изменяются только для отрисовки — цветовые значения самого изображения (хранящегося в объекте [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) или [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) ) не изменяются.</span><span class="sxs-lookup"><span data-stu-id="f9a5c-111">The colors are changed only for rendering — the color values of the image itself (stored in an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object) are not changed.</span></span>

<span data-ttu-id="f9a5c-112">Чтобы нарисовать повторно сопоставленное изображение, инициализируйте массив структур [**колормап**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="f9a5c-112">To draw a remapped image, initialize an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="f9a5c-113">Передайте адрес этого массива методу [**ImageAttributes:: сетремаптабле**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) объекта [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , а затем передайте адрес объекта **ImageAttributes** методу [методов DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="f9a5c-113">Pass the address of that array to the [**ImageAttributes::SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) method of an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object, and then pass the address of the **ImageAttributes** object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="f9a5c-114">В следующем примере объект [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла RemapInput.bmp.</span><span class="sxs-lookup"><span data-stu-id="f9a5c-114">The following example creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file RemapInput.bmp.</span></span> <span data-ttu-id="f9a5c-115">Код создает таблицу преобразования цветов, состоящую из одной структуры [**колормап**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="f9a5c-115">The code creates a color remap table that consists of a single [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structure.</span></span> <span data-ttu-id="f9a5c-116">Элемент **олдколор** структуры **колормап** красным, а элемент **невколор** — синим.</span><span class="sxs-lookup"><span data-stu-id="f9a5c-116">The **oldColor** member of the **ColorMap** structure is red, and the **newColor** member is blue.</span></span> <span data-ttu-id="f9a5c-117">Изображение рисуется один раз без повторного сопоставления и повторного сопоставления.</span><span class="sxs-lookup"><span data-stu-id="f9a5c-117">The image is drawn once without remapping and once with remapping.</span></span> <span data-ttu-id="f9a5c-118">В процессе повторного сопоставления все красные пиксели меняются на синие.</span><span class="sxs-lookup"><span data-stu-id="f9a5c-118">The remapping process changes all the red pixels to blue.</span></span>


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



<span data-ttu-id="f9a5c-119">На следующем рисунке показано исходное изображение слева и повторно назначенное изображение справа.</span><span class="sxs-lookup"><span data-stu-id="f9a5c-119">The following illustration shows the original image on the left and the remapped image on the right.</span></span>

![Иллюстрация, демонстрирующая две версии многоцветного изображения; Красная область первой версии является синей во второй версии](images/colortrans7.png)

 

 



