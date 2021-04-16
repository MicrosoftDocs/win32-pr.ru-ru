---
description: Метод GetNext извлекает дескриптор события, который используется для сигнализации об изменении в следующем времени.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Камсчедуле. четный (Дссчедуле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657353"
---
# <a name="camschedulegetevent-method"></a><span data-ttu-id="28437-103">Камсчедуле. четный, метод</span><span class="sxs-lookup"><span data-stu-id="28437-103">CAMSchedule.GetEvent method</span></span>

<span data-ttu-id="28437-104">`GetEvent`Метод получает дескриптор события, который используется для сигнализации об изменении в следующем времени.</span><span class="sxs-lookup"><span data-stu-id="28437-104">The `GetEvent` method retrieves an event handle, which is used to signal a change in the next advise time.</span></span>

## <a name="syntax"></a><span data-ttu-id="28437-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28437-105">Syntax</span></span>


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a><span data-ttu-id="28437-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28437-106">Parameters</span></span>

<span data-ttu-id="28437-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="28437-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28437-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28437-108">Return value</span></span>

<span data-ttu-id="28437-109">Возвращает маркер события.</span><span class="sxs-lookup"><span data-stu-id="28437-109">Returns a handle to an event.</span></span>

## <a name="remarks"></a><span data-ttu-id="28437-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28437-110">Remarks</span></span>

<span data-ttu-id="28437-111">Если следующее время уведомления изменилось другими словами, при добавлении нового запроса advise в начало списка планировщик сигнализирует об этом событии.</span><span class="sxs-lookup"><span data-stu-id="28437-111">If the next advise time changes in other words, if a new advise request is added to the front of the list the scheduler signals this event.</span></span> <span data-ttu-id="28437-112">Для определения следующего времени вызова в часах необходимо вызвать метод [**камсчедуле:: Advise**](camschedule-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="28437-112">The clock should call the [**CAMSchedule::Advise**](camschedule-advise.md) method to determine the next advise time.</span></span>

## <a name="requirements"></a><span data-ttu-id="28437-113">Требования</span><span class="sxs-lookup"><span data-stu-id="28437-113">Requirements</span></span>



| <span data-ttu-id="28437-114">Требование</span><span class="sxs-lookup"><span data-stu-id="28437-114">Requirement</span></span> | <span data-ttu-id="28437-115">Значение</span><span class="sxs-lookup"><span data-stu-id="28437-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28437-116">Header</span><span class="sxs-lookup"><span data-stu-id="28437-116">Header</span></span><br/>  | <dl> <span data-ttu-id="28437-117"><dt>Дссчедуле. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28437-117"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="28437-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="28437-118">Library</span></span><br/> | <dl> <span data-ttu-id="28437-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="28437-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28437-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28437-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28437-121">**Класс Камсчедуле**</span><span class="sxs-lookup"><span data-stu-id="28437-121">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




