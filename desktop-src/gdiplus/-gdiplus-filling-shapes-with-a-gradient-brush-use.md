---
description: Можно использовать градиентную кисть для заливки фигуры с постепенно изменяющимся цветом.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Заливка фигур с помощью градиентной кисти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6784d0bfd59fd37f217e8d7a1cdd230348807d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997494"
---
# <a name="filling-shapes-with-a-gradient-brush"></a><span data-ttu-id="86ef9-103">Заливка фигур с помощью градиентной кисти</span><span class="sxs-lookup"><span data-stu-id="86ef9-103">Filling Shapes with a Gradient Brush</span></span>

<span data-ttu-id="86ef9-104">Можно использовать градиентную кисть для заливки фигуры с постепенно изменяющимся цветом.</span><span class="sxs-lookup"><span data-stu-id="86ef9-104">You can use a gradient brush to fill a shape with a gradually changing color.</span></span> <span data-ttu-id="86ef9-105">Например, можно использовать горизонтальный градиент для заливки фигуры цветом, который изменяется постепенно по мере перемещения от левого края фигуры к правому краю.</span><span class="sxs-lookup"><span data-stu-id="86ef9-105">For example, you can use a horizontal gradient to fill a shape with color that changes gradually as you move from the left edge of the shape to the right edge.</span></span> <span data-ttu-id="86ef9-106">Представьте себе прямоугольник с левым ребром, который является черным (представлен красным, зеленым и синим компонентами 0, 0, 0) и правой границей красного цвета (представленной в 255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="86ef9-106">Imagine a rectangle with a left edge that is black (represented by red, green, and blue components 0, 0, 0) and a right edge that is red (represented by 255, 0, 0).</span></span> <span data-ttu-id="86ef9-107">Если размер прямоугольника составляет 256 пикселей, красный компонент данного пикселя будет на единицу больше, чем красный компонент пикселя слева.</span><span class="sxs-lookup"><span data-stu-id="86ef9-107">If the rectangle is 256 pixels wide, the red component of a given pixel will be one greater than the red component of the pixel to its left.</span></span> <span data-ttu-id="86ef9-108">В крайнем левом пикселе строки есть компоненты цвета (0, 0, 0), второй пиксель имеет (1, 0, 0), третий пиксель имеет (2, 0, 0) и т. д., пока не будет получен самый правый пиксель, имеющий компоненты цвета (255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="86ef9-108">The leftmost pixel in a row has color components (0, 0, 0), the second pixel has (1, 0, 0), the third pixel has (2, 0, 0), and so on, until you get to the rightmost pixel, which has color components (255, 0, 0).</span></span> <span data-ttu-id="86ef9-109">Эти интерполяции цветовых значений составляют градиент цвета.</span><span class="sxs-lookup"><span data-stu-id="86ef9-109">These interpolated color values make up the color gradient.</span></span>

<span data-ttu-id="86ef9-110">Линейный градиент меняет цвет при перемещении по горизонтали, по вертикали или параллельно на указанную наклонную линию.</span><span class="sxs-lookup"><span data-stu-id="86ef9-110">A linear gradient changes color as you move horizontally, vertically, or parallel to a specified slanted line.</span></span> <span data-ttu-id="86ef9-111">Цвет градиента контура изменяется при перемещении по внутреннему и границе пути.</span><span class="sxs-lookup"><span data-stu-id="86ef9-111">A path gradient changes color as you move about the interior and boundary of a path.</span></span> <span data-ttu-id="86ef9-112">Можно настроить градиенты вдоль пути для достижения широкого спектра эффектов.</span><span class="sxs-lookup"><span data-stu-id="86ef9-112">You can customize path gradients to achieve a wide variety of effects.</span></span>

<span data-ttu-id="86ef9-113">Интерфейс GDI+ предоставляет классы [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) и [**пасградиентбруш**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) , которые наследуются от класса [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="86ef9-113">GDI+ provides the [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) and [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) classes, both of which inherit from the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) class.</span></span>

<span data-ttu-id="86ef9-114">В следующих разделах более подробно рассматриваются линейные и градиенты вдоль пути:</span><span class="sxs-lookup"><span data-stu-id="86ef9-114">The following topics cover linear and path gradients in more detail:</span></span>

-   [<span data-ttu-id="86ef9-115">Создание линейного градиента</span><span class="sxs-lookup"><span data-stu-id="86ef9-115">Creating a Linear Gradient</span></span>](-gdiplus-creating-a-linear-gradient-use.md)
-   [<span data-ttu-id="86ef9-116">Создание градиента контура</span><span class="sxs-lookup"><span data-stu-id="86ef9-116">Creating a Path Gradient</span></span>](-gdiplus-creating-a-path-gradient-use.md)
-   [<span data-ttu-id="86ef9-117">Применение гамма-коррекции к градиенту</span><span class="sxs-lookup"><span data-stu-id="86ef9-117">Applying Gamma Correction to a Gradient</span></span>](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



