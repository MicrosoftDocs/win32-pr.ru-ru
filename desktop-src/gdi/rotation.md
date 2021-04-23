---
description: Многие приложения САПР предоставляют функции, поворачивающие объекты, отображаемые в клиентской области.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Поворот
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17be42f2826cbad09333b2c37b607dc50c7c9d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986000"
---
# <a name="rotation"></a><span data-ttu-id="8c858-103">Поворот</span><span class="sxs-lookup"><span data-stu-id="8c858-103">Rotation</span></span>

<span data-ttu-id="8c858-104">Многие приложения САПР предоставляют функции, поворачивающие объекты, отображаемые в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="8c858-104">Many CAD applications provide features that rotate objects drawn in the client area.</span></span> <span data-ttu-id="8c858-105">Приложения, которые включают возможности вращения, используют функцию [**сетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) , чтобы установить соответствующее преобразование пространства на страницу.</span><span class="sxs-lookup"><span data-stu-id="8c858-105">Applications that include rotation capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="8c858-106">Эта функция получает указатель на структуру [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) , содержащую соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="8c858-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="8c858-107">Члены eM11, eM12, eM21 и eM22 для XFORM указывают соответственно, косинус, синус, отрицательный синус и косинус угла поворота.</span><span class="sxs-lookup"><span data-stu-id="8c858-107">The eM11, eM12, eM21, and eM22 members of XFORM specify respectively, the cosine, sine, negative sine, and cosine of the angle of rotation.</span></span>

<span data-ttu-id="8c858-108">Когда происходит *вращение* , точки, составляющие объект, поворачиваются по отношению к источнику пространства координат.</span><span class="sxs-lookup"><span data-stu-id="8c858-108">When *rotation* occurs, the points that constitute an object are rotated with respect to the coordinate-space origin.</span></span> <span data-ttu-id="8c858-109">На следующем рисунке показан прямоугольник с 20 на 20 единиц, повернутый на 30 градусов при копировании из универсального пространства в пространство координат страницы.</span><span class="sxs-lookup"><span data-stu-id="8c858-109">The following illustration shows a 20-by-20-unit rectangle rotated 30 degrees when copied from world-coordinate space to page-coordinate space.</span></span>

![Иллюстрация, демонстрирующая два пространства координат; у каждого есть прямоугольник в другом расположении и с другим поворотом.](images/cstrn-11.png)

<span data-ttu-id="8c858-111">На предыдущем рисунке каждая точка в прямоугольнике была повернута на 30 градусов по отношению к источнику пространства координат.</span><span class="sxs-lookup"><span data-stu-id="8c858-111">In the preceding illustration, each point in the rectangle was rotated 30 degrees with respect to the coordinate-space origin.</span></span>

<span data-ttu-id="8c858-112">Следующий алгоритм выполняет вычисление новой координаты x (x) для точки (x, y), которая поворачивается углом A относительно начала координат пространства.</span><span class="sxs-lookup"><span data-stu-id="8c858-112">The following algorithm computes the new x-coordinate (x ') for a point (x,y ) that is rotated by angle A with respect to the coordinate-space origin.</span></span>

``` syntax
x' = (x * cos A) - (y * sin A) 
```

<span data-ttu-id="8c858-113">Следующий алгоритм выполняет вычисление координаты y (y) для точки (x, y), которая поворачивается углом A относительно начала координат.</span><span class="sxs-lookup"><span data-stu-id="8c858-113">The following algorithm computes the y-coordinate (y ') for a point (x,y ) that is rotated by the angle A with respect to the origin.</span></span>

``` syntax
y' = (x * sin A) + (y * cos A) 
```

<span data-ttu-id="8c858-114">Два преобразования вращения можно объединить в матрицу 2-2, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="8c858-114">The two rotation transformations can be combined in a 2-by-2 matrix as follows.</span></span>

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

<span data-ttu-id="8c858-115">Матрица размером 2 на 2, которая вызвала вращение, содержит следующие значения.</span><span class="sxs-lookup"><span data-stu-id="8c858-115">The 2-by-2 matrix that produced the rotation contains the following values.</span></span>

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a><span data-ttu-id="8c858-116">Наследование алгоритма вращения</span><span class="sxs-lookup"><span data-stu-id="8c858-116">Rotation Algorithm Derivation</span></span>

<span data-ttu-id="8c858-117">Алгоритмы вращения основаны на сложения тригонометрических функций, теорема о том, что тригонометрическая сумма двух углов (a1 и a2) может быть выражена в виде тригонометрических функции двух углов.</span><span class="sxs-lookup"><span data-stu-id="8c858-117">Rotation algorithms are based on trigonometry's addition theorem stating that the trigonometric function of a sum of two angles (A1 and A2 ) can be expressed in terms of the trigonometric functions of the two angles.</span></span>

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

<span data-ttu-id="8c858-118">На следующем рисунке показана точка p, повернутая против часовой стрелки, в новую позицию p.</span><span class="sxs-lookup"><span data-stu-id="8c858-118">The following illustration shows a point p rotated counterclockwise to a new position p'.</span></span> <span data-ttu-id="8c858-119">Кроме того, в нем показаны два треугольника, образованные линией, нарисованной от источника пространства координат до каждой точки, и линия, нарисованная из каждой точки через ось x.</span><span class="sxs-lookup"><span data-stu-id="8c858-119">In addition, it shows two triangles formed by a line drawn from the coordinate-space origin to each point and a line drawn from each point through the x-axis.</span></span>

![Схема, показывающая происхождение, p и p, и два треугольника](images/cstrn-12.png)

<span data-ttu-id="8c858-121">С помощью тригонометрии Координата x точки p можно получить, умножив длину гипотенузы h на косинус a1.</span><span class="sxs-lookup"><span data-stu-id="8c858-121">Using trigonometry, the x-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the cosine of A1.</span></span>

``` syntax
x = h * cos A1 
```

<span data-ttu-id="8c858-122">Координату y точки p можно получить, умножив длину гипотенузы h на синус a1.</span><span class="sxs-lookup"><span data-stu-id="8c858-122">The y-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the sine of A1.</span></span>

``` syntax
y = h * sin A1 
```

<span data-ttu-id="8c858-123">Аналогичным образом можно получить координату x точки p ", умножив длину гипотенузы h на косинус (a1 + a2).</span><span class="sxs-lookup"><span data-stu-id="8c858-123">Likewise, the x-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the cosine of (A1 +A2 ).</span></span>

``` syntax
x' = h * cos (A1 + A2) 
```

<span data-ttu-id="8c858-124">Наконец, координату y точки p "можно получить, умножив длину гипотенузы h на синус (a1 + a2).</span><span class="sxs-lookup"><span data-stu-id="8c858-124">Finally, the y-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the sine of (A1 +A2 ).</span></span>

``` syntax
y' = h * sin (A1 + A2) 
```

<span data-ttu-id="8c858-125">Используя сложение теорема, предыдущие алгоритмы становятся следующими:</span><span class="sxs-lookup"><span data-stu-id="8c858-125">Using the addition theorem, the preceding algorithms become the following:</span></span>

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

<span data-ttu-id="8c858-126">Алгоритмы вращения для заданной точки, повернутые по углу a2, можно получить, заменив x для каждого вхождения (h \* COS a1) и заменив y для каждого вхождения (h \* Sin a1).</span><span class="sxs-lookup"><span data-stu-id="8c858-126">The rotation algorithms for a given point rotated by angle A2 can be obtained by substituting x for each occurrence of (h \* cos A1 ) and by substituting y for each occurrence of (h \* sin A1 ).</span></span>

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



