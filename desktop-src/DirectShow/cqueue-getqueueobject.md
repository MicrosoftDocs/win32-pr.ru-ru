---
description: Извлекает следующий элемент из очереди.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Ккуеуе. Жеткуеуеобжект, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679682"
---
# <a name="cqueuegetqueueobject-method"></a><span data-ttu-id="3aadf-103">Ккуеуе. Жеткуеуеобжект, метод</span><span class="sxs-lookup"><span data-stu-id="3aadf-103">CQueue.GetQueueObject method</span></span>

<span data-ttu-id="3aadf-104">Извлекает следующий элемент из очереди.</span><span class="sxs-lookup"><span data-stu-id="3aadf-104">Retrieves the next item from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aadf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3aadf-105">Syntax</span></span>


```C++
T GetQueueObject();
```



## <a name="parameters"></a><span data-ttu-id="3aadf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3aadf-106">Parameters</span></span>

<span data-ttu-id="3aadf-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3aadf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3aadf-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3aadf-108">Return value</span></span>

<span data-ttu-id="3aadf-109">Возвращает объект типа **T** (тип шаблона).</span><span class="sxs-lookup"><span data-stu-id="3aadf-109">Returns an object of type **T** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="3aadf-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3aadf-110">Remarks</span></span>

<span data-ttu-id="3aadf-111">Этот метод блокируется, пока элемент не будет доступен в очереди.</span><span class="sxs-lookup"><span data-stu-id="3aadf-111">This method blocks until an item is available on the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aadf-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3aadf-112">Requirements</span></span>



| <span data-ttu-id="3aadf-113">Требование</span><span class="sxs-lookup"><span data-stu-id="3aadf-113">Requirement</span></span> | <span data-ttu-id="3aadf-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3aadf-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aadf-115">Header</span><span class="sxs-lookup"><span data-stu-id="3aadf-115">Header</span></span><br/>  | <dl> <span data-ttu-id="3aadf-116"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3aadf-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3aadf-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3aadf-117">Library</span></span><br/> | <dl> <span data-ttu-id="3aadf-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3aadf-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aadf-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3aadf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aadf-120">**Класс Ккуеуе**</span><span class="sxs-lookup"><span data-stu-id="3aadf-120">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




