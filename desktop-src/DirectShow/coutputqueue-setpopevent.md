---
description: Метод Сетпопевент указывает событие, сообщающее, когда объект удаляет образец из очереди.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Каутпуткуеуе. Сетпопевент, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674877"
---
# <a name="coutputqueuesetpopevent-method"></a><span data-ttu-id="6f2ec-103">Каутпуткуеуе. Сетпопевент, метод</span><span class="sxs-lookup"><span data-stu-id="6f2ec-103">COutputQueue.SetPopEvent method</span></span>

<span data-ttu-id="6f2ec-104">`SetPopEvent`Метод указывает событие, сообщающее, когда объект удаляет выборку из очереди.</span><span class="sxs-lookup"><span data-stu-id="6f2ec-104">The `SetPopEvent` method specifies an event that is signaled whenever the object removes a sample from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f2ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f2ec-105">Syntax</span></span>


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="6f2ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f2ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f2ec-107">*хевент*</span><span class="sxs-lookup"><span data-stu-id="6f2ec-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="6f2ec-108">Обработчик события, созданного вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="6f2ec-108">Handle to an event created by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f2ec-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f2ec-109">Return value</span></span>

<span data-ttu-id="6f2ec-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6f2ec-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f2ec-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6f2ec-111">Requirements</span></span>



| <span data-ttu-id="6f2ec-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6f2ec-112">Requirement</span></span> | <span data-ttu-id="6f2ec-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6f2ec-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f2ec-114">Header</span><span class="sxs-lookup"><span data-stu-id="6f2ec-114">Header</span></span><br/>  | <dl> <span data-ttu-id="6f2ec-115"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f2ec-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6f2ec-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6f2ec-116">Library</span></span><br/> | <dl> <span data-ttu-id="6f2ec-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6f2ec-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f2ec-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f2ec-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f2ec-119">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="6f2ec-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




