---
description: Соединение строк — это общая область, сформированная двумя строками, конец которых соответствует или перекрывается.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Соединение строк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2ab0bc53239b9a0d9327a26e25eed1c93c685b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555665"
---
# <a name="joining-lines"></a><span data-ttu-id="2138b-103">Соединение строк</span><span class="sxs-lookup"><span data-stu-id="2138b-103">Joining Lines</span></span>

<span data-ttu-id="2138b-104">Соединение строк — это общая область, сформированная двумя строками, конец которых соответствует или перекрывается.</span><span class="sxs-lookup"><span data-stu-id="2138b-104">A line join is the common area that is formed by two lines whose ends meet or overlap.</span></span> <span data-ttu-id="2138b-105">Windows GDI+ предоставляет четыре стиля соединения линий: срез, скос, круглый и срез обрезаны.</span><span class="sxs-lookup"><span data-stu-id="2138b-105">Windows GDI+ provides four line join styles: miter, bevel, round, and miter clipped.</span></span> <span data-ttu-id="2138b-106">Тип подключения линии является свойством класса [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="2138b-106">Line join style is a property of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="2138b-107">При указании стиля соединения линий для пера и последующем использовании этого пера для рисования контура заданный стиль соединения применяется ко всем подключенным линиям в пути.</span><span class="sxs-lookup"><span data-stu-id="2138b-107">When you specify a line join style for a pen and then use that pen to draw a path, the specified join style is applied to all the connected lines in the path.</span></span>

<span data-ttu-id="2138b-108">Стиль объединения линий можно указать с помощью метода [**Pen:: сетлинежоин**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) класса [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="2138b-108">You can specify the line join style by using the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="2138b-109">В следующем примере показано соединение багетной линии между горизонтальной линией и вертикальной линией:</span><span class="sxs-lookup"><span data-stu-id="2138b-109">The following example demonstrates a beveled line join between a horizontal line and a vertical line:</span></span>


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



<span data-ttu-id="2138b-110">На следующем рисунке показано соединение с рельефной линией.</span><span class="sxs-lookup"><span data-stu-id="2138b-110">The following illustration shows the resulting beveled line join.</span></span>

![Иллюстрация, показывающая две строки в правом углом с рельефным соединением](images/pens5.png)

<span data-ttu-id="2138b-112">В предыдущем примере значение (**линежоинбевел**), передаваемое методу [**Pen:: сетлинежоин**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) , является элементом перечисления [**линежоин**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) .</span><span class="sxs-lookup"><span data-stu-id="2138b-112">In the preceding example, the value (**LineJoinBevel**) passed to the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method is an element of the [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) enumeration.</span></span>

 

 



