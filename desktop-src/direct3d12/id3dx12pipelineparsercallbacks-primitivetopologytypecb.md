---
title: Метод ID3DX12PipelineParserCallbacks Примитиветопологитипекб (D3DX12. h)
description: Вызывает обратный вызов подобъекта типа топологии примитива объекта, реализующего этот интерфейс.
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- Метод Примитиветопологитипекб
- Метод Примитиветопологитипекб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Примитиветопологитипекб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01a2d73edd6ac94719905757d75a756c905c832
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713816"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a><span data-ttu-id="e00bd-106">ID3DX12PipelineParserCallbacks: метод:P Римитиветопологитипекб</span><span class="sxs-lookup"><span data-stu-id="e00bd-106">ID3DX12PipelineParserCallbacks::PrimitiveTopologyTypeCb method</span></span>

<span data-ttu-id="e00bd-107">Вызывает обратный вызов подобъекта типа топологии примитива объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="e00bd-107">Calls the primitive topology type subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e00bd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e00bd-108">Syntax</span></span>


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a><span data-ttu-id="e00bd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e00bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e00bd-110">*примитиветопологитипе*</span><span class="sxs-lookup"><span data-stu-id="e00bd-110">*PrimitiveTopologyType*</span></span> 
</dt> <dd>

<span data-ttu-id="e00bd-111">Тип: **[ **D3D12- \_ примитивный \_ \_ тип топологии**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span><span class="sxs-lookup"><span data-stu-id="e00bd-111">Type: **[**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span></span>

<span data-ttu-id="e00bd-112">Сведения о подобъекте типа примитивной топологии, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="e00bd-112">Details of the primitive topology type subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e00bd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e00bd-113">Return value</span></span>

<span data-ttu-id="e00bd-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="e00bd-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00bd-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e00bd-115">Requirements</span></span>



| <span data-ttu-id="e00bd-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e00bd-116">Requirement</span></span> | <span data-ttu-id="e00bd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e00bd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e00bd-118">Header</span><span class="sxs-lookup"><span data-stu-id="e00bd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e00bd-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e00bd-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="e00bd-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e00bd-120">Library</span></span><br/> | <dl> <span data-ttu-id="e00bd-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e00bd-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="e00bd-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e00bd-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e00bd-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e00bd-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e00bd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e00bd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00bd-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e00bd-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e00bd-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="e00bd-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="e00bd-127">**Тип D3D12- \_ примитивной \_ топологии \_**</span><span class="sxs-lookup"><span data-stu-id="e00bd-127">**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





