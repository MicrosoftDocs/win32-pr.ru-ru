---
title: Перенос функций, которые получают матрицы и преобразования
description: В следующей таблице перечислены функции IRI GL, которые получают состояние матриц и преобразований и их эквивалентов OpenGL.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- Перенос GL по IRI, матрицы
- Перенос из ДИАФРАГМы в ГК, матрицы
- Перенос на OpenGL из IRI GL, матрицы
- Перенос по стандарту OpenGL из IRI GL, матрицы
- матрицы
- Перенос GL в ГК, преобразования
- Перенос из IRI GL, преобразования
- перенос в OpenGL из IRI GL, преобразования
- Перенос по стандарту OpenGL из IRI GL, преобразования
- преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986582"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a><span data-ttu-id="0917b-113">Перенос функций, которые получают матрицы и преобразования</span><span class="sxs-lookup"><span data-stu-id="0917b-113">Porting Functions that Get Matrices and Transformations</span></span>

<span data-ttu-id="0917b-114">В следующей таблице перечислены функции IRI GL, которые получают состояние матриц и преобразований и их эквивалентов OpenGL.</span><span class="sxs-lookup"><span data-stu-id="0917b-114">The following table lists the IRIS GL functions that get the state of matrices and transformations and their OpenGL equivalents.</span></span>



| <span data-ttu-id="0917b-115">Запрос матрицы IRI GL</span><span class="sxs-lookup"><span data-stu-id="0917b-115">IRIS GL matrix query</span></span>                  | <span data-ttu-id="0917b-116">Запрос матрицы OpenGL Глжет</span><span class="sxs-lookup"><span data-stu-id="0917b-116">OpenGL glGet matrix query</span></span>         | <span data-ttu-id="0917b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0917b-117">Meaning</span></span>                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="0917b-118">**жетммоде**</span><span class="sxs-lookup"><span data-stu-id="0917b-118">**getmmode**</span></span>                          | <span data-ttu-id="0917b-119">\_режим матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="0917b-119">GL\_MATRIX\_MODE</span></span>                  | <span data-ttu-id="0917b-120">Возвращает текущий режим матрицы.</span><span class="sxs-lookup"><span data-stu-id="0917b-120">Returns the current matrix mode.</span></span>                                |
| <span data-ttu-id="0917b-121">**Матрица** в режиме **мвиевинг**</span><span class="sxs-lookup"><span data-stu-id="0917b-121">**getmatrix** in **MVIEWING** mode</span></span>    | <span data-ttu-id="0917b-122">\_ \_ Матрица моделвиев GL</span><span class="sxs-lookup"><span data-stu-id="0917b-122">GL\_MODELVIEW\_MATRIX</span></span>             | <span data-ttu-id="0917b-123">Возвращает копию текущей матрицы представления модели.</span><span class="sxs-lookup"><span data-stu-id="0917b-123">Returns a copy of the current model-view matrix.</span></span>                |
| <span data-ttu-id="0917b-124">**Матрица** в режиме **мпрожектион**</span><span class="sxs-lookup"><span data-stu-id="0917b-124">**getmatrix** in **MPROJECTION** mode</span></span> | <span data-ttu-id="0917b-125">\_матрица проекции GL \_</span><span class="sxs-lookup"><span data-stu-id="0917b-125">GL\_PROJECTION\_MATRIX</span></span>            | <span data-ttu-id="0917b-126">Возвращает копию текущей матрицы проекции.</span><span class="sxs-lookup"><span data-stu-id="0917b-126">Returns a copy of the current projection matrix.</span></span>                |
| <span data-ttu-id="0917b-127">**Матрица** в режиме **мтекстуре**</span><span class="sxs-lookup"><span data-stu-id="0917b-127">**getmatrix** in **MTEXTURE** mode</span></span>    | <span data-ttu-id="0917b-128">\_ \_ Матрица текстур GL</span><span class="sxs-lookup"><span data-stu-id="0917b-128">GL\_TEXTURE\_MATRIX</span></span>               | <span data-ttu-id="0917b-129">Возвращает копию текущей матрицы текстуры.</span><span class="sxs-lookup"><span data-stu-id="0917b-129">Returns a copy of the current texture matrix.</span></span>                   |
| <span data-ttu-id="0917b-130">Не применяется</span><span class="sxs-lookup"><span data-stu-id="0917b-130">Not applicable.</span></span>                       | <span data-ttu-id="0917b-131">\_Максимальная \_ \_ глубина СТЕКа \_ моделвиев GL</span><span class="sxs-lookup"><span data-stu-id="0917b-131">GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>  | <span data-ttu-id="0917b-132">Возвращает максимальную поддерживаемую глубину стека матриц представления модели.</span><span class="sxs-lookup"><span data-stu-id="0917b-132">Returns maximum supported depth of the model-view matrix stack.</span></span> |
| <span data-ttu-id="0917b-133">Не применяется</span><span class="sxs-lookup"><span data-stu-id="0917b-133">Not applicable.</span></span>                       | <span data-ttu-id="0917b-134">\_Максимальная \_ \_ глубина стека проекции GL \_</span><span class="sxs-lookup"><span data-stu-id="0917b-134">GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span> | <span data-ttu-id="0917b-135">Возвращает максимальную поддерживаемую глубину стека матрицы проекции.</span><span class="sxs-lookup"><span data-stu-id="0917b-135">Returns maximum supported depth of the projection matrix stack.</span></span> |
| <span data-ttu-id="0917b-136">Не применяется</span><span class="sxs-lookup"><span data-stu-id="0917b-136">Not applicable.</span></span>                       | <span data-ttu-id="0917b-137">\_Максимальная \_ \_ глубина СТЕКа \_ текстуры GL</span><span class="sxs-lookup"><span data-stu-id="0917b-137">GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>    | <span data-ttu-id="0917b-138">Возвращает максимальную поддерживаемую глубину стека матрицы текстур.</span><span class="sxs-lookup"><span data-stu-id="0917b-138">Returns maximum supported depth of the texture matrix stack.</span></span>    |
| <span data-ttu-id="0917b-139">Не применяется</span><span class="sxs-lookup"><span data-stu-id="0917b-139">Not applicable.</span></span>                       | <span data-ttu-id="0917b-140">\_ \_ глубина стека моделвиев GL \_</span><span class="sxs-lookup"><span data-stu-id="0917b-140">GL\_MODELVIEW\_STACK\_DEPTH</span></span>       | <span data-ttu-id="0917b-141">Возвращает число матриц в стеке представления модели.</span><span class="sxs-lookup"><span data-stu-id="0917b-141">Returns number of matrices on the model view stack.</span></span>             |
| <span data-ttu-id="0917b-142">Не применяется</span><span class="sxs-lookup"><span data-stu-id="0917b-142">Not applicable.</span></span>                       | <span data-ttu-id="0917b-143">\_ \_ глубина стека ПРОЕЦИРОВАНия GL \_</span><span class="sxs-lookup"><span data-stu-id="0917b-143">GL\_PROJECTION\_STACK\_DEPTH</span></span>      | <span data-ttu-id="0917b-144">Возвращает число матриц в стеке проекции.</span><span class="sxs-lookup"><span data-stu-id="0917b-144">Returns number of matrices on the projection stack.</span></span>             |
| <span data-ttu-id="0917b-145">Не применяется</span><span class="sxs-lookup"><span data-stu-id="0917b-145">Not applicable.</span></span>                       | <span data-ttu-id="0917b-146">\_ \_ глубина стека текстур GL \_</span><span class="sxs-lookup"><span data-stu-id="0917b-146">GL\_TEXTURE\_STACK\_DEPTH</span></span>         | <span data-ttu-id="0917b-147">Возвращает число матриц в стеке текстуры.</span><span class="sxs-lookup"><span data-stu-id="0917b-147">Returns number of matrices on the texture stack.</span></span>                |



 

<span data-ttu-id="0917b-148">??</span><span class="sxs-lookup"><span data-stu-id="0917b-148">??</span></span>

 

 




