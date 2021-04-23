---
title: Функция Вавеактивеаллтруе
description: Возвращает значение true, если выражение имеет значение true во всех активных желобах в текущем Wave.
ms.assetid: C4EC5A02-6070-4FF4-B855-F597FFFE66F0
keywords:
- Функция Вавеактивеаллтруе HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a26e0ce757257d6fdd8296239dcf086bff5f1666
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488529"
---
# <a name="waveactivealltrue-function"></a><span data-ttu-id="567f1-104">Функция Вавеактивеаллтруе</span><span class="sxs-lookup"><span data-stu-id="567f1-104">WaveActiveAllTrue function</span></span>

<span data-ttu-id="567f1-105">Возвращает значение true, если выражение имеет значение true во всех активных желобах в текущем Wave.</span><span class="sxs-lookup"><span data-stu-id="567f1-105">Returns true if the expression is true in all active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="567f1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="567f1-106">Syntax</span></span>

``` syntax
bool WaveActiveAllTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="567f1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="567f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="567f1-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="567f1-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="567f1-109">Логическое выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="567f1-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="567f1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="567f1-110">Return value</span></span>

<span data-ttu-id="567f1-111">Значение true, если выражение имеет значение true во всех дорожках.</span><span class="sxs-lookup"><span data-stu-id="567f1-111">True if the expression is true in all lanes.</span></span>

## <a name="remarks"></a><span data-ttu-id="567f1-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="567f1-112">Remarks</span></span>

<span data-ttu-id="567f1-113">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="567f1-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="567f1-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="567f1-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="567f1-115">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="567f1-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="567f1-116">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="567f1-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




