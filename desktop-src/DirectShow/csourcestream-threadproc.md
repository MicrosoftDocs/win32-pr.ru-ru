---
description: 'Метод Среадпрок является процедурой потока для рабочего потока. Этот метод реализует чистый виртуальный метод Камсреад:: Среадпрок.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Метод Ксаурцестреам. Среадпрок (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675075"
---
# <a name="csourcestreamthreadproc-method"></a><span data-ttu-id="37b45-104">Ксаурцестреам. Среадпрок, метод</span><span class="sxs-lookup"><span data-stu-id="37b45-104">CSourceStream.ThreadProc method</span></span>

<span data-ttu-id="37b45-105">`ThreadProc`Метод является процедурой потока для рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="37b45-105">The `ThreadProc` method is the thread procedure for the worker thread.</span></span> <span data-ttu-id="37b45-106">Этот метод реализует чистый виртуальный метод [**камсреад:: среадпрок**](camthread-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="37b45-106">This method implements the pure virtual [**CAMThread::ThreadProc**](camthread-threadproc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="37b45-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37b45-107">Syntax</span></span>


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="37b45-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="37b45-108">Parameters</span></span>

<span data-ttu-id="37b45-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="37b45-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37b45-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37b45-110">Return value</span></span>

<span data-ttu-id="37b45-111">Возвращает 0, если поток успешно завершился, или 1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="37b45-111">Returns 0 if the thread completed successfully or 1 otherwise.</span></span> <span data-ttu-id="37b45-112">Если возвращаемое значение равно 1, ресурсы потока по-прежнему могут быть распределены.</span><span class="sxs-lookup"><span data-stu-id="37b45-112">If the return value is 1, the thread's resources might still be allocated.</span></span>

## <a name="remarks"></a><span data-ttu-id="37b45-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37b45-113">Remarks</span></span>

<span data-ttu-id="37b45-114">Этот метод в течение неограниченного времени ожидает запросов потока, вызывая метод [**камсреад:: WebRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="37b45-114">This method waits indefinitely for thread requests, by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="37b45-115">Если он получает запрос [**ксаурцестреам:: Run**](csourcestream-run.md) или [**ксаурцестреам::P Аусе**](csourcestream-pause.md) , он вызывает метод [**ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="37b45-115">If it receives a [**CSourceStream::Run**](csourcestream-run.md) or [**CSourceStream::Pause**](csourcestream-pause.md) request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="37b45-116">Метод **добуфферпроцессинглуп** передает данные, пока не получит запрос [**Ксаурцестреам:: останавливаться**](csourcestream-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="37b45-116">The **DoBufferProcessingLoop** method pushes data until it receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span> <span data-ttu-id="37b45-117">Процедура потока завершает работу при получении запроса [**ксаурцестреам:: Exit**](csourcestream-exit.md) .</span><span class="sxs-lookup"><span data-stu-id="37b45-117">The thread procedure exits when it receives a [**CSourceStream::Exit**](csourcestream-exit.md) request.</span></span>

## <a name="requirements"></a><span data-ttu-id="37b45-118">Требования</span><span class="sxs-lookup"><span data-stu-id="37b45-118">Requirements</span></span>



| <span data-ttu-id="37b45-119">Требование</span><span class="sxs-lookup"><span data-stu-id="37b45-119">Requirement</span></span> | <span data-ttu-id="37b45-120">Значение</span><span class="sxs-lookup"><span data-stu-id="37b45-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b45-121">Header</span><span class="sxs-lookup"><span data-stu-id="37b45-121">Header</span></span><br/>  | <dl> <span data-ttu-id="37b45-122"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37b45-122"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="37b45-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="37b45-123">Library</span></span><br/> | <dl> <span data-ttu-id="37b45-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="37b45-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37b45-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37b45-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b45-126">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="37b45-126">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




