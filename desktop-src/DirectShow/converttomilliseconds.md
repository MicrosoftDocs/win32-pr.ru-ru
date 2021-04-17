---
description: Функция Конверттомиллисекондс преобразует время ссылки в миллисекунды.
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: Функция Конверттомиллисекондс (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertToMilliseconds
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 066f50856824a9bc7b5bbb8c4918c7cbfe5b9da5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665495"
---
# <a name="converttomilliseconds-function"></a><span data-ttu-id="c2c53-103">Функция Конверттомиллисекондс</span><span class="sxs-lookup"><span data-stu-id="c2c53-103">ConvertToMilliseconds function</span></span>

<span data-ttu-id="c2c53-104">`ConvertToMilliseconds`Функция преобразует время ссылки в миллисекунды.</span><span class="sxs-lookup"><span data-stu-id="c2c53-104">The `ConvertToMilliseconds` function converts a reference time to milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2c53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2c53-105">Syntax</span></span>


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a><span data-ttu-id="c2c53-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2c53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2c53-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="c2c53-107">*RT* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c2c53-108">Время ссылки в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="c2c53-108">Reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2c53-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2c53-109">Return value</span></span>

<span data-ttu-id="c2c53-110">Возвращает время ссылки, преобразованное в миллисекунды.</span><span class="sxs-lookup"><span data-stu-id="c2c53-110">Returns the reference time converted to milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2c53-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c2c53-111">Requirements</span></span>



| <span data-ttu-id="c2c53-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c2c53-112">Requirement</span></span> | <span data-ttu-id="c2c53-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c2c53-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c53-114">Header</span><span class="sxs-lookup"><span data-stu-id="c2c53-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c2c53-115"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2c53-115"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c2c53-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2c53-116">Library</span></span><br/> | <dl> <span data-ttu-id="c2c53-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c2c53-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2c53-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2c53-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2c53-119">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="c2c53-119">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




