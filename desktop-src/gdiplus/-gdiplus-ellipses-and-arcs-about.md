---
description: С ограничивающим прямоугольником задается эллипс. На следующем рисунке показан эллипс, а также его ограничивающий прямоугольник.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Эллипсы и дуги
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b1aaaff5ff27191ed7f0bf64ddbcb414be6319
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156191"
---
# <a name="ellipses-and-arcs"></a><span data-ttu-id="08c4d-104">Эллипсы и дуги</span><span class="sxs-lookup"><span data-stu-id="08c4d-104">Ellipses and Arcs</span></span>

<span data-ttu-id="08c4d-105">С ограничивающим прямоугольником задается эллипс.</span><span class="sxs-lookup"><span data-stu-id="08c4d-105">An ellipse is specified by its bounding rectangle.</span></span> <span data-ttu-id="08c4d-106">На следующем рисунке показан эллипс, а также его ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="08c4d-106">The following illustration shows an ellipse along with its bounding rectangle.</span></span>

![Иллюстрация эллипса, заключенного в ограничивающем прямоугольнике](images/aboutgdip02-art05.png)

<span data-ttu-id="08c4d-108">Чтобы нарисовать эллипс, необходим объект [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и объект [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="08c4d-108">To draw an ellipse, you need a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="08c4d-109">Объект **Graphics** предоставляет метод [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , а объект **Pen** сохраняет атрибуты эллипса, например толщину и цвет линии.</span><span class="sxs-lookup"><span data-stu-id="08c4d-109">The **Graphics** object provides the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, and the **Pen** object stores attributes of the ellipse, such as line width and color.</span></span> <span data-ttu-id="08c4d-110">Адрес объекта **Pen** передается в качестве одного из аргументов в метод DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="08c4d-110">The address of the **Pen** object is passed as one of the arguments to the DrawEllipse method.</span></span> <span data-ttu-id="08c4d-111">Остальные аргументы, передаваемые в метод DrawEllipse, задают ограничивающий прямоугольник для эллипса.</span><span class="sxs-lookup"><span data-stu-id="08c4d-111">The remaining arguments passed to the DrawEllipse method specify the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="08c4d-112">В следующем примере рисуется эллипс; ограничивающий прямоугольник имеет ширину 160, высоту 80 и левый верхний угол (100, 50).</span><span class="sxs-lookup"><span data-stu-id="08c4d-112">The following example draws an ellipse; the bounding rectangle has a width of 160, a height of 80, and an upper-left corner of (100, 50).</span></span>


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



<span data-ttu-id="08c4d-113">Метод [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) является перегруженным методом класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , поэтому существует несколько способов указать его с аргументами.</span><span class="sxs-lookup"><span data-stu-id="08c4d-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) is an overloaded method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="08c4d-114">Например, можно создать объект [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) и передать ссылку на объект **Rect** в качестве аргумента в метод DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="08c4d-114">For example, you can construct a [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawEllipse method.</span></span>


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



<span data-ttu-id="08c4d-115">Дуга — это часть эллипса.</span><span class="sxs-lookup"><span data-stu-id="08c4d-115">An arc is a portion of an ellipse.</span></span> <span data-ttu-id="08c4d-116">Чтобы нарисовать дугу, вызовите метод [драварк](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="08c4d-116">To draw an arc, you call the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="08c4d-117">Параметры метода Драварк совпадают с параметрами метода [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , за исключением того, что драварк требует начальный угол и угол поворота.</span><span class="sxs-lookup"><span data-stu-id="08c4d-117">The parameters of the DrawArc method are the same as the parameters of the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, except that DrawArc requires a starting angle and sweep angle.</span></span> <span data-ttu-id="08c4d-118">В следующем примере демонстрируется рисование дуги с начальным углом 30 градусов и углом поворота в 180 градусов.</span><span class="sxs-lookup"><span data-stu-id="08c4d-118">The following example draws an arc with a starting angle of 30 degrees and a sweep angle of 180 degrees.</span></span>


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



<span data-ttu-id="08c4d-119">На следующем рисунке показана дуга, эллипс и ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="08c4d-119">The following illustration shows the arc, the ellipse, and the bounding rectangle.</span></span>

![Иллюстрация эллипса в ограничивающем прямоугольнике; Нижняя левая половина эллипса отображается красным цветом](images/aboutgdip02-art06.png)

 

 



