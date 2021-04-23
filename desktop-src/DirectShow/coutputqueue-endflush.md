---
description: Метод Ендфлуш завершает операцию очистки.
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
ms.openlocfilehash: e18afec866176147c5c75a57fca522c4ebc5fcf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668885"
---
# <a name="coutputqueueendflush-method"></a><span data-ttu-id="38fe0-103">Каутпуткуеуе. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="38fe0-103">COutputQueue.EndFlush method</span></span>

<span data-ttu-id="38fe0-104">`EndFlush`Метод завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="38fe0-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="38fe0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38fe0-105">Syntax</span></span>


```C++
void EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="38fe0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38fe0-106">Parameters</span></span>

<span data-ttu-id="38fe0-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="38fe0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38fe0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38fe0-108">Return value</span></span>

<span data-ttu-id="38fe0-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="38fe0-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38fe0-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38fe0-110">Remarks</span></span>

<span data-ttu-id="38fe0-111">Если объект использует поток, этот метод ожидает события [**каутпуткуеуе:: m \_ евфлушкомплете**](coutputqueue-m-evflushcomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="38fe0-111">If the object is using a thread, this method waits for the [**COutputQueue::m\_evFlushComplete**](coutputqueue-m-evflushcomplete.md) event.</span></span> <span data-ttu-id="38fe0-112">Поток сигнализирует об этом событии после освобождения всех ожидающих выборок.</span><span class="sxs-lookup"><span data-stu-id="38fe0-112">The thread signals this event after it frees any pending samples.</span></span> <span data-ttu-id="38fe0-113">Если объект не использует поток, этот метод вызывает метод [**каутпуткуеуе:: фрисамплес**](coutputqueue-freesamples.md) .</span><span class="sxs-lookup"><span data-stu-id="38fe0-113">If the object is not using a thread, this method calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method.</span></span> <span data-ttu-id="38fe0-114">Затем `EndFlush` метод вызывает метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="38fe0-114">Then the `EndFlush` method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="38fe0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="38fe0-115">Requirements</span></span>



| <span data-ttu-id="38fe0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="38fe0-116">Requirement</span></span> | <span data-ttu-id="38fe0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="38fe0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38fe0-118">Header</span><span class="sxs-lookup"><span data-stu-id="38fe0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="38fe0-119"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38fe0-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="38fe0-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="38fe0-120">Library</span></span><br/> | <dl> <span data-ttu-id="38fe0-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="38fe0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38fe0-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38fe0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38fe0-123">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="38fe0-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




