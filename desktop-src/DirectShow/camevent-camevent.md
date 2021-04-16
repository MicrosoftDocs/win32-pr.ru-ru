---
description: Метод конструктора.
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
ms.openlocfilehash: a01d9d1f592675f58d19e81b800c966dddaca1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656884"
---
# <a name="cameventcamevent-constructor"></a><span data-ttu-id="b4cc0-103">Камевент. Камевент, конструктор</span><span class="sxs-lookup"><span data-stu-id="b4cc0-103">CAMEvent.CAMEvent constructor</span></span>

<span data-ttu-id="b4cc0-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="b4cc0-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4cc0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4cc0-105">Syntax</span></span>


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="b4cc0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4cc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4cc0-107">*фмануалресет*</span><span class="sxs-lookup"><span data-stu-id="b4cc0-107">*fManualReset*</span></span> 
</dt> <dd>

<span data-ttu-id="b4cc0-108">Логическое значение, указывающее, является ли объект событием ручного сброса или событием автоматического сброса.</span><span class="sxs-lookup"><span data-stu-id="b4cc0-108">Boolean value that specifies whether the object is a manual-reset event or an auto-reset event.</span></span> <span data-ttu-id="b4cc0-109">Если **значение — true**, то объект является событием ручного сброса.</span><span class="sxs-lookup"><span data-stu-id="b4cc0-109">If **TRUE**, the object is a manual-reset event.</span></span> <span data-ttu-id="b4cc0-110">В противном случае это событие автоматического сброса.</span><span class="sxs-lookup"><span data-stu-id="b4cc0-110">Otherwise, it is an auto-reset event.</span></span>

</dd> <dt>

<span data-ttu-id="b4cc0-111">*фр*</span><span class="sxs-lookup"><span data-stu-id="b4cc0-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b4cc0-112">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4cc0-112">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="b4cc0-113">Если конструктор завершается неудачно, этот параметр получает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b4cc0-113">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="b4cc0-114">Если это происходит, объект находится в недопустимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="b4cc0-114">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="b4cc0-115">Для обеспечения обратной совместимости с более ранними версиями стрмбасе. lib этот параметр по умолчанию **имеет значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b4cc0-115">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="b4cc0-116">Однако рекомендуется передать значение, отличное от **null** , чтобы вызывающий объект мог проверить состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b4cc0-116">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4cc0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4cc0-117">Remarks</span></span>

<span data-ttu-id="b4cc0-118">Событие начинается в несигнальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b4cc0-118">The event begins in a nonsignaled state.</span></span>

<span data-ttu-id="b4cc0-119">При использовании события автоматического сброса метод [**камевент:: wait**](camevent-wait.md) сбрасывает событие в несигнальное состояние при возврате из метода.</span><span class="sxs-lookup"><span data-stu-id="b4cc0-119">With an auto-reset event, the [**CAMEvent::Wait**](camevent-wait.md) method resets the event to nonsignaled when the method returns.</span></span> <span data-ttu-id="b4cc0-120">С событием ручного сброса событие остается сигнальным до тех пор, пока не будет вызван метод [**камевент:: Reset**](camevent-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="b4cc0-120">With a manual-reset event, the event remains signaled until you call the [**CAMEvent::Reset**](camevent-reset.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4cc0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b4cc0-121">Requirements</span></span>



| <span data-ttu-id="b4cc0-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b4cc0-122">Requirement</span></span> | <span data-ttu-id="b4cc0-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b4cc0-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4cc0-124">Header</span><span class="sxs-lookup"><span data-stu-id="b4cc0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b4cc0-125"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4cc0-125"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b4cc0-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4cc0-126">Library</span></span><br/> | <dl> <span data-ttu-id="b4cc0-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b4cc0-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4cc0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4cc0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4cc0-129">**Класс Камевент**</span><span class="sxs-lookup"><span data-stu-id="b4cc0-129">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




