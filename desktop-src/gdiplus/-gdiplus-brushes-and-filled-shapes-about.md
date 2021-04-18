---
description: Замкнутая фигура, например прямоугольник или эллипс, состоит из контура и внутренней части.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Кисти и закрашенные фигуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563461"
---
# <a name="brushes-and-filled-shapes"></a><span data-ttu-id="21e3b-103">Кисти и закрашенные фигуры</span><span class="sxs-lookup"><span data-stu-id="21e3b-103">Brushes and Filled Shapes</span></span>

<span data-ttu-id="21e3b-104">Замкнутая фигура, например прямоугольник или эллипс, состоит из контура и внутренней части.</span><span class="sxs-lookup"><span data-stu-id="21e3b-104">A closed figure such as a rectangle or an ellipse consists of an outline and an interior.</span></span> <span data-ttu-id="21e3b-105">Структура рисуется с помощью объекта [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , а внутренняя часть заполняется объектом [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="21e3b-105">The outline is drawn with a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and the interior is filled with a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="21e3b-106">Windows GDI+ предоставляет несколько классов кистей для заполнения внутренних частей замкнутых фигур: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**хатчбруш**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)и [**пасградиентбруш**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="21e3b-106">Windows GDI+ provides several brush classes for filling the interiors of closed figures: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), and [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span></span> <span data-ttu-id="21e3b-107">Все эти классы наследуют от класса **Brush** .</span><span class="sxs-lookup"><span data-stu-id="21e3b-107">All these classes inherit from the **Brush** class.</span></span> <span data-ttu-id="21e3b-108">На следующем рисунке показан прямоугольник, заполненный сплошной кистью, и эллипс, заполненный штриховым кистью.</span><span class="sxs-lookup"><span data-stu-id="21e3b-108">The following illustration shows a rectangle filled with a solid brush and an ellipse filled with a hatch brush.</span></span>

![Иллюстрация, демонстрирующая синий прямоугольник и пурпурный эллипс, заполненный синим шаблоном штриховки](images/aboutgdip02-art17.png)

 

-   [<span data-ttu-id="21e3b-110">Сплошные кисти</span><span class="sxs-lookup"><span data-stu-id="21e3b-110">Solid Brushes</span></span>](#solid-brushes)
-   [<span data-ttu-id="21e3b-111">Штриховые кисти</span><span class="sxs-lookup"><span data-stu-id="21e3b-111">Hatch Brushes</span></span>](#hatch-brushes)
-   [<span data-ttu-id="21e3b-112">Текстурные кисти</span><span class="sxs-lookup"><span data-stu-id="21e3b-112">Texture Brushes</span></span>](#texture-brushes)
-   [<span data-ttu-id="21e3b-113">Градиентные кисти</span><span class="sxs-lookup"><span data-stu-id="21e3b-113">Gradient Brushes</span></span>](#gradient-brushes)

## <a name="solid-brushes"></a><span data-ttu-id="21e3b-114">Сплошные кисти</span><span class="sxs-lookup"><span data-stu-id="21e3b-114">Solid Brushes</span></span>

<span data-ttu-id="21e3b-115">Для заполнения замкнутой фигуры необходим [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и объект [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="21e3b-115">To fill a closed shape, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="21e3b-116">Объект **Graphics** предоставляет методы, такие как [филлректангле](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) и [филлеллипсе](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), а объект **Brush** сохраняет атрибуты заливки, такие как цвет и шаблон.</span><span class="sxs-lookup"><span data-stu-id="21e3b-116">The **Graphics** object provides methods, such as [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) and [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), and the **Brush** object stores attributes of the fill, such as color and pattern.</span></span> <span data-ttu-id="21e3b-117">Адрес объекта **Brush** передается в качестве одного из аргументов метода Fill.</span><span class="sxs-lookup"><span data-stu-id="21e3b-117">The address of the **Brush** object is passed as one of the arguments to the fill method.</span></span> <span data-ttu-id="21e3b-118">В следующем примере заливка эллипса осуществляется с помощью сплошного красного цвета.</span><span class="sxs-lookup"><span data-stu-id="21e3b-118">The following example fills an ellipse with a solid red color.</span></span>


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



<span data-ttu-id="21e3b-119">Обратите внимание, что в предыдущем примере кисть относится к типу [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), который наследует от [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span><span class="sxs-lookup"><span data-stu-id="21e3b-119">Note that in the preceding example, the brush is of type [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), which inherits from [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span></span>

## <a name="hatch-brushes"></a><span data-ttu-id="21e3b-120">Штриховые кисти</span><span class="sxs-lookup"><span data-stu-id="21e3b-120">Hatch Brushes</span></span>

<span data-ttu-id="21e3b-121">При заполнении фигуры штриховой кистью необходимо указать цвет переднего плана, цвет фона и стиль штриховки.</span><span class="sxs-lookup"><span data-stu-id="21e3b-121">When you fill a shape with a hatch brush, you specify a foreground color, a background color, and a hatch style.</span></span> <span data-ttu-id="21e3b-122">Цвет переднего плана — это цвет штриховки.</span><span class="sxs-lookup"><span data-stu-id="21e3b-122">The foreground color is the color of the hatching.</span></span>


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



<span data-ttu-id="21e3b-123">Интерфейс GDI+ предоставляет более 50 стилей штриховки, указанных в [**хатчстиле**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span><span class="sxs-lookup"><span data-stu-id="21e3b-123">GDI+ provides more than 50 hatch styles, specified in [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span></span> <span data-ttu-id="21e3b-124">На следующем рисунке показаны три стиля: горизонтальный, ForwardDiagonalный и перекрестный.</span><span class="sxs-lookup"><span data-stu-id="21e3b-124">The three styles shown in the following illustration are Horizontal, ForwardDiagonal, and Cross.</span></span>

![Иллюстрация с тремя сине-окрашенными эллипсами с различными стилями штриховки](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a><span data-ttu-id="21e3b-126">Текстурные кисти</span><span class="sxs-lookup"><span data-stu-id="21e3b-126">Texture Brushes</span></span>

<span data-ttu-id="21e3b-127">Текстурная кисть позволяет заполнить фигуру шаблоном, хранящимся в растровом изображении.</span><span class="sxs-lookup"><span data-stu-id="21e3b-127">With a texture brush, you can fill a shape with a pattern stored in a bitmap.</span></span> <span data-ttu-id="21e3b-128">Например, предположим, что следующий рисунок хранится в файле на диске с именем MyTexture.bmp.</span><span class="sxs-lookup"><span data-stu-id="21e3b-128">For example, suppose the following picture is stored in a disk file named MyTexture.bmp.</span></span>

![снимок экрана с небольшим квадратом, заполненным различными цветами](images/aboutgdip02-art19.png)

<span data-ttu-id="21e3b-130&quot;>В следующем примере выполняется заливка эллипса путем повторения изображения, хранящегося в MyTexture.bmp.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;21e3b-130&quot;>The following example fills an ellipse by repeating the picture stored in MyTexture.bmp.</span></span>


```
Image myImage(L&quot;MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



<span data-ttu-id="21e3b-131">На следующем рисунке показан закрашенный эллипс.</span><span class="sxs-lookup"><span data-stu-id="21e3b-131">The following illustration shows the filled ellipse.</span></span>

![Иллюстрация, показывающая эллипс, заполненный ранее заданным шаблоном](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a><span data-ttu-id="21e3b-133">Градиентные кисти</span><span class="sxs-lookup"><span data-stu-id="21e3b-133">Gradient Brushes</span></span>

<span data-ttu-id="21e3b-134">Можно использовать градиентную кисть для заливки фигуры цветом, который постепенно меняется от одной части фигуры к другой.</span><span class="sxs-lookup"><span data-stu-id="21e3b-134">You can use a gradient brush to fill a shape with a color that changes gradually from one part of the shape to another.</span></span> <span data-ttu-id="21e3b-135">Например, горизонтальная Градиентная кисть изменит цвет при переходе с левой стороны фигуры на правую.</span><span class="sxs-lookup"><span data-stu-id="21e3b-135">For example, a horizontal gradient brush will change color as you move from the left side of a figure to the right side.</span></span> <span data-ttu-id="21e3b-136">В следующем примере заливка эллипса выполняется с помощью горизонтальной градиентной кисти, которая меняется с синего на зеленую при переходе от левой части эллипса к правой стороне.</span><span class="sxs-lookup"><span data-stu-id="21e3b-136">The following example fills an ellipse with a horizontal gradient brush that changes from blue to green as you move from the left side of the ellipse to the right side.</span></span>


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



<span data-ttu-id="21e3b-137">На следующем рисунке показан закрашенный эллипс.</span><span class="sxs-lookup"><span data-stu-id="21e3b-137">The following illustration shows the filled ellipse.</span></span>

![Иллюстрация с эллипсом с градиентной заливкой: синий справа — зеленый слева](images/aboutgdip02-art21.png)

<span data-ttu-id="21e3b-139">Кисть градиента контура может быть настроена на изменение цвета при перемещении от центра фигуры к границе.</span><span class="sxs-lookup"><span data-stu-id="21e3b-139">A path gradient brush can be configured to change color as you move from the center of a figure toward the boundary.</span></span>

![илустратион эллипса, темно-синий в центре, затенение светлого цвета на границе](images/aboutgdip02-art22.png)

<span data-ttu-id="21e3b-141">Кисти градиента вдоль пути являются достаточно гибкими.</span><span class="sxs-lookup"><span data-stu-id="21e3b-141">Path gradient brushes are quite flexible.</span></span> <span data-ttu-id="21e3b-142">Градиентная кисть, используемая для заливки треугольника на следующем рисунке, постепенно меняется от красного в центре к каждому из трех различных цветов в вершинах.</span><span class="sxs-lookup"><span data-stu-id="21e3b-142">The gradient brush used to fill the triangle in the following illustration changes gradually from red at the center to each of three different colors at the vertices.</span></span>

![Иллюстрация красного цвета в центре, заливка к другому цвету на каждой вершине](images/aboutgdip02-art23.png)

 

 



