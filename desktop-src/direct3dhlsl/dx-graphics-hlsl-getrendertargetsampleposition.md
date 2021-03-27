---
title: жетрендертаржетсамплепоситион
description: Возвращает позиции выборки (x, y) для данного образца индекса.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- Жетрендертаржетсамплепоситион HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0cd944b175522ab7d722ae791f3548c6633b71
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783312"
---
# <a name="getrendertargetsampleposition"></a><span data-ttu-id="d869e-104">жетрендертаржетсамплепоситион</span><span class="sxs-lookup"><span data-stu-id="d869e-104">GetRenderTargetSamplePosition</span></span>

<span data-ttu-id="d869e-105">Возвращает позиции выборки (x, y) для данного образца индекса.</span><span class="sxs-lookup"><span data-stu-id="d869e-105">Gets the sampling position (x,y) for a given sample index.</span></span>



|                                                                                  |
|----------------------------------------------------------------------------------|
| <span data-ttu-id="d869e-106">float<2> Жетрендертаржетсамплепоситион (в int<1> индекс</span><span class="sxs-lookup"><span data-stu-id="d869e-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span></span><br/><span data-ttu-id="d869e-107">);</span><span class="sxs-lookup"><span data-stu-id="d869e-107">);</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="d869e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d869e-108">Parameters</span></span>



| <span data-ttu-id="d869e-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="d869e-109">Item</span></span>                                                                                       | <span data-ttu-id="d869e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d869e-110">Description</span></span>                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="d869e-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Номер*</span><span class="sxs-lookup"><span data-stu-id="d869e-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Index*</span></span><br/> | <span data-ttu-id="d869e-112">\[в \] индексе выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="d869e-112">\[in\] A zero-based sample index.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d869e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d869e-113">Return Value</span></span>

<span data-ttu-id="d869e-114">Координата (x, y) данного образца.</span><span class="sxs-lookup"><span data-stu-id="d869e-114">The (x,y) position of the given sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="d869e-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="d869e-115">Remarks</span></span>

<span data-ttu-id="d869e-116">Используйте эту функцию и [**жетрендертаржетсамплекаунт**](dx-graphics-hlsl-getrendertargetsamplecount.md) , чтобы узнать число и положение местоположений выборки для целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="d869e-116">Use this function and [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="d869e-117">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d869e-117">Minimum Shader Model</span></span>

<span data-ttu-id="d869e-118">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d869e-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d869e-119">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d869e-119">Shader Model</span></span>                                                        | <span data-ttu-id="d869e-120">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d869e-120">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="d869e-121">[Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров</span><span class="sxs-lookup"><span data-stu-id="d869e-121">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="d869e-122">да</span><span class="sxs-lookup"><span data-stu-id="d869e-122">yes</span></span>       |
| [<span data-ttu-id="d869e-123">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d869e-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="d869e-124">Нет</span><span class="sxs-lookup"><span data-stu-id="d869e-124">no</span></span>        |
| [<span data-ttu-id="d869e-125">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d869e-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="d869e-126">Нет</span><span class="sxs-lookup"><span data-stu-id="d869e-126">no</span></span>        |
| [<span data-ttu-id="d869e-127">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d869e-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="d869e-128">Нет</span><span class="sxs-lookup"><span data-stu-id="d869e-128">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="d869e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d869e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d869e-130">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d869e-130">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





