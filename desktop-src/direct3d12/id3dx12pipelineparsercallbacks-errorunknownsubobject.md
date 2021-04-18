---
title: Метод ID3DX12PipelineParserCallbacks Еррорункновнсубобжект (D3DX12. h)
description: Вызывает обратный вызов ошибки неизвестного подобъекта для объекта, реализующего этот интерфейс.
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- Метод Еррорункновнсубобжект
- Метод Еррорункновнсубобжект, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Еррорункновнсубобжект
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713827"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a><span data-ttu-id="64e25-106">Метод ID3DX12PipelineParserCallbacks:: Еррорункновнсубобжект</span><span class="sxs-lookup"><span data-stu-id="64e25-106">ID3DX12PipelineParserCallbacks::ErrorUnknownSubobject method</span></span>

<span data-ttu-id="64e25-107">Вызывает обратный вызов ошибки неизвестного подобъекта для объекта, реализующего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="64e25-107">Calls the unknown subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e25-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64e25-108">Syntax</span></span>


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a><span data-ttu-id="64e25-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="64e25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64e25-110">*ункновнтипевалуе*</span><span class="sxs-lookup"><span data-stu-id="64e25-110">*UnknownTypeValue*</span></span> 
</dt> <dd>

<span data-ttu-id="64e25-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="64e25-111">Type: **UINT**</span></span>

<span data-ttu-id="64e25-112">Нераспознанный тип подобъекта предпринятого подобъекта.</span><span class="sxs-lookup"><span data-stu-id="64e25-112">The unrecognized subobject type of the attempted subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64e25-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64e25-113">Return value</span></span>

<span data-ttu-id="64e25-114">Не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="64e25-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="64e25-115">Требования</span><span class="sxs-lookup"><span data-stu-id="64e25-115">Requirements</span></span>



| <span data-ttu-id="64e25-116">Требование</span><span class="sxs-lookup"><span data-stu-id="64e25-116">Requirement</span></span> | <span data-ttu-id="64e25-117">Значение</span><span class="sxs-lookup"><span data-stu-id="64e25-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="64e25-118">Header</span><span class="sxs-lookup"><span data-stu-id="64e25-118">Header</span></span><br/>  | <dl> <span data-ttu-id="64e25-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="64e25-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="64e25-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="64e25-120">Library</span></span><br/> | <dl> <span data-ttu-id="64e25-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64e25-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="64e25-122">DLL</span><span class="sxs-lookup"><span data-stu-id="64e25-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="64e25-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64e25-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64e25-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64e25-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e25-125">Вспомогательные интерфейсы для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="64e25-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="64e25-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="64e25-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





