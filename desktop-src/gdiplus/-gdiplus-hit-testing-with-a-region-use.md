---
description: Цель проверки попадания заключается в том, чтобы определить, находится ли курсор над данным объектом, например значком или кнопкой.
ms.assetid: 9776b73e-191e-4a8e-9abe-e485ffed954c
title: Проверка нажатия с использованием региона
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24913d8d890e3e1ded87eb48e2d52f1726663a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997475"
---
# <a name="hit-testing-with-a-region"></a><span data-ttu-id="974e3-103">Проверка нажатия с использованием региона</span><span class="sxs-lookup"><span data-stu-id="974e3-103">Hit Testing with a Region</span></span>

<span data-ttu-id="974e3-104">Цель проверки попадания заключается в том, чтобы определить, находится ли курсор над данным объектом, например значком или кнопкой.</span><span class="sxs-lookup"><span data-stu-id="974e3-104">The purpose of hit testing is to determine whether the cursor is over a given object, such as an icon or a button.</span></span> <span data-ttu-id="974e3-105">В следующем примере создается область в форме креста путем формирования объединения двух прямоугольных областей.</span><span class="sxs-lookup"><span data-stu-id="974e3-105">The following example creates a plus-shaped region by forming the union of two rectangular regions.</span></span> <span data-ttu-id="974e3-106">Предположим, что переменная **Point** содержит расположение самого последнего щелчка.</span><span class="sxs-lookup"><span data-stu-id="974e3-106">Assume that the variable **point** holds the location of the most recent click.</span></span> <span data-ttu-id="974e3-107">Код проверяет, находится ли **точка** в форме креста.</span><span class="sxs-lookup"><span data-stu-id="974e3-107">The code checks to see whether **point** is in the plus-shaped region.</span></span> <span data-ttu-id="974e3-108">Если **Point** находится в регионе (попадание), область заполняется непрозрачной красной кистью.</span><span class="sxs-lookup"><span data-stu-id="974e3-108">If **point** is in the region (a hit), the region is filled with an opaque red brush.</span></span> <span data-ttu-id="974e3-109">В противном случае область заполняется полупрозрачной красной кистью.</span><span class="sxs-lookup"><span data-stu-id="974e3-109">Otherwise, the region is filled with a semitransparent red brush.</span></span>


```
Point point(60, 10);
// Assume that the variable "point" contains the location
// of the most recent click.
// To simulate a hit, assign (60, 10) to point.
// To simulate a miss, assign (0, 0) to point.
SolidBrush solidBrush(Color());
Region region1(Rect(50, 0, 50, 150));
Region region2(Rect(0, 50, 150, 50));
// Create a plus-shaped region by forming the union of region1 and region2.
// The union replaces region1.
region1.Union(&region2);
if(region1.IsVisible(point, &graphics))
{
   // The point is in the region. Use an opaque brush.
   solidBrush.SetColor(Color(255, 255, 0, 0));
}
else
{
   // The point is not in the region. Use a semitransparent brush.
   solidBrush.SetColor(Color(64, 255, 0, 0));
}
graphics.FillRegion(&solidBrush, &region1);
```



 

 



