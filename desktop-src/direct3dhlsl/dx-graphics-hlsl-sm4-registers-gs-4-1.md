---
title: Регистры — gs_4_1
description: В этом разделе содержатся справочные сведения о входных и выходных регистрах, реализованных в построителейх текстур Geometry версий 4 \_ 0 и 4 \_ 1.
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258601"
---
# <a name="registers---gs_4_1"></a><span data-ttu-id="ea731-103">Регистры — GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ea731-103">Registers - gs\_4\_1</span></span>

<span data-ttu-id="ea731-104">В этом разделе содержатся справочные сведения о входных и выходных регистрах, реализованных в построителейх текстур Geometry версий 4 \_ 0 и 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="ea731-104">This section contains reference information for the input and output registers implemented by geometry shader versions 4\_0 and 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="ea731-105">Входные регистры</span><span class="sxs-lookup"><span data-stu-id="ea731-105">Input Registers</span></span>



| <span data-ttu-id="ea731-106">Регистрация</span><span class="sxs-lookup"><span data-stu-id="ea731-106">Register</span></span>                 | <span data-ttu-id="ea731-107">Имя</span><span class="sxs-lookup"><span data-stu-id="ea731-107">Name</span></span> | <span data-ttu-id="ea731-108">Count</span><span class="sxs-lookup"><span data-stu-id="ea731-108">Count</span></span>              | <span data-ttu-id="ea731-109">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="ea731-109">R/W</span></span> | <span data-ttu-id="ea731-110">Измерение</span><span class="sxs-lookup"><span data-stu-id="ea731-110">Dimension</span></span>        | <span data-ttu-id="ea731-111">Индексация по r\#</span><span class="sxs-lookup"><span data-stu-id="ea731-111">Indexable by r\#</span></span> | <span data-ttu-id="ea731-112">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ea731-112">Defaults</span></span> | <span data-ttu-id="ea731-113">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="ea731-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="ea731-114">Cерверный\#</span><span class="sxs-lookup"><span data-stu-id="ea731-114">r\#</span></span>                      |      | <span data-ttu-id="ea731-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="ea731-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="ea731-116">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="ea731-116">R/W</span></span> | <span data-ttu-id="ea731-117">4</span><span class="sxs-lookup"><span data-stu-id="ea731-117">4</span></span>                | <span data-ttu-id="ea731-118">нет</span><span class="sxs-lookup"><span data-stu-id="ea731-118">No</span></span>               | <span data-ttu-id="ea731-119">None</span><span class="sxs-lookup"><span data-stu-id="ea731-119">None</span></span>     | <span data-ttu-id="ea731-120">Да</span><span class="sxs-lookup"><span data-stu-id="ea731-120">Yes</span></span>          |
| <span data-ttu-id="ea731-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ea731-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="ea731-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="ea731-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="ea731-123">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="ea731-123">R/W</span></span> | <span data-ttu-id="ea731-124">4</span><span class="sxs-lookup"><span data-stu-id="ea731-124">4</span></span>                | <span data-ttu-id="ea731-125">Да</span><span class="sxs-lookup"><span data-stu-id="ea731-125">Yes</span></span>              | <span data-ttu-id="ea731-126">Нет</span><span class="sxs-lookup"><span data-stu-id="ea731-126">None</span></span>     | <span data-ttu-id="ea731-127">Да</span><span class="sxs-lookup"><span data-stu-id="ea731-127">Yes</span></span>          |
| <span data-ttu-id="ea731-128">v \# \[ \] \[ элемент вершины\]</span><span class="sxs-lookup"><span data-stu-id="ea731-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="ea731-129">32</span><span class="sxs-lookup"><span data-stu-id="ea731-129">32</span></span>                 | <span data-ttu-id="ea731-130">R</span><span class="sxs-lookup"><span data-stu-id="ea731-130">R</span></span>   | <span data-ttu-id="ea731-131">4 (Comp) \* 6 (по вертикали)</span><span class="sxs-lookup"><span data-stu-id="ea731-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="ea731-132">Да</span><span class="sxs-lookup"><span data-stu-id="ea731-132">Yes</span></span>              | <span data-ttu-id="ea731-133">Нет</span><span class="sxs-lookup"><span data-stu-id="ea731-133">None</span></span>     | <span data-ttu-id="ea731-134">Да</span><span class="sxs-lookup"><span data-stu-id="ea731-134">Yes</span></span>          |
| <span data-ttu-id="ea731-135">вприм</span><span class="sxs-lookup"><span data-stu-id="ea731-135">vprim</span></span>                    |      | <span data-ttu-id="ea731-136">1</span><span class="sxs-lookup"><span data-stu-id="ea731-136">1</span></span>                  | <span data-ttu-id="ea731-137">R</span><span class="sxs-lookup"><span data-stu-id="ea731-137">R</span></span>   | <span data-ttu-id="ea731-138">1</span><span class="sxs-lookup"><span data-stu-id="ea731-138">1</span></span>                | <span data-ttu-id="ea731-139">Нет</span><span class="sxs-lookup"><span data-stu-id="ea731-139">No</span></span>               | <span data-ttu-id="ea731-140">None</span><span class="sxs-lookup"><span data-stu-id="ea731-140">None</span></span>     | <span data-ttu-id="ea731-141">Да</span><span class="sxs-lookup"><span data-stu-id="ea731-141">Yes</span></span>          |
| <span data-ttu-id="ea731-142">t\#</span><span class="sxs-lookup"><span data-stu-id="ea731-142">t\#</span></span>                      |      | <span data-ttu-id="ea731-143">128</span><span class="sxs-lookup"><span data-stu-id="ea731-143">128</span></span>                | <span data-ttu-id="ea731-144">R</span><span class="sxs-lookup"><span data-stu-id="ea731-144">R</span></span>   | <span data-ttu-id="ea731-145">1</span><span class="sxs-lookup"><span data-stu-id="ea731-145">1</span></span>                | <span data-ttu-id="ea731-146">Нет</span><span class="sxs-lookup"><span data-stu-id="ea731-146">No</span></span>               | <span data-ttu-id="ea731-147">None</span><span class="sxs-lookup"><span data-stu-id="ea731-147">None</span></span>     | <span data-ttu-id="ea731-148">Да</span><span class="sxs-lookup"><span data-stu-id="ea731-148">Yes</span></span>          |
| <span data-ttu-id="ea731-149">s\#</span><span class="sxs-lookup"><span data-stu-id="ea731-149">s\#</span></span>                      |      | <span data-ttu-id="ea731-150">16</span><span class="sxs-lookup"><span data-stu-id="ea731-150">16</span></span>                 | <span data-ttu-id="ea731-151">R</span><span class="sxs-lookup"><span data-stu-id="ea731-151">R</span></span>   | <span data-ttu-id="ea731-152">1</span><span class="sxs-lookup"><span data-stu-id="ea731-152">1</span></span>                | <span data-ttu-id="ea731-153">Нет</span><span class="sxs-lookup"><span data-stu-id="ea731-153">No</span></span>               | <span data-ttu-id="ea731-154">None</span><span class="sxs-lookup"><span data-stu-id="ea731-154">None</span></span>     | <span data-ttu-id="ea731-155">Да</span><span class="sxs-lookup"><span data-stu-id="ea731-155">Yes</span></span>          |
| <span data-ttu-id="ea731-156">\# \[ индекс CB\]</span><span class="sxs-lookup"><span data-stu-id="ea731-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="ea731-157">15</span><span class="sxs-lookup"><span data-stu-id="ea731-157">15</span></span>                 | <span data-ttu-id="ea731-158">R</span><span class="sxs-lookup"><span data-stu-id="ea731-158">R</span></span>   | <span data-ttu-id="ea731-159">4</span><span class="sxs-lookup"><span data-stu-id="ea731-159">4</span></span>                | <span data-ttu-id="ea731-160">Да (содержимое)</span><span class="sxs-lookup"><span data-stu-id="ea731-160">Yes(Contents)</span></span>    | <span data-ttu-id="ea731-161">Нет</span><span class="sxs-lookup"><span data-stu-id="ea731-161">None</span></span>     | <span data-ttu-id="ea731-162">Да</span><span class="sxs-lookup"><span data-stu-id="ea731-162">Yes</span></span>          |
| <span data-ttu-id="ea731-163">индекс блока ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="ea731-163">icb\[index\]</span></span>             |      | <span data-ttu-id="ea731-164">1</span><span class="sxs-lookup"><span data-stu-id="ea731-164">1</span></span>                  | <span data-ttu-id="ea731-165">R</span><span class="sxs-lookup"><span data-stu-id="ea731-165">R</span></span>   | <span data-ttu-id="ea731-166">4</span><span class="sxs-lookup"><span data-stu-id="ea731-166">4</span></span>                | <span data-ttu-id="ea731-167">Да (содержимое)</span><span class="sxs-lookup"><span data-stu-id="ea731-167">Yes(Contents)</span></span>    | <span data-ttu-id="ea731-168">Нет</span><span class="sxs-lookup"><span data-stu-id="ea731-168">None</span></span>     | <span data-ttu-id="ea731-169">Да</span><span class="sxs-lookup"><span data-stu-id="ea731-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="ea731-170">Выходные регистры</span><span class="sxs-lookup"><span data-stu-id="ea731-170">Output Registers</span></span>



| <span data-ttu-id="ea731-171">Регистрация</span><span class="sxs-lookup"><span data-stu-id="ea731-171">Register</span></span> | <span data-ttu-id="ea731-172">Имя</span><span class="sxs-lookup"><span data-stu-id="ea731-172">Name</span></span>            | <span data-ttu-id="ea731-173">Count</span><span class="sxs-lookup"><span data-stu-id="ea731-173">Count</span></span> | <span data-ttu-id="ea731-174">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="ea731-174">R/W</span></span> | <span data-ttu-id="ea731-175">Измерение</span><span class="sxs-lookup"><span data-stu-id="ea731-175">Dimension</span></span> | <span data-ttu-id="ea731-176">Индексация по r\#</span><span class="sxs-lookup"><span data-stu-id="ea731-176">Indexable by r\#</span></span> | <span data-ttu-id="ea731-177">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ea731-177">Defaults</span></span> | <span data-ttu-id="ea731-178">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="ea731-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="ea731-179">NULL</span><span class="sxs-lookup"><span data-stu-id="ea731-179">NULL</span></span>     | <span data-ttu-id="ea731-180">Отменить результат</span><span class="sxs-lookup"><span data-stu-id="ea731-180">Discard Result</span></span>  | <span data-ttu-id="ea731-181">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ea731-181">N/A</span></span>   | <span data-ttu-id="ea731-182">W</span><span class="sxs-lookup"><span data-stu-id="ea731-182">W</span></span>   | <span data-ttu-id="ea731-183">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ea731-183">N/A</span></span>       | <span data-ttu-id="ea731-184">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ea731-184">N/A</span></span>              | <span data-ttu-id="ea731-185">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ea731-185">N/A</span></span>      | <span data-ttu-id="ea731-186">Нет</span><span class="sxs-lookup"><span data-stu-id="ea731-186">No</span></span>           |
| <span data-ttu-id="ea731-187">вывода\#</span><span class="sxs-lookup"><span data-stu-id="ea731-187">o\#</span></span>      | <span data-ttu-id="ea731-188">Регистр выходных данных</span><span class="sxs-lookup"><span data-stu-id="ea731-188">Output Register</span></span> | <span data-ttu-id="ea731-189">32</span><span class="sxs-lookup"><span data-stu-id="ea731-189">32</span></span>    | <span data-ttu-id="ea731-190">W</span><span class="sxs-lookup"><span data-stu-id="ea731-190">W</span></span>   | <span data-ttu-id="ea731-191">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ea731-191">N/A</span></span>       | <span data-ttu-id="ea731-192">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ea731-192">N/A</span></span>              | <span data-ttu-id="ea731-193">4</span><span class="sxs-lookup"><span data-stu-id="ea731-193">4</span></span>        | <span data-ttu-id="ea731-194">Да</span><span class="sxs-lookup"><span data-stu-id="ea731-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="ea731-195">См. также</span><span class="sxs-lookup"><span data-stu-id="ea731-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea731-196">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ea731-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




