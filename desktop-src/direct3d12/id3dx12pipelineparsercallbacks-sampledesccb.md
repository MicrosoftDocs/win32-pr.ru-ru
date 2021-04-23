---
title: Метод ID3DX12PipelineParserCallbacks Сампледесккб (D3DX12. h)
description: Вызывает обратный вызов подобъекта описания образца для объекта, реализующего этот интерфейс.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Метод Сампледесккб
- Метод Сампледесккб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Сампледесккб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713484"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a><span data-ttu-id="ae755-106">Метод ID3DX12PipelineParserCallbacks:: Сампледесккб</span><span class="sxs-lookup"><span data-stu-id="ae755-106">ID3DX12PipelineParserCallbacks::SampleDescCb method</span></span>

<span data-ttu-id="ae755-107">Вызывает обратный вызов подобъекта описания образца для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ae755-107">Calls the sample description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae755-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae755-108">Syntax</span></span>


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a><span data-ttu-id="ae755-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae755-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae755-110">*Сампледеск* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="ae755-110">*SampleDesc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ae755-111">Тип: **[**\_ образец \_**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) "const** " для DXGI</span><span class="sxs-lookup"><span data-stu-id="ae755-111">Type: **const [**DXGI\_SAMPLE\_DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span></span>

<span data-ttu-id="ae755-112">Сведения о подобъекте образца Description, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="ae755-112">Details of the sample description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae755-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae755-113">Return value</span></span>

<span data-ttu-id="ae755-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="ae755-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae755-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ae755-115">Requirements</span></span>



| <span data-ttu-id="ae755-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ae755-116">Requirement</span></span> | <span data-ttu-id="ae755-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ae755-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ae755-118">Header</span><span class="sxs-lookup"><span data-stu-id="ae755-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ae755-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae755-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="ae755-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae755-120">Library</span></span><br/> | <dl> <span data-ttu-id="ae755-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae755-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="ae755-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ae755-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="ae755-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae755-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae755-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae755-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae755-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ae755-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="ae755-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="ae755-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="ae755-127">**\_пример \_ DESC в DXGI**</span><span class="sxs-lookup"><span data-stu-id="ae755-127">**DXGI\_SAMPLE\_DESC**</span></span>](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

