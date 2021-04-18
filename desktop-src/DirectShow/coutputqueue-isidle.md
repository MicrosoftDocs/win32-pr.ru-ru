---
description: Метод Idle определяет, ожидает ли объект данных.
ms.assetid: be1b5633-f9e9-497e-8b6f-5634eae91273
title: Метод Каутпуткуеуе. Idle (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsIdle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bf8b42189e356659e74398eaa3eefeb5f771a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668980"
---
# <a name="coutputqueueisidle-method"></a><span data-ttu-id="0ecf1-103">Каутпуткуеуе. Idle, метод</span><span class="sxs-lookup"><span data-stu-id="0ecf1-103">COutputQueue.IsIdle method</span></span>

<span data-ttu-id="0ecf1-104">`IsIdle`Метод определяет, ожидает ли объект данных.</span><span class="sxs-lookup"><span data-stu-id="0ecf1-104">The `IsIdle` method determines whether the object is waiting for data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ecf1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ecf1-105">Syntax</span></span>


```C++
BOOL IsIdle();
```



## <a name="parameters"></a><span data-ttu-id="0ecf1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ecf1-106">Parameters</span></span>

<span data-ttu-id="0ecf1-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0ecf1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ecf1-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ecf1-108">Return value</span></span>

<span data-ttu-id="0ecf1-109">Возвращает **значение true** , если поток ожидает, а образец массива пуст.</span><span class="sxs-lookup"><span data-stu-id="0ecf1-109">Returns **TRUE** if the thread is waiting and the sample array is empty.</span></span> <span data-ttu-id="0ecf1-110">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0ecf1-110">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ecf1-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0ecf1-111">Requirements</span></span>



| <span data-ttu-id="0ecf1-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0ecf1-112">Requirement</span></span> | <span data-ttu-id="0ecf1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0ecf1-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ecf1-114">Header</span><span class="sxs-lookup"><span data-stu-id="0ecf1-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0ecf1-115"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ecf1-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ecf1-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ecf1-116">Library</span></span><br/> | <dl> <span data-ttu-id="0ecf1-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0ecf1-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ecf1-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ecf1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ecf1-119">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="0ecf1-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




