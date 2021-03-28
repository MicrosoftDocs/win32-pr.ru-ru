---
title: Функция Abort (Корекрт \_ Terminate. h)
description: Отправляет сообщение об ошибке в информационную очередь и завершает текущий выполняемый вызов Draw или Dispatch.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- Функция Abort HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987266"
---
# <a name="abort-function"></a><span data-ttu-id="f157f-104">Функция abort</span><span class="sxs-lookup"><span data-stu-id="f157f-104">abort function</span></span>

<span data-ttu-id="f157f-105">Отправляет сообщение об ошибке в информационную очередь и завершает текущий выполняемый вызов Draw или Dispatch.</span><span class="sxs-lookup"><span data-stu-id="f157f-105">Submits an error message to the information queue and terminates the current draw or dispatch call being executed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f157f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f157f-106">Syntax</span></span>

``` syntax
void abort(
    
);
```

## <a name="parameters"></a><span data-ttu-id="f157f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f157f-107">Parameters</span></span>

<dl> <dt>

 
</dt> <dd>

<span data-ttu-id="f157f-108">None</span><span class="sxs-lookup"><span data-stu-id="f157f-108">None</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f157f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f157f-109">Return value</span></span>

<span data-ttu-id="f157f-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f157f-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f157f-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="f157f-111">Remarks</span></span>

<span data-ttu-id="f157f-112">Эта операция не выполняет никаких действий на средствах прорисовки, не поддерживающих эту операцию.</span><span class="sxs-lookup"><span data-stu-id="f157f-112">This operation does nothing on rasterizers that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="f157f-113">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f157f-113">Minimum Shader Model</span></span>

<span data-ttu-id="f157f-114">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f157f-114">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f157f-115">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f157f-115">Shader Model</span></span>                                                        | <span data-ttu-id="f157f-116">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f157f-116">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="f157f-117">Shader Model 4 (DirectX HLSL) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f157f-117">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f157f-118">да</span><span class="sxs-lookup"><span data-stu-id="f157f-118">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="f157f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f157f-119">Requirements</span></span>



| <span data-ttu-id="f157f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f157f-120">Requirement</span></span> | <span data-ttu-id="f157f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f157f-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f157f-122">Header</span><span class="sxs-lookup"><span data-stu-id="f157f-122">Header</span></span><br/> | <dl> <span data-ttu-id="f157f-123"><dt>Корекрт \_ Terminate. h</dt></span><span class="sxs-lookup"><span data-stu-id="f157f-123"><dt>Corecrt\_terminate.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f157f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f157f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f157f-125">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="f157f-125">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





