---
title: Специальные проблемы с переносом в ГК для ДИАФРАГМы
description: Специальные проблемы с переносом в ГК для ДИАФРАГМы
ms.assetid: dcf7967a-2867-4443-a1c8-8335c6fe016a
keywords:
- OpenGL в Windows, перенос GL по IRI
- перенос в OpenGL, IRI GL
- Перенос с OpenGL, IRI, GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1273a873f3a39a5d237f9a5845a72f87156e001c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661635"
---
# <a name="special-iris-gl-porting-issues"></a><span data-ttu-id="aa78b-106">Специальные проблемы с переносом в ГК для ДИАФРАГМы</span><span class="sxs-lookup"><span data-stu-id="aa78b-106">Special IRIS GL Porting Issues</span></span>

<span data-ttu-id="aa78b-107">В следующих разделах описываются методы переноса конкретных частей кода IRI в код OpenGL.</span><span class="sxs-lookup"><span data-stu-id="aa78b-107">The following topics describe techniques for porting specific parts of your IRIS GL code to OpenGL code.</span></span>

-   [<span data-ttu-id="aa78b-108">Перенос гресет</span><span class="sxs-lookup"><span data-stu-id="aa78b-108">Porting greset</span></span>](porting-greset.md)
-   [<span data-ttu-id="aa78b-109">Перенос функций "Get" в ГК</span><span class="sxs-lookup"><span data-stu-id="aa78b-109">Porting IRIS GL "Get" Functions</span></span>](porting-iris-gl-get-functions.md)
-   [<span data-ttu-id="aa78b-110">Перенос кода, для которого требуется текущая географические координаты</span><span class="sxs-lookup"><span data-stu-id="aa78b-110">Porting Code that Requires a Current Graphics Position</span></span>](porting-code-that-requires-a-current-graphics-position.md)
-   [<span data-ttu-id="aa78b-111">Перенос функций рисования</span><span class="sxs-lookup"><span data-stu-id="aa78b-111">Porting Drawing Functions</span></span>](porting-drawing-functions.md)
-   [<span data-ttu-id="aa78b-112">Перенос цвета, заливки и кода Вритемаск</span><span class="sxs-lookup"><span data-stu-id="aa78b-112">Porting Color, Shading, and Writemask Code</span></span>](porting-color--shading--and-writemask-code.md)
-   [<span data-ttu-id="aa78b-113">Перенос операций с пикселами</span><span class="sxs-lookup"><span data-stu-id="aa78b-113">Porting Pixel Operations</span></span>](porting-pixel-operations.md)
-   [<span data-ttu-id="aa78b-114">Перенос команд cueing и туман глубины</span><span class="sxs-lookup"><span data-stu-id="aa78b-114">Porting Depth Cueing and Fog Commands</span></span>](porting-depth-cueing-and-fog-commands.md)
-   [<span data-ttu-id="aa78b-115">Перенос функций кривой и поверхностей</span><span class="sxs-lookup"><span data-stu-id="aa78b-115">Porting Curve and Surface Functions</span></span>](porting-curve-and-surface-functions.md)
-   [<span data-ttu-id="aa78b-116">Перенос функций сглаживания</span><span class="sxs-lookup"><span data-stu-id="aa78b-116">Porting Antialiasing Functions</span></span>](porting-antialiasing-functions.md)
-   [<span data-ttu-id="aa78b-117">Вызовы буфера накопления при переносе</span><span class="sxs-lookup"><span data-stu-id="aa78b-117">Porting Accumulation Buffer Calls</span></span>](porting-accumulation-buffer-calls.md)
-   [<span data-ttu-id="aa78b-118">Перенос вызовов плоскости набора элементов</span><span class="sxs-lookup"><span data-stu-id="aa78b-118">Porting Stencil Plane Calls</span></span>](porting-stencil-plane-calls.md)
-   [<span data-ttu-id="aa78b-119">Перенос списков вывода</span><span class="sxs-lookup"><span data-stu-id="aa78b-119">Porting Display Lists</span></span>](porting-display-lists.md)
-   [<span data-ttu-id="aa78b-120">Перенос Дефс, привязок и наборов</span><span class="sxs-lookup"><span data-stu-id="aa78b-120">Porting Defs, Binds, and Sets</span></span>](porting-defs--binds--and-sets.md)
-   [<span data-ttu-id="aa78b-121">Перенос функций освещения и материалов</span><span class="sxs-lookup"><span data-stu-id="aa78b-121">Porting Lighting and Materials Functions</span></span>](porting-lighting-and-materials-functions.md)
-   [<span data-ttu-id="aa78b-122">Перенос функций текстуры</span><span class="sxs-lookup"><span data-stu-id="aa78b-122">Porting Texture Functions</span></span>](porting-texture-functions.md)
-   [<span data-ttu-id="aa78b-123">Перенос функций комплектации</span><span class="sxs-lookup"><span data-stu-id="aa78b-123">Porting Picking Functions</span></span>](porting-picking-functions.md)
-   [<span data-ttu-id="aa78b-124">Перенос функций обратной связи</span><span class="sxs-lookup"><span data-stu-id="aa78b-124">Porting Feedback Functions</span></span>](porting-feedback-functions.md)

 

 




