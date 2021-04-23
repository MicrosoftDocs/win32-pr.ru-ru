---
title: Структура CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
description: Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. См \_ . раздел State D3D12 графического \_ конвейера \_ \_ DESC and D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC. | Структура CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d52b9090fa1d3870027bbe360164627472c039e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713518"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a><span data-ttu-id="249e4-106">\_ \_ Структура потока состояния КОНВЕЙЕРа CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="249e4-106">CD3DX12\_PIPELINE\_STATE\_STREAM structure</span></span>

<span data-ttu-id="249e4-107">Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="249e4-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="249e4-108">См. раздел [**\_ State D3D12 графического \_ конвейера \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="249e4-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="249e4-109">\_Поток состояния конвейера CD3DX12 \_ \_ поддерживает обновление Windows 10 Creators Update и более новые, но не поддерживает новые функции обновления для дизайнеров, такие как создание экземпляров.</span><span class="sxs-lookup"><span data-stu-id="249e4-109">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer but doesn't support new features of the Fall Creators update, such as view instancing.</span></span> <span data-ttu-id="249e4-110">Для поддержки функций обновления "создатели обновлений" используйте вместо этого [**CD3DX12 \_ конвейер \_ состояния \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .</span><span class="sxs-lookup"><span data-stu-id="249e4-110">To support features of the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="249e4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="249e4-111">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
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



## <a name="members"></a><span data-ttu-id="249e4-112">Члены</span><span class="sxs-lookup"><span data-stu-id="249e4-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="249e4-113">**\_Поток состояния конвейера CD3DX12 \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="249e4-113">**CD3DX12\_PIPELINE\_STATE\_STREAM()**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-114">Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="249e4-114">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-115">**\_Поток состояния конвейера CD3DX12 \_ \_ (const D3D12 \_ графическое \_ конвейер \_ State \_ DESC& DESC)**</span><span class="sxs-lookup"><span data-stu-id="249e4-115">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-116">Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ , инициализируемый значениями, скопированными из структуры **\_ \_ \_ потока состояния конвейера CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="249e4-116">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-117">**\_Поток состояния конвейера CD3DX12 \_ \_ (const D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC& DESC)**</span><span class="sxs-lookup"><span data-stu-id="249e4-117">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-118">Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ , инициализируемый значениями, скопированными из структуры **\_ \_ \_ потока состояния конвейера CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="249e4-118">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-119">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="249e4-119">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-120">Возвращает содержимое \_ объекта потока состояния конвейера CD3DX12 в \_ \_ виде \_ графического \_ конвейера D3D12 \_ состояние \_ структуры по значению.</span><span class="sxs-lookup"><span data-stu-id="249e4-120">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="249e4-121">Обратите внимание, что D3D12 \_ графического \_ конвейера \_ \_ со значением DESC не включает элемент **CS** , поэтому при преобразовании это значение будет потеряно.</span><span class="sxs-lookup"><span data-stu-id="249e4-121">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-122">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="249e4-122">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-123">Возвращает содержимое \_ \_ объекта потока состояния конвейера CD3DX12 \_ как D3D12 \_ Вычисление \_ состояния конвейера в виде \_ \_ структуры по значению.</span><span class="sxs-lookup"><span data-stu-id="249e4-123">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="249e4-124">Обратите внимание, что D3D12 \_ Вычисление \_ состояния конвейера не \_ \_ включает элементы **инпутлайаут**, **ибстрипкутвалуе**, **примитиветопологитипе**, **VS**, **GS**, **стреамаутпут**, **HS**, **DS**, **PS**, **блендстате,** **депсстенЦилстате**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** или **SampleMask** , поэтому эти значения теряются при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="249e4-124">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-125">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="249e4-125">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-126">Описывает флаги состояния конвейера, которые управляют такими функциями, как "Отладка инструмента".</span><span class="sxs-lookup"><span data-stu-id="249e4-126">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="249e4-127">**нодемаск**</span><span class="sxs-lookup"><span data-stu-id="249e4-127">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-128">Описывает маску узла состояния конвейера, которая используется для указания узлов (физических адаптеров устройства), к которым применяется PSO в сценариях с несколькими адаптерами. Каждый бит маски соответствует одному узлу.</span><span class="sxs-lookup"><span data-stu-id="249e4-128">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="249e4-129">Для сценариев с одним адаптером присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="249e4-129">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-130">**прутсигнатуре**</span><span class="sxs-lookup"><span data-stu-id="249e4-130">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-131">Описывает корневую подпись.</span><span class="sxs-lookup"><span data-stu-id="249e4-131">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-132">**инпутлайаут**</span><span class="sxs-lookup"><span data-stu-id="249e4-132">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-133">Описывает формат входного буфера для этапа ассемблера ввода</span><span class="sxs-lookup"><span data-stu-id="249e4-133">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="249e4-134">**ибстрипкутвалуе**</span><span class="sxs-lookup"><span data-stu-id="249e4-134">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-135">Описывает особое значение индекса входного буфера, которое указывает на вырезание (прекращение) при использовании топологии ленты треугольника.</span><span class="sxs-lookup"><span data-stu-id="249e4-135">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-136">**примитиветопологитипе**</span><span class="sxs-lookup"><span data-stu-id="249e4-136">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-137">Описывает топологию примитива и ее порядок.</span><span class="sxs-lookup"><span data-stu-id="249e4-137">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-138">**ЛИНЕЙЧАТ**</span><span class="sxs-lookup"><span data-stu-id="249e4-138">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-139">Описывает шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="249e4-139">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-140">**GS**</span><span class="sxs-lookup"><span data-stu-id="249e4-140">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-141">Описывает шейдер Geometry.</span><span class="sxs-lookup"><span data-stu-id="249e4-141">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-142">**стреамаутпут**</span><span class="sxs-lookup"><span data-stu-id="249e4-142">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-143">Описывает потоковый выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="249e4-143">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-144">**HS**</span><span class="sxs-lookup"><span data-stu-id="249e4-144">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-145">Описывает шейдер поверхности.</span><span class="sxs-lookup"><span data-stu-id="249e4-145">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-146">**DS**</span><span class="sxs-lookup"><span data-stu-id="249e4-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-147">Описывает Шейдер доменов.</span><span class="sxs-lookup"><span data-stu-id="249e4-147">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-148">**PS**</span><span class="sxs-lookup"><span data-stu-id="249e4-148">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-149">Описывает шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="249e4-149">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-150">**CS**</span><span class="sxs-lookup"><span data-stu-id="249e4-150">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-151">Описывает вычисление шейдера.</span><span class="sxs-lookup"><span data-stu-id="249e4-151">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-152">**блендстате**</span><span class="sxs-lookup"><span data-stu-id="249e4-152">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-153">Описывает состояние смешения.</span><span class="sxs-lookup"><span data-stu-id="249e4-153">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-154">**депсстенЦилстате**</span><span class="sxs-lookup"><span data-stu-id="249e4-154">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-155">Описывает состояние шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="249e4-155">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-156">**дсвформат**</span><span class="sxs-lookup"><span data-stu-id="249e4-156">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-157">Описывает формат трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="249e4-157">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-158">**растеризерстате**</span><span class="sxs-lookup"><span data-stu-id="249e4-158">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-159">Описывает состояние средства программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="249e4-159">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-160">**ртвформатс**</span><span class="sxs-lookup"><span data-stu-id="249e4-160">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-161">Описывает форматы целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="249e4-161">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-162">**сампледеск**</span><span class="sxs-lookup"><span data-stu-id="249e4-162">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-163">Описывает количество образцов и качество.</span><span class="sxs-lookup"><span data-stu-id="249e4-163">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-164">**самплемаск**</span><span class="sxs-lookup"><span data-stu-id="249e4-164">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-165">Описывает образец маски, используемый в состоянии Blend.</span><span class="sxs-lookup"><span data-stu-id="249e4-165">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="249e4-166">**качедпсо**</span><span class="sxs-lookup"><span data-stu-id="249e4-166">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="249e4-167">Описывает кэшированный PSO.</span><span class="sxs-lookup"><span data-stu-id="249e4-167">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="249e4-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="249e4-168">Remarks</span></span>

<span data-ttu-id="249e4-169">\_Поток состояния конвейера CD3DX12 \_ \_ поддерживает обновление Windows 10 Creators Update и более новые версии, но не поддерживает типы подобъектов, добавленные в обновление Windows 10 для дизайнеров, например, для создания экземпляров представления.</span><span class="sxs-lookup"><span data-stu-id="249e4-169">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer, but doesn not support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="249e4-170">Чтобы обеспечить поддержку типов подобъектов, добавленных в обновление авторов, используйте вместо него [**\_ состояние конвейера CD3DX12 \_ \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .</span><span class="sxs-lookup"><span data-stu-id="249e4-170">To support subobject types added in the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

<span data-ttu-id="249e4-171">Доступные переменные-члены этой структуры являются typedef \_ \_ \_ шаблона подобъекта потока состояния конвейера CD3DX12 \_ , который объединяет данные маркера типа и подобъекта в один объект, подходящий для описания потока.</span><span class="sxs-lookup"><span data-stu-id="249e4-171">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="249e4-172">Эти определения типов:</span><span class="sxs-lookup"><span data-stu-id="249e4-172">Those typedefs are:</span></span>

<span data-ttu-id="249e4-173"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="249e4-173"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="249e4-174">Требования</span><span class="sxs-lookup"><span data-stu-id="249e4-174">Requirements</span></span>



| <span data-ttu-id="249e4-175">Требование</span><span class="sxs-lookup"><span data-stu-id="249e4-175">Requirement</span></span> | <span data-ttu-id="249e4-176">Значение</span><span class="sxs-lookup"><span data-stu-id="249e4-176">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="249e4-177">Header</span><span class="sxs-lookup"><span data-stu-id="249e4-177">Header</span></span><br/> | <dl> <span data-ttu-id="249e4-178"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="249e4-178"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="249e4-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="249e4-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="249e4-180">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="249e4-180">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="249e4-181">**\_STREAM1 состояния конвейера CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="249e4-181">**CD3DX12\_PIPELINE\_STATE\_STREAM1**</span></span>](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[<span data-ttu-id="249e4-182">**D3D12 \_ графика \_ состояния графического конвейера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="249e4-182">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="249e4-183">**\_DESC для \_ состояния конвейера D3D12 COMPUTE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="249e4-183">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





