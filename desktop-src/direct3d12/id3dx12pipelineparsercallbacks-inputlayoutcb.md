---
title: Метод ID3DX12PipelineParserCallbacks Инпутлайауткб (D3DX12. h)
description: Вызывает обратный вызов подобъекта входной структуры для объекта, реализующего этот интерфейс.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- Метод Инпутлайауткб
- Метод Инпутлайауткб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Инпутлайауткб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc28276ef893247577cf41de8f4aba5582c101d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713817"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a><span data-ttu-id="2f1a1-106">Метод ID3DX12PipelineParserCallbacks:: Инпутлайауткб</span><span class="sxs-lookup"><span data-stu-id="2f1a1-106">ID3DX12PipelineParserCallbacks::InputLayoutCb method</span></span>

<span data-ttu-id="2f1a1-107">Вызывает обратный вызов подобъекта входной структуры для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-107">Calls the input layout subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f1a1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f1a1-108">Syntax</span></span>


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a><span data-ttu-id="2f1a1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f1a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f1a1-110">*Инпутлайаут* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="2f1a1-110">*InputLayout* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2f1a1-111">Тип: **const [**D3D12 \_ входной \_ Макет \_ Layout**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span><span class="sxs-lookup"><span data-stu-id="2f1a1-111">Type: **const [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span></span>

<span data-ttu-id="2f1a1-112">Сведения о подобъекте макета входных данных, проанализированном из потока состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-112">Details of the input layout subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f1a1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f1a1-113">Return value</span></span>

<span data-ttu-id="2f1a1-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f1a1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2f1a1-115">Requirements</span></span>



| <span data-ttu-id="2f1a1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2f1a1-116">Requirement</span></span> | <span data-ttu-id="2f1a1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2f1a1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2f1a1-118">Header</span><span class="sxs-lookup"><span data-stu-id="2f1a1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2f1a1-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f1a1-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="2f1a1-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2f1a1-120">Library</span></span><br/> | <dl> <span data-ttu-id="2f1a1-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f1a1-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f1a1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2f1a1-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2f1a1-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f1a1-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f1a1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f1a1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f1a1-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2f1a1-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2f1a1-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="2f1a1-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="2f1a1-127">**D3D12 \_ входной \_ Макет \_**</span><span class="sxs-lookup"><span data-stu-id="2f1a1-127">**D3D12\_INPUT\_LAYOUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





