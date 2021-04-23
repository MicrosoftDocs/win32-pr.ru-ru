---
title: жетрендертаржетсамплекаунт
description: Возвращает число выборок для целевого объекта прорисовки.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- Жетрендертаржетсамплекаунт HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96c159a2ed63684b4bad2cbc6fa789c2dbd76edf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487161"
---
# <a name="getrendertargetsamplecount"></a><span data-ttu-id="ac99d-104">жетрендертаржетсамплекаунт</span><span class="sxs-lookup"><span data-stu-id="ac99d-104">GetRenderTargetSampleCount</span></span>

<span data-ttu-id="ac99d-105">Возвращает число выборок для целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="ac99d-105">Gets the number of samples for a render target.</span></span>



| <span data-ttu-id="ac99d-106">*Uint* Жетрендертаржетсамплекаунт ()</span><span class="sxs-lookup"><span data-stu-id="ac99d-106">*UINT* GetRenderTargetSampleCount()</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="ac99d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac99d-107">Parameters</span></span>



| <span data-ttu-id="ac99d-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="ac99d-108">Item</span></span>                                                                                 | <span data-ttu-id="ac99d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ac99d-109">Description</span></span> |
|--------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="ac99d-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span><span class="sxs-lookup"><span data-stu-id="ac99d-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="ac99d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac99d-111">Return Value</span></span>

<span data-ttu-id="ac99d-112">Число выборок.</span><span class="sxs-lookup"><span data-stu-id="ac99d-112">The number of samples.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac99d-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="ac99d-113">Remarks</span></span>

<span data-ttu-id="ac99d-114">Используйте эту функцию и [**жетрендертаржетсамплепоситион**](dx-graphics-hlsl-getrendertargetsampleposition.md) , чтобы узнать число и положение местоположений выборки для целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="ac99d-114">Use this function and [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="ac99d-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ac99d-115">Minimum Shader Model</span></span>

<span data-ttu-id="ac99d-116">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ac99d-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ac99d-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ac99d-117">Shader Model</span></span>                                                        | <span data-ttu-id="ac99d-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac99d-118">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="ac99d-119">[Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров</span><span class="sxs-lookup"><span data-stu-id="ac99d-119">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="ac99d-120">да</span><span class="sxs-lookup"><span data-stu-id="ac99d-120">yes</span></span>       |
| [<span data-ttu-id="ac99d-121">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac99d-121">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="ac99d-122">Нет</span><span class="sxs-lookup"><span data-stu-id="ac99d-122">no</span></span>        |
| [<span data-ttu-id="ac99d-123">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac99d-123">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="ac99d-124">Нет</span><span class="sxs-lookup"><span data-stu-id="ac99d-124">no</span></span>        |
| [<span data-ttu-id="ac99d-125">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac99d-125">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="ac99d-126">Нет</span><span class="sxs-lookup"><span data-stu-id="ac99d-126">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="ac99d-127">См. также</span><span class="sxs-lookup"><span data-stu-id="ac99d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac99d-128">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ac99d-128">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





