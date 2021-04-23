---
description: 'Класс Graphics предоставляет разнообразные методы рисования, включая показанные в следующем списке:'
ms.assetid: d3c8d16c-858a-42a9-a512-3fcfa144f5fc
title: Рисование линий и фигур с помощью пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904f53149038d6109365adddc11d3c37881a8def
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144857"
---
# <a name="using-a-pen-to-draw-lines-and-shapes"></a><span data-ttu-id="e57a5-103">Рисование линий и фигур с помощью пера</span><span class="sxs-lookup"><span data-stu-id="e57a5-103">Using a Pen to Draw Lines and Shapes</span></span>

<span data-ttu-id="e57a5-104">Класс [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) предоставляет разнообразные методы рисования, включая показанные в следующем списке:</span><span class="sxs-lookup"><span data-stu-id="e57a5-104">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides a variety of drawing methods including those shown in the following list:</span></span>

-   <span data-ttu-id="e57a5-105">[Методы DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span><span class="sxs-lookup"><span data-stu-id="e57a5-105">[DrawLine Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span></span>
-   <span data-ttu-id="e57a5-106">[Методы DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="e57a5-106">[DrawRectangle Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="e57a5-107">[Методы DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="e57a5-107">[DrawEllipse Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="e57a5-108">[Методы Драварк](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span><span class="sxs-lookup"><span data-stu-id="e57a5-108">[DrawArc Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span></span>
-   [<span data-ttu-id="e57a5-109">**Графика::D Равпас**</span><span class="sxs-lookup"><span data-stu-id="e57a5-109">**Graphics::DrawPath**</span></span>](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath)
-   <span data-ttu-id="e57a5-110">[Методы Дравкурве](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="e57a5-110">[DrawCurve Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span></span>
-   <span data-ttu-id="e57a5-111">[Методы Дравбезиер](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span><span class="sxs-lookup"><span data-stu-id="e57a5-111">[DrawBezier Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span></span>

<span data-ttu-id="e57a5-112">Одним из аргументов, передаваемых в такой метод рисования, является адрес объекта [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="e57a5-112">One of the arguments that you pass to such a drawing method is the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span>

<span data-ttu-id="e57a5-113">В следующих разделах более подробно рассматривается использование перьев.</span><span class="sxs-lookup"><span data-stu-id="e57a5-113">The following topics cover the use of pens in more detail:</span></span>

-   [<span data-ttu-id="e57a5-114">Рисование линий и прямоугольников с помощью пера</span><span class="sxs-lookup"><span data-stu-id="e57a5-114">Using a Pen to Draw Lines and Rectangles</span></span>](-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use.md)
-   [<span data-ttu-id="e57a5-115">Задание ширины и выравнивания пера</span><span class="sxs-lookup"><span data-stu-id="e57a5-115">Setting Pen Width and Alignment</span></span>](-gdiplus-setting-pen-width-and-alignment-use.md)
-   [<span data-ttu-id="e57a5-116">Рисование линии с наконечниками</span><span class="sxs-lookup"><span data-stu-id="e57a5-116">Drawing a Line with Line Caps</span></span>](-gdiplus-drawing-a-line-with-line-caps-use.md)
-   [<span data-ttu-id="e57a5-117">Соединение строк</span><span class="sxs-lookup"><span data-stu-id="e57a5-117">Joining Lines</span></span>](-gdiplus-joining-lines-use.md)
-   [<span data-ttu-id="e57a5-118">Рисование пользовательской пунктирной линии</span><span class="sxs-lookup"><span data-stu-id="e57a5-118">Drawing a Custom Dashed Line</span></span>](-gdiplus-drawing-a-custom-dashed-line-use.md)
-   [<span data-ttu-id="e57a5-119">Рисование линии, заполненной текстурой</span><span class="sxs-lookup"><span data-stu-id="e57a5-119">Drawing a Line Filled with a Texture</span></span>](-gdiplus-drawing-a-line-filled-with-a-texture-use.md)

 

 



