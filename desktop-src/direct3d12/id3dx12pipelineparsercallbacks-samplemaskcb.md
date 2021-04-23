---
title: Метод ID3DX12PipelineParserCallbacks Самплемасккб (D3DX12. h)
description: Вызывает обратный вызов подобъекта образца маски для объекта, реализующего этот интерфейс.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- Метод Самплемасккб
- Метод Самплемасккб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Самплемасккб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713483"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a><span data-ttu-id="3cda1-106">Метод ID3DX12PipelineParserCallbacks:: Самплемасккб</span><span class="sxs-lookup"><span data-stu-id="3cda1-106">ID3DX12PipelineParserCallbacks::SampleMaskCb method</span></span>

<span data-ttu-id="3cda1-107">Вызывает обратный вызов подобъекта образца маски для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="3cda1-107">Calls the sample mask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cda1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cda1-108">Syntax</span></span>


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a><span data-ttu-id="3cda1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cda1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cda1-110">*самплемаск*</span><span class="sxs-lookup"><span data-stu-id="3cda1-110">*SampleMask*</span></span> 
</dt> <dd>

<span data-ttu-id="3cda1-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3cda1-111">Type: **UINT**</span></span>

<span data-ttu-id="3cda1-112">Подробные сведения о примере подобъекта маски, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="3cda1-112">Details of the sample mask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cda1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cda1-113">Return value</span></span>

<span data-ttu-id="3cda1-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="3cda1-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cda1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3cda1-115">Requirements</span></span>



| <span data-ttu-id="3cda1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3cda1-116">Requirement</span></span> | <span data-ttu-id="3cda1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3cda1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3cda1-118">Header</span><span class="sxs-lookup"><span data-stu-id="3cda1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3cda1-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cda1-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="3cda1-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3cda1-120">Library</span></span><br/> | <dl> <span data-ttu-id="3cda1-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cda1-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="3cda1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3cda1-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="3cda1-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cda1-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cda1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cda1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cda1-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3cda1-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="3cda1-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="3cda1-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





