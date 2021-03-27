---
title: Сборка Shader Model 4
description: Сборка Shader Model 4
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068011"
---
# <a name="shader-model-4-assembly"></a><span data-ttu-id="a7b62-103">Сборка Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="a7b62-103">Shader Model 4 Assembly</span></span>

<span data-ttu-id="a7b62-104">Шейдер Model 4 требует программирования шейдеров в HLSL.</span><span class="sxs-lookup"><span data-stu-id="a7b62-104">Shader Model 4 requires you to program shaders in HLSL.</span></span> <span data-ttu-id="a7b62-105">Однако компилятор шейдера компилирует код HLSL в сборку, которая выполняется на устройстве.</span><span class="sxs-lookup"><span data-stu-id="a7b62-105">However, the shader compiler compiles the HLSL code into assembly that runs on the device.</span></span> <span data-ttu-id="a7b62-106">Если для отладки шейдеров используется PIX для Windows, можно выбрать отображение кода шейдера либо в HLSL, либо в сборке.</span><span class="sxs-lookup"><span data-stu-id="a7b62-106">If you are using PIX for Windows to debug your shaders, you can choose to display shader code in either HLSL or assembly.</span></span> <span data-ttu-id="a7b62-107">В этом разделе перечислены инструкции по сборке шейдера 4 и шейдера 4,1, которые могут возникнуть при отладке шейдера.</span><span class="sxs-lookup"><span data-stu-id="a7b62-107">This section lists the Shader Model 4 and Shader Model 4.1 assembly instructions that you may encounter when debugging a shader.</span></span>

<dl>

[<span data-ttu-id="a7b62-108">Модификаторы инструкций</span><span class="sxs-lookup"><span data-stu-id="a7b62-108">Instruction Modifiers</span></span>](instruction-modifiers.md)  
[<span data-ttu-id="a7b62-109">add</span><span class="sxs-lookup"><span data-stu-id="a7b62-109">add</span></span>](add--sm4---asm-.md)  
[<span data-ttu-id="a7b62-110">and</span><span class="sxs-lookup"><span data-stu-id="a7b62-110">and</span></span>](and--sm4---asm-.md)  
[<span data-ttu-id="a7b62-111">break</span><span class="sxs-lookup"><span data-stu-id="a7b62-111">break</span></span>](break--sm4---asm-.md)  
[<span data-ttu-id="a7b62-112">бреакк</span><span class="sxs-lookup"><span data-stu-id="a7b62-112">breakc</span></span>](breakc--sm4---asm-.md)  
[<span data-ttu-id="a7b62-113">call</span><span class="sxs-lookup"><span data-stu-id="a7b62-113">call</span></span>](call--sm4---asm-.md)  
[<span data-ttu-id="a7b62-114">каллк</span><span class="sxs-lookup"><span data-stu-id="a7b62-114">callc</span></span>](callc--sm4---asm-.md)  
[<span data-ttu-id="a7b62-115">case</span><span class="sxs-lookup"><span data-stu-id="a7b62-115">case</span></span>](case--sm4---asm-.md)  
[<span data-ttu-id="a7b62-116">continue</span><span class="sxs-lookup"><span data-stu-id="a7b62-116">continue</span></span>](continue--sm4---asm-.md)  
[<span data-ttu-id="a7b62-117">континуек</span><span class="sxs-lookup"><span data-stu-id="a7b62-117">continuec</span></span>](continuec--sm4---asm-.md)  
[<span data-ttu-id="a7b62-118">бавьте</span><span class="sxs-lookup"><span data-stu-id="a7b62-118">cut</span></span>](cut--sm4---asm-.md)  
[<span data-ttu-id="a7b62-119">дкл \_ константбуффер</span><span class="sxs-lookup"><span data-stu-id="a7b62-119">dcl\_constantBuffer</span></span>](dcl-constantbuffer.md)  
[<span data-ttu-id="a7b62-120">дкл \_ глобалфлагс</span><span class="sxs-lookup"><span data-stu-id="a7b62-120">dcl\_globalFlags</span></span>](dcl-globalflags.md)  
[<span data-ttu-id="a7b62-121">дкл \_ иммедиатеконстантбуффер</span><span class="sxs-lookup"><span data-stu-id="a7b62-121">dcl\_immediateConstantBuffer</span></span>](dcl-immediateconstantbuffer.md)  
[<span data-ttu-id="a7b62-122">дкл \_ индексаблетемп</span><span class="sxs-lookup"><span data-stu-id="a7b62-122">dcl\_indexableTemp</span></span>](dcl-indexabletemp.md)  
[<span data-ttu-id="a7b62-123">дкл \_ индексранже</span><span class="sxs-lookup"><span data-stu-id="a7b62-123">dcl\_indexRange</span></span>](dcl-indexrange.md)  
[<span data-ttu-id="a7b62-124">\_входные данные дкл</span><span class="sxs-lookup"><span data-stu-id="a7b62-124">dcl\_input</span></span>](dcl-input.md)  
[<span data-ttu-id="a7b62-125">дкл \_ входное \_ SV</span><span class="sxs-lookup"><span data-stu-id="a7b62-125">dcl\_input\_sv</span></span>](dcl-input-sv.md)  
[<span data-ttu-id="a7b62-126">дкл \_ входные вприм</span><span class="sxs-lookup"><span data-stu-id="a7b62-126">dcl\_input vPrim</span></span>](dcl-input-vprim.md)  
[<span data-ttu-id="a7b62-127">дкл \_ максаутпутвертекскаунт</span><span class="sxs-lookup"><span data-stu-id="a7b62-127">dcl\_maxOutputVertexCount</span></span>](dcl-maxoutputvertexcount.md)  
[<span data-ttu-id="a7b62-128">\_выходные данные дкл</span><span class="sxs-lookup"><span data-stu-id="a7b62-128">dcl\_output</span></span>](dcl-output.md)  
[<span data-ttu-id="a7b62-129">дкл \_ выходной \_ одепс</span><span class="sxs-lookup"><span data-stu-id="a7b62-129">dcl\_output\_oDepth</span></span>](dcl-output-odepth.md)  
[<span data-ttu-id="a7b62-130">дкл \_ выходной \_ СГВ</span><span class="sxs-lookup"><span data-stu-id="a7b62-130">dcl\_output\_sgv</span></span>](dcl-output-sgv.md)  
[<span data-ttu-id="a7b62-131">дкл \_ выходной \_ Сив</span><span class="sxs-lookup"><span data-stu-id="a7b62-131">dcl\_output\_siv</span></span>](dcl-output-siv.md)  
[<span data-ttu-id="a7b62-132">дкл \_ аутпуттопологи</span><span class="sxs-lookup"><span data-stu-id="a7b62-132">dcl\_outputTopology</span></span>](dcl-outputtopology.md)  
[<span data-ttu-id="a7b62-133">\_ресурс дкл</span><span class="sxs-lookup"><span data-stu-id="a7b62-133">dcl\_resource</span></span>](dcl-resource.md)  
[<span data-ttu-id="a7b62-134">\_образец дкл</span><span class="sxs-lookup"><span data-stu-id="a7b62-134">dcl\_sampler</span></span>](dcl-sampler.md)  
[<span data-ttu-id="a7b62-135">дкл \_ временные температуры</span><span class="sxs-lookup"><span data-stu-id="a7b62-135">dcl\_temps</span></span>](dcl-temps.md)  
[<span data-ttu-id="a7b62-136">default</span><span class="sxs-lookup"><span data-stu-id="a7b62-136">default</span></span>](default--sm4---asm-.md)  
[<span data-ttu-id="a7b62-137">наследование \_ RTX</span><span class="sxs-lookup"><span data-stu-id="a7b62-137">deriv\_rtx</span></span>](deriv-rtx--sm4---asm-.md)  
[<span data-ttu-id="a7b62-138">наследование \_ РТИ</span><span class="sxs-lookup"><span data-stu-id="a7b62-138">deriv\_rty</span></span>](deriv-rty--sm4---asm-.md)  
[<span data-ttu-id="a7b62-139">исключить</span><span class="sxs-lookup"><span data-stu-id="a7b62-139">discard</span></span>](discard--sm4---asm-.md)  
[<span data-ttu-id="a7b62-140">div</span><span class="sxs-lookup"><span data-stu-id="a7b62-140">div</span></span>](div--sm4---asm-.md)  
[<span data-ttu-id="a7b62-141">dp2</span><span class="sxs-lookup"><span data-stu-id="a7b62-141">dp2</span></span>](dp2--sm4---asm-.md)  
[<span data-ttu-id="a7b62-142">dp3</span><span class="sxs-lookup"><span data-stu-id="a7b62-142">dp3</span></span>](dp3--sm4---asm-.md)  
[<span data-ttu-id="a7b62-143">dp4</span><span class="sxs-lookup"><span data-stu-id="a7b62-143">dp4</span></span>](dp4--sm4---asm-.md)  
[<span data-ttu-id="a7b62-144">else</span><span class="sxs-lookup"><span data-stu-id="a7b62-144">else</span></span>](else--sm4---asm-.md)  
[<span data-ttu-id="a7b62-145">давать</span><span class="sxs-lookup"><span data-stu-id="a7b62-145">emit</span></span>](emit--sm4---asm-.md)  
[<span data-ttu-id="a7b62-146">емитсенкут</span><span class="sxs-lookup"><span data-stu-id="a7b62-146">emitThenCut</span></span>](emitthencut--sm4---asm-.md)  
[<span data-ttu-id="a7b62-147">endif</span><span class="sxs-lookup"><span data-stu-id="a7b62-147">endif</span></span>](endif--sm4---asm-.md)  
[<span data-ttu-id="a7b62-148">ендлуп</span><span class="sxs-lookup"><span data-stu-id="a7b62-148">endloop</span></span>](endloop--sm4---asm-.md)  
[<span data-ttu-id="a7b62-149">ендсвитч</span><span class="sxs-lookup"><span data-stu-id="a7b62-149">endswitch</span></span>](endswitch--sm4---asm-.md)  
[<span data-ttu-id="a7b62-150">eq</span><span class="sxs-lookup"><span data-stu-id="a7b62-150">eq</span></span>](eq--sm4---asm-.md)  
[<span data-ttu-id="a7b62-151">exp</span><span class="sxs-lookup"><span data-stu-id="a7b62-151">exp</span></span>](exp--sm4---asm-.md)  
[<span data-ttu-id="a7b62-152">фрк</span><span class="sxs-lookup"><span data-stu-id="a7b62-152">frc</span></span>](frc--sm4---asm-.md)  
[<span data-ttu-id="a7b62-153">фтои</span><span class="sxs-lookup"><span data-stu-id="a7b62-153">ftoi</span></span>](ftoi--sm4---asm-.md)  
[<span data-ttu-id="a7b62-154">фтау</span><span class="sxs-lookup"><span data-stu-id="a7b62-154">ftou</span></span>](ftou--sm4---asm-.md)  
[<span data-ttu-id="a7b62-155">ge</span><span class="sxs-lookup"><span data-stu-id="a7b62-155">ge</span></span>](ge--sm4---asm-.md)  
[<span data-ttu-id="a7b62-156">IAdd</span><span class="sxs-lookup"><span data-stu-id="a7b62-156">iadd</span></span>](iadd--sm4---asm-.md)  
[<span data-ttu-id="a7b62-157">ибфе</span><span class="sxs-lookup"><span data-stu-id="a7b62-157">ibfe</span></span>](dne--sm5---asm-.md)  
[<span data-ttu-id="a7b62-158">иек</span><span class="sxs-lookup"><span data-stu-id="a7b62-158">ieq</span></span>](ieq--sm4---asm-.md)  
[<span data-ttu-id="a7b62-159">if</span><span class="sxs-lookup"><span data-stu-id="a7b62-159">if</span></span>](if--sm4---asm-.md)  
[<span data-ttu-id="a7b62-160">иже</span><span class="sxs-lookup"><span data-stu-id="a7b62-160">ige</span></span>](ige--sm4---asm-.md)  
[<span data-ttu-id="a7b62-161">илт</span><span class="sxs-lookup"><span data-stu-id="a7b62-161">ilt</span></span>](ilt--sm4---asm-.md)  
[<span data-ttu-id="a7b62-162">имад</span><span class="sxs-lookup"><span data-stu-id="a7b62-162">imad</span></span>](imad--sm4---asm-.md)  
[<span data-ttu-id="a7b62-163">имин</span><span class="sxs-lookup"><span data-stu-id="a7b62-163">imin</span></span>](imin--sm4---asm-.md)  
[<span data-ttu-id="a7b62-164">imul</span><span class="sxs-lookup"><span data-stu-id="a7b62-164">imul</span></span>](imul--sm4---asm-.md)  
[<span data-ttu-id="a7b62-165">Строка</span><span class="sxs-lookup"><span data-stu-id="a7b62-165">ine</span></span>](ine--sm4---asm-.md)  
[<span data-ttu-id="a7b62-166">инег</span><span class="sxs-lookup"><span data-stu-id="a7b62-166">ineg</span></span>](ineg--sm4---asm-.md)  
[<span data-ttu-id="a7b62-167">ишл</span><span class="sxs-lookup"><span data-stu-id="a7b62-167">ishl</span></span>](ishl--sm4---asm-.md)  
[<span data-ttu-id="a7b62-168">ишр</span><span class="sxs-lookup"><span data-stu-id="a7b62-168">ishr</span></span>](ishr--sm4---asm-.md)  
[<span data-ttu-id="a7b62-169">итоф</span><span class="sxs-lookup"><span data-stu-id="a7b62-169">itof</span></span>](itof--sm4---asm-.md)  
[<span data-ttu-id="a7b62-170">label</span><span class="sxs-lookup"><span data-stu-id="a7b62-170">label</span></span>](label--sm4---asm-.md)  
[<span data-ttu-id="a7b62-171">LD</span><span class="sxs-lookup"><span data-stu-id="a7b62-171">ld</span></span>](ld--sm4---asm-.md)  
[<span data-ttu-id="a7b62-172">Журналь</span><span class="sxs-lookup"><span data-stu-id="a7b62-172">log</span></span>](log--sm4---asm-.md)  
[<span data-ttu-id="a7b62-173">loop</span><span class="sxs-lookup"><span data-stu-id="a7b62-173">loop</span></span>](loop--sm4---asm-.md)  
[<span data-ttu-id="a7b62-174">lt</span><span class="sxs-lookup"><span data-stu-id="a7b62-174">lt</span></span>](lt--sm4---asm-.md)  
[<span data-ttu-id="a7b62-175">отслеживания</span><span class="sxs-lookup"><span data-stu-id="a7b62-175">mad</span></span>](mad--sm4---asm-.md)  
[<span data-ttu-id="a7b62-176">max</span><span class="sxs-lookup"><span data-stu-id="a7b62-176">max</span></span>](max--sm4---asm-.md)  
[<span data-ttu-id="a7b62-177">min</span><span class="sxs-lookup"><span data-stu-id="a7b62-177">min</span></span>](min--sm4---asm-.md)  
[<span data-ttu-id="a7b62-178">функцию</span><span class="sxs-lookup"><span data-stu-id="a7b62-178">mov</span></span>](mov--sm4---asm-.md)  
[<span data-ttu-id="a7b62-179">мовк</span><span class="sxs-lookup"><span data-stu-id="a7b62-179">movc</span></span>](movc--sm4---asm-.md)  
[<span data-ttu-id="a7b62-180">mul</span><span class="sxs-lookup"><span data-stu-id="a7b62-180">mul</span></span>](mul--sm4---asm-.md)  
[<span data-ttu-id="a7b62-181">ne</span><span class="sxs-lookup"><span data-stu-id="a7b62-181">ne</span></span>](ne--sm4---asm-.md)  
[<span data-ttu-id="a7b62-182">NOP</span><span class="sxs-lookup"><span data-stu-id="a7b62-182">nop</span></span>](nop--sm4---asm-.md)  
<span data-ttu-id="a7b62-183">[not](not--sm4---asm-.md) (не);</span><span class="sxs-lookup"><span data-stu-id="a7b62-183">[not](not--sm4---asm-.md)</span></span>  
[<span data-ttu-id="a7b62-184">или диспетчер конфигурации служб</span><span class="sxs-lookup"><span data-stu-id="a7b62-184">or</span></span>](or--sm4---asm-.md)  
[<span data-ttu-id="a7b62-185">Resinfo:</span><span class="sxs-lookup"><span data-stu-id="a7b62-185">resinfo</span></span>](resinfo--sm4---asm-.md)  
[<span data-ttu-id="a7b62-186">обратно</span><span class="sxs-lookup"><span data-stu-id="a7b62-186">ret</span></span>](ret--sm4---asm-.md)  
[<span data-ttu-id="a7b62-187">ретк</span><span class="sxs-lookup"><span data-stu-id="a7b62-187">retc</span></span>](retc--sm4---asm-.md)  
[<span data-ttu-id="a7b62-188">Round \_ Ne</span><span class="sxs-lookup"><span data-stu-id="a7b62-188">round\_ne</span></span>](round-ne--sm4---asm-.md)  
[<span data-ttu-id="a7b62-189">Round \_ Ni</span><span class="sxs-lookup"><span data-stu-id="a7b62-189">round\_ni</span></span>](round-ni--sm4---asm-.md)  
[<span data-ttu-id="a7b62-190">скругленное число \_ Пи</span><span class="sxs-lookup"><span data-stu-id="a7b62-190">round\_pi</span></span>](round-pi--sm4---asm-.md)  
[<span data-ttu-id="a7b62-191">округлить по \_ оси z</span><span class="sxs-lookup"><span data-stu-id="a7b62-191">round\_z</span></span>](round-z--sm4---asm-.md)  
[<span data-ttu-id="a7b62-192">рск</span><span class="sxs-lookup"><span data-stu-id="a7b62-192">rsq</span></span>](rsq--sm4---asm-.md)  
[<span data-ttu-id="a7b62-193">Следующий</span><span class="sxs-lookup"><span data-stu-id="a7b62-193">sample</span></span>](sample--sm4---asm-.md)  
[<span data-ttu-id="a7b62-194">Пример \_ б</span><span class="sxs-lookup"><span data-stu-id="a7b62-194">sample\_b</span></span>](sample-b--sm4---asm-.md)  
[<span data-ttu-id="a7b62-195">Пример \_ с</span><span class="sxs-lookup"><span data-stu-id="a7b62-195">sample\_c</span></span>](sample-c--sm4---asm-.md)  
[<span data-ttu-id="a7b62-196">Пример \_ c \_ LZ</span><span class="sxs-lookup"><span data-stu-id="a7b62-196">sample\_c\_lz</span></span>](sample-c-lz--sm4---asm-.md)  
[<span data-ttu-id="a7b62-197">Пример \_ г</span><span class="sxs-lookup"><span data-stu-id="a7b62-197">sample\_d</span></span>](sample-d--sm4---asm-.md)  
[<span data-ttu-id="a7b62-198">Пример \_ l</span><span class="sxs-lookup"><span data-stu-id="a7b62-198">sample\_l</span></span>](sample-l--sm4---asm-.md)  
[<span data-ttu-id="a7b62-199">синкос</span><span class="sxs-lookup"><span data-stu-id="a7b62-199">sincos</span></span>](sincos--sm4---asm-.md)  
[<span data-ttu-id="a7b62-200">МНИМ</span><span class="sxs-lookup"><span data-stu-id="a7b62-200">sqrt</span></span>](sqrt--sm4---asm-.md)  
[<span data-ttu-id="a7b62-201">switch</span><span class="sxs-lookup"><span data-stu-id="a7b62-201">switch</span></span>](switch--sm4---asm-.md)  
[<span data-ttu-id="a7b62-202">удив</span><span class="sxs-lookup"><span data-stu-id="a7b62-202">udiv</span></span>](udiv--sm4---asm-.md)  
[<span data-ttu-id="a7b62-203">уже</span><span class="sxs-lookup"><span data-stu-id="a7b62-203">uge</span></span>](uge--sm4---asm-.md)  
[<span data-ttu-id="a7b62-204">метры</span><span class="sxs-lookup"><span data-stu-id="a7b62-204">ult</span></span>](ult--sm4---asm-.md)  
[<span data-ttu-id="a7b62-205">умад</span><span class="sxs-lookup"><span data-stu-id="a7b62-205">umad</span></span>](umad--sm4---asm-.md)  
[<span data-ttu-id="a7b62-206">Компания</span><span class="sxs-lookup"><span data-stu-id="a7b62-206">umax</span></span>](umax--sm4---asm-.md)  
[<span data-ttu-id="a7b62-207">умин</span><span class="sxs-lookup"><span data-stu-id="a7b62-207">umin</span></span>](umin--sm4---asm-.md)  
[<span data-ttu-id="a7b62-208">умул</span><span class="sxs-lookup"><span data-stu-id="a7b62-208">umul</span></span>](umul--sm4---asm-.md)  
[<span data-ttu-id="a7b62-209">ушр</span><span class="sxs-lookup"><span data-stu-id="a7b62-209">ushr</span></span>](ushr--sm4---asm-.md)  
[<span data-ttu-id="a7b62-210">утоф</span><span class="sxs-lookup"><span data-stu-id="a7b62-210">utof</span></span>](utof--sm4---asm-.md)  
[<span data-ttu-id="a7b62-211">xor</span><span class="sxs-lookup"><span data-stu-id="a7b62-211">xor</span></span>](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a><span data-ttu-id="a7b62-212">Сборка Shader модели 4,1</span><span class="sxs-lookup"><span data-stu-id="a7b62-212">Shader Model 4.1 Assembly</span></span>

<span data-ttu-id="a7b62-213">Модель шейдеров 4,1 поддерживает все инструкции и следующие дополнительные инструкции для 4,0 модели шейдера.</span><span class="sxs-lookup"><span data-stu-id="a7b62-213">Shader Model 4.1 supports all of the Shader Model 4.0 instructions and the following additional instructions:</span></span>

<dl>

[<span data-ttu-id="a7b62-214">gather4</span><span class="sxs-lookup"><span data-stu-id="a7b62-214">gather4</span></span>](gather4--sm4-1---asm-.md)  
[<span data-ttu-id="a7b62-215">ld2dms</span><span class="sxs-lookup"><span data-stu-id="a7b62-215">ld2dms</span></span>](ld2dms--sm4-1---asm-.md)  
[<span data-ttu-id="a7b62-216">лод</span><span class="sxs-lookup"><span data-stu-id="a7b62-216">lod</span></span>](lod--sm4-1---asm-.md)  
[<span data-ttu-id="a7b62-217">самплеинфо</span><span class="sxs-lookup"><span data-stu-id="a7b62-217">sampleinfo</span></span>](sampleinfo--sm4-1---asm-.md)  
[<span data-ttu-id="a7b62-218">самплепос</span><span class="sxs-lookup"><span data-stu-id="a7b62-218">samplepos</span></span>](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="a7b62-219">См. также</span><span class="sxs-lookup"><span data-stu-id="a7b62-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7b62-220">Справочник по шейдеру ASM</span><span class="sxs-lookup"><span data-stu-id="a7b62-220">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> <dt>

[<span data-ttu-id="a7b62-221">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="a7b62-221">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




