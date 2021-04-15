---
description: 'Метод Жетрекуессандле извлекает дескриптор события, сигнального методом Камсреад:: Каллворкер.'
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Камсреад. Жетрекуессандле, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 051a6a3e3daed1dae6df3bdbb42e36f07b852d85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689154"
---
# <a name="camthreadgetrequesthandle-method"></a><span data-ttu-id="86676-103">Камсреад. Жетрекуессандле, метод</span><span class="sxs-lookup"><span data-stu-id="86676-103">CAMThread.GetRequestHandle method</span></span>

<span data-ttu-id="86676-104">`GetRequestHandle`Метод получает дескриптор события, сигнальное методом [**камсреад:: каллворкер**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="86676-104">The `GetRequestHandle` method retrieves a handle to the event that is signaled by the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86676-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86676-105">Syntax</span></span>


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a><span data-ttu-id="86676-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86676-106">Parameters</span></span>

<span data-ttu-id="86676-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="86676-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86676-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86676-108">Return value</span></span>

<span data-ttu-id="86676-109">Возвращает маркер события.</span><span class="sxs-lookup"><span data-stu-id="86676-109">Returns an event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="86676-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86676-110">Remarks</span></span>

<span data-ttu-id="86676-111">Класс Камевент сохраняет закрытое событие ручного сброса, которое задается Каллворкер и сбрасывается методом [**камсреад:: Reply**](camthread-reply.md) .</span><span class="sxs-lookup"><span data-stu-id="86676-111">The CAMEvent class keeps a private manual-reset event, which is set by CallWorker and reset by the [**CAMThread::Reply**](camthread-reply.md) method.</span></span>

<span data-ttu-id="86676-112">При вызове функции, такой как WaitForMultipleObjects, используйте Жетрекуессандле для получения маркера события.</span><span class="sxs-lookup"><span data-stu-id="86676-112">If you call a function such as WaitForMultipleObjects, use GetRequestHandle to retrieve the event handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="86676-113">Требования</span><span class="sxs-lookup"><span data-stu-id="86676-113">Requirements</span></span>



| <span data-ttu-id="86676-114">Требование</span><span class="sxs-lookup"><span data-stu-id="86676-114">Requirement</span></span> | <span data-ttu-id="86676-115">Значение</span><span class="sxs-lookup"><span data-stu-id="86676-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86676-116">Header</span><span class="sxs-lookup"><span data-stu-id="86676-116">Header</span></span><br/>  | <dl> <span data-ttu-id="86676-117"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86676-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="86676-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="86676-118">Library</span></span><br/> | <dl> <span data-ttu-id="86676-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="86676-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86676-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86676-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86676-121">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="86676-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




