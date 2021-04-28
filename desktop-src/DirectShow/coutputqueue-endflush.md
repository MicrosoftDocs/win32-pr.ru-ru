---
description: Каутпуткуеуе. Ендфлуш, метод Ендфлуш завершает операцию очистки.
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Каутпуткуеуе. Ендфлуш, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37701526de66c8cd679f6849703c4eb2a1feb3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099012"
---
# <a name="coutputqueueendflush-method"></a><span data-ttu-id="c57bd-103">Каутпуткуеуе. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="c57bd-103">COutputQueue.EndFlush method</span></span>

<span data-ttu-id="c57bd-104">`EndFlush`Метод завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="c57bd-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c57bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c57bd-105">Syntax</span></span>


```C++
void EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="c57bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c57bd-106">Parameters</span></span>

<span data-ttu-id="c57bd-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c57bd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c57bd-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c57bd-108">Return value</span></span>

<span data-ttu-id="c57bd-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c57bd-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c57bd-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="c57bd-110">Remarks</span></span>

<span data-ttu-id="c57bd-111">Если объект использует поток, этот метод ожидает события [**каутпуткуеуе:: m \_ евфлушкомплете**](coutputqueue-m-evflushcomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="c57bd-111">If the object is using a thread, this method waits for the [**COutputQueue::m\_evFlushComplete**](coutputqueue-m-evflushcomplete.md) event.</span></span> <span data-ttu-id="c57bd-112">Поток сигнализирует об этом событии после освобождения всех ожидающих выборок.</span><span class="sxs-lookup"><span data-stu-id="c57bd-112">The thread signals this event after it frees any pending samples.</span></span> <span data-ttu-id="c57bd-113">Если объект не использует поток, этот метод вызывает метод [**каутпуткуеуе:: фрисамплес**](coutputqueue-freesamples.md) .</span><span class="sxs-lookup"><span data-stu-id="c57bd-113">If the object is not using a thread, this method calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method.</span></span> <span data-ttu-id="c57bd-114">Затем `EndFlush` метод вызывает метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c57bd-114">Then the `EndFlush` method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c57bd-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c57bd-115">Requirements</span></span>



| <span data-ttu-id="c57bd-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c57bd-116">Requirement</span></span> | <span data-ttu-id="c57bd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c57bd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c57bd-118">Header</span><span class="sxs-lookup"><span data-stu-id="c57bd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c57bd-119"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c57bd-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c57bd-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c57bd-120">Library</span></span><br/> | <dl> <span data-ttu-id="c57bd-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c57bd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c57bd-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c57bd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57bd-123">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="c57bd-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




