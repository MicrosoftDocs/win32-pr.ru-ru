---
title: Метод ID3DX12PipelineParserCallbacks Дскб (D3DX12. h)
description: Вызывает обратный вызов подобъекта шейдера домена для объекта, реализующего этот интерфейс.
ms.assetid: F4877211-4122-4418-9323-3F68B0BB3363
keywords:
- Метод Дскб
- Метод Дскб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Дскб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf5f68ca6e6e4891fa391a142d45a1496a42ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713833"
---
# <a name="id3dx12pipelineparsercallbacksdscb-method"></a><span data-ttu-id="df72b-106">ID3DX12PipelineParserCallbacks: метод:D СКБ</span><span class="sxs-lookup"><span data-stu-id="df72b-106">ID3DX12PipelineParserCallbacks::DSCb method</span></span>

<span data-ttu-id="df72b-107">Вызывает обратный вызов подобъекта шейдера домена для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="df72b-107">Calls the domain shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="df72b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df72b-108">Syntax</span></span>


```C++
void DSCb(
  [ref] const D3D12_SHADER_BYTECODE &DS
);
```



## <a name="parameters"></a><span data-ttu-id="df72b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="df72b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df72b-110">*Службы каталогов* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="df72b-110">*DS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="df72b-111">Тип: **Константный [**\_ \_ байт шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="df72b-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="df72b-112">Сведения о подобъекте шейдера домена, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="df72b-112">Details of the domain shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df72b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df72b-113">Return value</span></span>

<span data-ttu-id="df72b-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="df72b-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="df72b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="df72b-115">Requirements</span></span>



| <span data-ttu-id="df72b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="df72b-116">Requirement</span></span> | <span data-ttu-id="df72b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="df72b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="df72b-118">Header</span><span class="sxs-lookup"><span data-stu-id="df72b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="df72b-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="df72b-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="df72b-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="df72b-120">Library</span></span><br/> | <dl> <span data-ttu-id="df72b-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df72b-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="df72b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="df72b-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="df72b-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df72b-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df72b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df72b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df72b-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="df72b-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="df72b-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="df72b-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="df72b-127">**\_Байтовый код шейдера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="df72b-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





