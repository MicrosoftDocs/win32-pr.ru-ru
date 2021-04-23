---
description: Метод Close ожидает выхода из потока, а затем освобождает его ресурсы.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Метод Камсреад. Close (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689190"
---
# <a name="camthreadclose-method"></a><span data-ttu-id="9e8e1-103">Камсреад. Close, метод</span><span class="sxs-lookup"><span data-stu-id="9e8e1-103">CAMThread.Close method</span></span>

<span data-ttu-id="9e8e1-104">`Close`Метод ожидает выхода из потока, а затем освобождает его ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9e8e1-104">The `Close` method waits for the thread to exit, then releases its resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e8e1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e8e1-105">Syntax</span></span>


```C++
void Close();
```



## <a name="parameters"></a><span data-ttu-id="9e8e1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e8e1-106">Parameters</span></span>

<span data-ttu-id="9e8e1-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9e8e1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e8e1-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e8e1-108">Return value</span></span>

<span data-ttu-id="9e8e1-109">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="9e8e1-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e8e1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e8e1-110">Remarks</span></span>

<span data-ttu-id="9e8e1-111">Перед вызовом этого метода необходимо предоставить способ выхода из потока.</span><span class="sxs-lookup"><span data-stu-id="9e8e1-111">Before calling this method, you must provide a way for the thread to exit.</span></span> <span data-ttu-id="9e8e1-112">Например, в методе [**камсреад:: среадпрок**](camthread-threadproc.md) Определите запрос, который сообщает потоку о выходе.</span><span class="sxs-lookup"><span data-stu-id="9e8e1-112">For example, in your [**CAMThread::ThreadProc**](camthread-threadproc.md) method, define a request that signals the thread to exit.</span></span> <span data-ttu-id="9e8e1-113">Затем вызовите метод [**камсреад:: каллворкер**](camthread-callworker.md) с этим значением.</span><span class="sxs-lookup"><span data-stu-id="9e8e1-113">Then call the [**CAMThread::CallWorker**](camthread-callworker.md) method with that value.</span></span>

<span data-ttu-id="9e8e1-114">Метод деструктора [**~ камсреад**](camthread--camthread.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="9e8e1-114">The [**~ CAMThread**](camthread--camthread.md) destructor method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e8e1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9e8e1-115">Requirements</span></span>



| <span data-ttu-id="9e8e1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9e8e1-116">Requirement</span></span> | <span data-ttu-id="9e8e1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9e8e1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8e1-118">Header</span><span class="sxs-lookup"><span data-stu-id="9e8e1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9e8e1-119"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e8e1-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9e8e1-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9e8e1-120">Library</span></span><br/> | <dl> <span data-ttu-id="9e8e1-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9e8e1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e8e1-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e8e1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e8e1-123">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="9e8e1-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




