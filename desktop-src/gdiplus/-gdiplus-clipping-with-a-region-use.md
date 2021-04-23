---
description: Одним из свойств класса Graphics является отсеченная область. Вся прорисовка, выполненная данным объектом Graphics, ограничена областью отсечения этого графического объекта. Можно задать отсеченную область, вызвав метод Сетклип.
ms.assetid: 816a5845-ca03-46c6-bdda-e6a7d02ff614
title: Обрезка с использованием региона
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa19426d62d5d3af99150bf9ac8e8099628fe2f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565080"
---
# <a name="clipping-with-a-region"></a><span data-ttu-id="d478b-105">Обрезка с использованием региона</span><span class="sxs-lookup"><span data-stu-id="d478b-105">Clipping with a Region</span></span>

<span data-ttu-id="d478b-106">Одним из свойств класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) является отсеченная область.</span><span class="sxs-lookup"><span data-stu-id="d478b-106">One of the properties of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the clipping region.</span></span> <span data-ttu-id="d478b-107">Вся прорисовка, выполненная данным объектом **Graphics** , ограничена областью отсечения этого **графического** объекта.</span><span class="sxs-lookup"><span data-stu-id="d478b-107">All drawing done by a given **Graphics** object is restricted to the clipping region of that **Graphics** object.</span></span> <span data-ttu-id="d478b-108">Можно задать отсеченную область, вызвав метод **сетклип** .</span><span class="sxs-lookup"><span data-stu-id="d478b-108">You can set the clipping region by calling the **SetClip** method.</span></span>

<span data-ttu-id="d478b-109">В следующем примере создается путь, состоящий из одного многоугольника.</span><span class="sxs-lookup"><span data-stu-id="d478b-109">The following example constructs a path that consists of a single polygon.</span></span> <span data-ttu-id="d478b-110">Затем код конструирует регион на основе этого пути.</span><span class="sxs-lookup"><span data-stu-id="d478b-110">Then the code constructs a region based on that path.</span></span> <span data-ttu-id="d478b-111">Адрес региона передается методу **сетклип** объекта [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , а затем рисуются две строки.</span><span class="sxs-lookup"><span data-stu-id="d478b-111">The address of the region is passed to the **SetClip** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, and then two strings are drawn.</span></span>


```
// Create a path that consists of a single polygon.
Point polyPoints[] = {Point(10, 10), Point(150, 10), 
   Point(100, 75), Point(100, 150)};
GraphicsPath path;
path.AddPolygon(polyPoints, 4);
// Construct a region based on the path.
Region region(&path);
// Draw the outline of the region.
Pen pen(Color(255, 0, 0, 0));
graphics.DrawPath(&pen, &path);
// Set the clipping region of the Graphics object.
graphics.SetClip(&region);
// Draw some clipped strings.
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 36, FontStyleBold, UnitPixel);
SolidBrush solidBrush(Color(255, 255, 0, 0));
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 25), &solidBrush);
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 68), &solidBrush);
```



<span data-ttu-id="d478b-112">На следующем рисунке показаны обрезанные строки.</span><span class="sxs-lookup"><span data-stu-id="d478b-112">The following illustration shows the clipped strings.</span></span>

![Иллюстрация, демонстрирующая части двух предложений, которые появляются в фигурной форме](images/clip1.png)

 

 



