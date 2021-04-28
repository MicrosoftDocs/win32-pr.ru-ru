---
description: Метод конструктора Камевент. Камевент.
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Конструктор Камевент. Камевент (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cdd37ba72d9467c16d46b2aec3ec40c206466eaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096538"
---
# <a name="cameventcamevent-constructor"></a><span data-ttu-id="855b3-103">Камевент. Камевент, конструктор</span><span class="sxs-lookup"><span data-stu-id="855b3-103">CAMEvent.CAMEvent constructor</span></span>

<span data-ttu-id="855b3-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="855b3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="855b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="855b3-105">Syntax</span></span>


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="855b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="855b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="855b3-107">*фмануалресет*</span><span class="sxs-lookup"><span data-stu-id="855b3-107">*fManualReset*</span></span> 
</dt> <dd>

<span data-ttu-id="855b3-108">Логическое значение, указывающее, является ли объект событием ручного сброса или событием автоматического сброса.</span><span class="sxs-lookup"><span data-stu-id="855b3-108">Boolean value that specifies whether the object is a manual-reset event or an auto-reset event.</span></span> <span data-ttu-id="855b3-109">Если **значение — true**, то объект является событием ручного сброса.</span><span class="sxs-lookup"><span data-stu-id="855b3-109">If **TRUE**, the object is a manual-reset event.</span></span> <span data-ttu-id="855b3-110">В противном случае это событие автоматического сброса.</span><span class="sxs-lookup"><span data-stu-id="855b3-110">Otherwise, it is an auto-reset event.</span></span>

</dd> <dt>

<span data-ttu-id="855b3-111">*фр*</span><span class="sxs-lookup"><span data-stu-id="855b3-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="855b3-112">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="855b3-112">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="855b3-113">Если конструктор завершается неудачно, этот параметр получает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="855b3-113">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="855b3-114">Если это происходит, объект находится в недопустимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="855b3-114">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="855b3-115">Для обеспечения обратной совместимости с более ранними версиями стрмбасе. lib этот параметр по умолчанию **имеет значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="855b3-115">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="855b3-116">Однако рекомендуется передать значение, отличное от **null** , чтобы вызывающий объект мог проверить состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="855b3-116">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="855b3-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="855b3-117">Remarks</span></span>

<span data-ttu-id="855b3-118">Событие начинается в несигнальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="855b3-118">The event begins in a nonsignaled state.</span></span>

<span data-ttu-id="855b3-119">При использовании события автоматического сброса метод [**камевент:: wait**](camevent-wait.md) сбрасывает событие в несигнальное состояние при возврате из метода.</span><span class="sxs-lookup"><span data-stu-id="855b3-119">With an auto-reset event, the [**CAMEvent::Wait**](camevent-wait.md) method resets the event to nonsignaled when the method returns.</span></span> <span data-ttu-id="855b3-120">С событием ручного сброса событие остается сигнальным до тех пор, пока не будет вызван метод [**камевент:: Reset**](camevent-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="855b3-120">With a manual-reset event, the event remains signaled until you call the [**CAMEvent::Reset**](camevent-reset.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="855b3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="855b3-121">Requirements</span></span>



| <span data-ttu-id="855b3-122">Требование</span><span class="sxs-lookup"><span data-stu-id="855b3-122">Requirement</span></span> | <span data-ttu-id="855b3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="855b3-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="855b3-124">Header</span><span class="sxs-lookup"><span data-stu-id="855b3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="855b3-125"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="855b3-125"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="855b3-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="855b3-126">Library</span></span><br/> | <dl> <span data-ttu-id="855b3-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="855b3-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="855b3-128">См. также</span><span class="sxs-lookup"><span data-stu-id="855b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="855b3-129">**Класс Камевент**</span><span class="sxs-lookup"><span data-stu-id="855b3-129">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




