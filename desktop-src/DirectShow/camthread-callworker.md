---
description: Метод Каллворкер сигнализирует потоку запрос.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Камсреад. Каллворкер, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689202"
---
# <a name="camthreadcallworker-method"></a><span data-ttu-id="14b74-103">Камсреад. Каллворкер, метод</span><span class="sxs-lookup"><span data-stu-id="14b74-103">CAMThread.CallWorker method</span></span>

<span data-ttu-id="14b74-104">`CallWorker`Метод сигнализирует потоку запрос.</span><span class="sxs-lookup"><span data-stu-id="14b74-104">The `CallWorker` method signals the thread with a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b74-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14b74-105">Syntax</span></span>


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a><span data-ttu-id="14b74-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14b74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b74-107">*двпарам*</span><span class="sxs-lookup"><span data-stu-id="14b74-107">*dwParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14b74-108">Параметр запроса.</span><span class="sxs-lookup"><span data-stu-id="14b74-108">Request parameter.</span></span> <span data-ttu-id="14b74-109">Производный класс определяет значение параметра.</span><span class="sxs-lookup"><span data-stu-id="14b74-109">The derived class defines the meaning of the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b74-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14b74-110">Return value</span></span>

<span data-ttu-id="14b74-111">Возвращает значение, определяемое производным классом.</span><span class="sxs-lookup"><span data-stu-id="14b74-111">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b74-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14b74-112">Remarks</span></span>

<span data-ttu-id="14b74-113">Методы [**камсреад:: WebRequest**](camthread-getrequest.md) и [**Камсреад:: чеккрекуест**](camthread-checkrequest.md) извлекают значение параметра *двпарам* .</span><span class="sxs-lookup"><span data-stu-id="14b74-113">The [**CAMThread::GetRequest**](camthread-getrequest.md) and [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods retrieve the value of the *dwParam* parameter.</span></span> <span data-ttu-id="14b74-114">Метод WebRequest блокируется до `CallWorker` вызова метода.</span><span class="sxs-lookup"><span data-stu-id="14b74-114">The GetRequest method blocks until `CallWorker` is called.</span></span>

<span data-ttu-id="14b74-115">Этот метод блокируется до тех пор, пока не будет вызван метод [**камсреад:: Reply**](camthread-reply.md) .</span><span class="sxs-lookup"><span data-stu-id="14b74-115">This method blocks until the [**CAMThread::Reply**](camthread-reply.md) method is called.</span></span> <span data-ttu-id="14b74-116">Возвращаемое значение — это параметр, заданный для ответа.</span><span class="sxs-lookup"><span data-stu-id="14b74-116">The return value is the parameter given to Reply.</span></span>

<span data-ttu-id="14b74-117">Этот метод удерживает блокировку [**камсреад:: m \_ акцесслокк**](camthread-m-accesslock.md) для сериализации запросов.</span><span class="sxs-lookup"><span data-stu-id="14b74-117">This method holds the [**CAMThread::m\_AccessLock**](camthread-m-accesslock.md) lock to serialize requests.</span></span> <span data-ttu-id="14b74-118">Поэтому Вызывайте этот метод из самого потока или из любой функции члена, которая выполняется в контексте потока.</span><span class="sxs-lookup"><span data-stu-id="14b74-118">Therefore, do call this method from the thread itself or from any member function that executes in the context of the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b74-119">Требования</span><span class="sxs-lookup"><span data-stu-id="14b74-119">Requirements</span></span>



| <span data-ttu-id="14b74-120">Требование</span><span class="sxs-lookup"><span data-stu-id="14b74-120">Requirement</span></span> | <span data-ttu-id="14b74-121">Значение</span><span class="sxs-lookup"><span data-stu-id="14b74-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14b74-122">Header</span><span class="sxs-lookup"><span data-stu-id="14b74-122">Header</span></span><br/>  | <dl> <span data-ttu-id="14b74-123"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14b74-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="14b74-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14b74-124">Library</span></span><br/> | <dl> <span data-ttu-id="14b74-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="14b74-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14b74-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14b74-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b74-127">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="14b74-127">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




