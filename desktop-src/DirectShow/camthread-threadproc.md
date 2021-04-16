---
description: Метод Среадпрок является процедурой потока.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: Камсреад. Среадпрок, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657705"
---
# <a name="camthreadthreadproc-method"></a><span data-ttu-id="994ac-103">Камсреад. Среадпрок, метод</span><span class="sxs-lookup"><span data-stu-id="994ac-103">CAMThread.ThreadProc method</span></span>

<span data-ttu-id="994ac-104">`ThreadProc`Метод является процедурой потока.</span><span class="sxs-lookup"><span data-stu-id="994ac-104">The `ThreadProc` method is the thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="994ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="994ac-105">Syntax</span></span>


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a><span data-ttu-id="994ac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="994ac-106">Parameters</span></span>

<span data-ttu-id="994ac-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="994ac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="994ac-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="994ac-108">Return value</span></span>

<span data-ttu-id="994ac-109">Возвращает значение **типа DWORD** , значение которого определяется производным классом.</span><span class="sxs-lookup"><span data-stu-id="994ac-109">Returns a **DWORD** value whose meaning is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="994ac-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="994ac-110">Remarks</span></span>

<span data-ttu-id="994ac-111">Это чистый виртуальный метод.</span><span class="sxs-lookup"><span data-stu-id="994ac-111">This is a pure virtual method.</span></span> <span data-ttu-id="994ac-112">Реализуйте этот метод в производном классе для предоставления потоковой процедуры.</span><span class="sxs-lookup"><span data-stu-id="994ac-112">Implement this method in your derived class to supply a thread procedure.</span></span> <span data-ttu-id="994ac-113">Когда метод [**камсреад:: Create**](camthread-create.md) создает поток, он предоставляет адрес метода [**Камсреад:: инитиалсреадпрок**](camthread-initialthreadproc.md) , который, в свою очередь, вызывает метод среадпрок.</span><span class="sxs-lookup"><span data-stu-id="994ac-113">When the [**CAMThread::Create**](camthread-create.md) method creates a thread, it gives the address of the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method, which in turn calls your ThreadProc method.</span></span>

<span data-ttu-id="994ac-114">Как правило, метод Среадпрок будет вводить цикл, который получает запросы (путем вызова методов [**камсреад:: WebRequest**](camthread-getrequest.md) или [**Камсреад:: чеккрекуест**](camthread-checkrequest.md) ) и обрабатывает данные.</span><span class="sxs-lookup"><span data-stu-id="994ac-114">Typically, your ThreadProc method will enter a loop that retrieves requests (by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods) and processes data.</span></span>

<span data-ttu-id="994ac-115">При возврате из этого метода поток завершает работу.</span><span class="sxs-lookup"><span data-stu-id="994ac-115">When this method returns, the thread exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="994ac-116">Требования</span><span class="sxs-lookup"><span data-stu-id="994ac-116">Requirements</span></span>



| <span data-ttu-id="994ac-117">Требование</span><span class="sxs-lookup"><span data-stu-id="994ac-117">Requirement</span></span> | <span data-ttu-id="994ac-118">Значение</span><span class="sxs-lookup"><span data-stu-id="994ac-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="994ac-119">Header</span><span class="sxs-lookup"><span data-stu-id="994ac-119">Header</span></span><br/>  | <dl> <span data-ttu-id="994ac-120"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="994ac-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="994ac-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="994ac-121">Library</span></span><br/> | <dl> <span data-ttu-id="994ac-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="994ac-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="994ac-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="994ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="994ac-124">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="994ac-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




