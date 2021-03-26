---
description: 'При создании объекта Pen можно указать ширину пера в качестве одного из аргументов конструктора. Можно также изменить ширину пера с помощью метода Pen:: Сетвидс.'
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Задание ширины и выравнивания пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca59895cc73480b054302091342c8f8f4f410b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551358"
---
# <a name="setting-pen-width-and-alignment"></a><span data-ttu-id="9adc3-104">Задание ширины и выравнивания пера</span><span class="sxs-lookup"><span data-stu-id="9adc3-104">Setting Pen Width and Alignment</span></span>

<span data-ttu-id="9adc3-105">При создании объекта [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) можно указать ширину пера в качестве одного из аргументов конструктора.</span><span class="sxs-lookup"><span data-stu-id="9adc3-105">When you create a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object, you can supply the pen width as one of the arguments to the constructor.</span></span> <span data-ttu-id="9adc3-106">Можно также изменить ширину пера с помощью метода [**Pen:: сетвидс**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) .</span><span class="sxs-lookup"><span data-stu-id="9adc3-106">You can also change the pen width by using the [**Pen::SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) method.</span></span>

<span data-ttu-id="9adc3-107">Теоретическая линия имеет нулевую ширину.</span><span class="sxs-lookup"><span data-stu-id="9adc3-107">A theoretical line has a width of zero.</span></span> <span data-ttu-id="9adc3-108">При рисовании линии Пиксели центрируются по теоретической линии.</span><span class="sxs-lookup"><span data-stu-id="9adc3-108">When you draw a line, the pixels are centered on the theoretical line.</span></span> <span data-ttu-id="9adc3-109">В следующем примере указанная строка рисуется дважды: один с черным пером толщиной 1 и один раз с зеленым пером шириной 10.</span><span class="sxs-lookup"><span data-stu-id="9adc3-109">The following example draws a specified line twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



<span data-ttu-id="9adc3-110">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="9adc3-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="9adc3-111">Зеленые пиксели и черные пиксели центрируются по теоретической линии.</span><span class="sxs-lookup"><span data-stu-id="9adc3-111">The green pixels and the black pixels are centered on the theoretical line.</span></span>

![<span data-ttu-id="9adc3-112">Иллюстрация, показывающая тонкую, диагональную, черную линию, окруженную толстой зеленой линией</span><span class="sxs-lookup"><span data-stu-id="9adc3-112">illustration showing a thin, diagonal, black line surrounded by a wide, green line</span></span> ](images/pens1a.png)

<span data-ttu-id="9adc3-113">В следующем примере указанный прямоугольник рисуется дважды: один с черным пером толщиной 1 и один раз с зеленым пером шириной 10.</span><span class="sxs-lookup"><span data-stu-id="9adc3-113">The following example draws a specified rectangle twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span> <span data-ttu-id="9adc3-114">Код передает значение **пеналигнментцентер** (элемент перечисления [**пеналигнмент**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) ) методу [**Pen:: сеталигнмент**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) , чтобы указать, что пикселы, рисуемые зеленым пером, центрируются по границе прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="9adc3-114">The code passes the value **PenAlignmentCenter** (an element of the [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) enumeration) to the [**Pen::SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) method to specify that the pixels drawn with the green pen are centered on the boundary of the rectangle.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



<span data-ttu-id="9adc3-115">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="9adc3-115">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="9adc3-116">Зеленые пиксели центрируются по теоретическому прямоугольнику, который представлен черными пикселами.</span><span class="sxs-lookup"><span data-stu-id="9adc3-116">The green pixels are centered on the theoretical rectangle, which is represented by the black pixels.</span></span>

![Иллюстрация, показывающая тонкую черную линию в фигуре прямоугольника, окруженная зеленой зеленой линией](images/pens2.png)

<span data-ttu-id="9adc3-118">Можно изменить выравнивание зеленого пера, изменив третью оператор в предыдущем примере следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9adc3-118">You can change the green pen's alignment by modifying the third statement in the preceding example as follows:</span></span>


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



<span data-ttu-id="9adc3-119">Теперь пикселы в широкой зеленой линии появятся на внутреннем прямоугольнике, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="9adc3-119">Now the pixels in the wide green line appear on the inside of the rectangle as shown in the following illustration.</span></span>

![Иллюстрация, показывающая тонкую черную линию в фигуре прямоугольник, включающую широкую зеленую линию той же фигуры](images/pens3.png)

 

 



