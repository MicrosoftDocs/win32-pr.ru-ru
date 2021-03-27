---
title: Функция Вавеактивемин
description: Возвращает минимальное значение выражения для всех активных желобов в текущем звуковом процессе реплицирует его обратно во все активные дорожки.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- Функция Вавеактивемин HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070854"
---
# <a name="waveactivemin-function"></a><span data-ttu-id="98ccd-104">Функция Вавеактивемин</span><span class="sxs-lookup"><span data-stu-id="98ccd-104">WaveActiveMin function</span></span>

<span data-ttu-id="98ccd-105">Возвращает минимальное значение выражения для всех активных желобов в текущем звуковом процессе реплицирует его обратно во все активные дорожки.</span><span class="sxs-lookup"><span data-stu-id="98ccd-105">Returns the minimum value of the expression across all active lanes in the current wave replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="98ccd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98ccd-106">Syntax</span></span>

``` syntax
<type> WaveActiveMin(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="98ccd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ccd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98ccd-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="98ccd-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="98ccd-109">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="98ccd-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98ccd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98ccd-110">Return value</span></span>

<span data-ttu-id="98ccd-111">Минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="98ccd-111">The minimum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98ccd-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="98ccd-112">Remarks</span></span>

<span data-ttu-id="98ccd-113">Порядок операций не определен.</span><span class="sxs-lookup"><span data-stu-id="98ccd-113">The order of operations is undefined.</span></span>

<span data-ttu-id="98ccd-114">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="98ccd-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="98ccd-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="98ccd-115">Examples</span></span>

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a><span data-ttu-id="98ccd-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98ccd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ccd-117">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="98ccd-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="98ccd-118">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="98ccd-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




