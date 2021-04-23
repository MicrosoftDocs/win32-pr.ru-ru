---
title: Функция D3DX12ParsePipelineStream (D3dx12. h)
description: Анализирует описание потока состояния конвейера, вызывая пользовательский обратный вызов для каждого анализируемого экземпляра подобъекта.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- Функция D3DX12ParsePipelineStream
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720870"
---
# <a name="d3dx12parsepipelinestream-function"></a><span data-ttu-id="8079a-104">Функция D3DX12ParsePipelineStream</span><span class="sxs-lookup"><span data-stu-id="8079a-104">D3DX12ParsePipelineStream function</span></span>

<span data-ttu-id="8079a-105">Анализирует описание потока состояния конвейера, вызывая пользовательский обратный вызов для каждого анализируемого экземпляра подобъекта.</span><span class="sxs-lookup"><span data-stu-id="8079a-105">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8079a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8079a-106">Syntax</span></span>


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a><span data-ttu-id="8079a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8079a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8079a-108">*DESC* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="8079a-108">*Desc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8079a-109">Тип: **[**\_ поток состояния const D3D12 конвейера — \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span><span class="sxs-lookup"><span data-stu-id="8079a-109">Type: **const [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span></span>

<span data-ttu-id="8079a-110">Описание потока состояния конвейера для синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="8079a-110">The pipeline state stream description to parse.</span></span>

</dd> <dt>

<span data-ttu-id="8079a-111">*пкаллбаккс*</span><span class="sxs-lookup"><span data-stu-id="8079a-111">*pCallbacks*</span></span> 
</dt> <dd>

<span data-ttu-id="8079a-112">Тип: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span><span class="sxs-lookup"><span data-stu-id="8079a-112">Type: **[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span></span>

<span data-ttu-id="8079a-113">Структура, указывающая обратные вызовы для вызова для каждого типа подобъекта и дополнительные обратные вызовы для вызова в случае ошибки синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="8079a-113">A structure that specifies the callbacks to call for each subobject type and additional callbacks to call in the event of a parsing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8079a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8079a-114">Return value</span></span>

<span data-ttu-id="8079a-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8079a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8079a-116">Этот метод возвращает значение HRESULT Success (**S \_ OK** или **E \_ INVALIDARG** Error), если обнаружен неизвестный тип подобъекта, если описание потока пустое, равно null или содержит дубликаты подобъектов (включая производные подобъекты) или если *пкаллбаккс* имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="8079a-116">This method returns an HRESULT success (**S\_OK** or **E\_INVALIDARG** error if an unknown subobject type is encountered, if the stream description is empty, null, or contains duplicate subobjects (including derived subobjects), or if *pCallbacks* is null.</span></span> <span data-ttu-id="8079a-117">В каждом случае, когда \_ возвращается E INVALIDARG, сначала вызывается соответствующий обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="8079a-117">In each case that E\_INVALIDARG is returned, a corresponding callback is first called.</span></span>

## <a name="requirements"></a><span data-ttu-id="8079a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8079a-118">Requirements</span></span>



| <span data-ttu-id="8079a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8079a-119">Requirement</span></span> | <span data-ttu-id="8079a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8079a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8079a-121">Header</span><span class="sxs-lookup"><span data-stu-id="8079a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8079a-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8079a-122"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8079a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8079a-123">Library</span></span><br/> | <dl> <span data-ttu-id="8079a-124"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8079a-124"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8079a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8079a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="8079a-126"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8079a-126"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8079a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8079a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8079a-128">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="8079a-128">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





