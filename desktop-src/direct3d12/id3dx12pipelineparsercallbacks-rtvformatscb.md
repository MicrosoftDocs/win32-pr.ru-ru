---
title: Метод ID3DX12PipelineParserCallbacks Ртвформатскб (D3DX12. h)
description: Вызывает обратный вызов подобъекта массива формата целевого объекта прорисовки объекта, реализующего этот интерфейс.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- Метод Ртвформатскб
- Метод Ртвформатскб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Ртвформатскб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caaa1df508e1a448de3851d408f9aad5ac94d957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713814"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a><span data-ttu-id="44d8c-106">Метод ID3DX12PipelineParserCallbacks:: Ртвформатскб</span><span class="sxs-lookup"><span data-stu-id="44d8c-106">ID3DX12PipelineParserCallbacks::RTVFormatsCb method</span></span>

<span data-ttu-id="44d8c-107">Вызывает обратный вызов подобъекта массива формата целевого объекта прорисовки объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="44d8c-107">Calls the render target format array subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="44d8c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44d8c-108">Syntax</span></span>


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a><span data-ttu-id="44d8c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="44d8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d8c-110">*Ртвформатс* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="44d8c-110">*RTVFormats* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="44d8c-111">Тип: **Константный [**\_ \_ \_ массив формата D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span><span class="sxs-lookup"><span data-stu-id="44d8c-111">Type: **const [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span></span>

<span data-ttu-id="44d8c-112">Сведения о подобъекте массива целевого формата визуализации, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="44d8c-112">Details of the render target format array subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d8c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44d8c-113">Return value</span></span>

<span data-ttu-id="44d8c-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="44d8c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d8c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="44d8c-115">Requirements</span></span>



| <span data-ttu-id="44d8c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="44d8c-116">Requirement</span></span> | <span data-ttu-id="44d8c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="44d8c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44d8c-118">Header</span><span class="sxs-lookup"><span data-stu-id="44d8c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="44d8c-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="44d8c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="44d8c-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="44d8c-120">Library</span></span><br/> | <dl> <span data-ttu-id="44d8c-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44d8c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="44d8c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="44d8c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="44d8c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44d8c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d8c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44d8c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d8c-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="44d8c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="44d8c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="44d8c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="44d8c-127">**\_ \_ Массив формата D3D12 \_ RT**</span><span class="sxs-lookup"><span data-stu-id="44d8c-127">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





