---
description: Чтобы заполнить форму сплошным цветом, создайте объект SolidBrush, а затем передайте адрес этого объекта SolidBrush в качестве аргумента в один из методов Fill класса Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Заполнение фигуры сплошным цветом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4a6221d84c4a891d377d974f168468917799e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997498"
---
# <a name="filling-a-shape-with-a-solid-color"></a><span data-ttu-id="e2a30-103">Заполнение фигуры сплошным цветом</span><span class="sxs-lookup"><span data-stu-id="e2a30-103">Filling a Shape with a Solid Color</span></span>

<span data-ttu-id="e2a30-104">Чтобы заполнить форму сплошным цветом, создайте объект [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) , а затем передайте адрес этого объекта **SolidBrush** в качестве аргумента в один из методов Fill класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="e2a30-104">To fill a shape with a solid color, create a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object, and then pass the address of that **SolidBrush** object as an argument to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="e2a30-105">В следующем примере показано, как заполнить эллипс красным цветом:</span><span class="sxs-lookup"><span data-stu-id="e2a30-105">The following example shows how to fill an ellipse with the color red:</span></span>


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



<span data-ttu-id="e2a30-106">В предыдущем примере конструктор [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) принимает ссылку на объект [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) в качестве единственного аргумента.</span><span class="sxs-lookup"><span data-stu-id="e2a30-106">In the preceding example, the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor takes a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object reference as its only argument.</span></span> <span data-ttu-id="e2a30-107">Значения, используемые конструктором **Color** , представляют альфа-, красный, зеленый и синий компоненты цвета.</span><span class="sxs-lookup"><span data-stu-id="e2a30-107">The values used by the **Color** constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="e2a30-108">Каждое из этих значений должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="e2a30-108">Each of these values must be in the range 0 through 255.</span></span> <span data-ttu-id="e2a30-109">Первая 255 указывает, что цвет является полностью непрозрачным, а второй 255 указывает, что красный компонент имеет полную интенсивность.</span><span class="sxs-lookup"><span data-stu-id="e2a30-109">The first 255 indicates that the color is fully opaque, and the second 255 indicates that the red component is at full intensity.</span></span> <span data-ttu-id="e2a30-110">Два нуля указывают, что зеленый и синий компоненты имеют интенсивность 0.</span><span class="sxs-lookup"><span data-stu-id="e2a30-110">The two zeros indicate that the green and blue components both have an intensity of 0.</span></span>

<span data-ttu-id="e2a30-111">Четыре числа (0, 0, 100, 60), передаваемые методу [**Graphics:: филлеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) , определяют расположение и размер ограничивающего прямоугольника для эллипса.</span><span class="sxs-lookup"><span data-stu-id="e2a30-111">The four numbers (0, 0, 100, 60) passed to the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) method specify the location and size of the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="e2a30-112">Прямоугольник содержит левый верхний угол (0, 0), ширину 100 и высоту 60.</span><span class="sxs-lookup"><span data-stu-id="e2a30-112">The rectangle has an upper-left corner of (0, 0), a width of 100, and a height of 60.</span></span>

 

 
