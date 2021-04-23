---
title: Метод ID3DX12PipelineParserCallbacks Качедпсокб (D3DX12. h)
description: Вызывает обратный вызов подобъекта кэшированного PSO (объект состояния конвейера) объекта, реализующего этот интерфейс.
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- Метод Качедпсокб
- Метод Качедпсокб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Качедпсокб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703886"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a><span data-ttu-id="cd942-106">Метод ID3DX12PipelineParserCallbacks:: Качедпсокб</span><span class="sxs-lookup"><span data-stu-id="cd942-106">ID3DX12PipelineParserCallbacks::CachedPSOCb method</span></span>

<span data-ttu-id="cd942-107">Вызывает обратный вызов подобъекта кэшированного PSO (объект состояния конвейера) объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="cd942-107">Calls the cached PSO (Pipeline State Object) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd942-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd942-108">Syntax</span></span>


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a><span data-ttu-id="cd942-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd942-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd942-110">*Качедпсо* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="cd942-110">*CachedPSO* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cd942-111">Тип: **const [**D3D12 \_ кэшированное \_ \_ состояние конвейера**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span><span class="sxs-lookup"><span data-stu-id="cd942-111">Type: **const [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span></span>

<span data-ttu-id="cd942-112">Сведения о кэшированном подобъекте PSO (объект состояния конвейера), проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="cd942-112">Details of the cached PSO (Pipeline State Object) subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd942-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd942-113">Return value</span></span>

<span data-ttu-id="cd942-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="cd942-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd942-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cd942-115">Requirements</span></span>



| <span data-ttu-id="cd942-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cd942-116">Requirement</span></span> | <span data-ttu-id="cd942-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cd942-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd942-118">Header</span><span class="sxs-lookup"><span data-stu-id="cd942-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cd942-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd942-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="cd942-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cd942-120">Library</span></span><br/> | <dl> <span data-ttu-id="cd942-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd942-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="cd942-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cd942-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="cd942-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd942-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd942-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd942-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd942-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="cd942-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="cd942-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="cd942-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="cd942-127">**\_Состояние кэшированного \_ КОНВЕЙЕРа D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="cd942-127">**D3D12\_CACHED\_PIPELINE\_STATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





