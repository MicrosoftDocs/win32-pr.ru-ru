---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER (D3dx12. h)
description: Выполняет сборку внутреннего \_ \_ объекта потока состояния конвейера CD3DX12 \_ из сведений о подобъекте, переданных в соответствующие функции элементов. Эта структура реализует интерфейс ID3DX12PipelineParserCallbacks.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cc6228f690abd677e1adc8552293e440452ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694098"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a><span data-ttu-id="0ee29-105">\_ \_ \_ \_ Вспомогательная структура синтаксического анализа потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="0ee29-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_PARSE\_HELPER structure</span></span>

<span data-ttu-id="0ee29-106">Выполняет сборку внутреннего \_ \_ объекта потока состояния конвейера CD3DX12 \_ из сведений о подобъекте, переданных в соответствующие функции элементов.</span><span class="sxs-lookup"><span data-stu-id="0ee29-106">Builds an internal CD3DX12\_PIPELINE\_STATE\_STREAM object from subobject details passed into the corresponding member functions.</span></span> <span data-ttu-id="0ee29-107">Эта структура реализует интерфейс [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) .</span><span class="sxs-lookup"><span data-stu-id="0ee29-107">This struct implements the [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee29-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ee29-108">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER  : public ID3DX12PipelineParserCallbacks{
  CD3DX12_PIPELINE_STATE_STREAM1 PipelineStream;
  void                           FlagsCb(D3D12_PIPELINE_STATE_FLAGS Flags);
  void                           NodeMaskCb(UINT NodeMask);
  void                           RootSignatureCb(ID3D12RootSignature* pRootSignature);
  void                           InputLayoutCb(const D3D12_INPUT_LAYOUT_DESC& InputLayout);
  void                           IBStripCutValueCb(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue);
  void                           PrimitiveTopologyTypeCb(D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType);
  void                           VSCb(const D3D12_SHADER_BYTECODE& VS);
  void                           GSCb(const D3D12_SHADER_BYTECODE& GS);
  void                           StreamOutputCb(const D3D12_STREAM_OUTPUT_DESC& StreamOutput);
  void                           HSCb(const D3D12_SHADER_BYTECODE& HS);
  void                           DSCb(const D3D12_SHADER_BYTECODE& DS);
  void                           PSCb(const D3D12_SHADER_BYTECODE& PS);
  void                           CSCb(const D3D12_SHADER_BYTECODE& CS);
  void                           BlendStateCb(const D3D12_BLEND_DESC& BlendState);
  void                           DepthStencilStateCb(const D3D12_DEPTH_STENCIL_DESC& DepthStencilState);
  void                           DepthStencilState1Cb(const D3D12_DEPTH_STENCIL_DESC1& DepthStencilState);
  void                           DSVFormatCb(DXGI_FORMAT DSVFormat);
  void                           RasterizerStateCb(const D3D12_RASTERIZER_DESC& RasterizerState);
  void                           RTVFormatsCb(const D3D12_RT_FORMAT_ARRAY& RTVFormats);
  void                           SampleDescCb(const DXGI_SAMPLE_DESC& SampleDesc);
  void                           SampleMaskCb(UINT SampleMask);
  void                           ViewInstancingCb(const D3D12_VIEW_INSTANCING_DESC& ViewInstancingDesc);
  void                           CachedPSOCb(const D3D12_CACHED_PIPELINE_STATE& CachedPSO);
  void                           ErrorBadInputParameter(UINT);
  void                           ErrorDuplicateSubobject(D3D12_PIPELINE_STATE_SUBOBJECT_TYPE);
  void                           ErrorUnknownSubobject(UINT);
};
```



## <a name="members"></a><span data-ttu-id="0ee29-109">Члены</span><span class="sxs-lookup"><span data-stu-id="0ee29-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ee29-110">**пипелинестреам**</span><span class="sxs-lookup"><span data-stu-id="0ee29-110">**PipelineStream**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-111">Внутреннее [**\_ состояние конвейера \_ CD3DX12 \_ STREAM1**](cd3dx12-pipeline-state-stream1.md).</span><span class="sxs-lookup"><span data-stu-id="0ee29-111">The internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md).</span></span> <span data-ttu-id="0ee29-112">Его текущее состояние представляет собой совокупный результат методов обратного вызова, которые были вызваны для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="0ee29-112">Its current state represents the cumulative effect of callback methods that have been called on this object.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-113">**Флагскб ( \_ \_ \_ Флаги флагов состояния конвейера D3D12)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-113">**FlagsCb(D3D12\_PIPELINE\_STATE\_FLAGS Flags)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-114">Инициализирует член **flags** объекта **пипелинестреам** , используя значение параметра *flags* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-114">Initializes the **Flags** member of **PipelineStream** using the value of the *Flags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-115">**Нодемасккб (UINT Нодемаск)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-115">**NodeMaskCb(UINT NodeMask)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-116">Инициализирует член **нодемаск** объекта **пипелинестреам** , используя значение параметра *нодемаск* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-116">Initializes the **NodeMask** member of **PipelineStream** using the value of the *Nodemask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-117">**Рутсигнатурекб (ID3D12RootSignature \* прутсигнатуре)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-117">**RootSignatureCb(ID3D12RootSignature\* pRootSignature)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-118">Инициализирует член **прутсигнатуре** объекта **пипелинестреам** , используя значение параметра *прутсигнатуре* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-118">Initializes the **pRootSignature** member of **PipelineStream** using the value of the *pRootSignature* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-119">**Инпутлайауткб (const D3D12 \_ входной \_ макет \_ DESC& инпутлайаут)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-119">**InputLayoutCb(const D3D12\_INPUT\_LAYOUT\_DESC& InputLayout)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-120">Инициализирует член **инпутлайаут** объекта **пипелинестреам** , используя значение параметра *инпутлайаут* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-120">Initializes the **InputLayout** member of **PipelineStream** using the value of the *InputLayout* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-121">**Ибстрипкутвалуекб ( \_ БУФЕР D3D12 index, \_ \_ \_ вырезанное \_ значение ибстрипкутвалуе)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-121">**IBStripCutValueCb(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE IBStripCutValue)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-122">Инициализирует член **ибстрипкутвалуе** объекта **пипелинестреам** , используя значение параметра *ибстрипкутвалуе* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-122">Initializes the **IBStripCutValue** member of **PipelineStream** using the value of the *IBStripCutValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-123">**Примитиветопологитипекб (тип D3D12- \_ примитивной \_ топологии \_ примитиветопологитипе)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-123">**PrimitiveTopologyTypeCb(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE PrimitiveTopologyType)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-124">Инициализирует член **примитиветопологитипе** объекта **пипелинестреам** , используя значение параметра *примитиветопологитипе* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-124">Initializes the **PrimitiveTopologyType** member of **PipelineStream** using the value of the *PrimitiveTopologyType* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-125">**Вскб (константа- \_ байт шейдера const D3D12 \_& VS)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-125">**VSCb(const D3D12\_SHADER\_BYTECODE& VS)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-126">Инициализирует элемент **пипелинестреам** в **VS** (Вершинный шейдер), используя значение параметра *VS* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-126">Initializes the **VS** (vertex shader) member of **PipelineStream** using the value of the *VS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-127">**ГСКБ (константный D3D12- \_ байт шейдера const \_& GS)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-127">**GSCb(const D3D12\_SHADER\_BYTECODE& GS)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-128">Инициализирует элемент **пипелинестреам** в **GS** (Geometry Shader), используя значение параметра *GS* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-128">Initializes the **GS** (geometry shader) member of **PipelineStream** using the value of the *GS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-129">**Стреамаутпуткб (const D3D12 \_ Stream \_ вывода \_ DESC& стреамаутпут)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-129">**StreamOutputCb(const D3D12\_STREAM\_OUTPUT\_DESC& StreamOutput)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-130">Инициализирует член **стреамаутпут** объекта **пипелинестреам** , используя значение параметра *стреамаутпут* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-130">Initializes the **StreamOutput** member of **PipelineStream** using the value of the *StreamOutput* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-131">**Хскб (константа- \_ байт шейдера const D3D12 \_& HS)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-131">**HSCb(const D3D12\_SHADER\_BYTECODE& HS)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-132">Инициализирует элемент " **HS** " (шейдер поверхности) объекта **пипелинестреам** , используя значение параметра *HS* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-132">Initializes the **HS** (hull shader) member of **PipelineStream** using the value of the *HS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-133">**Дскб (константа- \_ байт шейдера const D3D12 \_& DS)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-133">**DSCb(const D3D12\_SHADER\_BYTECODE& DS)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-134">Инициализирует член **DS** (доменный шейдер) **пипелинестреам** , используя значение параметра *DS* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-134">Initializes the **DS** (domain shader) member of **PipelineStream** using the value of the *DS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-135">**Пскб (константа- \_ байт шейдера const D3D12 \_& PS)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-135">**PSCb(const D3D12\_SHADER\_BYTECODE& PS)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-136">Инициализирует член **PS** (Pixel Shader) элемента **пипелинестреам** , используя значение параметра *PS* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-136">Initializes the **PS** (pixel shader) member of **PipelineStream** using the value of the *PS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-137">**Кскб (константа- \_ байт шейдера const D3D12 \_& CS)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-137">**CSCb(const D3D12\_SHADER\_BYTECODE& CS)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-138">Инициализирует член **CS** объекта **пипелинестреам** , используя значение параметра *CS* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-138">Initializes the **CS** member of **PipelineStream** using the value of the *CS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-139">**Блендстатекб (const D3D12 \_ Blend \_ DESC& блендстате)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-139">**BlendStateCb(const D3D12\_BLEND\_DESC& BlendState)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-140">Инициализирует член **блендстате** объекта **пипелинестреам** , используя значение параметра *блендстате* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-140">Initializes the **BlendState** member of **PipelineStream** using the value of the *BlendState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-141">**ДепсстенЦилстатекб (const D3D12 \_ трафарет Depth, \_ \_ DESC& депсстенЦилстате)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-141">**DepthStencilStateCb(const D3D12\_DEPTH\_STENCIL\_DESC& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-142">Инициализирует член **депсстенЦилстате** объекта **пипелинестреам** , используя значение параметра *депсстенЦилстате* , а также набор [**\_ элементов глубины D3D12 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span><span class="sxs-lookup"><span data-stu-id="0ee29-142">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-143">**DepthStencilState1Cb (const D3D12 \_ \_ набор элементов глубины \_ DESC1& депсстенЦилстате)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-143">**DepthStencilState1Cb(const D3D12\_DEPTH\_STENCIL\_DESC1& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-144">Инициализирует член **депсстенЦилстате** объекта **пипелинестреам** , используя значение параметра *депсстенЦилстате* , [**D3D12 \_ \_ шаблона глубины \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span><span class="sxs-lookup"><span data-stu-id="0ee29-144">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-145">**Дсвформаткб ( \_ Формат DXGI дсвформат)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-145">**DSVFormatCb(DXGI\_FORMAT DSVFormat)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-146">Инициализирует член **дсвформат** объекта **пипелинестреам** , используя значение параметра *дсвформат* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-146">Initializes the **DSVFormat** member of **PipelineStream** using the value of the *DSVFormat* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-147">**Растеризерстатекб (const D3D12 средство \_ растеризации \_ "DESC"& растеризерстате)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-147">**RasterizerStateCb(const D3D12\_RASTERIZER\_DESC& RasterizerState)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-148">Инициализирует член **растеризерстате** объекта **пипелинестреам** , используя значение параметра *растеризерстате* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-148">Initializes the **RasterizerState** member of **PipelineStream** using the value of the *RasterizerState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-149">**Ртвформатскб (const D3D12 \_ \_ массив формата RT \_& ртвформатс)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-149">**RTVFormatsCb(const D3D12\_RT\_FORMAT\_ARRAY& RTVFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-150">Инициализирует член **ртвформатс** объекта **пипелинестреам** , используя значение параметра *ртвформатс* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-150">Initializes the **RTVFormats** member of **PipelineStream** using the value of the *RTVFormats* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-151">**Сампледесккб (const, \_ образец \_ DESC, пример& сампледеск)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-151">**SampleDescCb(const DXGI\_SAMPLE\_DESC& SampleDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-152">Инициализирует член **сампледеск** объекта **пипелинестреам** , используя значение параметра *сампледеск* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-152">Initializes the **SampleDesc** member of **PipelineStream** using the value of the *SampleDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-153">**Самплемасккб (UINT Самплемаск)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-153">**SampleMaskCb(UINT SampleMask)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-154">Инициализирует член **самплемаск** объекта **пипелинестреам** , используя значение параметра *самплемаск* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-154">Initializes the **SampleMask** member of **PipelineStream** using the value of the *SampleMask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-155">**ВиевинстанЦингкб (const D3D12 \_ представление \_ экземпляров \_ DESC& виевинстанЦингдеск)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-155">**ViewInstancingCb(const D3D12\_VIEW\_INSTANCING\_DESC& ViewInstancingDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-156">Инициализирует член **виевинстанЦингдеск** объекта **пипелинестреам** , используя значение параметра *виевинстанЦингдеск* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-156">Initializes the **ViewInstancingDesc** member of **PipelineStream** using the value of the *ViewInstancingDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-157">**Качедпсокб (const D3D12 \_ кэшированное \_ состояние конвейера \_& качедпсо)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-157">**CachedPSOCb(const D3D12\_CACHED\_PIPELINE\_STATE& CachedPSO)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-158">Инициализирует член **качедпсо** объекта **пипелинестреам** , используя значение параметра *качедпсо* .</span><span class="sxs-lookup"><span data-stu-id="0ee29-158">Initializes the **CachedPSO** member of **PipelineStream** using the value of the *CachedPSO* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-159">**Еррорбадинпутпараметер (UINT)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-159">**ErrorBadInputParameter(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-160">Не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="0ee29-160">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-161">**Еррордупликатесубобжект ( \_ \_ \_ тип подобъекта состояния конвейера D3D12 \_ )**</span><span class="sxs-lookup"><span data-stu-id="0ee29-161">**ErrorDuplicateSubobject(D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-162">Не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="0ee29-162">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="0ee29-163">**Еррорункновнсубобжект (UINT)**</span><span class="sxs-lookup"><span data-stu-id="0ee29-163">**ErrorUnknownSubobject(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="0ee29-164">Не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="0ee29-164">Does nothing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ee29-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ee29-165">Remarks</span></span>

<span data-ttu-id="0ee29-166">Если передается в качестве второго параметра функции [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) , сведения о внутреннем объекте [**\_ состояния конвейера CD3DX12 \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md) копируются из [**\_ \_ потока состояния конвейера \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) , переданного в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="0ee29-166">When passed as the second parameter to the [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) function, the details of the internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md) object are cloned from the [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passed as the first parameter.</span></span> <span data-ttu-id="0ee29-167">Этот процесс проверяет описание исходного потока.</span><span class="sxs-lookup"><span data-stu-id="0ee29-167">This process validates the source stream description.</span></span> <span data-ttu-id="0ee29-168">Если D3DX12ParsePipelineStream возвращает значение " **\_ ОК**", то как описание исходного потока, так и полученное **CD3DX12 \_ состояние конвейера \_ \_ STREAM1PipelineStream** являются допустимыми; в противном случае оба значения являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="0ee29-168">If D3DX12ParsePipelineStream returns **S\_OK**, then both the source stream description and the resulting **CD3DX12\_PIPELINE\_STATE\_STREAM1PipelineStream** are valid; otherwise both are invalid.</span></span> <span data-ttu-id="0ee29-169">Недопустимые потоки и другие ошибки выводятся только через возвращаемое значение D3DX12ParsePipelineStream; Эта структура реализует обратные вызовы ошибок, чтобы ничего не делать.</span><span class="sxs-lookup"><span data-stu-id="0ee29-169">Invalid streams and other errors are reported only through the return value of D3DX12ParsePipelineStream; this structure implements the error callbacks to do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee29-170">Требования</span><span class="sxs-lookup"><span data-stu-id="0ee29-170">Requirements</span></span>



| <span data-ttu-id="0ee29-171">Требование</span><span class="sxs-lookup"><span data-stu-id="0ee29-171">Requirement</span></span> | <span data-ttu-id="0ee29-172">Значение</span><span class="sxs-lookup"><span data-stu-id="0ee29-172">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee29-173">Header</span><span class="sxs-lookup"><span data-stu-id="0ee29-173">Header</span></span><br/> | <dl> <span data-ttu-id="0ee29-174"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ee29-174"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee29-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ee29-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee29-176">Вспомогательные структуры для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0ee29-176">Helper Structures for Direct3D 12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="0ee29-177">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="0ee29-177">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





