---
description: Преобразование «мир» является свойством класса Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Использование объемного преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263045"
---
# <a name="using-the-world-transformation"></a><span data-ttu-id="09a98-103">Использование объемного преобразования</span><span class="sxs-lookup"><span data-stu-id="09a98-103">Using the World Transformation</span></span>

<span data-ttu-id="09a98-104">Преобразование «мир» является свойством класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="09a98-104">The world transformation is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="09a98-105">Числа, определяющие объемное преобразование, хранятся в объекте [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , который представляет матрицу размером 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="09a98-105">The numbers that specify the world transformation are stored in a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object, which represents a 3 ×3 matrix.</span></span> <span data-ttu-id="09a98-106">Классы **Matrix** и **Graphics** имеют несколько методов для настройки чисел в матрице универсального преобразования.</span><span class="sxs-lookup"><span data-stu-id="09a98-106">The **Matrix** and **Graphics** classes have several methods for setting the numbers in the world transformation matrix.</span></span> <span data-ttu-id="09a98-107">Примеры в этом разделе посвящены управлению прямоугольниками, так как прямоугольники легко изображать, и можно легко увидеть влияние преобразований на прямоугольники.</span><span class="sxs-lookup"><span data-stu-id="09a98-107">The examples in this section manipulate rectangles because rectangles are easy to draw and it is easy to see the effects of transformations on rectangles.</span></span>

<span data-ttu-id="09a98-108">Начнем с создания прямоугольника 50 на 50 и нахождения его в источнике (0, 0).</span><span class="sxs-lookup"><span data-stu-id="09a98-108">We start by creating a 50 by 50 rectangle and locating it at the origin (0, 0).</span></span> <span data-ttu-id="09a98-109">Источник находится в левом верхнем углу клиентской области.</span><span class="sxs-lookup"><span data-stu-id="09a98-109">The origin is at the upper-left corner of the client area.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="09a98-110">Следующий код применяет преобразование масштабирования, которое расширяет прямоугольник с коэффициентом 1,75 в направлении x и сжимает прямоугольник на множители 0,5 в направлении по оси y:</span><span class="sxs-lookup"><span data-stu-id="09a98-110">The following code applies a scaling transformation that expands the rectangle by a factor of 1.75 in the x direction and shrinks the rectangle by a factor of 0.5 in the y direction:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="09a98-111">Результатом является прямоугольник, который больше в направлении x и короче по оси y, чем у оригинала.</span><span class="sxs-lookup"><span data-stu-id="09a98-111">The result is a rectangle that is longer in the x direction and shorter in the y direction than the original.</span></span>

<span data-ttu-id="09a98-112">Чтобы повернуть прямоугольник вместо его масштабирования, используйте следующий код вместо приведенного выше кода:</span><span class="sxs-lookup"><span data-stu-id="09a98-112">To rotate the rectangle instead of scaling it, use the following code instead of the preceding code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="09a98-113">Чтобы преобразовать прямоугольник, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="09a98-113">To translate the rectangle, use the following code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



