---
title: Функция Вавеактивебитксор
description: Возвращает побитовое ИСКЛЮЧАЮЩее число всех значений выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- Функция Вавеактивебитксор HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e55ce8a43311f4f4c428e97bff1e107ab5c7038
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070853"
---
# <a name="waveactivebitxor-function"></a><span data-ttu-id="4c519-104">Функция Вавеактивебитксор</span><span class="sxs-lookup"><span data-stu-id="4c519-104">WaveActiveBitXor function</span></span>

<span data-ttu-id="4c519-105">Возвращает побитовое ИСКЛЮЧАЮЩее число всех значений выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.</span><span class="sxs-lookup"><span data-stu-id="4c519-105">Returns the bitwise XOR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c519-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c519-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="4c519-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c519-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c519-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="4c519-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="4c519-109">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="4c519-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c519-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c519-110">Return value</span></span>

<span data-ttu-id="4c519-111">Побитовое значение XOR.</span><span class="sxs-lookup"><span data-stu-id="4c519-111">The bitwise XOR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c519-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="4c519-112">Remarks</span></span>

<span data-ttu-id="4c519-113">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="4c519-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="4c519-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c519-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c519-115">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="4c519-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="4c519-116">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="4c519-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




