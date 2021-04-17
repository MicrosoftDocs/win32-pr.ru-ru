---
title: Метод ID3DX12PipelineParserCallbacks Кскб (D3DX12. h)
description: Вызывает обратный вызов подобъекта COMPUTE Shader для объекта, реализующего этот интерфейс.
ms.assetid: DE1ABA3D-D372-4D7F-9DB6-4E3360EAFAC2
keywords:
- Метод Кскб
- Метод Кскб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Кскб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27dcf175d153211e06864cb73139b03f868d15db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703885"
---
# <a name="id3dx12pipelineparsercallbackscscb-method"></a><span data-ttu-id="5cb25-106">Метод ID3DX12PipelineParserCallbacks:: Кскб</span><span class="sxs-lookup"><span data-stu-id="5cb25-106">ID3DX12PipelineParserCallbacks::CSCb method</span></span>

<span data-ttu-id="5cb25-107">Вызывает обратный вызов подобъекта COMPUTE Shader для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="5cb25-107">Calls the compute shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cb25-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cb25-108">Syntax</span></span>


```C++
void CSCb(
  [ref] const D3D12_SHADER_BYTECODE &CS
);
```



## <a name="parameters"></a><span data-ttu-id="5cb25-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5cb25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cb25-110">*CS* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="5cb25-110">*CS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5cb25-111">Тип: **Константный [**\_ \_ байт шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="5cb25-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="5cb25-112">Сведения о подобъекте COMPUTE Shader, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="5cb25-112">Details of the compute shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cb25-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5cb25-113">Return value</span></span>

<span data-ttu-id="5cb25-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="5cb25-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cb25-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5cb25-115">Requirements</span></span>



| <span data-ttu-id="5cb25-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5cb25-116">Requirement</span></span> | <span data-ttu-id="5cb25-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5cb25-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb25-118">Header</span><span class="sxs-lookup"><span data-stu-id="5cb25-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5cb25-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cb25-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="5cb25-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5cb25-120">Library</span></span><br/> | <dl> <span data-ttu-id="5cb25-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5cb25-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="5cb25-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5cb25-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5cb25-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cb25-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cb25-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cb25-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb25-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5cb25-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5cb25-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="5cb25-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="5cb25-127">**\_Байтовый код шейдера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="5cb25-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





