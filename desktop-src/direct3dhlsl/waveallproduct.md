---
title: Функция Вавеактивепродукт
description: Умножает значения выражения на все активные дорожки в текущей волне и реплицирует их обратно во все активные дорожки.
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- Функция Вавеактивепродукт HLSL
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103891236"
---
# <a name="waveactiveproduct-function"></a><span data-ttu-id="badc2-104">Функция Вавеактивепродукт</span><span class="sxs-lookup"><span data-stu-id="badc2-104">WaveActiveProduct function</span></span>

<span data-ttu-id="badc2-105">Умножает значения выражения на все активные дорожки в текущей волне и реплицирует их обратно во все активные дорожки.</span><span class="sxs-lookup"><span data-stu-id="badc2-105">Multiplies the values of the expression together across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="badc2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="badc2-106">Syntax</span></span>

``` syntax
<type> WaveActiveProduct(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="badc2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="badc2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="badc2-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="badc2-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="badc2-109">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="badc2-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="badc2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="badc2-110">Return value</span></span>

<span data-ttu-id="badc2-111">Значение продукта.</span><span class="sxs-lookup"><span data-stu-id="badc2-111">The product value.</span></span>

## <a name="remarks"></a><span data-ttu-id="badc2-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="badc2-112">Remarks</span></span>

<span data-ttu-id="badc2-113">Порядок операций не определен.</span><span class="sxs-lookup"><span data-stu-id="badc2-113">The order of operations is undefined.</span></span>

<span data-ttu-id="badc2-114">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="badc2-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="badc2-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="badc2-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="badc2-116">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="badc2-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="badc2-117">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="badc2-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




