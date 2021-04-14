---
description: 'Массив выборок размера Каутпуткуеуе:: m \_ лбатчсизе.'
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'Элемент Каутпуткуеуе:: m_ppSamples (Аутпутк. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668767"
---
# <a name="coutputqueuem_ppsamples-member"></a><span data-ttu-id="e7690-103">Элемент Каутпуткуеуе:: m \_ ппсамплес</span><span class="sxs-lookup"><span data-stu-id="e7690-103">COutputQueue::m\_ppSamples member</span></span>

<span data-ttu-id="e7690-104">Массив выборок размера [**каутпуткуеуе:: m \_ лбатчсизе**](coutputqueue-m-lbatchsize.md).</span><span class="sxs-lookup"><span data-stu-id="e7690-104">Array of samples of size [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7690-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7690-105">Syntax</span></span>


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a><span data-ttu-id="e7690-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="e7690-106">Remarks</span></span>

<span data-ttu-id="e7690-107">Рабочий поток извлекает образцы из очереди и помещает их в этот массив.</span><span class="sxs-lookup"><span data-stu-id="e7690-107">The worker thread pulls samples from the queue and places them in this array.</span></span> <span data-ttu-id="e7690-108">Он передает массив в метод [**имеминпутпин:: рецеивемултипле**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .</span><span class="sxs-lookup"><span data-stu-id="e7690-108">It passes the array to the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span> <span data-ttu-id="e7690-109">Если объект не использует рабочий поток, объект помещает примеры непосредственно в этот массив.</span><span class="sxs-lookup"><span data-stu-id="e7690-109">If the object is not using a worker thread, the object places samples directly into this array.</span></span> <span data-ttu-id="e7690-110">Переменная члена [**\_ списка каутпуткуеуе:: m**](coutputqueue-m-list.md) содержит очередь.</span><span class="sxs-lookup"><span data-stu-id="e7690-110">The [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable holds the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7690-111">Требования</span><span class="sxs-lookup"><span data-stu-id="e7690-111">Requirements</span></span>



| <span data-ttu-id="e7690-112">Требование</span><span class="sxs-lookup"><span data-stu-id="e7690-112">Requirement</span></span> | <span data-ttu-id="e7690-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e7690-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7690-114">Header</span><span class="sxs-lookup"><span data-stu-id="e7690-114">Header</span></span><br/>  | <dl> <span data-ttu-id="e7690-115"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7690-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e7690-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e7690-116">Library</span></span><br/> | <dl> <span data-ttu-id="e7690-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e7690-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7690-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7690-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7690-119">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="e7690-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




