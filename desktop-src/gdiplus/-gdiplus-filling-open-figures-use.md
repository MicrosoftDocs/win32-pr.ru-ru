---
description: 'Можно заполнить путь, передав адрес объекта GraphicsPath методу Graphics:: Филлпас.'
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Заполнение открытых фигур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f4a4608b787d8b0af8b9e9c7100a43c0c76dc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559917"
---
# <a name="filling-open-figures"></a><span data-ttu-id="d0635-103">Заполнение открытых фигур</span><span class="sxs-lookup"><span data-stu-id="d0635-103">Filling Open Figures</span></span>

<span data-ttu-id="d0635-104">Можно заполнить путь, передав адрес объекта [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) методу [**Graphics:: филлпас**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) .</span><span class="sxs-lookup"><span data-stu-id="d0635-104">You can fill a path by passing the address of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object to the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method.</span></span> <span data-ttu-id="d0635-105">Метод **Graphics:: филлпас** заполняет путь в соответствии с режимом заполнения (альтернативным или обмоткой), установленным в данный момент для пути.</span><span class="sxs-lookup"><span data-stu-id="d0635-105">The **Graphics::FillPath** method fills the path according to the fill mode (alternate or winding) currently set for the path.</span></span> <span data-ttu-id="d0635-106">Если путь содержит какие-либо открытые фигуры, то путь будет заполнен так, как будто эти фигуры были закрыты.</span><span class="sxs-lookup"><span data-stu-id="d0635-106">If the path has any open figures, the path is filled as if those figures were closed.</span></span> <span data-ttu-id="d0635-107">GDI+ закрывает фигуру, рисуя прямую линию от конечной точки до ее начальной точки.</span><span class="sxs-lookup"><span data-stu-id="d0635-107">GDI+ closes a figure by drawing a straight line from its ending point to its starting point.</span></span>

<span data-ttu-id="d0635-108">В следующем примере создается путь, который содержит одну открытую фигуру (дугу) и одну замкнутую фигуру (эллипс).</span><span class="sxs-lookup"><span data-stu-id="d0635-108">The following example creates a path that has one open figure (an arc) and one closed figure (an ellipse).</span></span> <span data-ttu-id="d0635-109">Метод [**Graphics:: филлпас**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) заполняет путь в соответствии с заданным по умолчанию режимом заполнения, который является филлмодеалтернате.</span><span class="sxs-lookup"><span data-stu-id="d0635-109">The [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the path according to the default fill mode, which is FillModeAlternate.</span></span>


```
GraphicsPath path;

// Add an open figure.
path.AddArc(0, 0, 150, 120, 30, 120);

// Add an intrinsically closed figure.
path.AddEllipse(50, 50, 50, 100);

Pen pen(Color(128, 0, 0, 255), 5);
SolidBrush brush(Color(255, 255, 0, 0));

// The fill mode is FillModeAlternate by default.
graphics.FillPath(&brush, &path);
graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="d0635-110">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="d0635-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="d0635-111">Обратите внимание, что путь заполнен (в соответствии с Филлмодеалтернате), как если бы открытая фигура была замкнута с помощью прямой линии от конечной точки до ее начальной точки.</span><span class="sxs-lookup"><span data-stu-id="d0635-111">Note that path is filled (according to FillModeAlternate) as if the open figure were closed by a straight line from its ending point to its starting point.</span></span>

![Иллюстрация, показывающая высоту эллипса, которая пересекает нижнюю половину расширенного эллипса; объединение заполнено, но пересечение пусто](images/fillopenpath.png)

 

 



