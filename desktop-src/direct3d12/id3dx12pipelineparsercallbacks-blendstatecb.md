---
title: Метод ID3DX12PipelineParserCallbacks Блендстатекб (D3DX12. h)
description: Вызывает обратный вызов подобъекта описания состояния смешения для объекта, реализующего этот интерфейс.
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- Метод Блендстатекб
- Метод Блендстатекб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Блендстатекб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 119733fbe82203a6e423fb0ef9b07d3ecff70619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703887"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a><span data-ttu-id="624aa-106">Метод ID3DX12PipelineParserCallbacks:: Блендстатекб</span><span class="sxs-lookup"><span data-stu-id="624aa-106">ID3DX12PipelineParserCallbacks::BlendStateCb method</span></span>

<span data-ttu-id="624aa-107">Вызывает обратный вызов подобъекта описания состояния смешения для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="624aa-107">Calls the blend state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="624aa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="624aa-108">Syntax</span></span>


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a><span data-ttu-id="624aa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="624aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="624aa-110">*Блендстате* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="624aa-110">*BlendState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="624aa-111">Тип: **const [**D3D12 \_ Blend \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span><span class="sxs-lookup"><span data-stu-id="624aa-111">Type: **const [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span></span>

<span data-ttu-id="624aa-112">Сведения о подобъекте описания состояния смешения, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="624aa-112">Details of the blend state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="624aa-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="624aa-113">Return value</span></span>

<span data-ttu-id="624aa-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="624aa-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="624aa-115">Требования</span><span class="sxs-lookup"><span data-stu-id="624aa-115">Requirements</span></span>



| <span data-ttu-id="624aa-116">Требование</span><span class="sxs-lookup"><span data-stu-id="624aa-116">Requirement</span></span> | <span data-ttu-id="624aa-117">Значение</span><span class="sxs-lookup"><span data-stu-id="624aa-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="624aa-118">Header</span><span class="sxs-lookup"><span data-stu-id="624aa-118">Header</span></span><br/>  | <dl> <span data-ttu-id="624aa-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="624aa-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="624aa-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="624aa-120">Library</span></span><br/> | <dl> <span data-ttu-id="624aa-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="624aa-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="624aa-122">DLL</span><span class="sxs-lookup"><span data-stu-id="624aa-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="624aa-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="624aa-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="624aa-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="624aa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="624aa-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="624aa-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="624aa-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="624aa-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="624aa-127">**D3D12 \_ Blend, \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="624aa-127">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





