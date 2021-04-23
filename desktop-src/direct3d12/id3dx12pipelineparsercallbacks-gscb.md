---
title: Метод ID3DX12PipelineParserCallbacks ГСКБ (D3DX12. h)
description: Вызывает обратный вызов подобъекта шейдера Geometry для объекта, реализующего этот интерфейс.
ms.assetid: 0D8846C5-15E4-43EB-AA82-163BB514C5B7
keywords:
- Метод ГСКБ
- Метод ГСКБ, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод ГСКБ
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.GSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768e64ccdf06eccce731cafd0d40a9862b695e1d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713823"
---
# <a name="id3dx12pipelineparsercallbacksgscb-method"></a><span data-ttu-id="cf6ac-106">Метод ID3DX12PipelineParserCallbacks:: ГСКБ</span><span class="sxs-lookup"><span data-stu-id="cf6ac-106">ID3DX12PipelineParserCallbacks::GSCb method</span></span>

<span data-ttu-id="cf6ac-107">Вызывает обратный вызов подобъекта шейдера Geometry для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="cf6ac-107">Calls the geometry shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf6ac-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf6ac-108">Syntax</span></span>


```C++
void GSCb(
  [ref] const D3D12_SHADER_BYTECODE &GS
);
```



## <a name="parameters"></a><span data-ttu-id="cf6ac-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf6ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf6ac-110">*GS* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="cf6ac-110">*GS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cf6ac-111">Тип: **Константный [**\_ \_ байт шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="cf6ac-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="cf6ac-112">Сведения о подобъекте шейдера Geometry, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="cf6ac-112">Details of the geometry shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf6ac-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf6ac-113">Return value</span></span>

<span data-ttu-id="cf6ac-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="cf6ac-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf6ac-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cf6ac-115">Requirements</span></span>



| <span data-ttu-id="cf6ac-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cf6ac-116">Requirement</span></span> | <span data-ttu-id="cf6ac-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cf6ac-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6ac-118">Header</span><span class="sxs-lookup"><span data-stu-id="cf6ac-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cf6ac-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf6ac-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="cf6ac-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cf6ac-120">Library</span></span><br/> | <dl> <span data-ttu-id="cf6ac-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf6ac-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf6ac-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cf6ac-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="cf6ac-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf6ac-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf6ac-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf6ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf6ac-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="cf6ac-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="cf6ac-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="cf6ac-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="cf6ac-127">**\_Байтовый код шейдера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="cf6ac-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





