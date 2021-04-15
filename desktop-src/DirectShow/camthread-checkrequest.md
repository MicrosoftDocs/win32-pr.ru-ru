---
description: Метод Чеккрекуест проверяет наличие запроса без блокировки.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Камсреад. Чеккрекуест, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688866"
---
# <a name="camthreadcheckrequest-method"></a><span data-ttu-id="e0494-103">Камсреад. Чеккрекуест, метод</span><span class="sxs-lookup"><span data-stu-id="e0494-103">CAMThread.CheckRequest method</span></span>

<span data-ttu-id="e0494-104">`CheckRequest`Метод проверяет наличие запроса без блокировки.</span><span class="sxs-lookup"><span data-stu-id="e0494-104">The `CheckRequest` method checks if there is a request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0494-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0494-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a><span data-ttu-id="e0494-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0494-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0494-107">*ппарам*</span><span class="sxs-lookup"><span data-stu-id="e0494-107">*pParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0494-108">Указатель на переменную, которая получает значение, переданное в последнем вызове метода [**камсреад:: каллворкер**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="e0494-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0494-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0494-109">Return value</span></span>

<span data-ttu-id="e0494-110">Возвращает **значение true** , если имеется ожидающий запрос, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e0494-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0494-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0494-111">Remarks</span></span>

<span data-ttu-id="e0494-112">Этот метод является неблокирующей версией метода [**камсреад::-request**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="e0494-112">This method is a non-blocking version of the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span>

<span data-ttu-id="e0494-113">Если другой поток ожидает вызова Каллворкер, этот метод извлекает параметр запроса и возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="e0494-113">If another thread is waiting on a call to CallWorker, this method retrieves the request parameter and returns **TRUE**.</span></span> <span data-ttu-id="e0494-114">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e0494-114">Otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="e0494-115">Если метод возвращает **значение true**, вызовите метод [**Камсреад:: Reply**](camthread-reply.md) , чтобы освободить поток запроса.</span><span class="sxs-lookup"><span data-stu-id="e0494-115">If the method returns **TRUE**, call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0494-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e0494-116">Requirements</span></span>



| <span data-ttu-id="e0494-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e0494-117">Requirement</span></span> | <span data-ttu-id="e0494-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e0494-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0494-119">Header</span><span class="sxs-lookup"><span data-stu-id="e0494-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e0494-120"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0494-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e0494-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e0494-121">Library</span></span><br/> | <dl> <span data-ttu-id="e0494-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e0494-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0494-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0494-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0494-124">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="e0494-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




