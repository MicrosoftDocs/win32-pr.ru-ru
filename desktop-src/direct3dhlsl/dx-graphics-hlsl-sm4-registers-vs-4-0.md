---
title: Регистры — vs_4_0
description: В этом разделе содержатся справочные сведения по входным и выходным регистрам, реализованным построителем вершин версии 4 \_ 0.
ms.assetid: f471df6a-06f6-4783-ba8f-cf0a3b43727f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 425fc4174b1c4a103fc7db15b5f05ae2b6dd95e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996759"
---
# <a name="registers---vs_4_0"></a><span data-ttu-id="a0765-103">Регистры-VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0765-103">Registers - vs\_4\_0</span></span>

<span data-ttu-id="a0765-104">В этом разделе содержатся справочные сведения по входным и выходным регистрам, реализованным построителем вершин версии 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="a0765-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="a0765-105">Входные регистры</span><span class="sxs-lookup"><span data-stu-id="a0765-105">Input Registers</span></span>



| <span data-ttu-id="a0765-106">Регистрация</span><span class="sxs-lookup"><span data-stu-id="a0765-106">Register</span></span>      | <span data-ttu-id="a0765-107">Имя</span><span class="sxs-lookup"><span data-stu-id="a0765-107">Name</span></span> | <span data-ttu-id="a0765-108">Count</span><span class="sxs-lookup"><span data-stu-id="a0765-108">Count</span></span>              | <span data-ttu-id="a0765-109">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="a0765-109">R/W</span></span> | <span data-ttu-id="a0765-110">Измерение</span><span class="sxs-lookup"><span data-stu-id="a0765-110">Dimension</span></span> | <span data-ttu-id="a0765-111">Индексация по r\#</span><span class="sxs-lookup"><span data-stu-id="a0765-111">Indexable by r\#</span></span> | <span data-ttu-id="a0765-112">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a0765-112">Defaults</span></span> | <span data-ttu-id="a0765-113">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="a0765-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="a0765-114">Cерверный\#</span><span class="sxs-lookup"><span data-stu-id="a0765-114">r\#</span></span>           |      | <span data-ttu-id="a0765-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="a0765-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="a0765-116">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="a0765-116">R/W</span></span> | <span data-ttu-id="a0765-117">4</span><span class="sxs-lookup"><span data-stu-id="a0765-117">4</span></span>         | <span data-ttu-id="a0765-118">нет</span><span class="sxs-lookup"><span data-stu-id="a0765-118">No</span></span>               | <span data-ttu-id="a0765-119">None</span><span class="sxs-lookup"><span data-stu-id="a0765-119">None</span></span>     | <span data-ttu-id="a0765-120">Да</span><span class="sxs-lookup"><span data-stu-id="a0765-120">Yes</span></span>          |
| <span data-ttu-id="a0765-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="a0765-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="a0765-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="a0765-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="a0765-123">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="a0765-123">R/W</span></span> | <span data-ttu-id="a0765-124">4</span><span class="sxs-lookup"><span data-stu-id="a0765-124">4</span></span>         | <span data-ttu-id="a0765-125">Да</span><span class="sxs-lookup"><span data-stu-id="a0765-125">Yes</span></span>              | <span data-ttu-id="a0765-126">Нет</span><span class="sxs-lookup"><span data-stu-id="a0765-126">None</span></span>     | <span data-ttu-id="a0765-127">Да</span><span class="sxs-lookup"><span data-stu-id="a0765-127">Yes</span></span>          |
| <span data-ttu-id="a0765-128">3,3\#</span><span class="sxs-lookup"><span data-stu-id="a0765-128">v\#</span></span>           |      | <span data-ttu-id="a0765-129">16</span><span class="sxs-lookup"><span data-stu-id="a0765-129">16</span></span>                 | <span data-ttu-id="a0765-130">R</span><span class="sxs-lookup"><span data-stu-id="a0765-130">R</span></span>   | <span data-ttu-id="a0765-131">4</span><span class="sxs-lookup"><span data-stu-id="a0765-131">4</span></span>         | <span data-ttu-id="a0765-132">Да</span><span class="sxs-lookup"><span data-stu-id="a0765-132">Yes</span></span>              | <span data-ttu-id="a0765-133">Нет</span><span class="sxs-lookup"><span data-stu-id="a0765-133">None</span></span>     | <span data-ttu-id="a0765-134">Да</span><span class="sxs-lookup"><span data-stu-id="a0765-134">Yes</span></span>          |
| <span data-ttu-id="a0765-135">t\#</span><span class="sxs-lookup"><span data-stu-id="a0765-135">t\#</span></span>           |      | <span data-ttu-id="a0765-136">128</span><span class="sxs-lookup"><span data-stu-id="a0765-136">128</span></span>                | <span data-ttu-id="a0765-137">R</span><span class="sxs-lookup"><span data-stu-id="a0765-137">R</span></span>   | <span data-ttu-id="a0765-138">1</span><span class="sxs-lookup"><span data-stu-id="a0765-138">1</span></span>         | <span data-ttu-id="a0765-139">Нет</span><span class="sxs-lookup"><span data-stu-id="a0765-139">No</span></span>               | <span data-ttu-id="a0765-140">None</span><span class="sxs-lookup"><span data-stu-id="a0765-140">None</span></span>     | <span data-ttu-id="a0765-141">Да</span><span class="sxs-lookup"><span data-stu-id="a0765-141">Yes</span></span>          |
| <span data-ttu-id="a0765-142">s\#</span><span class="sxs-lookup"><span data-stu-id="a0765-142">s\#</span></span>           |      | <span data-ttu-id="a0765-143">16</span><span class="sxs-lookup"><span data-stu-id="a0765-143">16</span></span>                 | <span data-ttu-id="a0765-144">R</span><span class="sxs-lookup"><span data-stu-id="a0765-144">R</span></span>   | <span data-ttu-id="a0765-145">1</span><span class="sxs-lookup"><span data-stu-id="a0765-145">1</span></span>         | <span data-ttu-id="a0765-146">Нет</span><span class="sxs-lookup"><span data-stu-id="a0765-146">No</span></span>               | <span data-ttu-id="a0765-147">None</span><span class="sxs-lookup"><span data-stu-id="a0765-147">None</span></span>     | <span data-ttu-id="a0765-148">Да</span><span class="sxs-lookup"><span data-stu-id="a0765-148">Yes</span></span>          |
| <span data-ttu-id="a0765-149">\# \[ индекс CB\]</span><span class="sxs-lookup"><span data-stu-id="a0765-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="a0765-150">15</span><span class="sxs-lookup"><span data-stu-id="a0765-150">15</span></span>                 | <span data-ttu-id="a0765-151">R</span><span class="sxs-lookup"><span data-stu-id="a0765-151">R</span></span>   | <span data-ttu-id="a0765-152">4</span><span class="sxs-lookup"><span data-stu-id="a0765-152">4</span></span>         | <span data-ttu-id="a0765-153">Да (содержимое)</span><span class="sxs-lookup"><span data-stu-id="a0765-153">Yes(Contents)</span></span>    | <span data-ttu-id="a0765-154">Нет</span><span class="sxs-lookup"><span data-stu-id="a0765-154">None</span></span>     | <span data-ttu-id="a0765-155">Да</span><span class="sxs-lookup"><span data-stu-id="a0765-155">Yes</span></span>          |
| <span data-ttu-id="a0765-156">индекс блока ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="a0765-156">icb\[index\]</span></span>  |      | <span data-ttu-id="a0765-157">1</span><span class="sxs-lookup"><span data-stu-id="a0765-157">1</span></span>                  | <span data-ttu-id="a0765-158">R</span><span class="sxs-lookup"><span data-stu-id="a0765-158">R</span></span>   | <span data-ttu-id="a0765-159">4</span><span class="sxs-lookup"><span data-stu-id="a0765-159">4</span></span>         | <span data-ttu-id="a0765-160">Да (содержимое)</span><span class="sxs-lookup"><span data-stu-id="a0765-160">Yes(Contents)</span></span>    | <span data-ttu-id="a0765-161">Нет</span><span class="sxs-lookup"><span data-stu-id="a0765-161">None</span></span>     | <span data-ttu-id="a0765-162">Да</span><span class="sxs-lookup"><span data-stu-id="a0765-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="a0765-163">Выходные регистры</span><span class="sxs-lookup"><span data-stu-id="a0765-163">Output Registers</span></span>



| <span data-ttu-id="a0765-164">Регистрация</span><span class="sxs-lookup"><span data-stu-id="a0765-164">Register</span></span> | <span data-ttu-id="a0765-165">Имя</span><span class="sxs-lookup"><span data-stu-id="a0765-165">Name</span></span>            | <span data-ttu-id="a0765-166">Count</span><span class="sxs-lookup"><span data-stu-id="a0765-166">Count</span></span> | <span data-ttu-id="a0765-167">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="a0765-167">R/W</span></span> | <span data-ttu-id="a0765-168">Измерение</span><span class="sxs-lookup"><span data-stu-id="a0765-168">Dimension</span></span> | <span data-ttu-id="a0765-169">Индексация по r\#</span><span class="sxs-lookup"><span data-stu-id="a0765-169">Indexable by r\#</span></span> | <span data-ttu-id="a0765-170">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a0765-170">Defaults</span></span> | <span data-ttu-id="a0765-171">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="a0765-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="a0765-172">NULL</span><span class="sxs-lookup"><span data-stu-id="a0765-172">NULL</span></span>     | <span data-ttu-id="a0765-173">Отменить результат</span><span class="sxs-lookup"><span data-stu-id="a0765-173">Discard Result</span></span>  | <span data-ttu-id="a0765-174">Недоступно</span><span class="sxs-lookup"><span data-stu-id="a0765-174">N/A</span></span>   | <span data-ttu-id="a0765-175">W</span><span class="sxs-lookup"><span data-stu-id="a0765-175">W</span></span>   | <span data-ttu-id="a0765-176">Недоступно</span><span class="sxs-lookup"><span data-stu-id="a0765-176">N/A</span></span>       | <span data-ttu-id="a0765-177">Недоступно</span><span class="sxs-lookup"><span data-stu-id="a0765-177">N/A</span></span>              | <span data-ttu-id="a0765-178">Недоступно</span><span class="sxs-lookup"><span data-stu-id="a0765-178">N/A</span></span>      | <span data-ttu-id="a0765-179">Нет</span><span class="sxs-lookup"><span data-stu-id="a0765-179">No</span></span>           |
| <span data-ttu-id="a0765-180">вывода\#</span><span class="sxs-lookup"><span data-stu-id="a0765-180">o\#</span></span>      | <span data-ttu-id="a0765-181">Регистр выходных данных</span><span class="sxs-lookup"><span data-stu-id="a0765-181">Output Register</span></span> | <span data-ttu-id="a0765-182">16</span><span class="sxs-lookup"><span data-stu-id="a0765-182">16</span></span>    | <span data-ttu-id="a0765-183">W</span><span class="sxs-lookup"><span data-stu-id="a0765-183">W</span></span>   | <span data-ttu-id="a0765-184">Недоступно</span><span class="sxs-lookup"><span data-stu-id="a0765-184">N/A</span></span>       | <span data-ttu-id="a0765-185">Недоступно</span><span class="sxs-lookup"><span data-stu-id="a0765-185">N/A</span></span>              | <span data-ttu-id="a0765-186">4</span><span class="sxs-lookup"><span data-stu-id="a0765-186">4</span></span>        | <span data-ttu-id="a0765-187">Да</span><span class="sxs-lookup"><span data-stu-id="a0765-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="a0765-188">См. также</span><span class="sxs-lookup"><span data-stu-id="a0765-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0765-189">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="a0765-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




