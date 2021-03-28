---
title: Регистры — vs_4_1
description: В этом разделе содержатся справочные сведения по входным и выходным регистрам, реализованным построителем вершин версии 4 \_ 1.
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df2254c111303129327d255f94727a5e42ac1c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258600"
---
# <a name="registers---vs_4_1"></a><span data-ttu-id="fecf6-103">Регистры-VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="fecf6-103">Registers - vs\_4\_1</span></span>

<span data-ttu-id="fecf6-104">В этом разделе содержатся справочные сведения по входным и выходным регистрам, реализованным построителем вершин версии 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="fecf6-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="fecf6-105">Входные регистры</span><span class="sxs-lookup"><span data-stu-id="fecf6-105">Input Registers</span></span>



| <span data-ttu-id="fecf6-106">Регистрация</span><span class="sxs-lookup"><span data-stu-id="fecf6-106">Register</span></span>      | <span data-ttu-id="fecf6-107">Имя</span><span class="sxs-lookup"><span data-stu-id="fecf6-107">Name</span></span> | <span data-ttu-id="fecf6-108">Count</span><span class="sxs-lookup"><span data-stu-id="fecf6-108">Count</span></span>              | <span data-ttu-id="fecf6-109">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="fecf6-109">R/W</span></span> | <span data-ttu-id="fecf6-110">Измерение</span><span class="sxs-lookup"><span data-stu-id="fecf6-110">Dimension</span></span> | <span data-ttu-id="fecf6-111">Индексация по r\#</span><span class="sxs-lookup"><span data-stu-id="fecf6-111">Indexable by r\#</span></span> | <span data-ttu-id="fecf6-112">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fecf6-112">Defaults</span></span> | <span data-ttu-id="fecf6-113">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="fecf6-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="fecf6-114">Cерверный\#</span><span class="sxs-lookup"><span data-stu-id="fecf6-114">r\#</span></span>           |      | <span data-ttu-id="fecf6-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="fecf6-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="fecf6-116">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="fecf6-116">R/W</span></span> | <span data-ttu-id="fecf6-117">4</span><span class="sxs-lookup"><span data-stu-id="fecf6-117">4</span></span>         | <span data-ttu-id="fecf6-118">нет</span><span class="sxs-lookup"><span data-stu-id="fecf6-118">No</span></span>               | <span data-ttu-id="fecf6-119">None</span><span class="sxs-lookup"><span data-stu-id="fecf6-119">None</span></span>     | <span data-ttu-id="fecf6-120">Да</span><span class="sxs-lookup"><span data-stu-id="fecf6-120">Yes</span></span>          |
| <span data-ttu-id="fecf6-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="fecf6-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="fecf6-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="fecf6-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="fecf6-123">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="fecf6-123">R/W</span></span> | <span data-ttu-id="fecf6-124">4</span><span class="sxs-lookup"><span data-stu-id="fecf6-124">4</span></span>         | <span data-ttu-id="fecf6-125">Да</span><span class="sxs-lookup"><span data-stu-id="fecf6-125">Yes</span></span>              | <span data-ttu-id="fecf6-126">Нет</span><span class="sxs-lookup"><span data-stu-id="fecf6-126">None</span></span>     | <span data-ttu-id="fecf6-127">Да</span><span class="sxs-lookup"><span data-stu-id="fecf6-127">Yes</span></span>          |
| <span data-ttu-id="fecf6-128">3,3\#</span><span class="sxs-lookup"><span data-stu-id="fecf6-128">v\#</span></span>           |      | <span data-ttu-id="fecf6-129">32</span><span class="sxs-lookup"><span data-stu-id="fecf6-129">32</span></span>                 | <span data-ttu-id="fecf6-130">R</span><span class="sxs-lookup"><span data-stu-id="fecf6-130">R</span></span>   | <span data-ttu-id="fecf6-131">4</span><span class="sxs-lookup"><span data-stu-id="fecf6-131">4</span></span>         | <span data-ttu-id="fecf6-132">Да</span><span class="sxs-lookup"><span data-stu-id="fecf6-132">Yes</span></span>              | <span data-ttu-id="fecf6-133">Нет</span><span class="sxs-lookup"><span data-stu-id="fecf6-133">None</span></span>     | <span data-ttu-id="fecf6-134">Да</span><span class="sxs-lookup"><span data-stu-id="fecf6-134">Yes</span></span>          |
| <span data-ttu-id="fecf6-135">t\#</span><span class="sxs-lookup"><span data-stu-id="fecf6-135">t\#</span></span>           |      | <span data-ttu-id="fecf6-136">128</span><span class="sxs-lookup"><span data-stu-id="fecf6-136">128</span></span>                | <span data-ttu-id="fecf6-137">R</span><span class="sxs-lookup"><span data-stu-id="fecf6-137">R</span></span>   | <span data-ttu-id="fecf6-138">1</span><span class="sxs-lookup"><span data-stu-id="fecf6-138">1</span></span>         | <span data-ttu-id="fecf6-139">Нет</span><span class="sxs-lookup"><span data-stu-id="fecf6-139">No</span></span>               | <span data-ttu-id="fecf6-140">None</span><span class="sxs-lookup"><span data-stu-id="fecf6-140">None</span></span>     | <span data-ttu-id="fecf6-141">Да</span><span class="sxs-lookup"><span data-stu-id="fecf6-141">Yes</span></span>          |
| <span data-ttu-id="fecf6-142">s\#</span><span class="sxs-lookup"><span data-stu-id="fecf6-142">s\#</span></span>           |      | <span data-ttu-id="fecf6-143">16</span><span class="sxs-lookup"><span data-stu-id="fecf6-143">16</span></span>                 | <span data-ttu-id="fecf6-144">R</span><span class="sxs-lookup"><span data-stu-id="fecf6-144">R</span></span>   | <span data-ttu-id="fecf6-145">1</span><span class="sxs-lookup"><span data-stu-id="fecf6-145">1</span></span>         | <span data-ttu-id="fecf6-146">Нет</span><span class="sxs-lookup"><span data-stu-id="fecf6-146">No</span></span>               | <span data-ttu-id="fecf6-147">None</span><span class="sxs-lookup"><span data-stu-id="fecf6-147">None</span></span>     | <span data-ttu-id="fecf6-148">Да</span><span class="sxs-lookup"><span data-stu-id="fecf6-148">Yes</span></span>          |
| <span data-ttu-id="fecf6-149">\# \[ индекс CB\]</span><span class="sxs-lookup"><span data-stu-id="fecf6-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="fecf6-150">15</span><span class="sxs-lookup"><span data-stu-id="fecf6-150">15</span></span>                 | <span data-ttu-id="fecf6-151">R</span><span class="sxs-lookup"><span data-stu-id="fecf6-151">R</span></span>   | <span data-ttu-id="fecf6-152">4</span><span class="sxs-lookup"><span data-stu-id="fecf6-152">4</span></span>         | <span data-ttu-id="fecf6-153">Да (содержимое)</span><span class="sxs-lookup"><span data-stu-id="fecf6-153">Yes(Contents)</span></span>    | <span data-ttu-id="fecf6-154">Нет</span><span class="sxs-lookup"><span data-stu-id="fecf6-154">None</span></span>     | <span data-ttu-id="fecf6-155">Да</span><span class="sxs-lookup"><span data-stu-id="fecf6-155">Yes</span></span>          |
| <span data-ttu-id="fecf6-156">индекс блока ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="fecf6-156">icb\[index\]</span></span>  |      | <span data-ttu-id="fecf6-157">1</span><span class="sxs-lookup"><span data-stu-id="fecf6-157">1</span></span>                  | <span data-ttu-id="fecf6-158">R</span><span class="sxs-lookup"><span data-stu-id="fecf6-158">R</span></span>   | <span data-ttu-id="fecf6-159">4</span><span class="sxs-lookup"><span data-stu-id="fecf6-159">4</span></span>         | <span data-ttu-id="fecf6-160">Да (содержимое)</span><span class="sxs-lookup"><span data-stu-id="fecf6-160">Yes(Contents)</span></span>    | <span data-ttu-id="fecf6-161">Нет</span><span class="sxs-lookup"><span data-stu-id="fecf6-161">None</span></span>     | <span data-ttu-id="fecf6-162">Да</span><span class="sxs-lookup"><span data-stu-id="fecf6-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="fecf6-163">Выходные регистры</span><span class="sxs-lookup"><span data-stu-id="fecf6-163">Output Registers</span></span>



| <span data-ttu-id="fecf6-164">Регистрация</span><span class="sxs-lookup"><span data-stu-id="fecf6-164">Register</span></span> | <span data-ttu-id="fecf6-165">Имя</span><span class="sxs-lookup"><span data-stu-id="fecf6-165">Name</span></span>            | <span data-ttu-id="fecf6-166">Count</span><span class="sxs-lookup"><span data-stu-id="fecf6-166">Count</span></span> | <span data-ttu-id="fecf6-167">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="fecf6-167">R/W</span></span> | <span data-ttu-id="fecf6-168">Измерение</span><span class="sxs-lookup"><span data-stu-id="fecf6-168">Dimension</span></span> | <span data-ttu-id="fecf6-169">Индексация по r\#</span><span class="sxs-lookup"><span data-stu-id="fecf6-169">Indexable by r\#</span></span> | <span data-ttu-id="fecf6-170">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fecf6-170">Defaults</span></span> | <span data-ttu-id="fecf6-171">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="fecf6-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="fecf6-172">NULL</span><span class="sxs-lookup"><span data-stu-id="fecf6-172">NULL</span></span>     | <span data-ttu-id="fecf6-173">Отменить результат</span><span class="sxs-lookup"><span data-stu-id="fecf6-173">Discard Result</span></span>  | <span data-ttu-id="fecf6-174">Недоступно</span><span class="sxs-lookup"><span data-stu-id="fecf6-174">N/A</span></span>   | <span data-ttu-id="fecf6-175">W</span><span class="sxs-lookup"><span data-stu-id="fecf6-175">W</span></span>   | <span data-ttu-id="fecf6-176">Недоступно</span><span class="sxs-lookup"><span data-stu-id="fecf6-176">N/A</span></span>       | <span data-ttu-id="fecf6-177">Недоступно</span><span class="sxs-lookup"><span data-stu-id="fecf6-177">N/A</span></span>              | <span data-ttu-id="fecf6-178">Недоступно</span><span class="sxs-lookup"><span data-stu-id="fecf6-178">N/A</span></span>      | <span data-ttu-id="fecf6-179">Нет</span><span class="sxs-lookup"><span data-stu-id="fecf6-179">No</span></span>           |
| <span data-ttu-id="fecf6-180">вывода\#</span><span class="sxs-lookup"><span data-stu-id="fecf6-180">o\#</span></span>      | <span data-ttu-id="fecf6-181">Регистр выходных данных</span><span class="sxs-lookup"><span data-stu-id="fecf6-181">Output Register</span></span> | <span data-ttu-id="fecf6-182">32</span><span class="sxs-lookup"><span data-stu-id="fecf6-182">32</span></span>    | <span data-ttu-id="fecf6-183">W</span><span class="sxs-lookup"><span data-stu-id="fecf6-183">W</span></span>   | <span data-ttu-id="fecf6-184">Недоступно</span><span class="sxs-lookup"><span data-stu-id="fecf6-184">N/A</span></span>       | <span data-ttu-id="fecf6-185">Недоступно</span><span class="sxs-lookup"><span data-stu-id="fecf6-185">N/A</span></span>              | <span data-ttu-id="fecf6-186">4</span><span class="sxs-lookup"><span data-stu-id="fecf6-186">4</span></span>        | <span data-ttu-id="fecf6-187">Да</span><span class="sxs-lookup"><span data-stu-id="fecf6-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="fecf6-188">См. также</span><span class="sxs-lookup"><span data-stu-id="fecf6-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fecf6-189">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="fecf6-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




