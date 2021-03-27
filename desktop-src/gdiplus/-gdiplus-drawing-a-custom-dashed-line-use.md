---
description: Windows GDI+ предоставляет несколько стилей штриха, перечисленных в перечислении DashStyle. Если эти стандартные стили штриха не соответствуют вашим потребностям, можно создать пользовательский шаблон штриха.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Рисование пользовательской пунктирной линии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e108dcd6b32a47befcdd99d1f23e90c33d08446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987840"
---
# <a name="drawing-a-custom-dashed-line"></a><span data-ttu-id="0798a-104">Рисование пользовательской пунктирной линии</span><span class="sxs-lookup"><span data-stu-id="0798a-104">Drawing a Custom Dashed Line</span></span>

<span data-ttu-id="0798a-105">Windows GDI+ предоставляет несколько стилей штриха, перечисленных в перечислении [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) .</span><span class="sxs-lookup"><span data-stu-id="0798a-105">Windows GDI+ provides several dash styles that are listed in the [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) enumeration.</span></span> <span data-ttu-id="0798a-106">Если эти стандартные стили штриха не соответствуют вашим потребностям, можно создать пользовательский шаблон штриха.</span><span class="sxs-lookup"><span data-stu-id="0798a-106">If those standard dash styles don't suit your needs, you can create a custom dash pattern.</span></span>

<span data-ttu-id="0798a-107">Чтобы нарисовать пользовательскую пунктирную линию, поместите длины дефисов и пробелов в массив и передайте адрес массива в качестве аргумента методу [**Pen:: сетдашпаттерн**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) объекта [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="0798a-107">To draw a custom dashed line, put the lengths of the dashes and spaces in an array and pass the address of the array as an argument to the [**Pen::SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) method of a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="0798a-108">В следующем примере рисуется пользовательская пунктирная линия, основанная на массиве {5, 2, 15, 4}.</span><span class="sxs-lookup"><span data-stu-id="0798a-108">The following example draws a custom dashed line based on the array {5, 2, 15, 4}.</span></span> <span data-ttu-id="0798a-109">Если вы умножаете элементы массива на ширину пера, равную 5, вы получаете {25, 10, 75, 20}.</span><span class="sxs-lookup"><span data-stu-id="0798a-109">If you multiply the elements of the array by the pen width of 5, you get {25, 10, 75, 20}.</span></span> <span data-ttu-id="0798a-110">Длина отображаемых штрихов в диапазоне от 25 до 75, а длина пробелов в диапазоне от 10 до 20.</span><span class="sxs-lookup"><span data-stu-id="0798a-110">The displayed dashes alternate in length between 25 and 75, and the spaces alternate in length between 10 and 20.</span></span>


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



<span data-ttu-id="0798a-111">На следующем рисунке показана полученная пунктирная линия.</span><span class="sxs-lookup"><span data-stu-id="0798a-111">The following illustration shows the resulting dashed line.</span></span> <span data-ttu-id="0798a-112">Обратите внимание, что конечный дефис должен быть короче 25 единиц, чтобы строка могла заканчиваться на (405, 5).</span><span class="sxs-lookup"><span data-stu-id="0798a-112">Note that the final dash has to be shorter than 25 units so that the line can end at (405, 5).</span></span>

![Иллюстрация, показывающая пунктирную линию; Каждый сегмент представляет собой короткую строку, за которой следует длинная единица](images/pens6.png)

 

 



