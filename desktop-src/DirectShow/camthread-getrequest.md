---
description: Метод GetNext ожидает следующий запрос.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Метод Камсреад. WebRequest (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688998"
---
# <a name="camthreadgetrequest-method"></a><span data-ttu-id="d5dea-103">Камсреад. метод запроса</span><span class="sxs-lookup"><span data-stu-id="d5dea-103">CAMThread.GetRequest method</span></span>

<span data-ttu-id="d5dea-104">`GetRequest`Метод ожидает следующего запроса.</span><span class="sxs-lookup"><span data-stu-id="d5dea-104">The `GetRequest` method waits for the next request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5dea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5dea-105">Syntax</span></span>


```C++
DWORD GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="d5dea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5dea-106">Parameters</span></span>

<span data-ttu-id="d5dea-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d5dea-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5dea-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5dea-108">Return value</span></span>

<span data-ttu-id="d5dea-109">Возвращает значение, определяемое производным классом.</span><span class="sxs-lookup"><span data-stu-id="d5dea-109">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5dea-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5dea-110">Remarks</span></span>

<span data-ttu-id="d5dea-111">Этот метод блокируется до тех пор, пока другой поток не вызовет метод [**камсреад:: каллворкер**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="d5dea-111">This method blocks until another thread calls the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="d5dea-112">Затем возвращается параметр, который был передан в Каллворкер.</span><span class="sxs-lookup"><span data-stu-id="d5dea-112">Then it returns the parameter that was passed to CallWorker.</span></span> <span data-ttu-id="d5dea-113">Вызовите метод [**камсреад:: Reply**](camthread-reply.md) , чтобы освободить поток запроса.</span><span class="sxs-lookup"><span data-stu-id="d5dea-113">Call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5dea-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d5dea-114">Requirements</span></span>



| <span data-ttu-id="d5dea-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d5dea-115">Requirement</span></span> | <span data-ttu-id="d5dea-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d5dea-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5dea-117">Header</span><span class="sxs-lookup"><span data-stu-id="d5dea-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d5dea-118"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5dea-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d5dea-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5dea-119">Library</span></span><br/> | <dl> <span data-ttu-id="d5dea-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d5dea-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5dea-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5dea-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5dea-122">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="d5dea-122">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




