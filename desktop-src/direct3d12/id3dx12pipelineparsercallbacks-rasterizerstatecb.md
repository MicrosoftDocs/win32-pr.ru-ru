---
title: Метод ID3DX12PipelineParserCallbacks Растеризерстатекб (D3DX12. h)
description: Вызывает обратный вызов подобъекта описания состояния средства программной прорисовки для объекта, реализующего этот интерфейс.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- Метод Растеризерстатекб
- Метод Растеризерстатекб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Растеризерстатекб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a970e8061ed9199ba5a6a334c7b670218e93936
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713815"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a><span data-ttu-id="62e47-106">Метод ID3DX12PipelineParserCallbacks:: Растеризерстатекб</span><span class="sxs-lookup"><span data-stu-id="62e47-106">ID3DX12PipelineParserCallbacks::RasterizerStateCb method</span></span>

<span data-ttu-id="62e47-107">Вызывает обратный вызов подобъекта описания состояния средства программной прорисовки для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="62e47-107">Calls the rasterizer state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="62e47-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62e47-108">Syntax</span></span>


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="62e47-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="62e47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62e47-110">*Растеризерстате* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="62e47-110">*RasterizerState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="62e47-111">Тип: **const [**D3D12 средство \_ развертки \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span><span class="sxs-lookup"><span data-stu-id="62e47-111">Type: **const [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span></span>

<span data-ttu-id="62e47-112">Сведения о подобъекте описания состояния средства программной прорисовки, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="62e47-112">Details of the rasterizer state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62e47-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62e47-113">Return value</span></span>

<span data-ttu-id="62e47-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="62e47-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="62e47-115">Требования</span><span class="sxs-lookup"><span data-stu-id="62e47-115">Requirements</span></span>



| <span data-ttu-id="62e47-116">Требование</span><span class="sxs-lookup"><span data-stu-id="62e47-116">Requirement</span></span> | <span data-ttu-id="62e47-117">Значение</span><span class="sxs-lookup"><span data-stu-id="62e47-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="62e47-118">Header</span><span class="sxs-lookup"><span data-stu-id="62e47-118">Header</span></span><br/>  | <dl> <span data-ttu-id="62e47-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="62e47-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="62e47-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="62e47-120">Library</span></span><br/> | <dl> <span data-ttu-id="62e47-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62e47-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="62e47-122">DLL</span><span class="sxs-lookup"><span data-stu-id="62e47-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="62e47-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62e47-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62e47-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62e47-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e47-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="62e47-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="62e47-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="62e47-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="62e47-127">**D3D12 средство программной \_ прорисовки \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="62e47-127">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





