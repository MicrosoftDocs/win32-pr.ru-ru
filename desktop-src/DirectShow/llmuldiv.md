---
description: Функция Ллмулдив реализует формулу ((a \* b) + Rnd)/c, где каждый термин является 64-битным значением.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: Функция Ллмулдив (Вксутил. h)
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
ms.openlocfilehash: e45d22eec1536517bd2b57d875dd596e4a1e28db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665493"
---
# <a name="llmuldiv-function"></a><span data-ttu-id="5d912-103">Функция Ллмулдив</span><span class="sxs-lookup"><span data-stu-id="5d912-103">llMulDiv function</span></span>

<span data-ttu-id="5d912-104">`llMulDiv`Функция реализует формулу, `((a*b)+rnd)/c` в которой каждый термин является 64-битным значением.</span><span class="sxs-lookup"><span data-stu-id="5d912-104">The `llMulDiv` function implements the formula `((a*b)+rnd)/c` where each term is a 64-bit value.</span></span>

<span data-ttu-id="5d912-105">Метки времени и время поиска представляют собой 64-битные значения, поэтому эта функция полезна для выполнения преобразований в 32-разрядных системах.</span><span class="sxs-lookup"><span data-stu-id="5d912-105">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="5d912-106">Например, формула для байт в секунду —</span><span class="sxs-lookup"><span data-stu-id="5d912-106">For example, the formula for bytes-per-second is</span></span>


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



<span data-ttu-id="5d912-107">который можно вычислить как `llMulDiv(nBytes, rtTime, 10000000, 0)` .</span><span class="sxs-lookup"><span data-stu-id="5d912-107">which can be calculated as `llMulDiv(nBytes, rtTime, 10000000, 0)`.</span></span> <span data-ttu-id="5d912-108">Используйте параметр *Rnd* в качестве фактора округления.</span><span class="sxs-lookup"><span data-stu-id="5d912-108">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d912-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d912-109">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a><span data-ttu-id="5d912-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d912-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d912-111">*конкретного*</span><span class="sxs-lookup"><span data-stu-id="5d912-111">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="5d912-112">Множимое.</span><span class="sxs-lookup"><span data-stu-id="5d912-112">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="5d912-113">*b*</span><span class="sxs-lookup"><span data-stu-id="5d912-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="5d912-114">Множитель.</span><span class="sxs-lookup"><span data-stu-id="5d912-114">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="5d912-115">*c*</span><span class="sxs-lookup"><span data-stu-id="5d912-115">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="5d912-116">Равн.</span><span class="sxs-lookup"><span data-stu-id="5d912-116">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="5d912-117">*Функция*</span><span class="sxs-lookup"><span data-stu-id="5d912-117">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5d912-118">Коэффициент округления.</span><span class="sxs-lookup"><span data-stu-id="5d912-118">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d912-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d912-119">Return value</span></span>

<span data-ttu-id="5d912-120">Возвращает либо `(a * b + rnd)/c` вычисление, либо одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5d912-120">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="5d912-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5d912-121">Return code</span></span>                                                                                       | <span data-ttu-id="5d912-122">Описание</span><span class="sxs-lookup"><span data-stu-id="5d912-122">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d912-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="5d912-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="5d912-124">Произошло переполнение, так как результат слишком велик (положительный).</span><span class="sxs-lookup"><span data-stu-id="5d912-124">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="5d912-125"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="5d912-125"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="5d912-126">Произошло переполнение, так как результат слишком большой (отрицательный).</span><span class="sxs-lookup"><span data-stu-id="5d912-126">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5d912-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d912-127">Remarks</span></span>

<span data-ttu-id="5d912-128">Округление на деление в сторону нуля.</span><span class="sxs-lookup"><span data-stu-id="5d912-128">Rounding on the division is toward zero.</span></span> <span data-ttu-id="5d912-129">Деление на ноль считается условием переполнения.</span><span class="sxs-lookup"><span data-stu-id="5d912-129">Division by zero is counted as an overflow condition.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d912-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5d912-130">Requirements</span></span>



| <span data-ttu-id="5d912-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5d912-131">Requirement</span></span> | <span data-ttu-id="5d912-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5d912-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d912-133">Header</span><span class="sxs-lookup"><span data-stu-id="5d912-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5d912-134"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d912-134"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5d912-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d912-135">Library</span></span><br/> | <dl> <span data-ttu-id="5d912-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5d912-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d912-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d912-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d912-138">Различные вспомогательные функции</span><span class="sxs-lookup"><span data-stu-id="5d912-138">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="5d912-139">**Int64x32Div32**</span><span class="sxs-lookup"><span data-stu-id="5d912-139">**Int64x32Div32**</span></span>](int64x32div32.md)
</dt> </dl>

 

 




