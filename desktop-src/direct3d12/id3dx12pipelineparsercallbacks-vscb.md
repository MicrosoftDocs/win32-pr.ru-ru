---
title: Метод ID3DX12PipelineParserCallbacks Вскб (D3DX12. h)
description: Вызывает обратный вызов подобъекта вершинного шейдера объекта, реализующего этот интерфейс.
ms.assetid: 65A185B7-C790-4254-A3C5-EBBE9C38CA4E
keywords:
- Метод Вскб
- Метод Вскб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Вскб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.VSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef9ab27b2f9fd4b93190e2eea453397de297013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713813"
---
# <a name="id3dx12pipelineparsercallbacksvscb-method"></a><span data-ttu-id="23b8f-106">Метод ID3DX12PipelineParserCallbacks:: Вскб</span><span class="sxs-lookup"><span data-stu-id="23b8f-106">ID3DX12PipelineParserCallbacks::VSCb method</span></span>

<span data-ttu-id="23b8f-107">Вызывает обратный вызов подобъекта вершинного шейдера объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="23b8f-107">Calls the vertex shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="23b8f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23b8f-108">Syntax</span></span>


```C++
void VSCb(
  [ref] const D3D12_SHADER_BYTECODE &VS
);
```



## <a name="parameters"></a><span data-ttu-id="23b8f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="23b8f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23b8f-110">*VS* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="23b8f-110">*VS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="23b8f-111">Тип: **Константный [**\_ \_ байт шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="23b8f-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="23b8f-112">Сведения о подобъекте шейдера вершин, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="23b8f-112">Details of the vertex shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23b8f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23b8f-113">Return value</span></span>

<span data-ttu-id="23b8f-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="23b8f-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="23b8f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="23b8f-115">Requirements</span></span>



| <span data-ttu-id="23b8f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="23b8f-116">Requirement</span></span> | <span data-ttu-id="23b8f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="23b8f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23b8f-118">Header</span><span class="sxs-lookup"><span data-stu-id="23b8f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="23b8f-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="23b8f-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="23b8f-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="23b8f-120">Library</span></span><br/> | <dl> <span data-ttu-id="23b8f-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23b8f-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="23b8f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="23b8f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="23b8f-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23b8f-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23b8f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23b8f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b8f-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="23b8f-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="23b8f-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="23b8f-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="23b8f-127">**\_Байтовый код шейдера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="23b8f-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





