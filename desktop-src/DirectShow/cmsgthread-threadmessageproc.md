---
description: Обрабатывает запросы. Это Чистая виртуальная функция-член.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Кмсгсреад. Среадмессажепрок, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668891"
---
# <a name="cmsgthreadthreadmessageproc-method"></a><span data-ttu-id="739a8-104">Кмсгсреад. Среадмессажепрок, метод</span><span class="sxs-lookup"><span data-stu-id="739a8-104">CMsgThread.ThreadMessageProc method</span></span>

<span data-ttu-id="739a8-105">Обрабатывает запросы.</span><span class="sxs-lookup"><span data-stu-id="739a8-105">Processes requests.</span></span> <span data-ttu-id="739a8-106">Это Чистая виртуальная функция-член.</span><span class="sxs-lookup"><span data-stu-id="739a8-106">This is a pure virtual member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="739a8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="739a8-107">Syntax</span></span>


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="739a8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="739a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="739a8-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="739a8-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="739a8-110">Код запроса.</span><span class="sxs-lookup"><span data-stu-id="739a8-110">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="739a8-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="739a8-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="739a8-112">Необязательный параметр флага для запроса.</span><span class="sxs-lookup"><span data-stu-id="739a8-112">Optional flag parameter to request.</span></span>

</dd> <dt>

<span data-ttu-id="739a8-113">*лппарам*</span><span class="sxs-lookup"><span data-stu-id="739a8-113">*lpParam*</span></span> 
</dt> <dd>

<span data-ttu-id="739a8-114">Необязательный указатель на дополнительные данные или блок возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="739a8-114">Optional pointer to extra data or a return data block.</span></span>

</dd> <dt>

<span data-ttu-id="739a8-115">*певент*</span><span class="sxs-lookup"><span data-stu-id="739a8-115">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="739a8-116">Необязательный указатель на объект события.</span><span class="sxs-lookup"><span data-stu-id="739a8-116">Optional pointer to an event object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="739a8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="739a8-117">Return value</span></span>

<span data-ttu-id="739a8-118">Любые ненулевые возвращаемые значения приводят к выходу потока.</span><span class="sxs-lookup"><span data-stu-id="739a8-118">Any nonzero return causes the thread to exit.</span></span> <span data-ttu-id="739a8-119">Возвращает нуль, если только запрос на выход не был обработан в последнее время.</span><span class="sxs-lookup"><span data-stu-id="739a8-119">Returns zero unless an exit request has been processed recently.</span></span>

## <a name="remarks"></a><span data-ttu-id="739a8-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="739a8-120">Remarks</span></span>

<span data-ttu-id="739a8-121">Эта Чистая виртуальная функция должна быть переопределена в производном классе.</span><span class="sxs-lookup"><span data-stu-id="739a8-121">This pure virtual function must be overridden in your derived class.</span></span> <span data-ttu-id="739a8-122">Он будет вызываться один раз для каждого запроса, помещенного в очередь с помощью вызова функции-члена [**кмсгсреад::P утсреадмсг**](cmsgthread-putthreadmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="739a8-122">It will be called once for each request queued by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function.</span></span>

<span data-ttu-id="739a8-123">Функция члена определяет четыре параметра.</span><span class="sxs-lookup"><span data-stu-id="739a8-123">The member function defines the four parameters.</span></span> <span data-ttu-id="739a8-124">Как правило, для указания запроса используется параметр *uiacp* , а остальные три параметра будут дополнительными.</span><span class="sxs-lookup"><span data-stu-id="739a8-124">Typically, use the *uMsg* parameter to indicate the request, and the other three parameters will be optional additional parameters.</span></span> <span data-ttu-id="739a8-125">Вызывающее приложение может предоставить указатель на объект [**камевент**](camevent.md) в параметре *певент* , если это требуется приложению.</span><span class="sxs-lookup"><span data-stu-id="739a8-125">The calling application can supply a pointer to a [**CAMEvent**](camevent.md) object in the *pEvent* parameter if your application requires it.</span></span> <span data-ttu-id="739a8-126">Это событие необходимо задать после обработки события с помощью такого выражения, как:</span><span class="sxs-lookup"><span data-stu-id="739a8-126">You must set this event after processing the event by using an expression such as:</span></span>


```C++
pEvent->SetEvent
```



<span data-ttu-id="739a8-127">Один код запроса необходимо отложить, чтобы сообщить рабочему потоку о выходе из него.</span><span class="sxs-lookup"><span data-stu-id="739a8-127">One request code must be set aside to tell the worker thread to exit.</span></span> <span data-ttu-id="739a8-128">После получения этого запроса возвращается 1 из этой функции члена.</span><span class="sxs-lookup"><span data-stu-id="739a8-128">Upon receiving this request, return 1 from this member function.</span></span> <span data-ttu-id="739a8-129">Возвращает 0, если не нужно, чтобы рабочий поток завершил работу.</span><span class="sxs-lookup"><span data-stu-id="739a8-129">Return 0 if you do not want the worker thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="739a8-130">Требования</span><span class="sxs-lookup"><span data-stu-id="739a8-130">Requirements</span></span>



| <span data-ttu-id="739a8-131">Требование</span><span class="sxs-lookup"><span data-stu-id="739a8-131">Requirement</span></span> | <span data-ttu-id="739a8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="739a8-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="739a8-133">Header</span><span class="sxs-lookup"><span data-stu-id="739a8-133">Header</span></span><br/>  | <dl> <span data-ttu-id="739a8-134"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="739a8-134"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="739a8-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="739a8-135">Library</span></span><br/> | <dl> <span data-ttu-id="739a8-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="739a8-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="739a8-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="739a8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="739a8-138">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="739a8-138">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




