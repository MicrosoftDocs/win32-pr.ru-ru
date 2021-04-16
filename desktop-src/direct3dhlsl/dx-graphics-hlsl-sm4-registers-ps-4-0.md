---
title: Регистры — ps_4_0
description: В этом разделе содержатся справочные сведения о входных и выходных регистрах, реализованных построителем пиксельных шейдеров версии 4 \_ 0.
ms.assetid: 8b83667f-f599-4105-b68c-0d6aa7c528ab
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3dea9606419f32a168c08cc1efbebb5e285d3815
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411005"
---
# <a name="registers---ps_4_0"></a><span data-ttu-id="e1ff2-103">Регистры-PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e1ff2-103">Registers - ps\_4\_0</span></span>

<span data-ttu-id="e1ff2-104">В этом разделе содержатся справочные сведения о входных и выходных регистрах, реализованных построителем пиксельных шейдеров версии 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-104">This section contains reference information for the input and output registers implemented by pixel shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="e1ff2-105">Входные регистры</span><span class="sxs-lookup"><span data-stu-id="e1ff2-105">Input Registers</span></span>



| <span data-ttu-id="e1ff2-106">Регистрация</span><span class="sxs-lookup"><span data-stu-id="e1ff2-106">Register</span></span>      | <span data-ttu-id="e1ff2-107">Имя</span><span class="sxs-lookup"><span data-stu-id="e1ff2-107">Name</span></span> | <span data-ttu-id="e1ff2-108">Count</span><span class="sxs-lookup"><span data-stu-id="e1ff2-108">Count</span></span>              | <span data-ttu-id="e1ff2-109">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="e1ff2-109">R/W</span></span> | <span data-ttu-id="e1ff2-110">Измерение</span><span class="sxs-lookup"><span data-stu-id="e1ff2-110">Dimension</span></span> | <span data-ttu-id="e1ff2-111">Индексация по r\#</span><span class="sxs-lookup"><span data-stu-id="e1ff2-111">Indexable by r\#</span></span> | <span data-ttu-id="e1ff2-112">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e1ff2-112">Defaults</span></span> | <span data-ttu-id="e1ff2-113">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="e1ff2-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="e1ff2-114">Cерверный\#</span><span class="sxs-lookup"><span data-stu-id="e1ff2-114">r\#</span></span>           |      | <span data-ttu-id="e1ff2-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="e1ff2-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="e1ff2-116">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="e1ff2-116">R/W</span></span> | <span data-ttu-id="e1ff2-117">4</span><span class="sxs-lookup"><span data-stu-id="e1ff2-117">4</span></span>         | <span data-ttu-id="e1ff2-118">нет</span><span class="sxs-lookup"><span data-stu-id="e1ff2-118">No</span></span>               | <span data-ttu-id="e1ff2-119">None</span><span class="sxs-lookup"><span data-stu-id="e1ff2-119">None</span></span>     | <span data-ttu-id="e1ff2-120">Да</span><span class="sxs-lookup"><span data-stu-id="e1ff2-120">Yes</span></span>          |
| <span data-ttu-id="e1ff2-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="e1ff2-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="e1ff2-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="e1ff2-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="e1ff2-123">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="e1ff2-123">R/W</span></span> | <span data-ttu-id="e1ff2-124">4</span><span class="sxs-lookup"><span data-stu-id="e1ff2-124">4</span></span>         | <span data-ttu-id="e1ff2-125">Да</span><span class="sxs-lookup"><span data-stu-id="e1ff2-125">Yes</span></span>              | <span data-ttu-id="e1ff2-126">Нет</span><span class="sxs-lookup"><span data-stu-id="e1ff2-126">None</span></span>     | <span data-ttu-id="e1ff2-127">Да</span><span class="sxs-lookup"><span data-stu-id="e1ff2-127">Yes</span></span>          |
| <span data-ttu-id="e1ff2-128">3,3\#</span><span class="sxs-lookup"><span data-stu-id="e1ff2-128">v\#</span></span>           |      | <span data-ttu-id="e1ff2-129">32</span><span class="sxs-lookup"><span data-stu-id="e1ff2-129">32</span></span>                 | <span data-ttu-id="e1ff2-130">R</span><span class="sxs-lookup"><span data-stu-id="e1ff2-130">R</span></span>   | <span data-ttu-id="e1ff2-131">4</span><span class="sxs-lookup"><span data-stu-id="e1ff2-131">4</span></span>         | <span data-ttu-id="e1ff2-132">Да</span><span class="sxs-lookup"><span data-stu-id="e1ff2-132">Yes</span></span>              | <span data-ttu-id="e1ff2-133">Нет</span><span class="sxs-lookup"><span data-stu-id="e1ff2-133">None</span></span>     | <span data-ttu-id="e1ff2-134">Да</span><span class="sxs-lookup"><span data-stu-id="e1ff2-134">Yes</span></span>          |
| <span data-ttu-id="e1ff2-135">t\#</span><span class="sxs-lookup"><span data-stu-id="e1ff2-135">t\#</span></span>           |      | <span data-ttu-id="e1ff2-136">128</span><span class="sxs-lookup"><span data-stu-id="e1ff2-136">128</span></span>                | <span data-ttu-id="e1ff2-137">R</span><span class="sxs-lookup"><span data-stu-id="e1ff2-137">R</span></span>   | <span data-ttu-id="e1ff2-138">1</span><span class="sxs-lookup"><span data-stu-id="e1ff2-138">1</span></span>         | <span data-ttu-id="e1ff2-139">Нет</span><span class="sxs-lookup"><span data-stu-id="e1ff2-139">No</span></span>               | <span data-ttu-id="e1ff2-140">None</span><span class="sxs-lookup"><span data-stu-id="e1ff2-140">None</span></span>     | <span data-ttu-id="e1ff2-141">Да</span><span class="sxs-lookup"><span data-stu-id="e1ff2-141">Yes</span></span>          |
| <span data-ttu-id="e1ff2-142">s\#</span><span class="sxs-lookup"><span data-stu-id="e1ff2-142">s\#</span></span>           |      | <span data-ttu-id="e1ff2-143">16</span><span class="sxs-lookup"><span data-stu-id="e1ff2-143">16</span></span>                 | <span data-ttu-id="e1ff2-144">R</span><span class="sxs-lookup"><span data-stu-id="e1ff2-144">R</span></span>   | <span data-ttu-id="e1ff2-145">1</span><span class="sxs-lookup"><span data-stu-id="e1ff2-145">1</span></span>         | <span data-ttu-id="e1ff2-146">Нет</span><span class="sxs-lookup"><span data-stu-id="e1ff2-146">No</span></span>               | <span data-ttu-id="e1ff2-147">None</span><span class="sxs-lookup"><span data-stu-id="e1ff2-147">None</span></span>     | <span data-ttu-id="e1ff2-148">Да</span><span class="sxs-lookup"><span data-stu-id="e1ff2-148">Yes</span></span>          |
| <span data-ttu-id="e1ff2-149">\# \[ индекс CB\]</span><span class="sxs-lookup"><span data-stu-id="e1ff2-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="e1ff2-150">15</span><span class="sxs-lookup"><span data-stu-id="e1ff2-150">15</span></span>                 | <span data-ttu-id="e1ff2-151">R</span><span class="sxs-lookup"><span data-stu-id="e1ff2-151">R</span></span>   | <span data-ttu-id="e1ff2-152">4</span><span class="sxs-lookup"><span data-stu-id="e1ff2-152">4</span></span>         | <span data-ttu-id="e1ff2-153">Да (содержимое)</span><span class="sxs-lookup"><span data-stu-id="e1ff2-153">Yes(Contents)</span></span>    | <span data-ttu-id="e1ff2-154">Нет</span><span class="sxs-lookup"><span data-stu-id="e1ff2-154">None</span></span>     | <span data-ttu-id="e1ff2-155">Да</span><span class="sxs-lookup"><span data-stu-id="e1ff2-155">Yes</span></span>          |
| <span data-ttu-id="e1ff2-156">индекс блока ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="e1ff2-156">icb\[index\]</span></span>  |      | <span data-ttu-id="e1ff2-157">1</span><span class="sxs-lookup"><span data-stu-id="e1ff2-157">1</span></span>                  | <span data-ttu-id="e1ff2-158">R</span><span class="sxs-lookup"><span data-stu-id="e1ff2-158">R</span></span>   | <span data-ttu-id="e1ff2-159">4</span><span class="sxs-lookup"><span data-stu-id="e1ff2-159">4</span></span>         | <span data-ttu-id="e1ff2-160">Да (содержимое)</span><span class="sxs-lookup"><span data-stu-id="e1ff2-160">Yes(Contents)</span></span>    | <span data-ttu-id="e1ff2-161">Нет</span><span class="sxs-lookup"><span data-stu-id="e1ff2-161">None</span></span>     | <span data-ttu-id="e1ff2-162">Да</span><span class="sxs-lookup"><span data-stu-id="e1ff2-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="e1ff2-163">Выходные регистры</span><span class="sxs-lookup"><span data-stu-id="e1ff2-163">Output Registers</span></span>



| <span data-ttu-id="e1ff2-164">Регистрация</span><span class="sxs-lookup"><span data-stu-id="e1ff2-164">Register</span></span> | <span data-ttu-id="e1ff2-165">Имя</span><span class="sxs-lookup"><span data-stu-id="e1ff2-165">Name</span></span>            | <span data-ttu-id="e1ff2-166">Count</span><span class="sxs-lookup"><span data-stu-id="e1ff2-166">Count</span></span> | <span data-ttu-id="e1ff2-167">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="e1ff2-167">R/W</span></span> | <span data-ttu-id="e1ff2-168">Измерение</span><span class="sxs-lookup"><span data-stu-id="e1ff2-168">Dimension</span></span> | <span data-ttu-id="e1ff2-169">Индексация по r\#</span><span class="sxs-lookup"><span data-stu-id="e1ff2-169">Indexable by r\#</span></span> | <span data-ttu-id="e1ff2-170">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e1ff2-170">Defaults</span></span> | <span data-ttu-id="e1ff2-171">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="e1ff2-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="e1ff2-172">NULL</span><span class="sxs-lookup"><span data-stu-id="e1ff2-172">NULL</span></span>     | <span data-ttu-id="e1ff2-173">Отменить результат</span><span class="sxs-lookup"><span data-stu-id="e1ff2-173">Discard Result</span></span>  | <span data-ttu-id="e1ff2-174">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e1ff2-174">N/A</span></span>   | <span data-ttu-id="e1ff2-175">W</span><span class="sxs-lookup"><span data-stu-id="e1ff2-175">W</span></span>   | <span data-ttu-id="e1ff2-176">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e1ff2-176">N/A</span></span>       | <span data-ttu-id="e1ff2-177">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e1ff2-177">N/A</span></span>              | <span data-ttu-id="e1ff2-178">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e1ff2-178">N/A</span></span>      | <span data-ttu-id="e1ff2-179">Нет</span><span class="sxs-lookup"><span data-stu-id="e1ff2-179">No</span></span>           |
| <span data-ttu-id="e1ff2-180">вывода\#</span><span class="sxs-lookup"><span data-stu-id="e1ff2-180">o\#</span></span>      | <span data-ttu-id="e1ff2-181">Регистр выходных данных</span><span class="sxs-lookup"><span data-stu-id="e1ff2-181">Output Register</span></span> | <span data-ttu-id="e1ff2-182">8</span><span class="sxs-lookup"><span data-stu-id="e1ff2-182">8</span></span>     | <span data-ttu-id="e1ff2-183">W</span><span class="sxs-lookup"><span data-stu-id="e1ff2-183">W</span></span>   | <span data-ttu-id="e1ff2-184">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e1ff2-184">N/A</span></span>       | <span data-ttu-id="e1ff2-185">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e1ff2-185">N/A</span></span>              | <span data-ttu-id="e1ff2-186">4</span><span class="sxs-lookup"><span data-stu-id="e1ff2-186">4</span></span>        | <span data-ttu-id="e1ff2-187">нет</span><span class="sxs-lookup"><span data-stu-id="e1ff2-187">No</span></span>           |
| <span data-ttu-id="e1ff2-188">одепс</span><span class="sxs-lookup"><span data-stu-id="e1ff2-188">oDepth</span></span>   | <span data-ttu-id="e1ff2-189">Глубина вывода</span><span class="sxs-lookup"><span data-stu-id="e1ff2-189">Output Depth</span></span>    | <span data-ttu-id="e1ff2-190">1</span><span class="sxs-lookup"><span data-stu-id="e1ff2-190">1</span></span>     | <span data-ttu-id="e1ff2-191">W</span><span class="sxs-lookup"><span data-stu-id="e1ff2-191">W</span></span>   | <span data-ttu-id="e1ff2-192">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e1ff2-192">N/A</span></span>       | <span data-ttu-id="e1ff2-193">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e1ff2-193">N/A</span></span>              | <span data-ttu-id="e1ff2-194">1</span><span class="sxs-lookup"><span data-stu-id="e1ff2-194">1</span></span>        | <span data-ttu-id="e1ff2-195">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e1ff2-195">N/A</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="e1ff2-196">См. также</span><span class="sxs-lookup"><span data-stu-id="e1ff2-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1ff2-197">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="e1ff2-197">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




