---
description: Функция Int64x32Div32 реализует формулу ((a \* b) + Rnd)/c, где a — это 64-разрядное значение, а b, c, а RND — 32-разрядные значения.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Функция Int64x32Div32 (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679778"
---
# <a name="int64x32div32-function"></a><span data-ttu-id="e533e-103">Функция Int64x32Div32</span><span class="sxs-lookup"><span data-stu-id="e533e-103">Int64x32Div32 function</span></span>

<span data-ttu-id="e533e-104">`Int64x32Div32`Функция реализует формулу, `((a*b)+rnd)/c` где *a* — это 64-разрядное значение, а *b*, *c*, а *Rnd* — 32-разрядные значения.</span><span class="sxs-lookup"><span data-stu-id="e533e-104">The `Int64x32Div32` function implements the formula `((a*b)+rnd)/c` where *a* is a 64-bit value and *b*, *c*, and *rnd* are 32-bit values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e533e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e533e-105">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
);
```



## <a name="parameters"></a><span data-ttu-id="e533e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e533e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e533e-107">*конкретного*</span><span class="sxs-lookup"><span data-stu-id="e533e-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="e533e-108">Множимое.</span><span class="sxs-lookup"><span data-stu-id="e533e-108">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="e533e-109">*b*</span><span class="sxs-lookup"><span data-stu-id="e533e-109">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="e533e-110">Множитель.</span><span class="sxs-lookup"><span data-stu-id="e533e-110">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="e533e-111">*c*</span><span class="sxs-lookup"><span data-stu-id="e533e-111">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="e533e-112">Равн.</span><span class="sxs-lookup"><span data-stu-id="e533e-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="e533e-113">*Функция*</span><span class="sxs-lookup"><span data-stu-id="e533e-113">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e533e-114">Коэффициент округления.</span><span class="sxs-lookup"><span data-stu-id="e533e-114">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e533e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e533e-115">Return value</span></span>

<span data-ttu-id="e533e-116">Возвращает либо `(a * b + rnd)/c` вычисление, либо одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e533e-116">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="e533e-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e533e-117">Return code</span></span>                                                                                       | <span data-ttu-id="e533e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="e533e-118">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e533e-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="e533e-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="e533e-120">Произошло переполнение, так как результат слишком велик (положительный).</span><span class="sxs-lookup"><span data-stu-id="e533e-120">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="e533e-121"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="e533e-121"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="e533e-122">Произошло переполнение, так как результат слишком большой (отрицательный).</span><span class="sxs-lookup"><span data-stu-id="e533e-122">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e533e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e533e-123">Remarks</span></span>

<span data-ttu-id="e533e-124">Округление на деление в сторону нуля.</span><span class="sxs-lookup"><span data-stu-id="e533e-124">Rounding on the division is toward zero.</span></span> <span data-ttu-id="e533e-125">Деление на ноль считается условием переполнения.</span><span class="sxs-lookup"><span data-stu-id="e533e-125">Division by zero is counted as an overflow condition.</span></span>

<span data-ttu-id="e533e-126">Метки времени и время поиска представляют собой 64-битные значения, поэтому эта функция полезна для выполнения преобразований в 32-разрядных системах.</span><span class="sxs-lookup"><span data-stu-id="e533e-126">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="e533e-127">Например, в MPEG-1 ссылка на системный таймер составляет 90 кГц или 90 000 тактов в секунду.</span><span class="sxs-lookup"><span data-stu-id="e533e-127">For example, in MPEG-1 the system clock reference is 90-kHz, or 90,000 ticks per second.</span></span> <span data-ttu-id="e533e-128">Формула для преобразования этой формулы в ссылочное время (100-наносекундных единиц) —</span><span class="sxs-lookup"><span data-stu-id="e533e-128">The formula to convert this to reference time (100-nanosecond units) is</span></span>


```C++
(timestamp * 1000) / 9
```



<span data-ttu-id="e533e-129">который можно вычислить как `Int64x32Div32(timestamp, 1000, 9, 0)` .</span><span class="sxs-lookup"><span data-stu-id="e533e-129">which can be calculated as `Int64x32Div32(timestamp, 1000, 9, 0)`.</span></span> <span data-ttu-id="e533e-130">Используйте параметр *Rnd* в качестве фактора округления.</span><span class="sxs-lookup"><span data-stu-id="e533e-130">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="e533e-131">Требования</span><span class="sxs-lookup"><span data-stu-id="e533e-131">Requirements</span></span>



| <span data-ttu-id="e533e-132">Требование</span><span class="sxs-lookup"><span data-stu-id="e533e-132">Requirement</span></span> | <span data-ttu-id="e533e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e533e-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e533e-134">Header</span><span class="sxs-lookup"><span data-stu-id="e533e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="e533e-135"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e533e-135"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e533e-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e533e-136">Library</span></span><br/> | <dl> <span data-ttu-id="e533e-137"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e533e-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e533e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e533e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e533e-139">Различные вспомогательные функции</span><span class="sxs-lookup"><span data-stu-id="e533e-139">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="e533e-140">**ллмулдив**</span><span class="sxs-lookup"><span data-stu-id="e533e-140">**llMulDiv**</span></span>](llmuldiv.md)
</dt> </dl>

 

 




