---
description: Глобальное преобразование — это преобразование, которое применяется к каждому элементу, рисуемому данным графическим объектом.
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: Глобальные и локальные преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556120"
---
# <a name="global-and-local-transformations"></a><span data-ttu-id="cea79-103">Глобальные и локальные преобразования</span><span class="sxs-lookup"><span data-stu-id="cea79-103">Global and Local Transformations</span></span>

<span data-ttu-id="cea79-104">Глобальное преобразование — это преобразование, которое применяется к каждому элементу, рисуемому данным [**графическим**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объектом.</span><span class="sxs-lookup"><span data-stu-id="cea79-104">A global transformation is a transformation that applies to every item drawn by a given [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="cea79-105">Чтобы создать глобальное преобразование, создайте объект **Graphics** , а затем вызовите его метод [**Graphics:: сеттрансформ**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) .</span><span class="sxs-lookup"><span data-stu-id="cea79-105">To create a global transformation, construct a **Graphics** object, and then call its [**Graphics::SetTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) method.</span></span> <span data-ttu-id="cea79-106">Метод **Graphics:: сеттрансформ** управляет объектом [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , связанным с **графическим** объектом.</span><span class="sxs-lookup"><span data-stu-id="cea79-106">The **Graphics::SetTransform** method manipulates a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object that is associated with the **Graphics** object.</span></span> <span data-ttu-id="cea79-107">Преобразование, хранящееся в этом объекте **Matrix** , называется *мировым преобразованием*.</span><span class="sxs-lookup"><span data-stu-id="cea79-107">The transformation stored in that **Matrix** object is called the *world transformation*.</span></span> <span data-ttu-id="cea79-108">Преобразование «мир» может быть простым аффинное преобразованием или сложной последовательностью аффинных преобразований, но независимо от его сложности, преобразование «мир» хранится в одном объекте **Matrix** .</span><span class="sxs-lookup"><span data-stu-id="cea79-108">The world transformation can be a simple affine transformation or a complex sequence of affine transformations, but regardless of its complexity, the world transformation is stored in a single **Matrix** object.</span></span>

<span data-ttu-id="cea79-109">Класс [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) предоставляет несколько методов для создания составного универсального преобразования: [**Graphics:: мултиплитрансформ**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics:: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)и [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span><span class="sxs-lookup"><span data-stu-id="cea79-109">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides several methods for building up a composite world transformation: [**Graphics::MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics::ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform), and [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span></span> <span data-ttu-id="cea79-110">В следующем примере эллипс рисуется дважды: один раз перед созданием универсального преобразования и после.</span><span class="sxs-lookup"><span data-stu-id="cea79-110">The following example draws an ellipse twice: once before creating a world transformation and once after.</span></span> <span data-ttu-id="cea79-111">Преобразование сначала масштабируется с коэффициента 0,5 в направлении по оси y, затем преобразует 50 единиц в направлении x, а затем поворачивает на 30 градусов.</span><span class="sxs-lookup"><span data-stu-id="cea79-111">The transformation first scales by a factor of 0.5 in the y direction, then translates 50 units in the x direction, and then rotates 30 degrees.</span></span>


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



<span data-ttu-id="cea79-112">На следующем рисунке показан исходный эллипс и преобразованный эллипс.</span><span class="sxs-lookup"><span data-stu-id="cea79-112">The following illustration shows the original ellipse and the transformed ellipse.</span></span>

![снимок экрана: окно, содержащее два перекрывающихся эллипса; один из них является более узким и повернутым](images/aboutgdip05-art14.png)

> [!Note]  
> <span data-ttu-id="cea79-114">В предыдущем примере эллипс поворачивается относительно начала координат системы координат, расположенного в верхнем левом углу клиентской области.</span><span class="sxs-lookup"><span data-stu-id="cea79-114">In the previous example, the ellipse is rotated about the origin of the coordinate system, which is at the upper–left corner of the client area.</span></span> <span data-ttu-id="cea79-115">Результат будет отличаться от того, на котором вращается эллипс относительно своего центра.</span><span class="sxs-lookup"><span data-stu-id="cea79-115">This produces a different result than rotating the ellipse about its own center.</span></span>

 

<span data-ttu-id="cea79-116">Локальное преобразование — это преобразование, которое применяется к конкретному рисуемому элементу.</span><span class="sxs-lookup"><span data-stu-id="cea79-116">A local transformation is a transformation that applies to a specific item to be drawn.</span></span> <span data-ttu-id="cea79-117">Например, объект [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) имеет метод [**GraphicsPath:: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) , позволяющий преобразовывать точки данных этого пути.</span><span class="sxs-lookup"><span data-stu-id="cea79-117">For example, a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object has a [**GraphicsPath::Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) method that allows you to transform the data points of that path.</span></span> <span data-ttu-id="cea79-118">В следующем примере демонстрируется рисование прямоугольника без преобразования и контура с преобразованием «вращение».</span><span class="sxs-lookup"><span data-stu-id="cea79-118">The following example draws a rectangle with no transformation and a path with a rotation transformation.</span></span> <span data-ttu-id="cea79-119">(Предположим, что нет универсального преобразования.)</span><span class="sxs-lookup"><span data-stu-id="cea79-119">(Assume that there is no world transformation.)</span></span>


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="cea79-120">Можно сочетать преобразование «мир» с локальными преобразованиями для получения различных результатов.</span><span class="sxs-lookup"><span data-stu-id="cea79-120">You can combine the world transformation with local transformations to achieve a variety of results.</span></span> <span data-ttu-id="cea79-121">Например, можно использовать преобразование «мир» для изменения системы координат и использования локальных преобразований для вращения и масштабирования объектов, рисуемых в новой системе координат.</span><span class="sxs-lookup"><span data-stu-id="cea79-121">For example, you can use the world transformation to revise the coordinate system and use local transformations to rotate and scale objects drawn on the new coordinate system.</span></span>

<span data-ttu-id="cea79-122">Предположим, что требуется система координат с координатами 200 пикселей от левого края клиентской области и 150 пикселей от верхней части клиентской области.</span><span class="sxs-lookup"><span data-stu-id="cea79-122">Suppose you want a coordinate system that has its origin 200 pixels from the left edge of the client area and 150 pixels from the top of the client area.</span></span> <span data-ttu-id="cea79-123">Кроме того, предположим, что вы хотите, чтобы единица измерения была в пикселе, ось x указывала вправо, а ось y направлена вверх.</span><span class="sxs-lookup"><span data-stu-id="cea79-123">Furthermore, assume that you want the unit of measure to be the pixel, with the x-axis pointing to the right and the y-axis pointing up.</span></span> <span data-ttu-id="cea79-124">В системе координат по умолчанию ось y направлена вниз, поэтому необходимо выполнить отражение по горизонтальной оси.</span><span class="sxs-lookup"><span data-stu-id="cea79-124">The default coordinate system has the y-axis pointing down, so you need to perform a reflection across the horizontal axis.</span></span> <span data-ttu-id="cea79-125">На следующем рисунке показана матрица такого отражения.</span><span class="sxs-lookup"><span data-stu-id="cea79-125">The following illustration shows the matrix of such a reflection.</span></span>

![Иллюстрация, демонстрирующая матрицу "три-три"](images/aboutgdip05-art15.png)

<span data-ttu-id="cea79-127">Затем предположим, что вам нужно выполнить перевод единиц измерения 200 в правый и 150 единиц.</span><span class="sxs-lookup"><span data-stu-id="cea79-127">Next, assume you need to perform a translation 200 units to the right and 150 units down.</span></span>

<span data-ttu-id="cea79-128">В следующем примере определяется система координат, только что описанная заданием универсального преобразования [**графического**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта.</span><span class="sxs-lookup"><span data-stu-id="cea79-128">The following example establishes the coordinate system just described by setting the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



<span data-ttu-id="cea79-129">Следующий код (помещается после кода в предыдущем примере) создает путь, состоящий из одного прямоугольника с нижним левым углом в источнике новой системы координат.</span><span class="sxs-lookup"><span data-stu-id="cea79-129">The following code (placed after the code in the preceding example) creates a path that consists of a single rectangle with its lower-left corner at the origin of the new coordinate system.</span></span> <span data-ttu-id="cea79-130">Прямоугольник заполняется один раз без локального преобразования и один раз с локальным преобразованием.</span><span class="sxs-lookup"><span data-stu-id="cea79-130">The rectangle is filled once with no local transformation and once with a local transformation.</span></span> <span data-ttu-id="cea79-131">Локальное преобразование состоит из горизонтального масштабирования с коэффициентом 2, за которым следует поворот на 30 градусов.</span><span class="sxs-lookup"><span data-stu-id="cea79-131">The local transformation consists of a horizontal scaling by a factor of 2 followed by a 30-degree rotation.</span></span>


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



<span data-ttu-id="cea79-132">На следующем рисунке показана новая система координат и два прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="cea79-132">The following illustration shows the new coordinate system and the two rectangles.</span></span>

![снимок экрана оси x и y и синий квадрат, наложенный полупрозрачным ректаглем вокруг нижнего левого угла](images/aboutgdip05-art16.png)

 

 



