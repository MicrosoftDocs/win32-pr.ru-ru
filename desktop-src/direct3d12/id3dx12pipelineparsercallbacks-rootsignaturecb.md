---
title: Метод ID3DX12PipelineParserCallbacks Рутсигнатурекб (D3DX12. h)
description: Вызывает обратный вызов подобъекта корневой подписи объекта, реализующего этот интерфейс.
ms.assetid: FD467001-41B1-4A73-8E54-12C6B5EEAC3E
keywords:
- Метод Рутсигнатурекб
- Метод Рутсигнатурекб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Рутсигнатурекб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RootSignatureCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78160ff1e61432a0711876934215ff15afb918de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713487"
---
# <a name="id3dx12pipelineparsercallbacksrootsignaturecb-method"></a><span data-ttu-id="1382c-106">Метод ID3DX12PipelineParserCallbacks:: Рутсигнатурекб</span><span class="sxs-lookup"><span data-stu-id="1382c-106">ID3DX12PipelineParserCallbacks::RootSignatureCb method</span></span>

<span data-ttu-id="1382c-107">Вызывает обратный вызов подобъекта корневой подписи объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="1382c-107">Calls the root signature subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1382c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1382c-108">Syntax</span></span>


```C++
void RootSignatureCb(
   ID3D12RootSignature *RootSignature
);
```



## <a name="parameters"></a><span data-ttu-id="1382c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1382c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1382c-110">*рутсигнатуре*</span><span class="sxs-lookup"><span data-stu-id="1382c-110">*RootSignature*</span></span> 
</dt> <dd>

<span data-ttu-id="1382c-111">Тип: **[ **ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span><span class="sxs-lookup"><span data-stu-id="1382c-111">Type: **[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span></span>

<span data-ttu-id="1382c-112">Сведения о подобъекте корневой подписи, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="1382c-112">Details of the root signature subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1382c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1382c-113">Return value</span></span>

<span data-ttu-id="1382c-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="1382c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="1382c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1382c-115">Requirements</span></span>



| <span data-ttu-id="1382c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1382c-116">Requirement</span></span> | <span data-ttu-id="1382c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1382c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1382c-118">Header</span><span class="sxs-lookup"><span data-stu-id="1382c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1382c-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1382c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="1382c-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1382c-120">Library</span></span><br/> | <dl> <span data-ttu-id="1382c-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1382c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="1382c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1382c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="1382c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1382c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1382c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1382c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1382c-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1382c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="1382c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="1382c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="1382c-127">**ID3D12RootSignature**</span><span class="sxs-lookup"><span data-stu-id="1382c-127">**ID3D12RootSignature**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> </dl>

 

