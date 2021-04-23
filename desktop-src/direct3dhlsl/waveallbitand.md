---
title: Функция Вавеактивебитанд
description: Возвращает побитовое и для всех значений выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.
ms.assetid: 602884CD-E656-4DEB-A30A-8A7D127A2217
keywords:
- Функция Вавеактивебитанд HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b6a3b0b097ea8737e07a91fcfc6553f22b828f1
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070861"
---
# <a name="waveactivebitand-function"></a><span data-ttu-id="ce578-104">Функция Вавеактивебитанд</span><span class="sxs-lookup"><span data-stu-id="ce578-104">WaveActiveBitAnd function</span></span>

<span data-ttu-id="ce578-105">Возвращает побитовое и для всех значений выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.</span><span class="sxs-lookup"><span data-stu-id="ce578-105">Returns the bitwise AND of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce578-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce578-106">Syntax</span></span>


``` syntax
<int_type> WaveActiveBitAnd(
   <int_type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="ce578-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce578-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce578-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="ce578-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="ce578-109">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="ce578-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce578-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce578-110">Return value</span></span>

<span data-ttu-id="ce578-111">Побитовое значение и.</span><span class="sxs-lookup"><span data-stu-id="ce578-111">The bitwise AND value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce578-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce578-112">Remarks</span></span>

<span data-ttu-id="ce578-113">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="ce578-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="ce578-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce578-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce578-115">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="ce578-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="ce578-116">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="ce578-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




