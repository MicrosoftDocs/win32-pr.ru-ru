---
description: Так же, как плитки можно поместить рядом друг с другом, чтобы охватить этаж, прямоугольные изображения можно поместить рядом друг с другом, чтобы заполнить фигуру (мозаичное заполнение).
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Мозаичное заполнение фигуры изображением
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c0b6e2ce39f5bf5c43b0352b8997202aa7e856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144869"
---
# <a name="tiling-a-shape-with-an-image"></a><span data-ttu-id="d6df6-103">Мозаичное заполнение фигуры изображением</span><span class="sxs-lookup"><span data-stu-id="d6df6-103">Tiling a Shape with an Image</span></span>

<span data-ttu-id="d6df6-104">Так же, как плитки можно поместить рядом друг с другом, чтобы охватить этаж, прямоугольные изображения можно поместить рядом друг с другом, чтобы заполнить фигуру (мозаичное заполнение).</span><span class="sxs-lookup"><span data-stu-id="d6df6-104">Just as tiles can be placed next to each other to cover a floor, rectangular images can be placed next to each other to fill (tile) a shape.</span></span> <span data-ttu-id="d6df6-105">Чтобы замостить внутреннюю часть фигуры, используйте текстурную кисть.</span><span class="sxs-lookup"><span data-stu-id="d6df6-105">To tile the interior of a shape, use a texture brush.</span></span> <span data-ttu-id="d6df6-106">При создании объекта [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) одним из аргументов, передаваемых в конструктор, является адрес объекта [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="d6df6-106">When you construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, one of the arguments you pass to the constructor is the address of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="d6df6-107">При использовании кисти текстуры для заполнения внутренней фигуры фигура заполняется повторяющимися копиями этого изображения.</span><span class="sxs-lookup"><span data-stu-id="d6df6-107">When you use the texture brush to paint the interior of a shape, the shape is filled with repeated copies of this image.</span></span>

<span data-ttu-id="d6df6-108">Свойство режима обертывания объекта [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) определяет ориентацию изображения, так как оно повторяется в прямоугольной сетке.</span><span class="sxs-lookup"><span data-stu-id="d6df6-108">The wrap mode property of the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object determines how the image is oriented as it is repeated in a rectangular grid.</span></span> <span data-ttu-id="d6df6-109">Можно сделать так, чтобы все плитки в сетке имели одинаковую ориентацию, или можно сделать изображение отражаться от одного расположения сетки до следующего.</span><span class="sxs-lookup"><span data-stu-id="d6df6-109">You can make all the tiles in the grid have the same orientation, or you can make the image flip from one grid position to the next.</span></span> <span data-ttu-id="d6df6-110">Зеркальное отображение может быть горизонтальным, вертикальным или обоими.</span><span class="sxs-lookup"><span data-stu-id="d6df6-110">The flipping can be horizontal, vertical, or both.</span></span> <span data-ttu-id="d6df6-111">В следующих примерах демонстрируется мозаичное заполнение различными типами переворачивания.</span><span class="sxs-lookup"><span data-stu-id="d6df6-111">The following examples demonstrate tiling with different types of flipping.</span></span>

## <a name="tiling-an-image"></a><span data-ttu-id="d6df6-112">Мозаичное заполнение изображения</span><span class="sxs-lookup"><span data-stu-id="d6df6-112">Tiling an Image</span></span>

<span data-ttu-id="d6df6-113">В этом примере используется следующий рисунок 75 × 75 для мозаичного заполнения прямоугольника 200 x 200:</span><span class="sxs-lookup"><span data-stu-id="d6df6-113">This example uses the following 75 ×75 image to tile a 200 ×200 rectangle:</span></span>

![Иллюстрация, используемая в качестве основы других иллюстраций в этом разделе: дом и дерево на фоне и центрирование в прямоугольнике](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="d6df6-115">На следующем рисунке показано, как прямоугольник заполняется изображением.</span><span class="sxs-lookup"><span data-stu-id="d6df6-115">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="d6df6-116">Обратите внимание, что все плитки имеют одинаковую ориентацию. Зеркальное отображение отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d6df6-116">Note that all tiles have the same orientation; there is no flipping.</span></span>

![Иллюстрация, демонстрирующая базовое изображение, повторяющееся по горизонтали и вертикали в большом прямоугольнике](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a><span data-ttu-id="d6df6-118">Отражение изображения по горизонтали при мозаичном заполнении</span><span class="sxs-lookup"><span data-stu-id="d6df6-118">Flipping an Image Horizontally While Tiling</span></span>

<span data-ttu-id="d6df6-119">В этом примере используется изображение 75 × 75 для заполнения прямоугольника 200 x 200.</span><span class="sxs-lookup"><span data-stu-id="d6df6-119">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="d6df6-120">Режим переноса установлен для перелистывания изображения по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d6df6-120">The wrap mode is set to flip the image horizontally.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="d6df6-121">На следующем рисунке показано, как прямоугольник заполняется изображением.</span><span class="sxs-lookup"><span data-stu-id="d6df6-121">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="d6df6-122">Обратите внимание, что при переходе от одной плитки к следующей в определенной строке изображение помещается по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d6df6-122">Note that as you move from one tile to the next in a given row, the image is flipped horizontally.</span></span>

![Иллюстрация, показывающая базовый образ, повторяющийся по горизонтали, но даже пронумерованные экземпляры реверсируются по горизонтали](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a><span data-ttu-id="d6df6-124">Отражение изображения по вертикали при мозаичном заполнении</span><span class="sxs-lookup"><span data-stu-id="d6df6-124">Flipping an Image Vertically While Tiling</span></span>

<span data-ttu-id="d6df6-125">В этом примере используется изображение 75 × 75 для заполнения прямоугольника 200 x 200.</span><span class="sxs-lookup"><span data-stu-id="d6df6-125">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="d6df6-126">Режим переноса установлен для вертикальной перелистывания изображения.</span><span class="sxs-lookup"><span data-stu-id="d6df6-126">The wrap mode is set to flip the image vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="d6df6-127">На следующем рисунке показано, как прямоугольник заполняется изображением.</span><span class="sxs-lookup"><span data-stu-id="d6df6-127">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="d6df6-128">Обратите внимание, что при переходе от одной плитки к следующей в определенном столбце изображение помещается по вертикали.</span><span class="sxs-lookup"><span data-stu-id="d6df6-128">Note that as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![Иллюстрация, демонстрирующая базовое изображение, повторяющееся по горизонтали и вертикали, но строковые строки с четными числами реверсируются вертикально](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a><span data-ttu-id="d6df6-130">Зеркальное отображение изображения по горизонтали и вертикали при мозаичном заполнении</span><span class="sxs-lookup"><span data-stu-id="d6df6-130">Flipping an Image Horizontally and Vertically While Tiling</span></span>

<span data-ttu-id="d6df6-131">В этом примере используется изображение 75 × 75 для мозаичного заполнения прямоугольника 200 x 200.</span><span class="sxs-lookup"><span data-stu-id="d6df6-131">This example uses a 75 ×75 image to tile a 200 ×200 rectangle.</span></span> <span data-ttu-id="d6df6-132">Режим переноса установлен для отражения изображения как по горизонтали, так и по вертикали.</span><span class="sxs-lookup"><span data-stu-id="d6df6-132">The wrap mode is set to flip the image both horizontally and vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="d6df6-133">На следующем рисунке показано мозаичное заполнение прямоугольника изображением.</span><span class="sxs-lookup"><span data-stu-id="d6df6-133">The following illustration shows how the rectangle is tiled by the image.</span></span> <span data-ttu-id="d6df6-134">Обратите внимание, что при переходе от одной плитки к следующей в определенной строке изображение помещается по горизонтали, а при переходе от одной плитки к другой в заданном столбце изображение помещается по вертикали.</span><span class="sxs-lookup"><span data-stu-id="d6df6-134">Note that as you move from one tile to the next in a given row, the image is flipped horizontally, and as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![Иллюстрация, показывающая чередующиеся экземпляры базового изображения в каждой строке, переводится по горизонтали, а чередующиеся строки перемещаются по вертикали.](images/tile5.png)

 

 



