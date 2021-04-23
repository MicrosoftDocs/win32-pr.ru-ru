---
title: Метод ID3DX12PipelineParserCallbacks Флагскб (D3DX12. h)
description: Вызывает обратный вызов подобъекта flags объекта, реализующего этот интерфейс.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Метод Флагскб
- Метод Флагскб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Флагскб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30ac5a0ca3a749144e263a1d993166b8e13ddac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713825"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a><span data-ttu-id="d3574-106">Метод ID3DX12PipelineParserCallbacks:: Флагскб</span><span class="sxs-lookup"><span data-stu-id="d3574-106">ID3DX12PipelineParserCallbacks::FlagsCb method</span></span>

<span data-ttu-id="d3574-107">Вызывает обратный вызов подобъекта flags объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d3574-107">Calls the flags subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3574-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3574-108">Syntax</span></span>


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="d3574-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3574-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3574-110">*Флаги*</span><span class="sxs-lookup"><span data-stu-id="d3574-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="d3574-111">Тип: **[ **D3D12 \_ . \_ \_ флаги состояния конвейера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span><span class="sxs-lookup"><span data-stu-id="d3574-111">Type: **[**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span></span>

<span data-ttu-id="d3574-112">Сведения о подобъекте flags, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3574-112">Details of the flags subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3574-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3574-113">Return value</span></span>

<span data-ttu-id="d3574-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="d3574-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3574-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d3574-115">Requirements</span></span>



| <span data-ttu-id="d3574-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d3574-116">Requirement</span></span> | <span data-ttu-id="d3574-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d3574-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d3574-118">Header</span><span class="sxs-lookup"><span data-stu-id="d3574-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d3574-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3574-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d3574-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d3574-120">Library</span></span><br/> | <dl> <span data-ttu-id="d3574-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3574-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d3574-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d3574-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d3574-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3574-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3574-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3574-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3574-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d3574-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d3574-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="d3574-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="d3574-127">**\_ \_ Флаги состояния КОНВЕЙЕРа D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="d3574-127">**D3D12\_PIPELINE\_STATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





