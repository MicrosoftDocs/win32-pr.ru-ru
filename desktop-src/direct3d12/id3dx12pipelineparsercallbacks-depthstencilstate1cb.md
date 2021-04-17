---
title: Метод ID3DX12PipelineParserCallbacks DepthStencilState1Cb (D3DX12. h)
description: Вызывает обратный вызов подобъекта состояния трафарета глубины (D3D12 \_ \_ трафарета \_ DESC1) объекта, реализующего этот интерфейс.
ms.assetid: C1AE06E5-B1FF-44C2-9C56-1540B97AD883
keywords:
- Метод DepthStencilState1Cb
- Метод DepthStencilState1Cb, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод DepthStencilState1Cb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilState1Cb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a42cf85f60dcf27a5751f77a346931bfad6b03e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703657"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a><span data-ttu-id="d9b71-106">ID3DX12PipelineParserCallbacks: метод:D epthStencilState1Cb</span><span class="sxs-lookup"><span data-stu-id="d9b71-106">ID3DX12PipelineParserCallbacks::DepthStencilState1Cb method</span></span>

<span data-ttu-id="d9b71-107">Вызывает обратный вызов подобъекта состояния трафарета глубины ([**D3D12 \_ \_ трафарета \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d9b71-107">Calls the depth stencil state ([**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9b71-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9b71-108">Syntax</span></span>


```C++
void DepthStencilState1Cb(
  [ref] const D3D12_DEPTH_STENCIL_DESC1 &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="d9b71-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9b71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b71-110">*ДепсстенЦилстате* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="d9b71-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b71-111">Тип: **const [**D3D12 \_ \_ набор элементов глубины \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span><span class="sxs-lookup"><span data-stu-id="d9b71-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span></span>

<span data-ttu-id="d9b71-112">Сведения о подобъекте состояния шаблона глубины, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="d9b71-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b71-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9b71-113">Return value</span></span>

<span data-ttu-id="d9b71-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="d9b71-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b71-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d9b71-115">Requirements</span></span>



| <span data-ttu-id="d9b71-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d9b71-116">Requirement</span></span> | <span data-ttu-id="d9b71-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d9b71-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b71-118">Header</span><span class="sxs-lookup"><span data-stu-id="d9b71-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d9b71-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9b71-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d9b71-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9b71-120">Library</span></span><br/> | <dl> <span data-ttu-id="d9b71-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9b71-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9b71-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d9b71-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d9b71-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9b71-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b71-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9b71-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b71-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d9b71-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d9b71-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="d9b71-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="d9b71-127">**D3D12 \_ \_ трафарета глубины \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="d9b71-127">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 





