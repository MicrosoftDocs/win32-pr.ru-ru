---
description: Ставит в очередь запрос на выполнение от рабочего потока.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Кмсгсреад. Путсреадмсг, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669079"
---
# <a name="cmsgthreadputthreadmsg-method"></a><span data-ttu-id="f53fe-103">Кмсгсреад. Путсреадмсг, метод</span><span class="sxs-lookup"><span data-stu-id="f53fe-103">CMsgThread.PutThreadMsg method</span></span>

<span data-ttu-id="f53fe-104">Ставит в очередь запрос на выполнение от рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="f53fe-104">Queues a request for execution by the worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="f53fe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f53fe-105">Syntax</span></span>


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="f53fe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f53fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f53fe-107">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="f53fe-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f53fe-108">Код запроса.</span><span class="sxs-lookup"><span data-stu-id="f53fe-108">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="f53fe-109">*двмсгфлагс*</span><span class="sxs-lookup"><span data-stu-id="f53fe-109">*dwMsgFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="f53fe-110">Необязательный параметр flags.</span><span class="sxs-lookup"><span data-stu-id="f53fe-110">Optional flags parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f53fe-111">*лпмсгпарам*</span><span class="sxs-lookup"><span data-stu-id="f53fe-111">*lpMsgParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f53fe-112">Необязательный указатель на блок данных, содержащий дополнительные параметры или возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="f53fe-112">Optional pointer to a data block containing additional parameters or return values.</span></span> <span data-ttu-id="f53fe-113">Должен быть статическим или выделенным в куче, а также не автоматическим.</span><span class="sxs-lookup"><span data-stu-id="f53fe-113">Must be statically or heap-allocated and not automatic.</span></span>

</dd> <dt>

<span data-ttu-id="f53fe-114">*певент*</span><span class="sxs-lookup"><span data-stu-id="f53fe-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="f53fe-115">Необязательный указатель на объект события, который должен быть сигнальным при завершении.</span><span class="sxs-lookup"><span data-stu-id="f53fe-115">Optional pointer to an event object to be signaled upon completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f53fe-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f53fe-116">Return value</span></span>

<span data-ttu-id="f53fe-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f53fe-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f53fe-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f53fe-118">Remarks</span></span>

<span data-ttu-id="f53fe-119">Эта функция-член ставит в очередь запрос на выполнение от рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="f53fe-119">This member function queues a request for execution by the worker thread.</span></span> <span data-ttu-id="f53fe-120">Параметры этой функции-члена будут помещены в очередь (в объекте [**КМСГ**](cmsg.md) ) и переданы в функцию-член [**Кмсгсреад:: среадмессажепрок**](cmsgthread-threadmessageproc.md) рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="f53fe-120">The parameters of this member function will be queued (in a [**CMsg**](cmsg.md) object) and passed to the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function of the worker thread.</span></span> <span data-ttu-id="f53fe-121">Эта функция – член возвращает сразу после постановки в очередь запроса и не ожидает выполнения запроса потоком.</span><span class="sxs-lookup"><span data-stu-id="f53fe-121">This member function returns immediately after queuing the request and does not wait for the thread to fulfill the request.</span></span> <span data-ttu-id="f53fe-122">Функция члена **кмсгсреад:: среадмессажепрок** производного класса определяет четыре параметра.</span><span class="sxs-lookup"><span data-stu-id="f53fe-122">The **CMsgThread::ThreadMessageProc** member function of the derived class defines the four parameters.</span></span>

<span data-ttu-id="f53fe-123">Эта функция-член использует безопасный список с многопоточностью, поэтому можно безопасно сделать несколько вызовов этой функции-члена из разных потоков.</span><span class="sxs-lookup"><span data-stu-id="f53fe-123">This member function uses a multithread safe list, so multiple calls to this member function from different threads can be made safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="f53fe-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f53fe-124">Requirements</span></span>



| <span data-ttu-id="f53fe-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f53fe-125">Requirement</span></span> | <span data-ttu-id="f53fe-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f53fe-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f53fe-127">Header</span><span class="sxs-lookup"><span data-stu-id="f53fe-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f53fe-128"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f53fe-128"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f53fe-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f53fe-129">Library</span></span><br/> | <dl> <span data-ttu-id="f53fe-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f53fe-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f53fe-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f53fe-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f53fe-132">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="f53fe-132">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




