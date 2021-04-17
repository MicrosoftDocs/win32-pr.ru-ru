---
description: Метод Чекктиме определяет, вызвано ли указанное время.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Ккмдкуеуе. Чекктиме, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680014"
---
# <a name="ccmdqueuechecktime-method"></a><span data-ttu-id="c49f4-103">Ккмдкуеуе. Чекктиме, метод</span><span class="sxs-lookup"><span data-stu-id="c49f4-103">CCmdQueue.CheckTime method</span></span>

<span data-ttu-id="c49f4-104">`CheckTime`Метод определяет, вызвано ли указанное время.</span><span class="sxs-lookup"><span data-stu-id="c49f4-104">The `CheckTime` method determines if a specified time is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="c49f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c49f4-105">Syntax</span></span>


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a><span data-ttu-id="c49f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c49f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c49f4-107">*time*</span><span class="sxs-lookup"><span data-stu-id="c49f4-107">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="c49f4-108">Время для проверки.</span><span class="sxs-lookup"><span data-stu-id="c49f4-108">Time to check.</span></span>

</dd> <dt>

<span data-ttu-id="c49f4-109">*бстреам*</span><span class="sxs-lookup"><span data-stu-id="c49f4-109">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="c49f4-110">**Значение true** , если параметр *времени* является значением потокового времени; Значение **false** , если *время* является значением времени презентации.</span><span class="sxs-lookup"><span data-stu-id="c49f4-110">**TRUE** if the *time* parameter is a stream-time value; **FALSE** if *time* is a presentation-time value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c49f4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c49f4-111">Return value</span></span>

<span data-ttu-id="c49f4-112">Возвращает **значение true** , если указанное время еще не прошло.</span><span class="sxs-lookup"><span data-stu-id="c49f4-112">Returns **TRUE** if the specified time has not yet passed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c49f4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c49f4-113">Requirements</span></span>



| <span data-ttu-id="c49f4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c49f4-114">Requirement</span></span> | <span data-ttu-id="c49f4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c49f4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c49f4-116">Header</span><span class="sxs-lookup"><span data-stu-id="c49f4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c49f4-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c49f4-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c49f4-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c49f4-118">Library</span></span><br/> | <dl> <span data-ttu-id="c49f4-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c49f4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c49f4-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c49f4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c49f4-121">**Класс Ккмдкуеуе**</span><span class="sxs-lookup"><span data-stu-id="c49f4-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




