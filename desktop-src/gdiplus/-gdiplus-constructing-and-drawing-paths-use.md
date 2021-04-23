---
description: Путь — это последовательность графических примитивов (линий, прямоугольников, кривых, текста и т. д.), которыми можно манипулировать и рисовать как единое целое. Путь можно разделить на фигуры, которые либо открыты, либо закрыты. Фигура может содержать несколько примитивов.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Построение и рисование контуров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe5f1528e58e3df19afbc83bb6acfdc2a6fca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997519"
---
# <a name="constructing-and-drawing-paths"></a><span data-ttu-id="46768-105">Построение и рисование контуров</span><span class="sxs-lookup"><span data-stu-id="46768-105">Constructing and Drawing Paths</span></span>

<span data-ttu-id="46768-106">Путь — это последовательность графических примитивов (линий, прямоугольников, кривых, текста и т. д.), которыми можно манипулировать и рисовать как единое целое.</span><span class="sxs-lookup"><span data-stu-id="46768-106">A path is a sequence of graphics primitives (lines, rectangles, curves, text, and the like) that can be manipulated and drawn as a single unit.</span></span> <span data-ttu-id="46768-107">Путь можно разделить на *фигуры* , которые либо открыты, либо закрыты.</span><span class="sxs-lookup"><span data-stu-id="46768-107">A path can be divided into *figures* that are either open or closed.</span></span> <span data-ttu-id="46768-108">Фигура может содержать несколько примитивов.</span><span class="sxs-lookup"><span data-stu-id="46768-108">A figure can contain several primitives.</span></span>

<span data-ttu-id="46768-109">Вы можете нарисовать путь, вызвав метод [**Graphics::D равпас**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , и вы можете заполнить путь, вызвав метод [**Graphics:: филлпас**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) класса **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="46768-109">You can draw a path by calling the [**Graphics::DrawPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, and you can fill a path by calling the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method of the **Graphics** class.</span></span>

<span data-ttu-id="46768-110">В следующих разделах пути рассматриваются более подробно:</span><span class="sxs-lookup"><span data-stu-id="46768-110">The following topics cover paths in more detail:</span></span>

-   [<span data-ttu-id="46768-111">Создание геометрических объектов из линий, кривых и фигур</span><span class="sxs-lookup"><span data-stu-id="46768-111">Creating Figures from Lines, Curves, and Shapes</span></span>](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [<span data-ttu-id="46768-112">Заполнение открытых фигур</span><span class="sxs-lookup"><span data-stu-id="46768-112">Filling Open Figures</span></span>](-gdiplus-filling-open-figures-use.md)

 

 



