---
description: Флаг, указывающий, доставляет ли объект выборки в точных пакетах.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Элемент Каутпуткуеуе:: m_bBatchExact (Аутпутк. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669013"
---
# <a name="coutputqueuem_bbatchexact-member"></a><span data-ttu-id="edc61-103">Элемент Каутпуткуеуе:: m \_ ббатчексакт</span><span class="sxs-lookup"><span data-stu-id="edc61-103">COutputQueue::m\_bBatchExact member</span></span>

<span data-ttu-id="edc61-104">Флаг, указывающий, доставляет ли объект выборки в точных пакетах.</span><span class="sxs-lookup"><span data-stu-id="edc61-104">Flag that specifies whether the object delivers samples in exact batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="edc61-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edc61-105">Syntax</span></span>


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a><span data-ttu-id="edc61-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="edc61-106">Remarks</span></span>

<span data-ttu-id="edc61-107">Если значение равно **true**, объект ожидает, пока не будет выполнен полный пакет примеров мультимедиа перед доставкой.</span><span class="sxs-lookup"><span data-stu-id="edc61-107">If the value is **TRUE**, the object waits until it has a complete batch of media samples before delivering any.</span></span> <span data-ttu-id="edc61-108">В противном случае он доставляет образцы по мере их поступления.</span><span class="sxs-lookup"><span data-stu-id="edc61-108">Otherwise, it delivers samples as they arrive.</span></span> <span data-ttu-id="edc61-109">Переменная члена [**каутпуткуеуе:: m \_ лбатчсизе**](coutputqueue-m-lbatchsize.md) определяет размер пакета.</span><span class="sxs-lookup"><span data-stu-id="edc61-109">The [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md) member variable defines the batch size.</span></span>

## <a name="requirements"></a><span data-ttu-id="edc61-110">Требования</span><span class="sxs-lookup"><span data-stu-id="edc61-110">Requirements</span></span>



| <span data-ttu-id="edc61-111">Требование</span><span class="sxs-lookup"><span data-stu-id="edc61-111">Requirement</span></span> | <span data-ttu-id="edc61-112">Значение</span><span class="sxs-lookup"><span data-stu-id="edc61-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edc61-113">Header</span><span class="sxs-lookup"><span data-stu-id="edc61-113">Header</span></span><br/>  | <dl> <span data-ttu-id="edc61-114"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edc61-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="edc61-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="edc61-115">Library</span></span><br/> | <dl> <span data-ttu-id="edc61-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="edc61-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edc61-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edc61-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edc61-118">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="edc61-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




