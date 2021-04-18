---
title: Метод ID3DX12PipelineParserCallbacks Нодемасккб (D3DX12. h)
description: Вызывает обратный вызов подобъекта нодемаск объекта, реализующего этот интерфейс.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Метод Нодемасккб
- Метод Нодемасккб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Нодемасккб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf1cc03f60259c395ca8c459ddd5a308e3dcd6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713490"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a><span data-ttu-id="acab2-106">Метод ID3DX12PipelineParserCallbacks:: Нодемасккб</span><span class="sxs-lookup"><span data-stu-id="acab2-106">ID3DX12PipelineParserCallbacks::NodemaskCb method</span></span>

<span data-ttu-id="acab2-107">Вызывает обратный вызов подобъекта нодемаск объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="acab2-107">Calls the nodemask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="acab2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acab2-108">Syntax</span></span>


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a><span data-ttu-id="acab2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="acab2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acab2-110">*нодемаск*</span><span class="sxs-lookup"><span data-stu-id="acab2-110">*Nodemask*</span></span> 
</dt> <dd>

<span data-ttu-id="acab2-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="acab2-111">Type: **UINT**</span></span>

<span data-ttu-id="acab2-112">Сведения о подобъекте нодемаск, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="acab2-112">Details of the nodemask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acab2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acab2-113">Return value</span></span>

<span data-ttu-id="acab2-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="acab2-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="acab2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="acab2-115">Requirements</span></span>



| <span data-ttu-id="acab2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="acab2-116">Requirement</span></span> | <span data-ttu-id="acab2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="acab2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="acab2-118">Header</span><span class="sxs-lookup"><span data-stu-id="acab2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="acab2-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="acab2-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="acab2-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="acab2-120">Library</span></span><br/> | <dl> <span data-ttu-id="acab2-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acab2-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="acab2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="acab2-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="acab2-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acab2-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acab2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acab2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acab2-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="acab2-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="acab2-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="acab2-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





