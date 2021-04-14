---
description: Метод Фрисамплес освобождает все отложенные выборки.
ms.assetid: 61b7fe6e-41cc-4d5e-b083-bbc400d04e39
title: Каутпуткуеуе. Фрисамплес, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.FreeSamples
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70d0680d2a1a3ac020be84f244e1cc02bb6efad0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668884"
---
# <a name="coutputqueuefreesamples-method"></a><span data-ttu-id="27ee3-103">Каутпуткуеуе. Фрисамплес, метод</span><span class="sxs-lookup"><span data-stu-id="27ee3-103">COutputQueue.FreeSamples method</span></span>

<span data-ttu-id="27ee3-104">`FreeSamples`Метод освобождает все ожидающие выборки.</span><span class="sxs-lookup"><span data-stu-id="27ee3-104">The `FreeSamples` method frees all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="27ee3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27ee3-105">Syntax</span></span>


```C++
void FreeSamples();
```



## <a name="parameters"></a><span data-ttu-id="27ee3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="27ee3-106">Parameters</span></span>

<span data-ttu-id="27ee3-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="27ee3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27ee3-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27ee3-108">Return value</span></span>

<span data-ttu-id="27ee3-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="27ee3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="27ee3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27ee3-110">Remarks</span></span>

<span data-ttu-id="27ee3-111">Этот метод удаляет все ожидающие выборки из очереди и из образца массива.</span><span class="sxs-lookup"><span data-stu-id="27ee3-111">This method removes any pending samples from the queue and from the sample array.</span></span>

## <a name="requirements"></a><span data-ttu-id="27ee3-112">Требования</span><span class="sxs-lookup"><span data-stu-id="27ee3-112">Requirements</span></span>



| <span data-ttu-id="27ee3-113">Требование</span><span class="sxs-lookup"><span data-stu-id="27ee3-113">Requirement</span></span> | <span data-ttu-id="27ee3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="27ee3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27ee3-115">Header</span><span class="sxs-lookup"><span data-stu-id="27ee3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="27ee3-116"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27ee3-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="27ee3-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="27ee3-117">Library</span></span><br/> | <dl> <span data-ttu-id="27ee3-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="27ee3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27ee3-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27ee3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27ee3-120">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="27ee3-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




