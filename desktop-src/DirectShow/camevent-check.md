---
description: Метод check проверяет, задано ли событие, без блокировки.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: Метод Камевент. Check (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665113"
---
# <a name="cameventcheck-method"></a><span data-ttu-id="48fef-103">Камевент. Check, метод</span><span class="sxs-lookup"><span data-stu-id="48fef-103">CAMEvent.Check method</span></span>

<span data-ttu-id="48fef-104">`Check`Метод проверяет, задано ли событие, без блокировки.</span><span class="sxs-lookup"><span data-stu-id="48fef-104">The `Check` method checks whether the event is set, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="48fef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48fef-105">Syntax</span></span>


```C++
BOOL Check();
```



## <a name="parameters"></a><span data-ttu-id="48fef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="48fef-106">Parameters</span></span>

<span data-ttu-id="48fef-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="48fef-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="48fef-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48fef-108">Remarks</span></span>

<span data-ttu-id="48fef-109">Возвращает **значение true** , если событие задано, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="48fef-109">Returns **TRUE** if the event is set, or **FALSE** otherwise.</span></span> <span data-ttu-id="48fef-110">Этот метод вызывает метод [**камевент:: wait**](camevent-wait.md) с нулевым временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="48fef-110">This method calls the [**CAMEvent::Wait**](camevent-wait.md) method with a time-out of zero.</span></span> <span data-ttu-id="48fef-111">Если объект является событием автоматического сброса, этот метод сбрасывает событие.</span><span class="sxs-lookup"><span data-stu-id="48fef-111">If the object is an auto-reset event, this method resets the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="48fef-112">Требования</span><span class="sxs-lookup"><span data-stu-id="48fef-112">Requirements</span></span>



| <span data-ttu-id="48fef-113">Требование</span><span class="sxs-lookup"><span data-stu-id="48fef-113">Requirement</span></span> | <span data-ttu-id="48fef-114">Значение</span><span class="sxs-lookup"><span data-stu-id="48fef-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48fef-115">Header</span><span class="sxs-lookup"><span data-stu-id="48fef-115">Header</span></span><br/>  | <dl> <span data-ttu-id="48fef-116"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48fef-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="48fef-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="48fef-117">Library</span></span><br/> | <dl> <span data-ttu-id="48fef-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="48fef-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48fef-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48fef-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48fef-120">**Класс Камевент**</span><span class="sxs-lookup"><span data-stu-id="48fef-120">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




