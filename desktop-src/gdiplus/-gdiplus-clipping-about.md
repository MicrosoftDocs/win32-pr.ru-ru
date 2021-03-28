---
description: Обрезка включает в себя ограничения рисования в определенном регионе. На следующем рисунке показана строка &\# 0034; Привет&\# 0034; обрезаны до области в форме сердца.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Обрезка (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 156ae2209a3b7135cde2804103531eaf7b519d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080639"
---
# <a name="clipping-gdi"></a><span data-ttu-id="9f814-104">Обрезка (GDI+)</span><span class="sxs-lookup"><span data-stu-id="9f814-104">Clipping (GDI+)</span></span>

<span data-ttu-id="9f814-105">Обрезка включает в себя ограничения рисования в определенном регионе.</span><span class="sxs-lookup"><span data-stu-id="9f814-105">Clipping involves restricting drawing to a certain region.</span></span> <span data-ttu-id="9f814-106">На следующем рисунке показана строка "Hello", обрезанная до области в форме сердца.</span><span class="sxs-lookup"><span data-stu-id="9f814-106">The following illustration shows the string "Hello" clipped to a heart-shaped region.</span></span>

![Иллюстрация, демонстрирующая части строки "Hello" в красном сердце](images/aboutgdip02-art30.png)

<span data-ttu-id="9f814-108">Регионы можно создавать на основе контуров, а пути могут содержать контуры строк, поэтому для обрезки можно использовать обрезку текста.</span><span class="sxs-lookup"><span data-stu-id="9f814-108">Regions can be constructed from paths, and paths can contain the outlines of strings, so you can use outlined text for clipping.</span></span> <span data-ttu-id="9f814-109">На следующем рисунке показан набор концентрических эллипсов, обрезанных по внутренней части строки текста.</span><span class="sxs-lookup"><span data-stu-id="9f814-109">The following illustration shows a set of concentric ellipses clipped to the interior of a string of text.</span></span>

![Иллюстрация, показывающая строку "Hello", заполненную шаблоном концентрических кругов](images/aboutgdip02-art31.png)

<span data-ttu-id="9f814-111">Чтобы рисовать с помощью обрезки, создайте объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , вызовите его метод [сетклип](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) , а затем вызовите методы рисования такого же **графического** объекта.</span><span class="sxs-lookup"><span data-stu-id="9f814-111">To draw with clipping, create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, call its [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method, and then call the drawing methods of that same **Graphics** object.</span></span> <span data-ttu-id="9f814-112">В следующем примере рисуется линия, обрезанная до прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="9f814-112">The following example draws a line that is clipped to a rectangular region.</span></span>


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



<span data-ttu-id="9f814-113">На следующем рисунке показана прямоугольная область вместе с обрезанной линией.</span><span class="sxs-lookup"><span data-stu-id="9f814-113">The following illustration shows the rectangular region along with the clipped line.</span></span>

![Иллюстрация, демонстрирующая прямоугольник с диагональным линиям сверху вниз](images/aboutgdip02-art31a.png)

 

 



