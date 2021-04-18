---
title: Метод ID3DX12PipelineParserCallbacks Еррорбадинпутпараметер (D3DX12. h)
description: Вызывает недопустимый обратный вызов ошибки входного параметра объекта, реализующего этот интерфейс.
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- Метод Еррорбадинпутпараметер
- Метод Еррорбадинпутпараметер, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Еррорбадинпутпараметер
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5181e8d9fb83b7338adc3af5c0ce44aec1b447d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713830"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a><span data-ttu-id="3d22a-106">Метод ID3DX12PipelineParserCallbacks:: Еррорбадинпутпараметер</span><span class="sxs-lookup"><span data-stu-id="3d22a-106">ID3DX12PipelineParserCallbacks::ErrorBadInputParameter method</span></span>

<span data-ttu-id="3d22a-107">Вызывает недопустимый обратный вызов ошибки входного параметра объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="3d22a-107">Calls the bad input parameter error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d22a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d22a-108">Syntax</span></span>


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a><span data-ttu-id="3d22a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d22a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d22a-110">*ParameterIndex*</span><span class="sxs-lookup"><span data-stu-id="3d22a-110">*ParameterIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="3d22a-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3d22a-111">Type: **UINT**</span></span>

<span data-ttu-id="3d22a-112">Расположение параметра, содержащего неверные входные данные.</span><span class="sxs-lookup"><span data-stu-id="3d22a-112">The position of the parameter that contains bad input.</span></span> <span data-ttu-id="3d22a-113">Самый левый параметр находится в позиции 1, а не на позиции 0.</span><span class="sxs-lookup"><span data-stu-id="3d22a-113">The left-most parameter is at position 1, not position 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d22a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d22a-114">Return value</span></span>

<span data-ttu-id="3d22a-115">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="3d22a-115">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d22a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3d22a-116">Requirements</span></span>



| <span data-ttu-id="3d22a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3d22a-117">Requirement</span></span> | <span data-ttu-id="3d22a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3d22a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3d22a-119">Header</span><span class="sxs-lookup"><span data-stu-id="3d22a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3d22a-120"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d22a-120"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="3d22a-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3d22a-121">Library</span></span><br/> | <dl> <span data-ttu-id="3d22a-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d22a-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="3d22a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3d22a-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="3d22a-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d22a-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d22a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d22a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d22a-126">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3d22a-126">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="3d22a-127">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="3d22a-127">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





