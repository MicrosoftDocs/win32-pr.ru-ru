---
description: Метод, находящиеся в очереди, определяет, использует ли объект рабочий поток для доставки образцов.
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: Метод Каутпуткуеуе. onqueueed (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 47093acedb3a28d633ea2c8b0bbdbba3c1493de7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665341"
---
# <a name="coutputqueueisqueued-method"></a><span data-ttu-id="7c515-103">Каутпуткуеуе. в очереди — метод</span><span class="sxs-lookup"><span data-stu-id="7c515-103">COutputQueue.IsQueued method</span></span>

<span data-ttu-id="7c515-104">`IsQueued`Метод определяет, использует ли объект рабочий поток для доставки образцов.</span><span class="sxs-lookup"><span data-stu-id="7c515-104">The `IsQueued` method determines whether the object is using a worker thread to deliver samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c515-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c515-105">Syntax</span></span>


```C++
BOOL IsQueued();
```



## <a name="parameters"></a><span data-ttu-id="7c515-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c515-106">Parameters</span></span>

<span data-ttu-id="7c515-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7c515-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c515-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c515-108">Return value</span></span>

<span data-ttu-id="7c515-109">Возвращает **значение true** , если объект использует рабочий поток, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7c515-109">Returns **TRUE** if the object is using a worker thread, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c515-110">Требования</span><span class="sxs-lookup"><span data-stu-id="7c515-110">Requirements</span></span>



| <span data-ttu-id="7c515-111">Требование</span><span class="sxs-lookup"><span data-stu-id="7c515-111">Requirement</span></span> | <span data-ttu-id="7c515-112">Значение</span><span class="sxs-lookup"><span data-stu-id="7c515-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c515-113">Header</span><span class="sxs-lookup"><span data-stu-id="7c515-113">Header</span></span><br/>  | <dl> <span data-ttu-id="7c515-114"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c515-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c515-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7c515-115">Library</span></span><br/> | <dl> <span data-ttu-id="7c515-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7c515-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c515-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c515-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c515-118">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="7c515-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




