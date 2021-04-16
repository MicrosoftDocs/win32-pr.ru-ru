---
description: Метод Нотифисреад уведомляет поток о том, что очередь содержит данные.
ms.assetid: d91cde3f-2876-4fb4-a124-f1460bba2cc9
title: Каутпуткуеуе. Нотифисреад, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NotifyThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bb5f965bac15e99140955e8ee2519feaadfef85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665150"
---
# <a name="coutputqueuenotifythread-method"></a><span data-ttu-id="17189-103">Каутпуткуеуе. Нотифисреад, метод</span><span class="sxs-lookup"><span data-stu-id="17189-103">COutputQueue.NotifyThread method</span></span>

<span data-ttu-id="17189-104">`NotifyThread`Метод уведомляет поток о том, что очередь содержит данные.</span><span class="sxs-lookup"><span data-stu-id="17189-104">The `NotifyThread` method notifies the thread that the queue contains data.</span></span>

## <a name="syntax"></a><span data-ttu-id="17189-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17189-105">Syntax</span></span>


```C++
void NotifyThread();
```



## <a name="parameters"></a><span data-ttu-id="17189-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17189-106">Parameters</span></span>

<span data-ttu-id="17189-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="17189-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17189-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17189-108">Return value</span></span>

<span data-ttu-id="17189-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="17189-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17189-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17189-110">Remarks</span></span>

<span data-ttu-id="17189-111">Перед вызовом этого метода следует удерживать критическую секцию.</span><span class="sxs-lookup"><span data-stu-id="17189-111">Hold the critical section before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="17189-112">Требования</span><span class="sxs-lookup"><span data-stu-id="17189-112">Requirements</span></span>



| <span data-ttu-id="17189-113">Требование</span><span class="sxs-lookup"><span data-stu-id="17189-113">Requirement</span></span> | <span data-ttu-id="17189-114">Значение</span><span class="sxs-lookup"><span data-stu-id="17189-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17189-115">Header</span><span class="sxs-lookup"><span data-stu-id="17189-115">Header</span></span><br/>  | <dl> <span data-ttu-id="17189-116"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17189-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="17189-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="17189-117">Library</span></span><br/> | <dl> <span data-ttu-id="17189-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="17189-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17189-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17189-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17189-120">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="17189-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




