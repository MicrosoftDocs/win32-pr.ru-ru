---
description: Многоугольник — это замкнутая фигура с тремя или более прямыми сторонами.
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: многоугольники
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67ec2d062579df0510c100a80d06715be4199e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809640"
---
# <a name="polygons"></a><span data-ttu-id="7dd27-103">многоугольники</span><span class="sxs-lookup"><span data-stu-id="7dd27-103">Polygons</span></span>

<span data-ttu-id="7dd27-104">Многоугольник — это замкнутая фигура с тремя или более прямыми сторонами.</span><span class="sxs-lookup"><span data-stu-id="7dd27-104">A polygon is a closed figure with three or more straight sides.</span></span> <span data-ttu-id="7dd27-105">Например, треугольником является многоугольник с тремя сторонами, прямоугольник — многоугольник с четырьмя сторонами, а пятиугольник — многоугольник с пятью сторонами.</span><span class="sxs-lookup"><span data-stu-id="7dd27-105">For example, a triangle is a polygon with three sides, a rectangle is a polygon with four sides, and a pentagon is a polygon with five sides.</span></span> <span data-ttu-id="7dd27-106">На следующем рисунке показаны несколько многоугольников.</span><span class="sxs-lookup"><span data-stu-id="7dd27-106">The following illustration shows several polygons.</span></span>

![Иллюстрация, демонстрирующая пять многоугольников различных фигур, размеров и цветов](images/aboutgdip02-art07.png)

<span data-ttu-id="7dd27-108">Чтобы нарисовать многоугольник, необходим [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект, объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) и массив объектов [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (или [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)).</span><span class="sxs-lookup"><span data-stu-id="7dd27-108">To draw a polygon, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and an array of [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (or [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) objects.</span></span> <span data-ttu-id="7dd27-109">Объект **Graphics** предоставляет метод [дравполигон](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="7dd27-109">The **Graphics** object provides the [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="7dd27-110">Объект **Pen** сохраняет атрибуты многоугольника, такие как ширина и цвет линии, а массив объектов **Point** хранит точки, которые должны быть соединены прямыми линиями.</span><span class="sxs-lookup"><span data-stu-id="7dd27-110">The **Pen** object stores attributes of the polygon, such as line width and color, and the array of **Point** objects stores the points to be connected by straight lines.</span></span> <span data-ttu-id="7dd27-111">Адреса объекта **Pen** и массива объектов **Point** передаются в качестве аргументов в метод дравполигон.</span><span class="sxs-lookup"><span data-stu-id="7dd27-111">The addresses of the **Pen** object and the array of **Point** objects are passed as arguments to the DrawPolygon method.</span></span> <span data-ttu-id="7dd27-112">В следующем примере рисуется трехмерный многоугольник.</span><span class="sxs-lookup"><span data-stu-id="7dd27-112">The following example draws a three-sided polygon.</span></span> <span data-ttu-id="7dd27-113">Обратите внимание, что в **мипоинтаррай** есть только три точки: (0, 0), (50, 30) и (30, 60).</span><span class="sxs-lookup"><span data-stu-id="7dd27-113">Note that there are only three points in **myPointArray**: (0, 0), (50, 30), and (30, 60).</span></span> <span data-ttu-id="7dd27-114">Метод Дравполигон автоматически закрывает многоугольник, рисуя строку из (30, 60) обратно в начальную точку (0, 0);</span><span class="sxs-lookup"><span data-stu-id="7dd27-114">The DrawPolygon method automatically closes the polygon by drawing a line from (30, 60) back to the starting point (0, 0);</span></span>


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



<span data-ttu-id="7dd27-115">На следующем рисунке показан многоугольник.</span><span class="sxs-lookup"><span data-stu-id="7dd27-115">The following illustration shows the polygon.</span></span>

![Иллюстрация, демонстрирующая треугольник относительно осей координат](images/aboutgdip02-art08.png)

 

 



