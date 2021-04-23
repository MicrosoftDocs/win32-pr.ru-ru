---
title: Константы D3DCOMPILE (D3DCompiler. h)
description: Константы D3DCOMPILE указывают, как компилятор компилирует код HLSL.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273717"
---
# <a name="d3dcompile-constants"></a><span data-ttu-id="b1afc-103">Константы D3DCOMPILE</span><span class="sxs-lookup"><span data-stu-id="b1afc-103">D3DCOMPILE Constants</span></span>

<span data-ttu-id="b1afc-104">Константы D3DCOMPILE указывают, как компилятор компилирует код HLSL.</span><span class="sxs-lookup"><span data-stu-id="b1afc-104">The D3DCOMPILE constants specify how the compiler compiles the HLSL code.</span></span>

<dl> <dt>

<span data-ttu-id="b1afc-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**\_Отладка D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="b1afc-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE\_DEBUG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="b1afc-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-107">Направляет компилятору команду на вставку в выходной код отладочного файла, строки, типа или символьной информации.</span><span class="sxs-lookup"><span data-stu-id="b1afc-107">Directs the compiler to insert debug file/line/type/symbol information into the output code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ пропустить \_ проверку**</span><span class="sxs-lookup"><span data-stu-id="b1afc-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE\_SKIP\_VALIDATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-109">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="b1afc-109">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-110">Указывает компилятору не проверять созданный код на соответствие известным возможностям и ограничениям.</span><span class="sxs-lookup"><span data-stu-id="b1afc-110">Directs the compiler not to validate the generated code against known capabilities and constraints.</span></span> <span data-ttu-id="b1afc-111">Рекомендуется использовать эту константу только с шейдерами, которые были успешно скомпилированы в прошлом.</span><span class="sxs-lookup"><span data-stu-id="b1afc-111">We recommend that you use this constant only with shaders that have been successfully compiled in the past.</span></span> <span data-ttu-id="b1afc-112">DirectX всегда проверяет шейдеры перед их назначением устройству.</span><span class="sxs-lookup"><span data-stu-id="b1afc-112">DirectX always validates shaders before it sets them to a device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**\_Оптимизация D3DCOMPILE Skip \_**</span><span class="sxs-lookup"><span data-stu-id="b1afc-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE\_SKIP\_OPTIMIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-114">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="b1afc-114">(1 << 2)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-115">Указывает компилятору пропустить этапы оптимизации во время создания кода.</span><span class="sxs-lookup"><span data-stu-id="b1afc-115">Directs the compiler to skip optimization steps during code generation.</span></span> <span data-ttu-id="b1afc-116">Эту константу рекомендуется устанавливать только в целях отладки.</span><span class="sxs-lookup"><span data-stu-id="b1afc-116">We recommend that you set this constant for debug purposes only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**\_ \_ Основная строка матрицы D3DCOMPILE Pack \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1afc-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_ROW\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-118">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="b1afc-118">(1 << 3)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-119">Направляет компилятору упаковку матриц в построчном порядке для входных и выходных данных шейдера.</span><span class="sxs-lookup"><span data-stu-id="b1afc-119">Directs the compiler to pack matrices in row-major order on input and output from the shader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**\_ \_ Столбец матрицы D3DCOMPILE Pack — \_ \_ основной**</span><span class="sxs-lookup"><span data-stu-id="b1afc-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_COLUMN\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-121">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="b1afc-121">(1 << 4)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-122">Направляет компилятору упаковку матриц в пошаговом порядке столбцов для ввода и вывода шейдера.</span><span class="sxs-lookup"><span data-stu-id="b1afc-122">Directs the compiler to pack matrices in column-major order on input and output from the shader.</span></span> <span data-ttu-id="b1afc-123">Этот тип упаковки, как правило, более эффективен, так как ряд точечных продуктов может выполнять умножение векторных матриц.</span><span class="sxs-lookup"><span data-stu-id="b1afc-123">This type of packing is generally more efficient because a series of dot-products can then perform vector-matrix multiplication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**\_Частичная \_ точность D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="b1afc-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE\_PARTIAL\_PRECISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-125">(1 << 5)</span><span class="sxs-lookup"><span data-stu-id="b1afc-125">(1 << 5)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-126">Направляет компилятор для выполнения всех вычислений с частичной точностью.</span><span class="sxs-lookup"><span data-stu-id="b1afc-126">Directs the compiler to perform all computations with partial precision.</span></span> <span data-ttu-id="b1afc-127">Если задать эту константу, скомпилированный код может работать быстрее на определенном оборудовании.</span><span class="sxs-lookup"><span data-stu-id="b1afc-127">If you set this constant, the compiled code might run faster on some hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ Force \_ и \_ программное обеспечение \_ без \_ согласия**</span><span class="sxs-lookup"><span data-stu-id="b1afc-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE\_FORCE\_VS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-129">(1 << 6)</span><span class="sxs-lookup"><span data-stu-id="b1afc-129">(1 << 6)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-130">Направляет компилятору компиляцию вершинного шейдера для следующего более высокого профиля шейдера.</span><span class="sxs-lookup"><span data-stu-id="b1afc-130">Directs the compiler to compile a vertex shader for the next highest shader profile.</span></span> <span data-ttu-id="b1afc-131">Эта константа включает отладку и оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="b1afc-131">This constant turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ принудительно использовать \_ \_ программное обеспечение PS \_ без \_ согласия**</span><span class="sxs-lookup"><span data-stu-id="b1afc-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE\_FORCE\_PS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-133">(1 << 7)</span><span class="sxs-lookup"><span data-stu-id="b1afc-133">(1 << 7)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-134">Направляет компилятору компиляцию пиксельного шейдера для следующего более высокого профиля шейдера.</span><span class="sxs-lookup"><span data-stu-id="b1afc-134">Directs the compiler to compile a pixel shader for the next highest shader profile.</span></span> <span data-ttu-id="b1afc-135">Эта константа также включает отладку и оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="b1afc-135">This constant also turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ без \_ предшейдера**</span><span class="sxs-lookup"><span data-stu-id="b1afc-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE\_NO\_PRESHADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-137">(1 << 8)</span><span class="sxs-lookup"><span data-stu-id="b1afc-137">(1 << 8)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-138">Указывает компилятору отключить предшейдеры.</span><span class="sxs-lookup"><span data-stu-id="b1afc-138">Directs the compiler to disable Preshaders.</span></span> <span data-ttu-id="b1afc-139">Если задать эту константу, компилятор не выберет статическое выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="b1afc-139">If you set this constant, the compiler does not pull out static expression for evaluation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ избегать \_ \_ управления потоком**</span><span class="sxs-lookup"><span data-stu-id="b1afc-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE\_AVOID\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-141">(1 << 9)</span><span class="sxs-lookup"><span data-stu-id="b1afc-141">(1 << 9)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-142">Указывает компилятору не использовать конструкции управления потоком там, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="b1afc-142">Directs the compiler to not use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ предпочитать \_ \_ Управление потоком**</span><span class="sxs-lookup"><span data-stu-id="b1afc-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE\_PREFER\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-144">(1 << 10)</span><span class="sxs-lookup"><span data-stu-id="b1afc-144">(1 << 10)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-145">Указывает компилятору использовать конструкции управления потоком там, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="b1afc-145">Directs the compiler to use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ включить \_ точность**</span><span class="sxs-lookup"><span data-stu-id="b1afc-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE\_ENABLE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-147">(1 << 11)</span><span class="sxs-lookup"><span data-stu-id="b1afc-147">(1 << 11)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-148">Вызывает принудительную компиляцию, что может привести к невозможности использования устаревшего синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="b1afc-148">Forces strict compile, which might not allow for legacy syntax.</span></span>

<span data-ttu-id="b1afc-149">По умолчанию компилятор отключает жесткость в устаревшем синтаксисе.</span><span class="sxs-lookup"><span data-stu-id="b1afc-149">By default, the compiler disables strictness on deprecated syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ включить \_ обратную \_ Совместимость**</span><span class="sxs-lookup"><span data-stu-id="b1afc-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-151">(1 << 12)</span><span class="sxs-lookup"><span data-stu-id="b1afc-151">(1 << 12)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-152">Указывает компилятору включить более старые шейдеры для компиляции до 5 \_ 0 целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="b1afc-152">Directs the compiler to enable older shaders to compile to 5\_0 targets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE \_**</span><span class="sxs-lookup"><span data-stu-id="b1afc-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE\_IEEE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-154">(1 << 13)</span><span class="sxs-lookup"><span data-stu-id="b1afc-154">(1 << 13)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-155">Вызывает принудительную компиляцию IEEE.</span><span class="sxs-lookup"><span data-stu-id="b1afc-155">Forces the IEEE strict compile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**\_LEVEL0 оптимизация \_ D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="b1afc-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-157">(1 << 14)</span><span class="sxs-lookup"><span data-stu-id="b1afc-157">(1 << 14)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-158">Указывает компилятору использовать самый низкий уровень оптимизации.</span><span class="sxs-lookup"><span data-stu-id="b1afc-158">Directs the compiler to use the lowest optimization level.</span></span> <span data-ttu-id="b1afc-159">Если задать эту константу, компилятор может создать более медленный код, но быстро создаст код.</span><span class="sxs-lookup"><span data-stu-id="b1afc-159">If you set this constant, the compiler might produce slower code but produces the code more quickly.</span></span> <span data-ttu-id="b1afc-160">Установите эту константу при итеративной разработке шейдера.</span><span class="sxs-lookup"><span data-stu-id="b1afc-160">Set this constant when you develop the shader iteratively.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**\_Level1 оптимизация \_ D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="b1afc-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-162">0</span><span class="sxs-lookup"><span data-stu-id="b1afc-162">0</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-163">Указывает компилятору использовать второй минимальный уровень оптимизации.</span><span class="sxs-lookup"><span data-stu-id="b1afc-163">Directs the compiler to use the second lowest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**\_Level2 оптимизация \_ D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="b1afc-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-165">((1 << 14) \| (1 << 15))</span><span class="sxs-lookup"><span data-stu-id="b1afc-165">((1 << 14) \| (1 << 15))</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-166">Указывает компилятору использовать второй высший уровень оптимизации.</span><span class="sxs-lookup"><span data-stu-id="b1afc-166">Directs the compiler to use the second highest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**\_LEVEL3 оптимизация \_ D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="b1afc-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-168">(1 << 15)</span><span class="sxs-lookup"><span data-stu-id="b1afc-168">(1 << 15)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-169">Указывает компилятору использовать самый высокий уровень оптимизации.</span><span class="sxs-lookup"><span data-stu-id="b1afc-169">Directs the compiler to use the highest optimization level.</span></span> <span data-ttu-id="b1afc-170">Если задать эту константу, компилятор создаст лучший код, но это может занять значительно больше времени.</span><span class="sxs-lookup"><span data-stu-id="b1afc-170">If you set this constant, the compiler produces the best possible code but might take significantly longer to do so.</span></span> <span data-ttu-id="b1afc-171">Установите эту константу для окончательных сборок приложения, когда производительность является наиболее важным фактором.</span><span class="sxs-lookup"><span data-stu-id="b1afc-171">Set this constant for final builds of an application when performance is the most important factor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**\_Предупреждения D3DCOMPILE \_ — \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="b1afc-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**D3DCOMPILE\_WARNINGS\_ARE\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-173">(1 << 18)</span><span class="sxs-lookup"><span data-stu-id="b1afc-173">(1 << 18)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-174">Указывает компилятору обрабатывать все предупреждения как ошибки при компиляции кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="b1afc-174">Directs the compiler to treat all warnings as errors when it compiles the shader code.</span></span> <span data-ttu-id="b1afc-175">Рекомендуется использовать эту константу для нового кода шейдера, чтобы можно было разрешить все предупреждения и уменьшить число ненужных ошибок в коде.</span><span class="sxs-lookup"><span data-stu-id="b1afc-175">We recommend that you use this constant for new shader code, so that you can resolve all warnings and lower the number of hard-to-find code defects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**\_Ресурсы D3DCOMPILE \_ могут быть \_ псевдонимами**</span><span class="sxs-lookup"><span data-stu-id="b1afc-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE\_RESOURCES\_MAY\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-177">(1 << 19)</span><span class="sxs-lookup"><span data-stu-id="b1afc-177">(1 << 19)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-178">Указывает компилятору предположить, что неупорядоченные представления доступа (Уавс) и представления ресурсов шейдера (СРВС) могут быть псевдонимами для CS \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="b1afc-178">Directs the compiler to assume that unordered access views (UAVs) and shader resource views (SRVs) may alias for cs\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="b1afc-179">Эта константа компилятора является новой, начиная с \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="b1afc-179">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ включить \_ неограниченные \_ таблицы дескрипторов \_**</span><span class="sxs-lookup"><span data-stu-id="b1afc-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE\_ENABLE\_UNBOUNDED\_DESCRIPTOR\_TABLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-181">(1 << 20)</span><span class="sxs-lookup"><span data-stu-id="b1afc-181">(1 << 20)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-182">Указывает компилятору включить неограниченные таблицы дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="b1afc-182">Directs the compiler to enable unbounded descriptor tables.</span></span>

> [!Note]  
> <span data-ttu-id="b1afc-183">Эта константа компилятора является новой, начиная с \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="b1afc-183">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1afc-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ все \_ ресурсы \_ привязаны**</span><span class="sxs-lookup"><span data-stu-id="b1afc-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE\_ALL\_RESOURCES\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1afc-185">(1 << 21)</span><span class="sxs-lookup"><span data-stu-id="b1afc-185">(1 << 21)</span></span>
</dt> <dt>



<span data-ttu-id="b1afc-186">Указывает компилятору убедиться, что все ресурсы привязаны.</span><span class="sxs-lookup"><span data-stu-id="b1afc-186">Directs the compiler to ensure all resources are bound.</span></span>

> [!Note]  
> <span data-ttu-id="b1afc-187">Эта константа компилятора является новой, начиная с \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="b1afc-187">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1afc-188">Требования</span><span class="sxs-lookup"><span data-stu-id="b1afc-188">Requirements</span></span>



| <span data-ttu-id="b1afc-189">Требование</span><span class="sxs-lookup"><span data-stu-id="b1afc-189">Requirement</span></span> | <span data-ttu-id="b1afc-190">Значение</span><span class="sxs-lookup"><span data-stu-id="b1afc-190">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1afc-191">Header</span><span class="sxs-lookup"><span data-stu-id="b1afc-191">Header</span></span><br/> | <dl> <span data-ttu-id="b1afc-192"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1afc-192"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1afc-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1afc-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1afc-194">Константы D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="b1afc-194">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





