---
description: Метод Бегинфлуш начинает операцию очистки.
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
ms.openlocfilehash: 462c3027e38bd94f061eb927c0d52576e29c997b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668886"
---
# <a name="coutputqueuebeginflush-method"></a><span data-ttu-id="21197-103">Каутпуткуеуе. Бегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="21197-103">COutputQueue.BeginFlush method</span></span>

<span data-ttu-id="21197-104">`BeginFlush`Метод начинает операцию записи на диск.</span><span class="sxs-lookup"><span data-stu-id="21197-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="21197-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21197-105">Syntax</span></span>


```C++
void BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="21197-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="21197-106">Parameters</span></span>

<span data-ttu-id="21197-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="21197-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21197-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21197-108">Return value</span></span>

<span data-ttu-id="21197-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="21197-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21197-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21197-110">Remarks</span></span>

<span data-ttu-id="21197-111">Этот метод задает для переменной члена [**каутпуткуеуе:: m \_ Бфлушинг**](coutputqueue-m-bflushing.md) **значение true**.</span><span class="sxs-lookup"><span data-stu-id="21197-111">This method sets the [**COutputQueue::m\_bFlushing**](coutputqueue-m-bflushing.md) member variable to **TRUE**.</span></span> <span data-ttu-id="21197-112">Если объект использует поток, поток вызывает метод [**каутпуткуеуе:: фрисамплес**](coutputqueue-freesamples.md) , чтобы освободить все ожидающие выборки.</span><span class="sxs-lookup"><span data-stu-id="21197-112">If the object is using a thread, the thread calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method to free any pending samples.</span></span> <span data-ttu-id="21197-113">В противном случае объект вызывает **фрисамплес** во время метода [**Каутпуткуеуе:: ендфлуш**](coutputqueue-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="21197-113">Otherwise, the object calls **FreeSamples** during the [**COutputQueue::EndFlush**](coutputqueue-endflush.md) method.</span></span> <span data-ttu-id="21197-114">Этот метод также задает значение false для переменной члена [**каутпуткуеуе:: m \_ HR**](coutputqueue-m-hr.md) \_ , что приводит к отмене всех новых выборок объектом.</span><span class="sxs-lookup"><span data-stu-id="21197-114">This method also sets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_FALSE, which causes the object to discard all new samples.</span></span>

<span data-ttu-id="21197-115">Объект передает уведомление о сбросе на диск, вызывая метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="21197-115">The object passes the flush notification downstream by calling the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="21197-116">Требования</span><span class="sxs-lookup"><span data-stu-id="21197-116">Requirements</span></span>



| <span data-ttu-id="21197-117">Требование</span><span class="sxs-lookup"><span data-stu-id="21197-117">Requirement</span></span> | <span data-ttu-id="21197-118">Значение</span><span class="sxs-lookup"><span data-stu-id="21197-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21197-119">Header</span><span class="sxs-lookup"><span data-stu-id="21197-119">Header</span></span><br/>  | <dl> <span data-ttu-id="21197-120"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21197-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="21197-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21197-121">Library</span></span><br/> | <dl> <span data-ttu-id="21197-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="21197-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21197-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21197-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21197-124">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="21197-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




