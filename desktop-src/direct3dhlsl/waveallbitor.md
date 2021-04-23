---
title: Функция Вавеактивебитор
description: Возвращает побитовое или для всех значений выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- Функция Вавеактивебитор HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6870ac8406a581e358b00ef728562dc59118a933
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070855"
---
# <a name="waveactivebitor-function"></a><span data-ttu-id="55005-104">Функция Вавеактивебитор</span><span class="sxs-lookup"><span data-stu-id="55005-104">WaveActiveBitOr function</span></span>

<span data-ttu-id="55005-105">Возвращает побитовое или для всех значений выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.</span><span class="sxs-lookup"><span data-stu-id="55005-105">Returns the bitwise OR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="55005-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55005-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitOr(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="55005-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="55005-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55005-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="55005-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="55005-109">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="55005-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55005-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55005-110">Return value</span></span>

<span data-ttu-id="55005-111">Побитовое значение или.</span><span class="sxs-lookup"><span data-stu-id="55005-111">The bitwise OR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55005-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="55005-112">Remarks</span></span>

<span data-ttu-id="55005-113">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="55005-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="55005-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55005-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55005-115">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="55005-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="55005-116">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="55005-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




