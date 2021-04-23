---
title: Код порта, которому требуется текущая географические координаты
description: OpenGL не поддерживает текущую графическую точку. Функции IRI GL, которые зависят от текущей положения графики, такие как Move, Draw и РМВ, не имеют эквивалентов в OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- Перенос GL в ГК, текущее расположение графика
- Перенос из ДИАФРАГМы в ГК, текущее расположение графика
- перенос в OpenGL из ДИАФРАГМы, текущая географические координаты
- Перенос по стандарту OpenGL из IRI GL, текущая графическая графика
- Текущее расположение графика
- растровые позиции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/27/2019
ms.locfileid: "103785133"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a><span data-ttu-id="cd693-110">Код порта, которому требуется текущая географические координаты</span><span class="sxs-lookup"><span data-stu-id="cd693-110">Port code that needs a current graphics position</span></span>

<span data-ttu-id="cd693-111">OpenGL не поддерживает текущую графическую точку.</span><span class="sxs-lookup"><span data-stu-id="cd693-111">OpenGL does not maintain a current graphics position.</span></span> <span data-ttu-id="cd693-112">Функции IRI GL, которые зависят от текущей положения графики, такие как **Move**, **Draw** и **РМВ**, не имеют эквивалентов в OpenGL.</span><span class="sxs-lookup"><span data-stu-id="cd693-112">IRIS GL functions that depend on the current graphics position, such as **move**, **draw**, and **rmv**, have no equivalents in OpenGL.</span></span>

<span data-ttu-id="cd693-113">В предыдущих версиях системы IRI GL включались команды рисования, основанные на текущей положении в графике, хотя их использование не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cd693-113">Older versions of IRIS GL included drawing commands that relied upon the current graphics position, though their use has been discouraged.</span></span> <span data-ttu-id="cd693-114">Вам потребуется переписать код, если вы пополагались на текущую координату графики любым способом или использовали любую из следующих подпрограмм:</span><span class="sxs-lookup"><span data-stu-id="cd693-114">You will need to rewrite your code if you relied on the current graphics position in any way, or used any of the following routines:</span></span>

-   <span data-ttu-id="cd693-115">**Рисование** и **Перемещение**</span><span class="sxs-lookup"><span data-stu-id="cd693-115">**draw** and **move**</span></span>
-   <span data-ttu-id="cd693-116">**ПМВ**, **Народно** и **пклос**</span><span class="sxs-lookup"><span data-stu-id="cd693-116">**pmv**, **pdr**, and **pclos**</span></span>
-   <span data-ttu-id="cd693-117">**RDR**, **РМВ**, **рпдр** и **рпмв**</span><span class="sxs-lookup"><span data-stu-id="cd693-117">**rdr**, **rmv**, **rpdr**, and **rpmv**</span></span>
-   <span data-ttu-id="cd693-118">**объекты GPO**</span><span class="sxs-lookup"><span data-stu-id="cd693-118">**getgpos**</span></span>

<span data-ttu-id="cd693-119">OpenGL имеет концепцию растровой позиции, которая соответствует позиции текущего символа в формате IRI GL.</span><span class="sxs-lookup"><span data-stu-id="cd693-119">OpenGL has a concept of raster position that corresponds to IRIS GL's current character position.</span></span> <span data-ttu-id="cd693-120">Дополнительные сведения о позиционировании растровых данных см. в разделе [перенос операций пикселей](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="cd693-120">For more information on raster positioning, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="cd693-121">Этот раздел содержит сведения о следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="cd693-121">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="cd693-122">Перенос команд на экран и очистку буфера</span><span class="sxs-lookup"><span data-stu-id="cd693-122">Porting Screen and Buffer Clearing Commands</span></span>](porting-screen-and-buffer-clearing-commands.md)
-   [<span data-ttu-id="cd693-123">Перенос матриц и функций преобразования</span><span class="sxs-lookup"><span data-stu-id="cd693-123">Porting Matrix and Transformation Functions</span></span>](porting-matrix-and-transformation-functions.md)
-   [<span data-ttu-id="cd693-124">Перенос кода режима МСИНГЛЕ</span><span class="sxs-lookup"><span data-stu-id="cd693-124">Porting MSINGLE Mode Code</span></span>](porting-msingle-mode-code.md)
-   [<span data-ttu-id="cd693-125">Перенос функций, которые получают матрицы и преобразования</span><span class="sxs-lookup"><span data-stu-id="cd693-125">Porting Functions that Get Matrices and Transformations</span></span>](porting-functions-that-get-matrices-and-transformations.md)
-   [<span data-ttu-id="cd693-126">Перенос окна просмотра, Скринмаскс и Скрбоксес</span><span class="sxs-lookup"><span data-stu-id="cd693-126">Porting Viewports, Screenmasks, and Scrboxes</span></span>](porting-viewports--screenmasks--and-scrboxes.md)
-   [<span data-ttu-id="cd693-127">Перенос плоскостей</span><span class="sxs-lookup"><span data-stu-id="cd693-127">Porting Clipping Planes</span></span>](porting-clipping-planes.md)

 

 




