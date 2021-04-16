---
title: Функция Вавеактивемакс
description: Возвращает максимальное значение выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- Функция Вавеактивемакс HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2020
ms.locfileid: "104414260"
---
# <a name="waveactivemax-function"></a><span data-ttu-id="a8348-104">Функция Вавеактивемакс</span><span class="sxs-lookup"><span data-stu-id="a8348-104">WaveActiveMax function</span></span>

<span data-ttu-id="a8348-105">Возвращает максимальное значение выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.</span><span class="sxs-lookup"><span data-stu-id="a8348-105">Returns the maximum value of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8348-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8348-106">Syntax</span></span>

``` syntax
<type> WaveActiveMax(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="a8348-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8348-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8348-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="a8348-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="a8348-109">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="a8348-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8348-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8348-110">Return value</span></span>

<span data-ttu-id="a8348-111">Максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="a8348-111">The maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8348-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8348-112">Remarks</span></span>

<span data-ttu-id="a8348-113">Порядок операций не определен.</span><span class="sxs-lookup"><span data-stu-id="a8348-113">The order of operations is undefined.</span></span>

<span data-ttu-id="a8348-114">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="a8348-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="a8348-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="a8348-115">Examples</span></span>

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a><span data-ttu-id="a8348-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8348-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8348-117">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="a8348-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="a8348-118">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="a8348-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




