---
title: Структура CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
description: Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. См \_ . раздел State D3D12 графического \_ конвейера \_ \_ DESC and D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC. | Структура CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd04f58f4f123850c60b67ff9358f6f1f934373
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713517"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a><span data-ttu-id="0406e-106">\_ \_ Структура STREAM1 состояния КОНВЕЙЕРа CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="0406e-106">CD3DX12\_PIPELINE\_STATE\_STREAM1 structure</span></span>

<span data-ttu-id="0406e-107">Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0406e-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="0406e-108">См. раздел [**\_ State D3D12 графического \_ конвейера \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="0406e-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="0406e-109">\_Состояние конвейера CD3DX12 \_ \_ STREAM1 поддерживает обновление Windows 10 Creators Update с новыми функциями, такими как создание экземпляров для просмотра.</span><span class="sxs-lookup"><span data-stu-id="0406e-109">CD3DX12\_PIPELINE\_STATE\_STREAM1 supports the Windows 10 Fall Creators Update with new features such as view instancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="0406e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0406e-110">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM1 {
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1();
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```



## <a name="members"></a><span data-ttu-id="0406e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="0406e-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="0406e-112">**\_STREAM1 состояния конвейера CD3DX12 \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="0406e-112">**CD3DX12\_PIPELINE\_STATE\_STREAM1()**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-113">Создает новый, неинициализированный экземпляр CD3DX12 \_ состояния конвейера \_ \_ STREAM1.</span><span class="sxs-lookup"><span data-stu-id="0406e-113">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-114">**\_Состояние конвейера CD3DX12 \_ \_ STREAM1 (const D3D12 \_ графическое \_ конвейер \_ State \_ DESC& DESC)**</span><span class="sxs-lookup"><span data-stu-id="0406e-114">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-115">Создает новый экземпляр \_ состояния конвейера CD3DX12 \_ \_ STREAM1, который инициализируется значениями, скопированными из структуры **\_ \_ \_ STREAM1 состояния конвейера CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="0406e-115">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-116">**CD3DX12 \_ состояние конвейера \_ \_ STREAM1 (const D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC& DESC)**</span><span class="sxs-lookup"><span data-stu-id="0406e-116">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-117">Создает новый экземпляр \_ состояния конвейера CD3DX12 \_ \_ STREAM1, который инициализируется значениями, скопированными из структуры **\_ \_ \_ STREAM1 состояния конвейера CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="0406e-117">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-118">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="0406e-118">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-119">Возвращает содержимое \_ объекта STREAM1 состояния конвейера CD3DX12 в \_ \_ виде \_ графического \_ конвейера D3D12 \_ \_ . Структура по значению.</span><span class="sxs-lookup"><span data-stu-id="0406e-119">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="0406e-120">Обратите внимание, что D3D12 \_ графического \_ конвейера \_ \_ со значением DESC не включает элемент **CS** , поэтому при преобразовании это значение будет потеряно.</span><span class="sxs-lookup"><span data-stu-id="0406e-120">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-121">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="0406e-121">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-122">Возвращает содержимое \_ \_ объекта STREAM1 состояния конвейера CD3DX12 \_ как D3D12 \_ Вычисление \_ состояния конвейера \_ \_ по значению.</span><span class="sxs-lookup"><span data-stu-id="0406e-122">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="0406e-123">Обратите внимание, что D3D12 \_ Вычисление \_ состояния конвейера не \_ \_ включает элементы **инпутлайаут**, **ибстрипкутвалуе**, **примитиветопологитипе**, **VS**, **GS**, **стреамаутпут**, **HS**, **DS**, **PS**, **блендстате,** **депсстенЦилстате**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** или **SampleMask** , поэтому эти значения теряются при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="0406e-123">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-124">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="0406e-124">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-125">Описывает флаги состояния конвейера, которые управляют такими функциями, как "Отладка инструмента".</span><span class="sxs-lookup"><span data-stu-id="0406e-125">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="0406e-126">**нодемаск**</span><span class="sxs-lookup"><span data-stu-id="0406e-126">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-127">Описывает маску узла состояния конвейера, которая используется для указания узлов (физических адаптеров устройства), к которым применяется PSO в сценариях с несколькими адаптерами. Каждый бит маски соответствует одному узлу.</span><span class="sxs-lookup"><span data-stu-id="0406e-127">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="0406e-128">Для сценариев с одним адаптером присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="0406e-128">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-129">**прутсигнатуре**</span><span class="sxs-lookup"><span data-stu-id="0406e-129">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-130">Описывает корневую подпись.</span><span class="sxs-lookup"><span data-stu-id="0406e-130">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-131">**инпутлайаут**</span><span class="sxs-lookup"><span data-stu-id="0406e-131">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-132">Описывает формат входного буфера для этапа ассемблера ввода</span><span class="sxs-lookup"><span data-stu-id="0406e-132">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="0406e-133">**ибстрипкутвалуе**</span><span class="sxs-lookup"><span data-stu-id="0406e-133">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-134">Описывает особое значение индекса входного буфера, которое указывает на вырезание (прекращение) при использовании топологии ленты треугольника.</span><span class="sxs-lookup"><span data-stu-id="0406e-134">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-135">**примитиветопологитипе**</span><span class="sxs-lookup"><span data-stu-id="0406e-135">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-136">Описывает топологию примитива и ее порядок.</span><span class="sxs-lookup"><span data-stu-id="0406e-136">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-137">**ЛИНЕЙЧАТ**</span><span class="sxs-lookup"><span data-stu-id="0406e-137">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-138">Описывает шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="0406e-138">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-139">**GS**</span><span class="sxs-lookup"><span data-stu-id="0406e-139">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-140">Описывает шейдер Geometry.</span><span class="sxs-lookup"><span data-stu-id="0406e-140">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-141">**стреамаутпут**</span><span class="sxs-lookup"><span data-stu-id="0406e-141">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-142">Описывает потоковый выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="0406e-142">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-143">**HS**</span><span class="sxs-lookup"><span data-stu-id="0406e-143">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-144">Описывает шейдер поверхности.</span><span class="sxs-lookup"><span data-stu-id="0406e-144">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-145">**DS**</span><span class="sxs-lookup"><span data-stu-id="0406e-145">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-146">Описывает Шейдер доменов.</span><span class="sxs-lookup"><span data-stu-id="0406e-146">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-147">**PS**</span><span class="sxs-lookup"><span data-stu-id="0406e-147">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-148">Описывает шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="0406e-148">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-149">**CS**</span><span class="sxs-lookup"><span data-stu-id="0406e-149">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-150">Описывает вычисление шейдера.</span><span class="sxs-lookup"><span data-stu-id="0406e-150">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-151">**блендстате**</span><span class="sxs-lookup"><span data-stu-id="0406e-151">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-152">Описывает состояние смешения.</span><span class="sxs-lookup"><span data-stu-id="0406e-152">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-153">**депсстенЦилстате**</span><span class="sxs-lookup"><span data-stu-id="0406e-153">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-154">Описывает состояние шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="0406e-154">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-155">**дсвформат**</span><span class="sxs-lookup"><span data-stu-id="0406e-155">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-156">Описывает формат трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="0406e-156">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-157">**растеризерстате**</span><span class="sxs-lookup"><span data-stu-id="0406e-157">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-158">Описывает состояние средства программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="0406e-158">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-159">**ртвформатс**</span><span class="sxs-lookup"><span data-stu-id="0406e-159">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-160">Описывает форматы целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="0406e-160">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-161">**сампледеск**</span><span class="sxs-lookup"><span data-stu-id="0406e-161">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-162">Описывает количество образцов и качество.</span><span class="sxs-lookup"><span data-stu-id="0406e-162">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-163">**самплемаск**</span><span class="sxs-lookup"><span data-stu-id="0406e-163">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-164">Описывает образец маски, используемый в состоянии Blend.</span><span class="sxs-lookup"><span data-stu-id="0406e-164">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="0406e-165">**качедпсо**</span><span class="sxs-lookup"><span data-stu-id="0406e-165">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="0406e-166">Описывает кэшированный PSO.</span><span class="sxs-lookup"><span data-stu-id="0406e-166">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0406e-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0406e-167">Remarks</span></span>

<span data-ttu-id="0406e-168">[**CD3DX12 \_ \_ \_ Поток состояния конвейера**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) поддерживает обновление для дизайнеров Windows 10, но не поддерживает типы подобъектов, добавленные в обновление Windows 10 Creators Update, например для создания экземпляров представления.</span><span class="sxs-lookup"><span data-stu-id="0406e-168">[**CD3DX12\_PIPELINE\_STATE\_STREAM**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) supports the Windows 10 Fall Creators Update, but doesn't support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="0406e-169">Для поддержки новых типов подобъектов используйте \_ \_ вместо него состояние конвейера CD3DX12 \_ STREAM1.</span><span class="sxs-lookup"><span data-stu-id="0406e-169">To support the new subobject types, use CD3DX12\_PIPELINE\_STATE\_STREAM1 instead.</span></span>

<span data-ttu-id="0406e-170">Доступные переменные-члены этой структуры являются typedef \_ \_ \_ шаблона подобъекта потока состояния конвейера CD3DX12 \_ , который объединяет данные маркера типа и подобъекта в один объект, подходящий для описания потока.</span><span class="sxs-lookup"><span data-stu-id="0406e-170">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="0406e-171">Эти определения типов:</span><span class="sxs-lookup"><span data-stu-id="0406e-171">Those typedefs are:</span></span>

<span data-ttu-id="0406e-172"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="0406e-172"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0406e-173">Требования</span><span class="sxs-lookup"><span data-stu-id="0406e-173">Requirements</span></span>



| <span data-ttu-id="0406e-174">Требование</span><span class="sxs-lookup"><span data-stu-id="0406e-174">Requirement</span></span> | <span data-ttu-id="0406e-175">Значение</span><span class="sxs-lookup"><span data-stu-id="0406e-175">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0406e-176">Header</span><span class="sxs-lookup"><span data-stu-id="0406e-176">Header</span></span><br/> | <dl> <span data-ttu-id="0406e-177"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0406e-177"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0406e-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0406e-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0406e-179">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="0406e-179">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="0406e-180">**\_Поток состояния конвейера CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0406e-180">**CD3DX12\_PIPELINE\_STATE\_STREAM**</span></span>](cd3dx12-pipeline-state-stream.md)
</dt> <dt>

[<span data-ttu-id="0406e-181">**D3D12 \_ графика \_ состояния графического конвейера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0406e-181">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="0406e-182">**\_DESC для \_ состояния конвейера D3D12 COMPUTE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0406e-182">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





