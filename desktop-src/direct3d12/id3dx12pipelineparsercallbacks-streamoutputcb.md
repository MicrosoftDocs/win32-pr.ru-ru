---
title: Метод ID3DX12PipelineParserCallbacks Стреамаутпуткб (D3DX12. h)
description: Вызывает обратный вызов подобъекта описания потока вывода объекта, реализующего этот интерфейс.
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- Метод Стреамаутпуткб
- Метод Стреамаутпуткб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Стреамаутпуткб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713482"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a><span data-ttu-id="10734-106">Метод ID3DX12PipelineParserCallbacks:: Стреамаутпуткб</span><span class="sxs-lookup"><span data-stu-id="10734-106">ID3DX12PipelineParserCallbacks::StreamOutputCb method</span></span>

<span data-ttu-id="10734-107">Вызывает обратный вызов подобъекта описания потока вывода объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="10734-107">Calls the stream output description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="10734-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10734-108">Syntax</span></span>


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a><span data-ttu-id="10734-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="10734-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10734-110">*Стреамаутпут* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="10734-110">*StreamOutput* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="10734-111">Тип: **const [**D3D12 \_ поток \_ вывода \_ Output**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span><span class="sxs-lookup"><span data-stu-id="10734-111">Type: **const [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span></span>

<span data-ttu-id="10734-112">Сведения о подобъекте описания выходного потока, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="10734-112">Details of the stream output description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10734-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10734-113">Return value</span></span>

<span data-ttu-id="10734-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="10734-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="10734-115">Требования</span><span class="sxs-lookup"><span data-stu-id="10734-115">Requirements</span></span>



| <span data-ttu-id="10734-116">Требование</span><span class="sxs-lookup"><span data-stu-id="10734-116">Requirement</span></span> | <span data-ttu-id="10734-117">Значение</span><span class="sxs-lookup"><span data-stu-id="10734-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10734-118">Header</span><span class="sxs-lookup"><span data-stu-id="10734-118">Header</span></span><br/>  | <dl> <span data-ttu-id="10734-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="10734-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="10734-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="10734-120">Library</span></span><br/> | <dl> <span data-ttu-id="10734-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10734-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="10734-122">DLL</span><span class="sxs-lookup"><span data-stu-id="10734-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="10734-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10734-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10734-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10734-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10734-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="10734-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="10734-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="10734-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="10734-127">**D3D12 \_ поток \_ вывода \_**</span><span class="sxs-lookup"><span data-stu-id="10734-127">**D3D12\_STREAM\_OUTPUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





