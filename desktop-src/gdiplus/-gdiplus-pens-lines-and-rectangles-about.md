---
description: Для рисования линий с помощью Windows GDI+ необходимо создать графический объект и объект Pen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Перья, линии и прямоугольники
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e9749b1c1af6ca4808e797d016267bb251e6fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985140"
---
# <a name="pens-lines-and-rectangles"></a><span data-ttu-id="f7137-103">Перья, линии и прямоугольники</span><span class="sxs-lookup"><span data-stu-id="f7137-103">Pens, Lines, and Rectangles</span></span>

<span data-ttu-id="f7137-104">Для рисования линий с помощью Windows GDI+ необходимо создать [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="f7137-104">To draw lines with Windows GDI+ you need to create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="f7137-105">Объект **Graphics** предоставляет методы, которые на самом деле выполняют рисование, а объект **Pen** сохраняет атрибуты линии, такие как цвет, ширина и стиль.</span><span class="sxs-lookup"><span data-stu-id="f7137-105">The **Graphics** object provides the methods that actually do the drawing, and the **Pen** object stores attributes of the line, such as color, width, and style.</span></span> <span data-ttu-id="f7137-106">Рисование линии — это просто вопрос вызова метода [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) объекта **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="f7137-106">Drawing a line is simply a matter of calling the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object.</span></span> <span data-ttu-id="f7137-107">Адрес объекта **Pen** передается в качестве одного из аргументов метода DrawLine.</span><span class="sxs-lookup"><span data-stu-id="f7137-107">The address of the **Pen** object is passed as one of the arguments to the DrawLine method.</span></span> <span data-ttu-id="f7137-108">В следующем примере рисуется линия с точки (4, 2) до точки (12, 6).</span><span class="sxs-lookup"><span data-stu-id="f7137-108">The following example draws a line from the point (4, 2) to the point (12, 6).</span></span>


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



<span data-ttu-id="f7137-109">Метод [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) является перегруженным методом класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , поэтому существует несколько способов указать его с аргументами.</span><span class="sxs-lookup"><span data-stu-id="f7137-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="f7137-110">Например, можно создать два объекта [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) и передать ссылки на объекты **Point** в качестве аргументов метода DrawLine.</span><span class="sxs-lookup"><span data-stu-id="f7137-110">For example, you can construct two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects and pass references to the **Point** objects as arguments to the DrawLine method.</span></span>


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



<span data-ttu-id="f7137-111">При создании объекта [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) можно указать определенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="f7137-111">You can specify certain attributes when you construct a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="f7137-112">Например, один конструктор [пера](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) позволяет указать цвет и ширину.</span><span class="sxs-lookup"><span data-stu-id="f7137-112">For example, one [Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) constructor allows you to specify color and width.</span></span> <span data-ttu-id="f7137-113">В следующем примере рисуется синяя линия толщины 2 из (0, 0) до (60, 30).</span><span class="sxs-lookup"><span data-stu-id="f7137-113">The following example draws a blue line of width 2 from (0, 0) to (60, 30).</span></span>


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



<span data-ttu-id="f7137-114">Объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) также имеет атрибуты, например тип штриха, который можно использовать для указания характеристик линии.</span><span class="sxs-lookup"><span data-stu-id="f7137-114">The [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object also has attributes, such as dash style, that you can use to specify features of the line.</span></span> <span data-ttu-id="f7137-115">Например, в следующем примере пунктирная линия рисуется от (100, 50) до (300, 80).</span><span class="sxs-lookup"><span data-stu-id="f7137-115">For example, the following example draws a dashed line from (100, 50) to (300, 80).</span></span>


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



<span data-ttu-id="f7137-116">Можно использовать различные методы объекта [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) для задания множества дополнительных атрибутов линии.</span><span class="sxs-lookup"><span data-stu-id="f7137-116">You can use various methods of the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to set many more attributes of the line.</span></span> <span data-ttu-id="f7137-117">Методы [**Pen:: сетстарткап**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) и [**Pen:: сетендкап**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) определяют внешний вид концов линии. конечными элементами могут быть плоские, квадратные, скругленные, треугольные или пользовательские фигуры.</span><span class="sxs-lookup"><span data-stu-id="f7137-117">The [**Pen::SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) and [**Pen::SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) methods specify the appearance of the ends of the line; the ends can be flat, square, rounded, triangular, or a custom shape.</span></span> <span data-ttu-id="f7137-118">Метод [**Pen:: сетлинежоин**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) позволяет указать, будут ли Соединенные линии отсечены друг от друга (соединены с острыми углами), рельефными, скругленными или обрезанными.</span><span class="sxs-lookup"><span data-stu-id="f7137-118">The [**Pen::SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method lets you specify whether connected lines are mitered (joined with sharp corners), beveled, rounded, or clipped.</span></span> <span data-ttu-id="f7137-119">На следующем рисунке показаны линии с различными стилями крепления и объединения.</span><span class="sxs-lookup"><span data-stu-id="f7137-119">The following illustration shows lines with various cap and join styles.</span></span>

![Иллюстрация двух линий, демонстрирующих скругленные и круговые концы, скругленные и угловые углы и две стили стрелок](images/aboutgdip02-art04.png)

<span data-ttu-id="f7137-121">Рисование прямоугольников с помощью GDI+ похоже на рисование линий.</span><span class="sxs-lookup"><span data-stu-id="f7137-121">Drawing rectangles with GDI+ is similar to drawing lines.</span></span> <span data-ttu-id="f7137-122">Чтобы нарисовать прямоугольник, необходим [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="f7137-122">To draw a rectangle, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="f7137-123">Объект **Graphics** предоставляет метод [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) , а объект **Pen** сохраняет атрибуты, такие как толщина линии и цвет.</span><span class="sxs-lookup"><span data-stu-id="f7137-123">The **Graphics** object provides a [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores attributes, such as line width and color.</span></span> <span data-ttu-id="f7137-124">Адрес объекта **Pen** передается в метод DrawRectangle в качестве одного из аргументов.</span><span class="sxs-lookup"><span data-stu-id="f7137-124">The address of the **Pen** object is passed as one of the arguments to the DrawRectangle method.</span></span> <span data-ttu-id="f7137-125">В следующем примере показано рисование прямоугольника с верхним левым углом в (100, 50), шириной 80 и высотой 40.</span><span class="sxs-lookup"><span data-stu-id="f7137-125">The following example draws a rectangle with its upper-left corner at (100, 50), a width of 80, and a height of 40.</span></span>


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



<span data-ttu-id="f7137-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) является перегруженным методом класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , поэтому его можно указать с помощью аргументов.</span><span class="sxs-lookup"><span data-stu-id="f7137-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="f7137-127">Например, можно создать объект [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) и передать ссылку на объект **Rect** в качестве аргумента в метод DrawRectangle.</span><span class="sxs-lookup"><span data-stu-id="f7137-127">For example, you can construct a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawRectangle method.</span></span>


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



<span data-ttu-id="f7137-128">Объект [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) имеет методы для управления и сбора сведений об прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="f7137-128">A [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object has methods for manipulating and gathering information about the rectangle.</span></span> <span data-ttu-id="f7137-129">Например, методы [Deflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) и [offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) изменяют размер и расположение прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="f7137-129">For example, the [Inflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) and [Offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) methods change the size and position of the rectangle.</span></span> <span data-ttu-id="f7137-130">Метод [**Rect:: интерсектсвис**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) указывает, пересекается ли прямоугольник с другим заданным прямоугольником, а метод [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) сообщает, находится ли заданная точка внутри прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="f7137-130">The [**Rect::IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) method tells you whether the rectangle intersects another given rectangle, and the [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) method tells you whether a given point is inside the rectangle.</span></span>

 

 
