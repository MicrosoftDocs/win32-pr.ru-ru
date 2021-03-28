---
description: Начало или конец строки можно нарисовать в одной из нескольких фигур, именуемых наконечниками конца строки. Windows GDI+ поддерживает несколько отрезков строки, например круг, квадрат, ромб и наконечник.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Рисование линии с наконечниками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee4dd12a3068fe5200e0f1ae786765170ccba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987956"
---
# <a name="drawing-a-line-with-line-caps"></a><span data-ttu-id="508f0-104">Рисование линии с наконечниками</span><span class="sxs-lookup"><span data-stu-id="508f0-104">Drawing a Line with Line Caps</span></span>

<span data-ttu-id="508f0-105">Начало или конец строки можно нарисовать в одной из нескольких фигур, именуемых наконечниками конца строки.</span><span class="sxs-lookup"><span data-stu-id="508f0-105">You can draw the start or end of a line in one of several shapes called line caps.</span></span> <span data-ttu-id="508f0-106">Windows GDI+ поддерживает несколько отрезков строки, например круг, квадрат, ромб и наконечник.</span><span class="sxs-lookup"><span data-stu-id="508f0-106">Windows GDI+ supports several line caps, such as round, square, diamond, and arrowhead.</span></span>

<span data-ttu-id="508f0-107">Можно указать концы строк в начале строки (начало), конец строки (конец) или тире штриховой линии (пунктирная линия).</span><span class="sxs-lookup"><span data-stu-id="508f0-107">You can specify line caps for the start of a line (start cap), the end of a line (end cap), or the dashes of a dashed line (dash cap).</span></span>

<span data-ttu-id="508f0-108">В следующем примере рисуется линия с наконечником стрелки в одном конце и круглым наконечником на другом конце:</span><span class="sxs-lookup"><span data-stu-id="508f0-108">The following example draws a line with an arrowhead at one end and a round cap at the other end:</span></span>


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



<span data-ttu-id="508f0-109">На следующем рисунке показана результирующая строка.</span><span class="sxs-lookup"><span data-stu-id="508f0-109">The following illustration shows the resulting line.</span></span>

![Иллюстрация, показывающая горизонтальную линию со стрелкой в левой части и окружностью справа](images/pens4.png)

<span data-ttu-id="508f0-111">**Линекапаррованчор** и **линекапраунданчор** являются элементами перечисления [**линекап**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) .</span><span class="sxs-lookup"><span data-stu-id="508f0-111">**LineCapArrowAnchor** and **LineCapRoundAnchor** are elements of the [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) enumeration.</span></span>

 

 



