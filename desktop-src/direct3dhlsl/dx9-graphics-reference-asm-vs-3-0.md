---
title: vs_3_0
description: Программируемый шейдер вершин состоит из набора инструкций, которые работают с данными вершин. Регистрирует перенос данных в ALU и из него. Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22a0e6e84aff34dcec44713dc4382e391ad05c2b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103891192"
---
# <a name="vs_3_0"></a><span data-ttu-id="b5f40-105">VS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b5f40-105">vs\_3\_0</span></span>

<span data-ttu-id="b5f40-106">Программируемый шейдер вершин состоит из набора инструкций, которые работают с данными вершин.</span><span class="sxs-lookup"><span data-stu-id="b5f40-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="b5f40-107">Регистрирует перенос данных в ALU и из него.</span><span class="sxs-lookup"><span data-stu-id="b5f40-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="b5f40-108">Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.</span><span class="sxs-lookup"><span data-stu-id="b5f40-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="b5f40-109">Версия шейдера вершин VS \_ 3 \_ 0 расширяет набор функций, поддерживаемый VS \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="b5f40-109">Vertex shader version vs\_3\_0 extends the feature set supported by vs\_2\_x.</span></span> <span data-ttu-id="b5f40-110">Каждая из функций в VS \_ 2 \_ X, для которой требуется установить ограничение, доступна в VS \_ 3 \_ 0 без обязательного ограничения.</span><span class="sxs-lookup"><span data-stu-id="b5f40-110">Each of the features in vs\_2\_X that requires a cap to be set, is available in vs\_3\_0 without requiring the cap.</span></span>

-   <span data-ttu-id="b5f40-111">[Инструкции. VS \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) содержит список доступных инструкций.</span><span class="sxs-lookup"><span data-stu-id="b5f40-111">[Instructions - vs\_3\_0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="b5f40-112">[Регистры-VS \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) содержит список различных типов регистров, используемых вершиной шейдера ALU.</span><span class="sxs-lookup"><span data-stu-id="b5f40-112">[Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="b5f40-113">[Модификаторы регистра вершинного шейдера](dx9-graphics-reference-asm-vs-registers-modifiers.md) используются для изменения способа работы инструкции.</span><span class="sxs-lookup"><span data-stu-id="b5f40-113">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="b5f40-114">[Модификаторы исходного регистра вершинного шейдера](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) изменяют данные исходной регистрации перед выполнением инструкции.</span><span class="sxs-lookup"><span data-stu-id="b5f40-114">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="b5f40-115">[Исходный регистр группирующие](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) обеспечивает дополнительный контроль над тем, какие компоненты регистрации считываются, копируются или записываются.</span><span class="sxs-lookup"><span data-stu-id="b5f40-115">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="b5f40-116">[Маскирование регистров назначения](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) определяет, какие компоненты записываются в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="b5f40-116">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="b5f40-117">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="b5f40-117">New Features</span></span>

<span data-ttu-id="b5f40-118">В следующих разделах перечислены новые функции версии шейдера вершин и \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="b5f40-118">New features of vertex shader version vs\_3\_0 are listed in the following sections.</span></span>

### <a name="indexing-registers"></a><span data-ttu-id="b5f40-119">Регистры индексации</span><span class="sxs-lookup"><span data-stu-id="b5f40-119">Indexing Registers</span></span>

<span data-ttu-id="b5f40-120">В более ранних моделях шейдеров можно было индексировать только банк регистров констант.</span><span class="sxs-lookup"><span data-stu-id="b5f40-120">In the earlier shader models, only the constant register bank could be indexed.</span></span> <span data-ttu-id="b5f40-121">В этой модели можно индексировать следующие банки регистров, используя регистр счетчиков циклов (aL):</span><span class="sxs-lookup"><span data-stu-id="b5f40-121">In this model, the following register banks can be indexed, using the loop counter register (aL):</span></span>

-   <span data-ttu-id="b5f40-122">Входной регистр (v \# )</span><span class="sxs-lookup"><span data-stu-id="b5f40-122">Input register (v\#)</span></span>
-   <span data-ttu-id="b5f40-123">Выходной регистр (o \# )</span><span class="sxs-lookup"><span data-stu-id="b5f40-123">Output register (o\#)</span></span>

### <a name="vertex-textures"></a><span data-ttu-id="b5f40-124">Текстуры вершин</span><span class="sxs-lookup"><span data-stu-id="b5f40-124">Vertex Textures</span></span>

<span data-ttu-id="b5f40-125">Эта модель шейдера поддерживает поиск текстур в шейдере вершин с помощью текслдл.</span><span class="sxs-lookup"><span data-stu-id="b5f40-125">This shader model supports texture lookup in the vertex shader using texldl.</span></span> <span data-ttu-id="b5f40-126">Ядро вершин имеет четыре этапа образца текстуры (отличающиеся от образца карт смещения и выборки текстур в подсистеме пикселей), которые можно использовать, чтобы выбрать текстуры на этих этапах.</span><span class="sxs-lookup"><span data-stu-id="b5f40-126">The vertex engine has four texture sampler stages (distinct from the displacement map sampler and the texture samplers in the pixel engine) that can be used to sample textures set at those stages.</span></span> <span data-ttu-id="b5f40-127">См. сведения о [текстурах вершин в VS \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span><span class="sxs-lookup"><span data-stu-id="b5f40-127">See [Vertex Textures in vs\_3\_0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span></span>

### <a name="vertex-stream-frequency"></a><span data-ttu-id="b5f40-128">Частота потока вершин</span><span class="sxs-lookup"><span data-stu-id="b5f40-128">Vertex Stream Frequency</span></span>

<span data-ttu-id="b5f40-129">Эта функция позволяет инициализировать подмножество входных регистров со скоростью, отличной от одной для каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="b5f40-129">This feature allows a subset of the input registers to be initialized at a rate different from once per vertex.</span></span> <span data-ttu-id="b5f40-130">См. раздел [Рисование неиндексированной геометрии](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span><span class="sxs-lookup"><span data-stu-id="b5f40-130">See [Drawing Non-Indexed Geometry](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span></span>

### <a name="shader-output"></a><span data-ttu-id="b5f40-131">Выходные данные шейдера</span><span class="sxs-lookup"><span data-stu-id="b5f40-131">Shader Output</span></span>

<span data-ttu-id="b5f40-132">Как и в VS \_ 2 \_ 0, выходные данные шейдера могут зависеть от статического управления потоком.</span><span class="sxs-lookup"><span data-stu-id="b5f40-132">Similar to vs\_2\_0, the output of the shader can vary with static flow control.</span></span> <span data-ttu-id="b5f40-133">Будьте внимательны при динамической ветвлении, так как это может привести к тому, что выходные данные шейдера будут зависеть от каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="b5f40-133">Be careful with dynamic branching as this can cause shader outputs to vary per vertex.</span></span> <span data-ttu-id="b5f40-134">Это приведет к непредсказуемым результатам на другом оборудовании.</span><span class="sxs-lookup"><span data-stu-id="b5f40-134">This will produce unpredictable results on different hardware.</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="b5f40-135">Динамическое управление потоком</span><span class="sxs-lookup"><span data-stu-id="b5f40-135">Dynamic flow control</span></span>

<span data-ttu-id="b5f40-136">Поддерживаются все инструкции динамического управления потоком.</span><span class="sxs-lookup"><span data-stu-id="b5f40-136">All dynamic flow control instructions are supported.</span></span> <span data-ttu-id="b5f40-137">Максимально допустимое значение глубины вложения — 24.</span><span class="sxs-lookup"><span data-stu-id="b5f40-137">The maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="b5f40-138">(Дополнительные сведения см. в статье [ограничения вложений управления потоком](dx9-graphics-reference-asm-vs-instructions-flow-control.md) .)</span><span class="sxs-lookup"><span data-stu-id="b5f40-138">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="temporary-registers"></a><span data-ttu-id="b5f40-139">Временные регистры</span><span class="sxs-lookup"><span data-stu-id="b5f40-139">Temporary Registers</span></span>

<span data-ttu-id="b5f40-140">Поддерживается всего 32 временных регистров (r \# ).</span><span class="sxs-lookup"><span data-stu-id="b5f40-140">A total of 32 temporary registers (r\#) is supported.</span></span>

### <a name="static-flow-control"></a><span data-ttu-id="b5f40-141">Статическое управление потоком</span><span class="sxs-lookup"><span data-stu-id="b5f40-141">Static Flow Control</span></span>

<span data-ttu-id="b5f40-142">Максимальная глубина вложенности для представителя [цикла](loop---vs.md)-VS / [-VS](rep---vs.md) равна 4.</span><span class="sxs-lookup"><span data-stu-id="b5f40-142">The maximum nesting depth for [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) is 4.</span></span> <span data-ttu-id="b5f40-143">Максимальная глубина вложенности для [Call-VS](call---vs.md) / [каллнз bool-](callnz-bool---vs.md)VS / [каллнз пред-VS](callnz-pred---vs.md) равно 4.</span><span class="sxs-lookup"><span data-stu-id="b5f40-143">The maximum nesting depth for [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[callnz pred - vs](callnz-pred---vs.md) is 4.</span></span> <span data-ttu-id="b5f40-144">[Если для bool-VS](if-bool---vs.md), максимально допустимое значение глубины вложения равно 24.</span><span class="sxs-lookup"><span data-stu-id="b5f40-144">For [if bool - vs](if-bool---vs.md), the maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="b5f40-145">(Дополнительные сведения см. в статье [ограничения вложений управления потоком](dx9-graphics-reference-asm-vs-instructions-flow-control.md) .)</span><span class="sxs-lookup"><span data-stu-id="b5f40-145">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="predication"></a><span data-ttu-id="b5f40-146">Предикация</span><span class="sxs-lookup"><span data-stu-id="b5f40-146">Predication</span></span>

<span data-ttu-id="b5f40-147">Инструкция затенения поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b5f40-147">Instruction predication is supported.</span></span> <span data-ttu-id="b5f40-148">Для задания регистра предикатов используйте [сетп \_ comp-VS](setp-comp---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="b5f40-148">Use [setp\_comp - vs](setp-comp---vs.md) to set the predicate register.</span></span>

### <a name="instruction-count"></a><span data-ttu-id="b5f40-149">Число инструкций</span><span class="sxs-lookup"><span data-stu-id="b5f40-149">Instruction Count</span></span>

<span data-ttu-id="b5f40-150">Каждый шейдер вершин может находиться в любом месте от 512 до количества слотов в MaxVertexShader30InstructionSlots в [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="b5f40-150">Each vertex shader is allowed anywhere from 512 up to the number of slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> <span data-ttu-id="b5f40-151">Количество выполняемых инструкций может быть намного выше из-за поддержки цикла или представителя; Однако это ограничивается Максвшадеринструктионсексекутед в D3DCAPS9, который должен быть не менее 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="b5f40-151">The number of instructions run can be much higher because of the loop/rep support; however, this is capped by MaxVShaderInstructionsExecuted in D3DCAPS9 which should be at least 0xFFFF.</span></span>

### <a name="device-caps"></a><span data-ttu-id="b5f40-152">Ограничения устройств</span><span class="sxs-lookup"><span data-stu-id="b5f40-152">Device Caps</span></span>

<span data-ttu-id="b5f40-153">Если шейдер вершин 3 \_ 0 поддерживается, в оборудовании поддерживаются следующие ограничения (как минимум):</span><span class="sxs-lookup"><span data-stu-id="b5f40-153">If Vertex Shader 3\_0 is supported, the following caps are supported in hardware (at a minimum):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5f40-154">Колпачок</span><span class="sxs-lookup"><span data-stu-id="b5f40-154">Cap</span></span></th>
<th><span data-ttu-id="b5f40-155">Функция</span><span class="sxs-lookup"><span data-stu-id="b5f40-155">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5f40-156">Заглушки шейдеров</span><span class="sxs-lookup"><span data-stu-id="b5f40-156">Shader caps</span></span></td>
<td><ul>
<li><span data-ttu-id="b5f40-157">Динамикфловконтролдепс — 24</span><span class="sxs-lookup"><span data-stu-id="b5f40-157">DynamicFlowControlDepth is 24</span></span></li>
<li><span data-ttu-id="b5f40-158">Нумтемпс — 32</span><span class="sxs-lookup"><span data-stu-id="b5f40-158">NumTemps is 32</span></span></li>
<li><span data-ttu-id="b5f40-159">Статикфловконтролдепс — 4</span><span class="sxs-lookup"><span data-stu-id="b5f40-159">StaticFlowControlDepth is 4</span></span></li>
<li><span data-ttu-id="b5f40-160">Затенения поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b5f40-160">Predication is supported.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5f40-161">Гуардбандлефт, Гуардбандтоп, Гуардбандригхт, Гуардбандботтом</span><span class="sxs-lookup"><span data-stu-id="b5f40-161">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span></span></td>
<td><span data-ttu-id="b5f40-162">8 КБ</span><span class="sxs-lookup"><span data-stu-id="b5f40-162">8K</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5f40-163">вертексшадерверсион</span><span class="sxs-lookup"><span data-stu-id="b5f40-163">VertexShaderVersion</span></span></td>
<td><span data-ttu-id="b5f40-164">3_0</span><span class="sxs-lookup"><span data-stu-id="b5f40-164">3_0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5f40-165">максвертексшадерконст</span><span class="sxs-lookup"><span data-stu-id="b5f40-165">MaxVertexShaderConst</span></span></td>
<td><span data-ttu-id="b5f40-166">256</span><span class="sxs-lookup"><span data-stu-id="b5f40-166">256</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5f40-167">MaxVertexShader30InstructionSlots</span><span class="sxs-lookup"><span data-stu-id="b5f40-167">MaxVertexShader30InstructionSlots</span></span></td>
<td><span data-ttu-id="b5f40-168">512</span><span class="sxs-lookup"><span data-stu-id="b5f40-168">512</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5f40-169">Поддержка тумана</span><span class="sxs-lookup"><span data-stu-id="b5f40-169">Fog support</span></span></td>
<td><span data-ttu-id="b5f40-170">D3DPRASTERCAPS_FOGVERTEX</span><span class="sxs-lookup"><span data-stu-id="b5f40-170">D3DPRASTERCAPS_FOGVERTEX</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5f40-171">вертекстекстурефилтеркапс</span><span class="sxs-lookup"><span data-stu-id="b5f40-171">VertexTextureFilterCaps</span></span></td>
<td><ul>
<li><span data-ttu-id="b5f40-172"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="b5f40-172"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span></span></li>
<li><span data-ttu-id="b5f40-173"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="b5f40-173"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5f40-174"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span><span class="sxs-lookup"><span data-stu-id="b5f40-174"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span></span></td>
<td><span data-ttu-id="b5f40-175">Элементы вершины в объявлении вершины могут совместно использовать одно и то же смещение потока.</span><span class="sxs-lookup"><span data-stu-id="b5f40-175">Vertex elements in a vertex declaration can share the same stream offset.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5f40-176">Форматы вершин</span><span class="sxs-lookup"><span data-stu-id="b5f40-176">Vertex formats</span></span></td>
<td><ul>
<li><span data-ttu-id="b5f40-177">D3DDECLTYPE_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="b5f40-177">D3DDECLTYPE_UBYTE4</span></span></li>
<li><span data-ttu-id="b5f40-178">D3DDECLTYPE_UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="b5f40-178">D3DDECLTYPE_UBYTE4N</span></span></li>
<li><span data-ttu-id="b5f40-179">D3DDECLTYPE_SHORT2N</span><span class="sxs-lookup"><span data-stu-id="b5f40-179">D3DDECLTYPE_SHORT2N</span></span></li>
<li><span data-ttu-id="b5f40-180">D3DDECLTYPE_SHORT4N</span><span class="sxs-lookup"><span data-stu-id="b5f40-180">D3DDECLTYPE_SHORT4N</span></span></li>
<li><span data-ttu-id="b5f40-181">D3DDECLTYPE_FLOAT16_2</span><span class="sxs-lookup"><span data-stu-id="b5f40-181">D3DDECLTYPE_FLOAT16_2</span></span></li>
<li><span data-ttu-id="b5f40-182">D3DDECLTYPE_FLOAT16_4</span><span class="sxs-lookup"><span data-stu-id="b5f40-182">D3DDECLTYPE_FLOAT16_4</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b5f40-183">См. также</span><span class="sxs-lookup"><span data-stu-id="b5f40-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5f40-184">Шейдеры вершин</span><span class="sxs-lookup"><span data-stu-id="b5f40-184">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 