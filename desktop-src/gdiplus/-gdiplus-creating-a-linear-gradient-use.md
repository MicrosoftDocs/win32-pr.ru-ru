---
description: GDI+ предоставляет горизонтальные, вертикальные и диагональные линейные градиенты. По умолчанию цвет линейного градиента изменяется единообразно. Однако линейный градиент можно настроить таким образом, чтобы цвет был изменен неоднородным образом.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Создание линейного градиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559257"
---
# <a name="creating-a-linear-gradient"></a><span data-ttu-id="6ce9b-105">Создание линейного градиента</span><span class="sxs-lookup"><span data-stu-id="6ce9b-105">Creating a Linear Gradient</span></span>

<span data-ttu-id="6ce9b-106">GDI+ предоставляет горизонтальные, вертикальные и диагональные линейные градиенты.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-106">GDI+ provides horizontal, vertical, and diagonal linear gradients.</span></span> <span data-ttu-id="6ce9b-107">По умолчанию цвет линейного градиента изменяется единообразно.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-107">By default, the color in a linear gradient changes uniformly.</span></span> <span data-ttu-id="6ce9b-108">Однако линейный градиент можно настроить таким образом, чтобы цвет был изменен неоднородным образом.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-108">However, you can customize a linear gradient so that the color changes in a non-uniform fashion.</span></span>

-   [<span data-ttu-id="6ce9b-109">Горизонтальные линейные градиенты</span><span class="sxs-lookup"><span data-stu-id="6ce9b-109">Horizontal Linear Gradients</span></span>](#horizontal-linear-gradients)
-   [<span data-ttu-id="6ce9b-110">Настройка линейных градиентов</span><span class="sxs-lookup"><span data-stu-id="6ce9b-110">Customizing Linear Gradients</span></span>](#customizing-linear-gradients)
-   [<span data-ttu-id="6ce9b-111">Диагональные линейные градиенты</span><span class="sxs-lookup"><span data-stu-id="6ce9b-111">Diagonal Linear Gradients</span></span>](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a><span data-ttu-id="6ce9b-112">Горизонтальные линейные градиенты</span><span class="sxs-lookup"><span data-stu-id="6ce9b-112">Horizontal Linear Gradients</span></span>

<span data-ttu-id="6ce9b-113">В следующем примере кисть горизонтального линейного градиента используется для заливки линии, эллипса и прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-113">The following example uses a horizontal linear gradient brush to fill a line, an ellipse, and a rectangle:</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // opaque red
   Color(255, 0, 0, 255));  // opaque blue

Pen pen(&linGrBrush);

graphics.DrawLine(&pen, 0, 10, 200, 10);
graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="6ce9b-114">Конструктор [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) получает четыре аргумента: две точки и два цвета.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-114">The [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor receives four arguments: two points and two colors.</span></span> <span data-ttu-id="6ce9b-115">Первая точка (0, 10) связана с первым цветом (красным), а вторая точка (200, 10) связана со вторым цветом (синим).</span><span class="sxs-lookup"><span data-stu-id="6ce9b-115">The first point (0, 10) is associated with the first color (red), and the second point (200, 10) is associated with the second color (blue).</span></span> <span data-ttu-id="6ce9b-116">Как и следовало ожидания, линия, нарисованная от (0,0) до (200, 10), постепенно меняется от красного к синему.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-116">As you would expect, the line drawn from (0, 10) to (200, 10) changes gradually from red to blue.</span></span>

<span data-ttu-id="6ce9b-117">10 в точках (50, 10) и (200, 10) не важны.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-117">The 10s in the points (50, 10) and (200, 10) are not important.</span></span> <span data-ttu-id="6ce9b-118">Важно то, что две точки имеют одинаковую вторую координату — линия, соединяющая их, является горизонтальной.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-118">What's important is that the two points have the same second coordinate — the line connecting them is horizontal.</span></span> <span data-ttu-id="6ce9b-119">Эллипс и прямоугольник также постепенно меняются от красного к голубому, так как горизонтальная координата — от 0 до 200.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-119">The ellipse and the rectangle also change gradually from red to blue as the horizontal coordinate goes from 0 to 200.</span></span>

<span data-ttu-id="6ce9b-120">На следующем рисунке показана линия, эллипс и прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-120">The following illustration shows the line, the ellipse, and the rectangle.</span></span> <span data-ttu-id="6ce9b-121">Обратите внимание, что цветовой градиент повторяется, так как горизонтальная координата возрастает за пределами 200.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-121">Note that the color gradient repeats itself as the horizontal coordinate increases beyond 200.</span></span>

![Иллюстрация, показывающая горизонтальный градиент, который заполняет линию и эллипс, и прямоугольник, который длиннее эллипса](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a><span data-ttu-id="6ce9b-123">Настройка линейных градиентов</span><span class="sxs-lookup"><span data-stu-id="6ce9b-123">Customizing Linear Gradients</span></span>

<span data-ttu-id="6ce9b-124">В предыдущем примере компоненты цвета меняются линейно по мере перемещения от горизонтальной координаты 0 к горизонтальной координате 200.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-124">In the preceding example, the color components change linearly as you move from a horizontal coordinate of 0 to a horizontal coordinate of 200.</span></span> <span data-ttu-id="6ce9b-125">Например, точка, первая координата которой находится на расстоянии от 0 до 200, будет иметь синий компонент, наполовину от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-125">For example, a point whose first coordinate is halfway between 0 and 200 will have a blue component that is halfway between 0 and 255.</span></span>

<span data-ttu-id="6ce9b-126">GDI+ позволяет настраивать способ изменения цвета от одного края градиента к другому.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-126">GDI+ allows you to adjust the way a color varies from one edge of a gradient to the other.</span></span> <span data-ttu-id="6ce9b-127">Предположим, что необходимо создать градиентную кисть, которая меняется с черного на красный в соответствии со следующей таблицей.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-127">Suppose you want to create a gradient brush that changes from black to red according to the following table.</span></span>



| <span data-ttu-id="6ce9b-128">Координата по горизонтали</span><span class="sxs-lookup"><span data-stu-id="6ce9b-128">Horizontal coordinate</span></span> | <span data-ttu-id="6ce9b-129">Компоненты RGB</span><span class="sxs-lookup"><span data-stu-id="6ce9b-129">RGB components</span></span> |
|-----------------------|----------------|
| <span data-ttu-id="6ce9b-130">0</span><span class="sxs-lookup"><span data-stu-id="6ce9b-130">0</span></span>                     | <span data-ttu-id="6ce9b-131">(0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="6ce9b-131">(0, 0, 0)</span></span>      |
| <span data-ttu-id="6ce9b-132">40</span><span class="sxs-lookup"><span data-stu-id="6ce9b-132">40</span></span>                    | <span data-ttu-id="6ce9b-133">(128, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="6ce9b-133">(128, 0, 0)</span></span>    |
| <span data-ttu-id="6ce9b-134">200</span><span class="sxs-lookup"><span data-stu-id="6ce9b-134">200</span></span>                   | <span data-ttu-id="6ce9b-135">(255, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="6ce9b-135">(255, 0, 0)</span></span>    |



 

<span data-ttu-id="6ce9b-136">Обратите внимание, что красный компонент имеет половину интенсивность, когда горизонтальная координата составляет всего 20% от 0 до 200.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-136">Note that the red component is at half intensity when the horizontal coordinate is only 20 percent of the way from 0 to 200.</span></span>

<span data-ttu-id="6ce9b-137">В следующем примере вызывается метод [**LinearGradientBrush:: сетбленд**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) объекта [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) , чтобы связать три относительных интенситиес с тремя относительными позициями.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-137">The following example calls the [**LinearGradientBrush::SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) method of a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) object to associate three relative intensities with three relative positions.</span></span> <span data-ttu-id="6ce9b-138">Как и в предыдущей таблице, относительная интенсивность 0,5 связана с относительной позицией 0,2.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-138">As in the preceding table, a relative intensity of 0.5 is associated with a relative position of 0.2.</span></span> <span data-ttu-id="6ce9b-139">Код заполняет эллипс и прямоугольник с помощью градиентной кисти.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-139">The code fills an ellipse and a rectangle with the gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 0, 0, 0),     // opaque black 
   Color(255, 255, 0, 0));  // opaque red

REAL relativeIntensities[] = {0.0f, 0.5f, 1.0f};
REAL relativePositions[]   = {0.0f, 0.2f, 1.0f};

linGrBrush.SetBlend(relativeIntensities, relativePositions, 3);

graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="6ce9b-140">На следующем рисунке показан итоговый эллипс и прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-140">The following illustration shows the resulting ellipse and rectangle.</span></span>

![Иллюстрация, демонстрирующая горизонтальный градиент, который заполняет эллипс и прямоугольник, который длиннее эллипса](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a><span data-ttu-id="6ce9b-142">Диагональные линейные градиенты</span><span class="sxs-lookup"><span data-stu-id="6ce9b-142">Diagonal Linear Gradients</span></span>

<span data-ttu-id="6ce9b-143">Градиенты в предыдущих примерах были горизонтальными; Это значит, что цвет меняется постепенно по мере перемещения вдоль любой горизонтальной линии.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-143">The gradients in the preceding examples have been horizontal; that is, the color changes gradually as you move along any horizontal line.</span></span> <span data-ttu-id="6ce9b-144">Можно также определить вертикальные градиенты и диагональные градиенты.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-144">You can also define vertical gradients and diagonal gradients.</span></span> <span data-ttu-id="6ce9b-145">Следующий код передает точки (0, 0) и (200, 100) в конструктор [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="6ce9b-145">The following code passes the points (0, 0) and (200, 100) to a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor.</span></span> <span data-ttu-id="6ce9b-146">Цвет синего цвета связан с (0, 0), а зеленый цвет связан с (200, 100).</span><span class="sxs-lookup"><span data-stu-id="6ce9b-146">The color blue is associated with (0, 0), and the color green is associated with (200, 100).</span></span> <span data-ttu-id="6ce9b-147">Линия (с толщиной пера 10) и эллипс заполняются с помощью кисти линейного градиента.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-147">A line (with pen width 10) and an ellipse are filled with the linear gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 0),
   Point(200, 100),
   Color(255, 0, 0, 255),   // opaque blue
   Color(255, 0, 255, 0));  // opaque green

Pen pen(&linGrBrush, 10);

graphics.DrawLine(&pen, 0, 0, 600, 300);
graphics.FillEllipse(&linGrBrush, 10, 100, 200, 100);
```



<span data-ttu-id="6ce9b-148">На следующем рисунке показана линия и эллипс.</span><span class="sxs-lookup"><span data-stu-id="6ce9b-148">The following illustration shows the line and the ellipse.</span></span> <span data-ttu-id="6ce9b-149">Обратите внимание, что цвет эллипса постепенно меняется по мере перемещения вдоль любой линии, которая находится параллельно с линией, проходящего через (0, 0) и (200, 100).</span><span class="sxs-lookup"><span data-stu-id="6ce9b-149">Note that the color in the ellipse changes gradually as you move along any line that is parallel to the line passing through (0, 0) and (200, 100).</span></span>

![Иллюстрация, показывающая диагональный градиент, который заполняет эллипс и диагональную линию](images/lineargradient3.png)

 

 



