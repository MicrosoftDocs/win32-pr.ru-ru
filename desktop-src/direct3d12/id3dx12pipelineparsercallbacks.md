---
title: Интерфейс ID3DX12PipelineParserCallbacks (D3DX12. h)
description: Интерфейс, представляющий коллекцию обратных вызовов парсера и ошибок, используемых вспомогательной функцией D3DX12parsePipelineStream.
ms.assetid: CBC04D17-2E19-4755-B1CB-FC42BF5083E5
keywords:
- Интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, описание
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0061746da589c30e4745dfa3e4dc573f7b5d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703882"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a><span data-ttu-id="81846-105">Интерфейс ID3DX12PipelineParserCallbacks</span><span class="sxs-lookup"><span data-stu-id="81846-105">ID3DX12PipelineParserCallbacks interface</span></span>

<span data-ttu-id="81846-106">Интерфейс, представляющий коллекцию обратных вызовов парсера и ошибок, используемых вспомогательной функцией [**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md) .</span><span class="sxs-lookup"><span data-stu-id="81846-106">An interface that represents a collection of parser and error callbacks used by the [**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md) helper function.</span></span>

-   [<span data-ttu-id="81846-107">Методы</span><span class="sxs-lookup"><span data-stu-id="81846-107">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="81846-108">Методы</span><span class="sxs-lookup"><span data-stu-id="81846-108">Methods</span></span>

<span data-ttu-id="81846-109">Интерфейс **ID3DX12PipelineParserCallbacks** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="81846-109">The **ID3DX12PipelineParserCallbacks** interface has these methods.</span></span>



| <span data-ttu-id="81846-110">Метод</span><span class="sxs-lookup"><span data-stu-id="81846-110">Method</span></span>                                                                                    | <span data-ttu-id="81846-111">Описание</span><span class="sxs-lookup"><span data-stu-id="81846-111">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81846-112">**BlendStateCb**</span><span class="sxs-lookup"><span data-stu-id="81846-112">**BlendStateCb**</span></span>](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | <span data-ttu-id="81846-113">Вызывает обратный вызов подобъекта описания состояния смешения для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-113">Calls the blend state description subobject callback of an object that implements this interface.</span></span><br/>                                                                 |
| [<span data-ttu-id="81846-114">**CachedPSOCb**</span><span class="sxs-lookup"><span data-stu-id="81846-114">**CachedPSOCb**</span></span>](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | <span data-ttu-id="81846-115">Вызывает обратный вызов подобъекта кэшированного PSO (объект состояния конвейера) объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-115">Calls the cached PSO (Pipeline State Object) subobject callback of an object that implements this interface.</span></span><br/>                                                      |
| [<span data-ttu-id="81846-116">**CSCb**</span><span class="sxs-lookup"><span data-stu-id="81846-116">**CSCb**</span></span>](id3dx12pipelineparsercallbacks-cscb.md)                                       | <span data-ttu-id="81846-117">Вызывает обратный вызов подобъекта COMPUTE Shader для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-117">Calls the compute shader subobject callback of an object that implements this interface.</span></span><br/>                                                                          |
| [<span data-ttu-id="81846-118">**DepthStencilState1Cb**</span><span class="sxs-lookup"><span data-stu-id="81846-118">**DepthStencilState1Cb**</span></span>](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | <span data-ttu-id="81846-119">Вызывает обратный вызов подобъекта состояния трафарета глубины ([**D3D12 \_ \_ трафарета \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-119">Calls the depth stencil state ([**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) subobject callback of an object that implements this interface.</span></span><br/> |
| [<span data-ttu-id="81846-120">**DepthStencilStateCb**</span><span class="sxs-lookup"><span data-stu-id="81846-120">**DepthStencilStateCb**</span></span>](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | <span data-ttu-id="81846-121">Вызывает обратный вызов подобъекта формата значения шаблона глубины объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-121">Calls the depth stencil value format subobject callback of an object that implements this interface.</span></span><br/>                                                              |
| [<span data-ttu-id="81846-122">**DepthStencilStateCb**</span><span class="sxs-lookup"><span data-stu-id="81846-122">**DepthStencilStateCb**</span></span>](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | <span data-ttu-id="81846-123">Вызывает обратный вызов подобъекта состояния шаблона глубины объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-123">Calls the depth stencil state subobject callback of an object that implements this interface.</span></span><br/>                                                                     |
| [<span data-ttu-id="81846-124">**DSCb**</span><span class="sxs-lookup"><span data-stu-id="81846-124">**DSCb**</span></span>](id3dx12pipelineparsercallbacks-dscb.md)                                       | <span data-ttu-id="81846-125">Вызывает обратный вызов подобъекта шейдера домена для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-125">Calls the domain shader subobject callback of an object that implements this interface.</span></span><br/>                                                                           |
| [<span data-ttu-id="81846-126">**ErrorBadInputParameter**</span><span class="sxs-lookup"><span data-stu-id="81846-126">**ErrorBadInputParameter**</span></span>](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | <span data-ttu-id="81846-127">Вызывает недопустимый обратный вызов ошибки входного параметра объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-127">Calls the bad input parameter error callback of an object that implements this interface.</span></span><br/>                                                                         |
| [<span data-ttu-id="81846-128">**ErrorDuplicateSubobject**</span><span class="sxs-lookup"><span data-stu-id="81846-128">**ErrorDuplicateSubobject**</span></span>](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | <span data-ttu-id="81846-129">Вызывает обратный вызов ошибки повторяющегося объекта для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-129">Calls the duplicate subobject error callback of an object that implements this interface.</span></span><br/>                                                                         |
| [<span data-ttu-id="81846-130">**ErrorUnknownSubobject**</span><span class="sxs-lookup"><span data-stu-id="81846-130">**ErrorUnknownSubobject**</span></span>](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | <span data-ttu-id="81846-131">Вызывает обратный вызов ошибки неизвестного подобъекта для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-131">Calls the unknown subobject error callback of an object that implements this interface.</span></span><br/>                                                                           |
| [<span data-ttu-id="81846-132">**FlagsCb**</span><span class="sxs-lookup"><span data-stu-id="81846-132">**FlagsCb**</span></span>](id3dx12pipelineparsercallbacks-flagscb.md)                                 | <span data-ttu-id="81846-133">Вызывает обратный вызов подобъекта flags объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-133">Calls the flags subobject callback of an object that implements this interface.</span></span><br/>                                                                                   |
| [<span data-ttu-id="81846-134">**GSCb**</span><span class="sxs-lookup"><span data-stu-id="81846-134">**GSCb**</span></span>](id3dx12pipelineparsercallbacks-gscb.md)                                       | <span data-ttu-id="81846-135">Вызывает обратный вызов подобъекта шейдера Geometry для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-135">Calls the geometry shader subobject callback of an object that implements this interface.</span></span><br/>                                                                         |
| [<span data-ttu-id="81846-136">**HSCb**</span><span class="sxs-lookup"><span data-stu-id="81846-136">**HSCb**</span></span>](id3dx12pipelineparsercallbacks-hscb.md)                                       | <span data-ttu-id="81846-137">Вызывает обратный вызов подобъекта шейдера поверхности объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-137">Calls the hull shader subobject callback of an object that implements this interface.</span></span><br/>                                                                             |
| [<span data-ttu-id="81846-138">**IBStripCutValueCb**</span><span class="sxs-lookup"><span data-stu-id="81846-138">**IBStripCutValueCb**</span></span>](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | <span data-ttu-id="81846-139">Вызывает обратный вызов подобъекта полосы буферного индекса для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-139">Calls the index buffer strip-cut value subobject callback of an object that implements this interface.</span></span><br/>                                                            |
| [<span data-ttu-id="81846-140">**InputLayoutCb**</span><span class="sxs-lookup"><span data-stu-id="81846-140">**InputLayoutCb**</span></span>](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | <span data-ttu-id="81846-141">Вызывает обратный вызов подобъекта входной структуры для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-141">Calls the input layout subobject callback of an object that implements this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="81846-142">**нодемасккб**</span><span class="sxs-lookup"><span data-stu-id="81846-142">**NodemaskCb**</span></span>](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | <span data-ttu-id="81846-143">Вызывает обратный вызов подобъекта нодемаск объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-143">Calls the nodemask subobject callback of an object that implements this interface.</span></span><br/>                                                                                |
| [<span data-ttu-id="81846-144">**PrimitiveTopologyTypeCb**</span><span class="sxs-lookup"><span data-stu-id="81846-144">**PrimitiveTopologyTypeCb**</span></span>](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | <span data-ttu-id="81846-145">Вызывает обратный вызов подобъекта типа топологии примитива объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-145">Calls the primitive topology type subobject callback of an object that implements this interface.</span></span><br/>                                                                 |
| [<span data-ttu-id="81846-146">**PSCb**</span><span class="sxs-lookup"><span data-stu-id="81846-146">**PSCb**</span></span>](id3dx12pipelineparsercallbacks-pscb.md)                                       | <span data-ttu-id="81846-147">Вызывает обратный вызов подобъекта пиксельного шейдера для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-147">Calls the pixel shader subobject callback of an object that implements this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="81846-148">**RasterizerStateCb**</span><span class="sxs-lookup"><span data-stu-id="81846-148">**RasterizerStateCb**</span></span>](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | <span data-ttu-id="81846-149">Вызывает обратный вызов подобъекта описания состояния средства программной прорисовки для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-149">Calls the rasterizer state description subobject callback of an object that implements this interface.</span></span><br/>                                                            |
| [<span data-ttu-id="81846-150">**рутсигнатурекб**</span><span class="sxs-lookup"><span data-stu-id="81846-150">**RootSignatureCB**</span></span>](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | <span data-ttu-id="81846-151">Вызывает обратный вызов подобъекта корневой подписи объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-151">Calls the root signature subobject callback of an object that implements this interface.</span></span><br/>                                                                          |
| [<span data-ttu-id="81846-152">**RTVFormatsCb**</span><span class="sxs-lookup"><span data-stu-id="81846-152">**RTVFormatsCb**</span></span>](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | <span data-ttu-id="81846-153">Вызывает обратный вызов подобъекта массива формата целевого объекта прорисовки объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-153">Calls the render target format array subobject callback of an object that implements this interface.</span></span><br/>                                                              |
| [<span data-ttu-id="81846-154">**SampleDescCb**</span><span class="sxs-lookup"><span data-stu-id="81846-154">**SampleDescCb**</span></span>](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | <span data-ttu-id="81846-155">Вызывает обратный вызов подобъекта описания образца для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-155">Calls the sample description subobject callback of an object that implements this interface.</span></span><br/>                                                                      |
| [<span data-ttu-id="81846-156">**SampleMaskCb**</span><span class="sxs-lookup"><span data-stu-id="81846-156">**SampleMaskCb**</span></span>](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | <span data-ttu-id="81846-157">Вызывает обратный вызов подобъекта образца маски для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-157">Calls the sample mask subobject callback of an object that implements this interface.</span></span><br/>                                                                             |
| [<span data-ttu-id="81846-158">**StreamOutputCb**</span><span class="sxs-lookup"><span data-stu-id="81846-158">**StreamOutputCb**</span></span>](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | <span data-ttu-id="81846-159">Вызывает обратный вызов подобъекта описания потока вывода объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-159">Calls the stream output description subobject callback of an object that implements this interface.</span></span><br/>                                                               |
| [<span data-ttu-id="81846-160">**VSCb**</span><span class="sxs-lookup"><span data-stu-id="81846-160">**VSCb**</span></span>](id3dx12pipelineparsercallbacks-vscb.md)                                       | <span data-ttu-id="81846-161">Вызывает обратный вызов подобъекта вершинного шейдера объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81846-161">Calls the vertex shader subobject callback of an object that implements this interface.</span></span><br/>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="81846-162">Требования</span><span class="sxs-lookup"><span data-stu-id="81846-162">Requirements</span></span>



| <span data-ttu-id="81846-163">Требование</span><span class="sxs-lookup"><span data-stu-id="81846-163">Requirement</span></span> | <span data-ttu-id="81846-164">Значение</span><span class="sxs-lookup"><span data-stu-id="81846-164">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81846-165">Header</span><span class="sxs-lookup"><span data-stu-id="81846-165">Header</span></span><br/>  | <dl> <span data-ttu-id="81846-166"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="81846-166"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="81846-167">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81846-167">Library</span></span><br/> | <dl> <span data-ttu-id="81846-168"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81846-168"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="81846-169">DLL</span><span class="sxs-lookup"><span data-stu-id="81846-169">DLL</span></span><br/>     | <dl> <span data-ttu-id="81846-170"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81846-170"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81846-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81846-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81846-172">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="81846-172">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="81846-173">**D3DX12parsePipelineStream**</span><span class="sxs-lookup"><span data-stu-id="81846-173">**D3DX12parsePipelineStream**</span></span>](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 





