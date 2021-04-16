---
title: Метод ID3DX12PipelineParserCallbacks ДепсстенЦилстатекб (D3DX12. h) (DSV)
description: Вызывает обратный вызов подобъекта формата значения шаблона глубины объекта, реализующего этот интерфейс.
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
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
ms.openlocfilehash: fd40b138c357c143deafffe01252b3c8b3e87cda
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187909"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h-for-depth-stencil-value"></a><span data-ttu-id="31979-106">Метод ID3DX12PipelineParserCallbacks ДепсстенЦилстатекб (D3DX12. h) для значения шаблона глубины</span><span class="sxs-lookup"><span data-stu-id="31979-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h) for depth stencil value</span></span>

<span data-ttu-id="31979-107">Вызывает обратный вызов подобъекта формата значения шаблона глубины объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="31979-107">Calls the depth stencil value format subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="31979-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31979-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="31979-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="31979-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31979-110">*депсстенЦилстате*</span><span class="sxs-lookup"><span data-stu-id="31979-110">*DepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="31979-111">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="31979-111">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="31979-112">Сведения о подобъекте формата значения трафарета глубины, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="31979-112">Details of the depth stencil value format subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31979-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31979-113">Return value</span></span>

<span data-ttu-id="31979-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="31979-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="31979-115">Требования</span><span class="sxs-lookup"><span data-stu-id="31979-115">Requirements</span></span>



| <span data-ttu-id="31979-116">Требование</span><span class="sxs-lookup"><span data-stu-id="31979-116">Requirement</span></span> | <span data-ttu-id="31979-117">Значение</span><span class="sxs-lookup"><span data-stu-id="31979-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="31979-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="31979-118">Header</span></span><br/>  | <dl> <span data-ttu-id="31979-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="31979-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="31979-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31979-120">Library</span></span><br/> | <dl> <span data-ttu-id="31979-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31979-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="31979-122">DLL</span><span class="sxs-lookup"><span data-stu-id="31979-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="31979-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31979-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31979-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31979-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31979-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="31979-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="31979-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="31979-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="31979-127">**\_Формат DXGI**</span><span class="sxs-lookup"><span data-stu-id="31979-127">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

