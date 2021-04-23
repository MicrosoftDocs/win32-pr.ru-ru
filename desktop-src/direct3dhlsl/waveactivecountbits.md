---
title: Функция Вавеактивекаунтбитс
description: Подсчитывает количество логических переменных, которые имеют значение true во всех активных желобах в текущей волновой области, и реплицирует результат во все желобы в волне.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- Функция Вавеактивекаунтбитс HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c4d2db55e9e3a0ad8f0a66be183d6e39d2a8b9c
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2020
ms.locfileid: "104339781"
---
# <a name="waveactivecountbits-function"></a><span data-ttu-id="9bafe-104">Функция Вавеактивекаунтбитс</span><span class="sxs-lookup"><span data-stu-id="9bafe-104">WaveActiveCountBits function</span></span>

<span data-ttu-id="9bafe-105">Подсчитывает количество логических переменных, которые имеют значение true во всех активных желобах в текущей волновой области, и реплицирует результат во все желобы в волне.</span><span class="sxs-lookup"><span data-stu-id="9bafe-105">Counts the number of boolean variables which evaluate to true across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bafe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bafe-106">Syntax</span></span>


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="9bafe-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bafe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bafe-108">*ббит*</span><span class="sxs-lookup"><span data-stu-id="9bafe-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="9bafe-109">Логические переменные для вычисления.</span><span class="sxs-lookup"><span data-stu-id="9bafe-109">The boolean variables to evaluate.</span></span> <span data-ttu-id="9bafe-110">Предоставление явного логического значения true Возвращает число активных дорожек.</span><span class="sxs-lookup"><span data-stu-id="9bafe-110">Providing an explicit true Boolean value returns the number of active lanes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bafe-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bafe-111">Return value</span></span>

<span data-ttu-id="9bafe-112">Число, которое вычисляется на значение true во всех активных желобах в текущей волны.</span><span class="sxs-lookup"><span data-stu-id="9bafe-112">The number of which evaluate to true across all active lanes in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bafe-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="9bafe-113">Remarks</span></span>

<span data-ttu-id="9bafe-114">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="9bafe-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="9bafe-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="9bafe-115">Examples</span></span>

<span data-ttu-id="9bafe-116">Это может быть реализовано более эффективно, чем полное Вавеактивесум, как описано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="9bafe-116">This can be implemented more efficiently than a full WaveActiveSum, as described in the following example:</span></span>

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a><span data-ttu-id="9bafe-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bafe-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bafe-118">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="9bafe-118">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="9bafe-119">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="9bafe-119">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




