---
title: Метод ID3DX12PipelineParserCallbacks Пскб (D3DX12. h)
description: Вызывает обратный вызов подобъекта пиксельного шейдера для объекта, реализующего этот интерфейс.
ms.assetid: 3397B018-C26A-426F-88BB-89013BACBEEA
keywords:
- Метод Пскб
- Метод Пскб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Пскб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c972702c215556b953797a6e332f8e86c480b094
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713489"
---
# <a name="id3dx12pipelineparsercallbackspscb-method"></a><span data-ttu-id="0d80a-106">ID3DX12PipelineParserCallbacks: метод:P СКБ</span><span class="sxs-lookup"><span data-stu-id="0d80a-106">ID3DX12PipelineParserCallbacks::PSCb method</span></span>

<span data-ttu-id="0d80a-107">Вызывает обратный вызов подобъекта пиксельного шейдера для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0d80a-107">Calls the pixel shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d80a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d80a-108">Syntax</span></span>


```C++
void PSCb(
  [ref] const D3D12_SHADER_BYTECODE &PS
);
```



## <a name="parameters"></a><span data-ttu-id="0d80a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d80a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d80a-110">*PS* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="0d80a-110">*PS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0d80a-111">Тип: **Константный [**\_ \_ байт шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="0d80a-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="0d80a-112">Сведения о подобъекте шейдера пикселей, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="0d80a-112">Details of the pixel shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d80a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d80a-113">Return value</span></span>

<span data-ttu-id="0d80a-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="0d80a-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d80a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0d80a-115">Requirements</span></span>



| <span data-ttu-id="0d80a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="0d80a-116">Requirement</span></span> | <span data-ttu-id="0d80a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0d80a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0d80a-118">Header</span><span class="sxs-lookup"><span data-stu-id="0d80a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0d80a-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d80a-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="0d80a-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0d80a-120">Library</span></span><br/> | <dl> <span data-ttu-id="0d80a-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d80a-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="0d80a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0d80a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d80a-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d80a-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d80a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d80a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d80a-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0d80a-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="0d80a-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="0d80a-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="0d80a-127">**\_Байтовый код шейдера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="0d80a-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





