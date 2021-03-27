---
title: Функция Вавеактивеанитруе
description: Возвращает значение true, если выражение имеет значение true в любом из активных желобов в текущей волны.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- Функция Вавеактивеанитруе HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104997174"
---
# <a name="waveactiveanytrue-function"></a><span data-ttu-id="aeb76-104">Функция Вавеактивеанитруе</span><span class="sxs-lookup"><span data-stu-id="aeb76-104">WaveActiveAnyTrue function</span></span>

<span data-ttu-id="aeb76-105">Возвращает значение true, если выражение имеет значение true в любом из активных желобов в текущей волны.</span><span class="sxs-lookup"><span data-stu-id="aeb76-105">Returns true if the expression is true in any of the active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeb76-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aeb76-106">Syntax</span></span>

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="aeb76-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aeb76-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb76-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="aeb76-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb76-109">Логическое выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="aeb76-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb76-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aeb76-110">Return value</span></span>

<span data-ttu-id="aeb76-111">Значение true, если выражение имеет значение true в любой полосе.</span><span class="sxs-lookup"><span data-stu-id="aeb76-111">True if the expression is true in any lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeb76-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="aeb76-112">Remarks</span></span>

<span data-ttu-id="aeb76-113">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="aeb76-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="aeb76-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aeb76-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb76-115">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="aeb76-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="aeb76-116">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="aeb76-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




