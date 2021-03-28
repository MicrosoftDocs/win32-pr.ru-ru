---
title: Функция Вавеактивебаллот
description: Возвращает uint4, содержащий битовую маску вычисления логического выражения для всех активных желобов в текущем волне.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- Функция Вавеактивебаллот HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104533596"
---
# <a name="waveactiveballot-function"></a><span data-ttu-id="0935c-104">Функция Вавеактивебаллот</span><span class="sxs-lookup"><span data-stu-id="0935c-104">WaveActiveBallot function</span></span>

<span data-ttu-id="0935c-105">Возвращает uint4, содержащий битовую маску вычисления логического выражения для всех активных желобов в текущем волне.</span><span class="sxs-lookup"><span data-stu-id="0935c-105">Returns a uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> 

## <a name="syntax"></a><span data-ttu-id="0935c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0935c-106">Syntax</span></span>

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="0935c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0935c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0935c-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="0935c-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="0935c-109">Логическое выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="0935c-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0935c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0935c-110">Return value</span></span>

<span data-ttu-id="0935c-111">Объект uint4, содержащий битовую маску вычисления логического выражения для всех активных желобов в текущей волны.</span><span class="sxs-lookup"><span data-stu-id="0935c-111">A uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> <span data-ttu-id="0935c-112">Наименьший значащий бит соответствует полосе с нулевым индексом.</span><span class="sxs-lookup"><span data-stu-id="0935c-112">The least-significant bit corresponds to the lane with index zero.</span></span> <span data-ttu-id="0935c-113">Биты, соответствующие неактивным дорожкам, будут равны нулю.</span><span class="sxs-lookup"><span data-stu-id="0935c-113">The bits corresponding to inactive lanes will be zero.</span></span> <span data-ttu-id="0935c-114">Биты, которые больше или равны [**вавежетланекаунт**](wavegetlanecount.md) , будут равны нулю.</span><span class="sxs-lookup"><span data-stu-id="0935c-114">The bits that are greater than or equal to [**WaveGetLaneCount**](wavegetlanecount.md) will be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0935c-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="0935c-115">Remarks</span></span>

<span data-ttu-id="0935c-116">Разные GPU имеют разную ширину процессоров SIMD (число полос).</span><span class="sxs-lookup"><span data-stu-id="0935c-116">Different GPUs have different SIMD processor widths (lane counts).</span></span> <span data-ttu-id="0935c-117">Большая часть этих функций **вавекскскс** может работать на уровне абстракции, где скрыта ширина виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0935c-117">Most of these **WaveXXX** functions are able to operate at level of abstraction where SIMD machine width is concealed.</span></span> <span data-ttu-id="0935c-118">Чтобы обеспечить максимальную переносимость кода на графических процессорах, используйте встроенные функции, не зависящие от ширины компьютера.</span><span class="sxs-lookup"><span data-stu-id="0935c-118">To maximize portability of code across GPUs, use the intrinsics that don’t rely on machine width.</span></span> <span data-ttu-id="0935c-119">Например, вы можете использовать следующие службы.</span><span class="sxs-lookup"><span data-stu-id="0935c-119">For example, use:</span></span>

``` syntax
uint result = WaveActiveCountBits( bBit );
```

<span data-ttu-id="0935c-120">вместо следующего кода:</span><span class="sxs-lookup"><span data-stu-id="0935c-120">Instead of:</span></span>

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

<span data-ttu-id="0935c-121">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="0935c-121">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="0935c-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="0935c-122">Examples</span></span>

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a><span data-ttu-id="0935c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0935c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0935c-124">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="0935c-124">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="0935c-125">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="0935c-125">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




