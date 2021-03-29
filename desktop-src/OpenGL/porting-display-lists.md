---
title: Перенос списков вывода
description: Реализация списков дисплеев OpenGL похожа на стандартную реализацию IRI, но два исключения в OpenGL не позволяют изменять списки вывода после их создания и не могут вызывать функции из списков вывода.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- Перенос GL по IRI, списки вывода
- Перенос из IRI GL, списки вывода
- перенос в OpenGL из IRI GL, списки вывода
- Перенос по стандарту OpenGL из IRI GL, списки вывода
- списки для показа, перенос из IRI GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328819"
---
# <a name="porting-display-lists"></a><span data-ttu-id="a19dd-108">Перенос списков вывода</span><span class="sxs-lookup"><span data-stu-id="a19dd-108">Porting Display Lists</span></span>

<span data-ttu-id="a19dd-109">Реализация списков дисплеев OpenGL похожа на стандартную реализацию IRI, за исключением двух исключений: в OpenGL нельзя изменять отображаемые списки после их создания и нельзя вызывать функции из списков вывода.</span><span class="sxs-lookup"><span data-stu-id="a19dd-109">The OpenGL implementation of display lists is similar to the IRIS GL implementation, with two exceptions: in OpenGL you can't edit display lists once you've created them and you can't call functions from within display lists.</span></span>

<span data-ttu-id="a19dd-110">Поскольку нельзя изменять или вызывать функции из списков вывода, эти функции IRI GL не имеют эквивалента в OpenGL:</span><span class="sxs-lookup"><span data-stu-id="a19dd-110">Because you can't edit or call functions from within display lists, these IRIS GL functions have no equivalent in OpenGL:</span></span>

-   <span data-ttu-id="a19dd-111">**едитобж**</span><span class="sxs-lookup"><span data-stu-id="a19dd-111">**editobj**</span></span>
-   <span data-ttu-id="a19dd-112">**обжделете**, **обжинсерт** и **обжреплаце**</span><span class="sxs-lookup"><span data-stu-id="a19dd-112">**objdelete**, **objinsert**, and **objreplace**</span></span>
-   <span data-ttu-id="a19dd-113">**макетаг**, **жентаг**, **истаг** и **делтаг**</span><span class="sxs-lookup"><span data-stu-id="a19dd-113">**maketag**, **gentag**, **istag**, and **deltag**</span></span>
-   <span data-ttu-id="a19dd-114">**каллфунк**</span><span class="sxs-lookup"><span data-stu-id="a19dd-114">**callfunc**</span></span>

<span data-ttu-id="a19dd-115">В IRI GL для создания списков вывода используются функции **макеобж** и **клосеобж** .</span><span class="sxs-lookup"><span data-stu-id="a19dd-115">In IRIS GL, you use the **makeobj** and **closeobj** functions to create display lists.</span></span> <span data-ttu-id="a19dd-116">В OpenGL используются [**глневлист**](glnewlist.md) и [**глендлист**](glendlist.md).</span><span class="sxs-lookup"><span data-stu-id="a19dd-116">In OpenGL, you use [**glNewList**](glnewlist.md) and [**glEndList**](glendlist.md).</span></span>

<span data-ttu-id="a19dd-117">В следующей таблице перечислены функции списка вывода IRI GL с эквивалентными функциями OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a19dd-117">The following table lists the IRIS GL display list functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="a19dd-118">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="a19dd-118">IRIS GL function</span></span> | <span data-ttu-id="a19dd-119">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="a19dd-119">OpenGL function</span></span>                                                      | <span data-ttu-id="a19dd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a19dd-120">Meaning</span></span>                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a19dd-121">**макеобж**</span><span class="sxs-lookup"><span data-stu-id="a19dd-121">**makeobj**</span></span>      | <span data-ttu-id="a19dd-122">**глневлист**</span><span class="sxs-lookup"><span data-stu-id="a19dd-122">**glNewList**</span></span>                                                        | <span data-ttu-id="a19dd-123">Создает новый список экранов.</span><span class="sxs-lookup"><span data-stu-id="a19dd-123">Creates a new display list.</span></span>                                   |
| <span data-ttu-id="a19dd-124">**клосеобж**</span><span class="sxs-lookup"><span data-stu-id="a19dd-124">**closeobj**</span></span>     | <span data-ttu-id="a19dd-125">**глендлист**</span><span class="sxs-lookup"><span data-stu-id="a19dd-125">**glEndList**</span></span>                                                        | <span data-ttu-id="a19dd-126">Сигнализирует о завершении списка отображений.</span><span class="sxs-lookup"><span data-stu-id="a19dd-126">Signals end of display list.</span></span>                                  |
| <span data-ttu-id="a19dd-127">**каллобж**</span><span class="sxs-lookup"><span data-stu-id="a19dd-127">**callobj**</span></span>      | <span data-ttu-id="a19dd-128">[**глкалллист**](glcalllist.md), [ **глкалллистс**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="a19dd-128">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="a19dd-129">Выполняет список или списки дисплеев.</span><span class="sxs-lookup"><span data-stu-id="a19dd-129">Executes display list or lists.</span></span>                               |
| <span data-ttu-id="a19dd-130">**исобж**</span><span class="sxs-lookup"><span data-stu-id="a19dd-130">**isobj**</span></span>        | [<span data-ttu-id="a19dd-131">**глислист**</span><span class="sxs-lookup"><span data-stu-id="a19dd-131">**glIsList**</span></span>](glislist.md)                                         | <span data-ttu-id="a19dd-132">Тесты для существования списка отображений.</span><span class="sxs-lookup"><span data-stu-id="a19dd-132">Tests for display list existence.</span></span>                             |
| <span data-ttu-id="a19dd-133">**делобж**</span><span class="sxs-lookup"><span data-stu-id="a19dd-133">**delobj**</span></span>       | [<span data-ttu-id="a19dd-134">**глделетелистс**</span><span class="sxs-lookup"><span data-stu-id="a19dd-134">**glDeleteLists**</span></span>](gldeletelists.md)                               | <span data-ttu-id="a19dd-135">Удаляет смежную группу списков вывода.</span><span class="sxs-lookup"><span data-stu-id="a19dd-135">Deletes contiguous group of display lists.</span></span>                    |
| <span data-ttu-id="a19dd-136">**женобж**</span><span class="sxs-lookup"><span data-stu-id="a19dd-136">**genobj**</span></span>       | [<span data-ttu-id="a19dd-137">**глженлистс**</span><span class="sxs-lookup"><span data-stu-id="a19dd-137">**glGenLists**</span></span>](glgenlists.md)                                     | <span data-ttu-id="a19dd-138">Формирует заданное число смежных пустых списков вывода.</span><span class="sxs-lookup"><span data-stu-id="a19dd-138">Generates the given number of contiguous empty display lists.</span></span> |



 

<span data-ttu-id="a19dd-139">Этот раздел содержит сведения о следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="a19dd-139">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="a19dd-140">Перенос функции bbox2</span><span class="sxs-lookup"><span data-stu-id="a19dd-140">Porting the bbox2 Function</span></span>](porting-the-bbox2-function.md)
-   [<span data-ttu-id="a19dd-141">Перенос измененных списков вывода</span><span class="sxs-lookup"><span data-stu-id="a19dd-141">Porting Edited Display Lists</span></span>](porting-edited-display-lists.md)
-   [<span data-ttu-id="a19dd-142">Пример порта списка дисплеев</span><span class="sxs-lookup"><span data-stu-id="a19dd-142">A Sample Port of a Display List</span></span>](a-sample-port-of-a-display-list.md)

 

 




