---
title: Метод ID3DX12PipelineParserCallbacks Еррордупликатесубобжект (D3DX12. h)
description: Вызывает обратный вызов ошибки повторяющегося объекта для объекта, реализующего этот интерфейс.
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- Метод Еррордупликатесубобжект
- Метод Еррордупликатесубобжект, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Еррордупликатесубобжект
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b00dae4675ff05a43e566a8ead815ea24f6c16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713829"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a><span data-ttu-id="8d68b-106">Метод ID3DX12PipelineParserCallbacks:: Еррордупликатесубобжект</span><span class="sxs-lookup"><span data-stu-id="8d68b-106">ID3DX12PipelineParserCallbacks::ErrorDuplicateSubobject method</span></span>

<span data-ttu-id="8d68b-107">Вызывает обратный вызов ошибки повторяющегося объекта для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8d68b-107">Calls the duplicate subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d68b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d68b-108">Syntax</span></span>


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a><span data-ttu-id="8d68b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d68b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d68b-110">*дупликатетипе*</span><span class="sxs-lookup"><span data-stu-id="8d68b-110">*DuplicateType*</span></span> 
</dt> <dd>

<span data-ttu-id="8d68b-111">Тип: **[ **\_ \_ \_ \_ тип подобъекта состояния конвейера D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span><span class="sxs-lookup"><span data-stu-id="8d68b-111">Type: **[**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span></span>

<span data-ttu-id="8d68b-112">Тип подобъекта, который был дублирован.</span><span class="sxs-lookup"><span data-stu-id="8d68b-112">The subobject type that was duplicated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d68b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d68b-113">Return value</span></span>

<span data-ttu-id="8d68b-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="8d68b-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d68b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8d68b-115">Requirements</span></span>



| <span data-ttu-id="8d68b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8d68b-116">Requirement</span></span> | <span data-ttu-id="8d68b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8d68b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8d68b-118">Header</span><span class="sxs-lookup"><span data-stu-id="8d68b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8d68b-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d68b-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8d68b-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8d68b-120">Library</span></span><br/> | <dl> <span data-ttu-id="8d68b-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d68b-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d68b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8d68b-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="8d68b-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d68b-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d68b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d68b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d68b-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8d68b-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8d68b-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="8d68b-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="8d68b-127">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="8d68b-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

