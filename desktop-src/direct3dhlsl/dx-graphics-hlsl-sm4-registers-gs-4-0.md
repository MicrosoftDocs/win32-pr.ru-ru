---
title: Регистры — gs_4_0
description: В этом разделе содержатся справочные сведения о входных и выходных регистрах, реализованных шейдером Geometry версии 4 \_ 0.
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532195"
---
# <a name="registers---gs_4_0"></a><span data-ttu-id="20028-103">Регистры — GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="20028-103">Registers - gs\_4\_0</span></span>

<span data-ttu-id="20028-104">В этом разделе содержатся справочные сведения о входных и выходных регистрах, реализованных шейдером Geometry версии 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="20028-104">This section contains reference information for the input and output registers implemented by geometry shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="20028-105">Входные регистры</span><span class="sxs-lookup"><span data-stu-id="20028-105">Input Registers</span></span>



| <span data-ttu-id="20028-106">Регистрация</span><span class="sxs-lookup"><span data-stu-id="20028-106">Register</span></span>                 | <span data-ttu-id="20028-107">Имя</span><span class="sxs-lookup"><span data-stu-id="20028-107">Name</span></span> | <span data-ttu-id="20028-108">Count</span><span class="sxs-lookup"><span data-stu-id="20028-108">Count</span></span>              | <span data-ttu-id="20028-109">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="20028-109">R/W</span></span> | <span data-ttu-id="20028-110">Измерение</span><span class="sxs-lookup"><span data-stu-id="20028-110">Dimension</span></span>        | <span data-ttu-id="20028-111">Индексация по r\#</span><span class="sxs-lookup"><span data-stu-id="20028-111">Indexable by r\#</span></span> | <span data-ttu-id="20028-112">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="20028-112">Defaults</span></span> | <span data-ttu-id="20028-113">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="20028-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="20028-114">Cерверный\#</span><span class="sxs-lookup"><span data-stu-id="20028-114">r\#</span></span>                      |      | <span data-ttu-id="20028-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="20028-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="20028-116">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="20028-116">R/W</span></span> | <span data-ttu-id="20028-117">4</span><span class="sxs-lookup"><span data-stu-id="20028-117">4</span></span>                | <span data-ttu-id="20028-118">нет</span><span class="sxs-lookup"><span data-stu-id="20028-118">No</span></span>               | <span data-ttu-id="20028-119">None</span><span class="sxs-lookup"><span data-stu-id="20028-119">None</span></span>     | <span data-ttu-id="20028-120">Да</span><span class="sxs-lookup"><span data-stu-id="20028-120">Yes</span></span>          |
| <span data-ttu-id="20028-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="20028-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="20028-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="20028-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="20028-123">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="20028-123">R/W</span></span> | <span data-ttu-id="20028-124">4</span><span class="sxs-lookup"><span data-stu-id="20028-124">4</span></span>                | <span data-ttu-id="20028-125">Да</span><span class="sxs-lookup"><span data-stu-id="20028-125">Yes</span></span>              | <span data-ttu-id="20028-126">Нет</span><span class="sxs-lookup"><span data-stu-id="20028-126">None</span></span>     | <span data-ttu-id="20028-127">Да</span><span class="sxs-lookup"><span data-stu-id="20028-127">Yes</span></span>          |
| <span data-ttu-id="20028-128">v \# \[ \] \[ элемент вершины\]</span><span class="sxs-lookup"><span data-stu-id="20028-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="20028-129">32</span><span class="sxs-lookup"><span data-stu-id="20028-129">32</span></span>                 | <span data-ttu-id="20028-130">R</span><span class="sxs-lookup"><span data-stu-id="20028-130">R</span></span>   | <span data-ttu-id="20028-131">4 (Comp) \* 6 (по вертикали)</span><span class="sxs-lookup"><span data-stu-id="20028-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="20028-132">Да</span><span class="sxs-lookup"><span data-stu-id="20028-132">Yes</span></span>              | <span data-ttu-id="20028-133">Нет</span><span class="sxs-lookup"><span data-stu-id="20028-133">None</span></span>     | <span data-ttu-id="20028-134">Да</span><span class="sxs-lookup"><span data-stu-id="20028-134">Yes</span></span>          |
| <span data-ttu-id="20028-135">вприм</span><span class="sxs-lookup"><span data-stu-id="20028-135">vprim</span></span>                    |      | <span data-ttu-id="20028-136">1</span><span class="sxs-lookup"><span data-stu-id="20028-136">1</span></span>                  | <span data-ttu-id="20028-137">R</span><span class="sxs-lookup"><span data-stu-id="20028-137">R</span></span>   | <span data-ttu-id="20028-138">1</span><span class="sxs-lookup"><span data-stu-id="20028-138">1</span></span>                | <span data-ttu-id="20028-139">Нет</span><span class="sxs-lookup"><span data-stu-id="20028-139">No</span></span>               | <span data-ttu-id="20028-140">None</span><span class="sxs-lookup"><span data-stu-id="20028-140">None</span></span>     | <span data-ttu-id="20028-141">Да</span><span class="sxs-lookup"><span data-stu-id="20028-141">Yes</span></span>          |
| <span data-ttu-id="20028-142">t\#</span><span class="sxs-lookup"><span data-stu-id="20028-142">t\#</span></span>                      |      | <span data-ttu-id="20028-143">128</span><span class="sxs-lookup"><span data-stu-id="20028-143">128</span></span>                | <span data-ttu-id="20028-144">R</span><span class="sxs-lookup"><span data-stu-id="20028-144">R</span></span>   | <span data-ttu-id="20028-145">1</span><span class="sxs-lookup"><span data-stu-id="20028-145">1</span></span>                | <span data-ttu-id="20028-146">Нет</span><span class="sxs-lookup"><span data-stu-id="20028-146">No</span></span>               | <span data-ttu-id="20028-147">None</span><span class="sxs-lookup"><span data-stu-id="20028-147">None</span></span>     | <span data-ttu-id="20028-148">Да</span><span class="sxs-lookup"><span data-stu-id="20028-148">Yes</span></span>          |
| <span data-ttu-id="20028-149">s\#</span><span class="sxs-lookup"><span data-stu-id="20028-149">s\#</span></span>                      |      | <span data-ttu-id="20028-150">16</span><span class="sxs-lookup"><span data-stu-id="20028-150">16</span></span>                 | <span data-ttu-id="20028-151">R</span><span class="sxs-lookup"><span data-stu-id="20028-151">R</span></span>   | <span data-ttu-id="20028-152">1</span><span class="sxs-lookup"><span data-stu-id="20028-152">1</span></span>                | <span data-ttu-id="20028-153">Нет</span><span class="sxs-lookup"><span data-stu-id="20028-153">No</span></span>               | <span data-ttu-id="20028-154">None</span><span class="sxs-lookup"><span data-stu-id="20028-154">None</span></span>     | <span data-ttu-id="20028-155">Да</span><span class="sxs-lookup"><span data-stu-id="20028-155">Yes</span></span>          |
| <span data-ttu-id="20028-156">\# \[ индекс CB\]</span><span class="sxs-lookup"><span data-stu-id="20028-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="20028-157">15</span><span class="sxs-lookup"><span data-stu-id="20028-157">15</span></span>                 | <span data-ttu-id="20028-158">R</span><span class="sxs-lookup"><span data-stu-id="20028-158">R</span></span>   | <span data-ttu-id="20028-159">4</span><span class="sxs-lookup"><span data-stu-id="20028-159">4</span></span>                | <span data-ttu-id="20028-160">Да (содержимое)</span><span class="sxs-lookup"><span data-stu-id="20028-160">Yes(Contents)</span></span>    | <span data-ttu-id="20028-161">Нет</span><span class="sxs-lookup"><span data-stu-id="20028-161">None</span></span>     | <span data-ttu-id="20028-162">Да</span><span class="sxs-lookup"><span data-stu-id="20028-162">Yes</span></span>          |
| <span data-ttu-id="20028-163">индекс блока ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="20028-163">icb\[index\]</span></span>             |      | <span data-ttu-id="20028-164">1</span><span class="sxs-lookup"><span data-stu-id="20028-164">1</span></span>                  | <span data-ttu-id="20028-165">R</span><span class="sxs-lookup"><span data-stu-id="20028-165">R</span></span>   | <span data-ttu-id="20028-166">4</span><span class="sxs-lookup"><span data-stu-id="20028-166">4</span></span>                | <span data-ttu-id="20028-167">Да (содержимое)</span><span class="sxs-lookup"><span data-stu-id="20028-167">Yes(Contents)</span></span>    | <span data-ttu-id="20028-168">Нет</span><span class="sxs-lookup"><span data-stu-id="20028-168">None</span></span>     | <span data-ttu-id="20028-169">Да</span><span class="sxs-lookup"><span data-stu-id="20028-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="20028-170">Выходные регистры</span><span class="sxs-lookup"><span data-stu-id="20028-170">Output Registers</span></span>



| <span data-ttu-id="20028-171">Регистрация</span><span class="sxs-lookup"><span data-stu-id="20028-171">Register</span></span> | <span data-ttu-id="20028-172">Имя</span><span class="sxs-lookup"><span data-stu-id="20028-172">Name</span></span>            | <span data-ttu-id="20028-173">Count</span><span class="sxs-lookup"><span data-stu-id="20028-173">Count</span></span> | <span data-ttu-id="20028-174">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="20028-174">R/W</span></span> | <span data-ttu-id="20028-175">Измерение</span><span class="sxs-lookup"><span data-stu-id="20028-175">Dimension</span></span> | <span data-ttu-id="20028-176">Индексация по r\#</span><span class="sxs-lookup"><span data-stu-id="20028-176">Indexable by r\#</span></span> | <span data-ttu-id="20028-177">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="20028-177">Defaults</span></span> | <span data-ttu-id="20028-178">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="20028-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="20028-179">NULL</span><span class="sxs-lookup"><span data-stu-id="20028-179">NULL</span></span>     | <span data-ttu-id="20028-180">Отменить результат</span><span class="sxs-lookup"><span data-stu-id="20028-180">Discard Result</span></span>  | <span data-ttu-id="20028-181">Недоступно</span><span class="sxs-lookup"><span data-stu-id="20028-181">N/A</span></span>   | <span data-ttu-id="20028-182">W</span><span class="sxs-lookup"><span data-stu-id="20028-182">W</span></span>   | <span data-ttu-id="20028-183">Недоступно</span><span class="sxs-lookup"><span data-stu-id="20028-183">N/A</span></span>       | <span data-ttu-id="20028-184">Недоступно</span><span class="sxs-lookup"><span data-stu-id="20028-184">N/A</span></span>              | <span data-ttu-id="20028-185">Недоступно</span><span class="sxs-lookup"><span data-stu-id="20028-185">N/A</span></span>      | <span data-ttu-id="20028-186">Нет</span><span class="sxs-lookup"><span data-stu-id="20028-186">No</span></span>           |
| <span data-ttu-id="20028-187">вывода\#</span><span class="sxs-lookup"><span data-stu-id="20028-187">o\#</span></span>      | <span data-ttu-id="20028-188">Регистр выходных данных</span><span class="sxs-lookup"><span data-stu-id="20028-188">Output Register</span></span> | <span data-ttu-id="20028-189">32</span><span class="sxs-lookup"><span data-stu-id="20028-189">32</span></span>    | <span data-ttu-id="20028-190">W</span><span class="sxs-lookup"><span data-stu-id="20028-190">W</span></span>   | <span data-ttu-id="20028-191">Недоступно</span><span class="sxs-lookup"><span data-stu-id="20028-191">N/A</span></span>       | <span data-ttu-id="20028-192">Недоступно</span><span class="sxs-lookup"><span data-stu-id="20028-192">N/A</span></span>              | <span data-ttu-id="20028-193">4</span><span class="sxs-lookup"><span data-stu-id="20028-193">4</span></span>        | <span data-ttu-id="20028-194">Да</span><span class="sxs-lookup"><span data-stu-id="20028-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="20028-195">См. также</span><span class="sxs-lookup"><span data-stu-id="20028-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20028-196">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="20028-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




