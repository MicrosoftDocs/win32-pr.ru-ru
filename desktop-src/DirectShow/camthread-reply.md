---
description: Метод Reply отвечает на запрос.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Метод Камсреад. Reply (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689290"
---
# <a name="camthreadreply-method"></a><span data-ttu-id="d571a-103">Камсреад. Reply, метод</span><span class="sxs-lookup"><span data-stu-id="d571a-103">CAMThread.Reply method</span></span>

<span data-ttu-id="d571a-104">`Reply`Метод отвечает на запрос.</span><span class="sxs-lookup"><span data-stu-id="d571a-104">The `Reply` method replies to a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d571a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d571a-105">Syntax</span></span>


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a><span data-ttu-id="d571a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d571a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d571a-107">*dw*</span><span class="sxs-lookup"><span data-stu-id="d571a-107">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="d571a-108">Значение, возвращаемое методом [**камсреад:: каллворкер**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="d571a-108">Value to return in the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d571a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d571a-109">Return value</span></span>

<span data-ttu-id="d571a-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d571a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d571a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d571a-111">Remarks</span></span>

<span data-ttu-id="d571a-112">Метод Каллворкер блокируется до вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="d571a-112">The CallWorker method blocks until this method is called.</span></span> <span data-ttu-id="d571a-113">Параметр *DW* предоставляет возвращаемое значение для каллворкер.</span><span class="sxs-lookup"><span data-stu-id="d571a-113">The *dw* parameter supplies the return value for CallWorker.</span></span> <span data-ttu-id="d571a-114">Вызовите этот метод в процедуре потока после получения запроса, чтобы освободить поток запроса.</span><span class="sxs-lookup"><span data-stu-id="d571a-114">Call this method in your thread procedure after you retrieve a request, to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="d571a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d571a-115">Requirements</span></span>



| <span data-ttu-id="d571a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d571a-116">Requirement</span></span> | <span data-ttu-id="d571a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d571a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d571a-118">Header</span><span class="sxs-lookup"><span data-stu-id="d571a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d571a-119"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d571a-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d571a-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d571a-120">Library</span></span><br/> | <dl> <span data-ttu-id="d571a-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d571a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d571a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d571a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d571a-123">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="d571a-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




