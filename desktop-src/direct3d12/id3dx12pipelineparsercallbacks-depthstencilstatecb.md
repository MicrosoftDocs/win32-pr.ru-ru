---
title: Метод ID3DX12PipelineParserCallbacks ДепсстенЦилстатекб (D3DX12. h)
description: Вызывает обратный вызов подобъекта состояния шаблона глубины объекта, реализующего этот интерфейс.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
keywords:
- Метод ДепсстенЦилстатекб
- Метод ДепсстенЦилстатекб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод ДепсстенЦилстатекб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 913dbddef0c509174d3600798a6e1380d6098808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694088"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a><span data-ttu-id="ba814-106">Метод ID3DX12PipelineParserCallbacks ДепсстенЦилстатекб (D3DX12. h)</span><span class="sxs-lookup"><span data-stu-id="ba814-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h)</span></span>

<span data-ttu-id="ba814-107">Вызывает обратный вызов подобъекта состояния шаблона глубины объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ba814-107">Calls the depth stencil state subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba814-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba814-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="ba814-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba814-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba814-110">*ДепсстенЦилстате* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="ba814-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ba814-111">Тип: **const [**D3D12 \_ \_ набор элементов \_ глубины**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span><span class="sxs-lookup"><span data-stu-id="ba814-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span></span>

<span data-ttu-id="ba814-112">Сведения о подобъекте состояния шаблона глубины, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="ba814-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba814-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba814-113">Return value</span></span>

<span data-ttu-id="ba814-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="ba814-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba814-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ba814-115">Requirements</span></span>



| <span data-ttu-id="ba814-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ba814-116">Requirement</span></span> | <span data-ttu-id="ba814-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ba814-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ba814-118">Header</span><span class="sxs-lookup"><span data-stu-id="ba814-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ba814-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba814-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="ba814-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ba814-120">Library</span></span><br/> | <dl> <span data-ttu-id="ba814-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba814-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="ba814-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ba814-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="ba814-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba814-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba814-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba814-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba814-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ba814-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="ba814-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="ba814-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="ba814-127">**D3D12 \_ \_ трафарета \_ глубины**</span><span class="sxs-lookup"><span data-stu-id="ba814-127">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





