---
description: Помещает элемент в очередь.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: Ккуеуе. Путкуеуеобжект, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5371c843bb348f50539535a3df9a0f6aed00893e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669089"
---
# <a name="cqueueputqueueobject-method"></a><span data-ttu-id="586e5-103">Ккуеуе. Путкуеуеобжект, метод</span><span class="sxs-lookup"><span data-stu-id="586e5-103">CQueue.PutQueueObject method</span></span>

<span data-ttu-id="586e5-104">Помещает элемент в очередь.</span><span class="sxs-lookup"><span data-stu-id="586e5-104">Puts an item onto the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="586e5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="586e5-105">Syntax</span></span>


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a><span data-ttu-id="586e5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="586e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="586e5-107">*object*</span><span class="sxs-lookup"><span data-stu-id="586e5-107">*object*</span></span> 
</dt> <dd>

<span data-ttu-id="586e5-108">Объект типа **T** (тип шаблона).</span><span class="sxs-lookup"><span data-stu-id="586e5-108">Object of type **T** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="586e5-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="586e5-109">Return value</span></span>

<span data-ttu-id="586e5-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="586e5-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="586e5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="586e5-111">Remarks</span></span>

<span data-ttu-id="586e5-112">Этот метод блокируется до тех пор, пока в очереди элемента не будет свободного пространства.</span><span class="sxs-lookup"><span data-stu-id="586e5-112">This method blocks until there is space in the queue for the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="586e5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="586e5-113">Requirements</span></span>



| <span data-ttu-id="586e5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="586e5-114">Requirement</span></span> | <span data-ttu-id="586e5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="586e5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="586e5-116">Header</span><span class="sxs-lookup"><span data-stu-id="586e5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="586e5-117"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="586e5-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="586e5-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="586e5-118">Library</span></span><br/> | <dl> <span data-ttu-id="586e5-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="586e5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="586e5-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="586e5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="586e5-121">**Класс Ккуеуе**</span><span class="sxs-lookup"><span data-stu-id="586e5-121">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




