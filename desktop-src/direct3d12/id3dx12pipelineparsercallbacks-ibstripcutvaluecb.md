---
title: Метод ID3DX12PipelineParserCallbacks Ибстрипкутвалуекб (D3DX12. h)
description: Вызывает обратный вызов подобъекта полосы буферного индекса для объекта, реализующего этот интерфейс.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- Метод Ибстрипкутвалуекб
- Метод Ибстрипкутвалуекб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Ибстрипкутвалуекб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713820"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a><span data-ttu-id="6d722-106">Метод ID3DX12PipelineParserCallbacks:: Ибстрипкутвалуекб</span><span class="sxs-lookup"><span data-stu-id="6d722-106">ID3DX12PipelineParserCallbacks::IBStripCutValueCb method</span></span>

<span data-ttu-id="6d722-107">Вызывает обратный вызов подобъекта полосы буферного индекса для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6d722-107">Calls the index buffer strip-cut value subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d722-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d722-108">Syntax</span></span>


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a><span data-ttu-id="6d722-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d722-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d722-110">*ибстрипкутвалуе*</span><span class="sxs-lookup"><span data-stu-id="6d722-110">*IBStripCutValue*</span></span> 
</dt> <dd>

<span data-ttu-id="6d722-111">Тип: **[ **D3D12 \_ \_ \_ \_ \_ значение вырезанной полосы буфера индекса**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span><span class="sxs-lookup"><span data-stu-id="6d722-111">Type: **[**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span></span>

<span data-ttu-id="6d722-112">Сведения о полосе буферов индексов — вырезанное значение подобъект, проанализированный из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="6d722-112">Details of the index buffer strip-cut value subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d722-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d722-113">Return value</span></span>

<span data-ttu-id="6d722-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="6d722-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d722-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6d722-115">Requirements</span></span>



| <span data-ttu-id="6d722-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6d722-116">Requirement</span></span> | <span data-ttu-id="6d722-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6d722-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6d722-118">Header</span><span class="sxs-lookup"><span data-stu-id="6d722-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6d722-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d722-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="6d722-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d722-120">Library</span></span><br/> | <dl> <span data-ttu-id="6d722-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d722-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d722-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6d722-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6d722-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d722-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d722-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d722-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d722-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="6d722-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6d722-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="6d722-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="6d722-127">**\_Отрезать \_ \_ \_ \_ значение для буфера D3D12 индекса**</span><span class="sxs-lookup"><span data-stu-id="6d722-127">**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





