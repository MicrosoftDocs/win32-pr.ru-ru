---
description: Каутпуткуеуе. Бегинфлуш, метод Бегинфлуш начинает операцию очистки.
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Каутпуткуеуе. Бегинфлуш, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7c6168daf766ec11e18e86673d9d25542b50462
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099032"
---
# <a name="coutputqueuebeginflush-method"></a><span data-ttu-id="72ee4-103">Каутпуткуеуе. Бегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="72ee4-103">COutputQueue.BeginFlush method</span></span>

<span data-ttu-id="72ee4-104">`BeginFlush`Метод начинает операцию записи на диск.</span><span class="sxs-lookup"><span data-stu-id="72ee4-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="72ee4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72ee4-105">Syntax</span></span>


```C++
void BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="72ee4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72ee4-106">Parameters</span></span>

<span data-ttu-id="72ee4-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="72ee4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72ee4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72ee4-108">Return value</span></span>

<span data-ttu-id="72ee4-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="72ee4-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72ee4-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="72ee4-110">Remarks</span></span>

<span data-ttu-id="72ee4-111">Этот метод задает для переменной члена [**каутпуткуеуе:: m \_ Бфлушинг**](coutputqueue-m-bflushing.md) **значение true**.</span><span class="sxs-lookup"><span data-stu-id="72ee4-111">This method sets the [**COutputQueue::m\_bFlushing**](coutputqueue-m-bflushing.md) member variable to **TRUE**.</span></span> <span data-ttu-id="72ee4-112">Если объект использует поток, поток вызывает метод [**каутпуткуеуе:: фрисамплес**](coutputqueue-freesamples.md) , чтобы освободить все ожидающие выборки.</span><span class="sxs-lookup"><span data-stu-id="72ee4-112">If the object is using a thread, the thread calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method to free any pending samples.</span></span> <span data-ttu-id="72ee4-113">В противном случае объект вызывает **фрисамплес** во время метода [**Каутпуткуеуе:: ендфлуш**](coutputqueue-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="72ee4-113">Otherwise, the object calls **FreeSamples** during the [**COutputQueue::EndFlush**](coutputqueue-endflush.md) method.</span></span> <span data-ttu-id="72ee4-114">Этот метод также задает значение false для переменной члена [**каутпуткуеуе:: m \_ HR**](coutputqueue-m-hr.md) \_ , что приводит к отмене всех новых выборок объектом.</span><span class="sxs-lookup"><span data-stu-id="72ee4-114">This method also sets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_FALSE, which causes the object to discard all new samples.</span></span>

<span data-ttu-id="72ee4-115">Объект передает уведомление о сбросе на диск, вызывая метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="72ee4-115">The object passes the flush notification downstream by calling the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="72ee4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="72ee4-116">Requirements</span></span>



| <span data-ttu-id="72ee4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="72ee4-117">Requirement</span></span> | <span data-ttu-id="72ee4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="72ee4-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72ee4-119">Header</span><span class="sxs-lookup"><span data-stu-id="72ee4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="72ee4-120"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72ee4-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="72ee4-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="72ee4-121">Library</span></span><br/> | <dl> <span data-ttu-id="72ee4-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="72ee4-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72ee4-123">См. также</span><span class="sxs-lookup"><span data-stu-id="72ee4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ee4-124">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="72ee4-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




