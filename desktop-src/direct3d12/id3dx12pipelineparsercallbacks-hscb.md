---
title: Метод ID3DX12PipelineParserCallbacks Хскб (D3DX12. h)
description: Вызывает обратный вызов подобъекта шейдера поверхности объекта, реализующего этот интерфейс.
ms.assetid: B2967E7F-391F-4A76-A087-E0B925018EE3
keywords:
- Метод Хскб
- Метод Хскб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Хскб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.HSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7d351e0b3827087cb51c38af173badd28d698c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713822"
---
# <a name="id3dx12pipelineparsercallbackshscb-method"></a><span data-ttu-id="1f1bb-106">Метод ID3DX12PipelineParserCallbacks:: Хскб</span><span class="sxs-lookup"><span data-stu-id="1f1bb-106">ID3DX12PipelineParserCallbacks::HSCb method</span></span>

<span data-ttu-id="1f1bb-107">Вызывает обратный вызов подобъекта шейдера поверхности объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="1f1bb-107">Calls the hull shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f1bb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f1bb-108">Syntax</span></span>


```C++
void HSCb(
  [ref] const D3D12_SHADER_BYTECODE &HS
);
```



## <a name="parameters"></a><span data-ttu-id="1f1bb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f1bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f1bb-110">*HS* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="1f1bb-110">*HS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1f1bb-111">Тип: **Константный [**\_ \_ байт шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="1f1bb-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="1f1bb-112">Сведения о подобъекте шейдера поверхности, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="1f1bb-112">Details of the hull shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f1bb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f1bb-113">Return value</span></span>

<span data-ttu-id="1f1bb-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="1f1bb-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f1bb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1f1bb-115">Requirements</span></span>



| <span data-ttu-id="1f1bb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1f1bb-116">Requirement</span></span> | <span data-ttu-id="1f1bb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1f1bb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1bb-118">Header</span><span class="sxs-lookup"><span data-stu-id="1f1bb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1f1bb-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f1bb-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="1f1bb-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1f1bb-120">Library</span></span><br/> | <dl> <span data-ttu-id="1f1bb-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f1bb-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="1f1bb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1f1bb-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="1f1bb-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f1bb-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f1bb-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f1bb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1bb-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1f1bb-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="1f1bb-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="1f1bb-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="1f1bb-127">**\_Байтовый код шейдера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="1f1bb-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





