---
description: Метод Онваитенд вызывается, когда заканчивается время ожидания.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Кбасевидеорендерер. Онваитенд, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656968"
---
# <a name="cbasevideorendereronwaitend-method"></a><span data-ttu-id="e9d85-103">Кбасевидеорендерер. Онваитенд, метод</span><span class="sxs-lookup"><span data-stu-id="e9d85-103">CBaseVideoRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="e9d85-104">Метод Онваитенд вызывается, когда заканчивается время ожидания.</span><span class="sxs-lookup"><span data-stu-id="e9d85-104">The OnWaitEnd method is called when a wait time ends.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d85-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9d85-105">Syntax</span></span>


```C++
void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="e9d85-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9d85-106">Parameters</span></span>

<span data-ttu-id="e9d85-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e9d85-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9d85-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9d85-108">Return value</span></span>

<span data-ttu-id="e9d85-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e9d85-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9d85-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9d85-110">Remarks</span></span>

<span data-ttu-id="e9d85-111">Эта функция члена выполняет только ведение журнала производительности.</span><span class="sxs-lookup"><span data-stu-id="e9d85-111">This member function does only performance logging.</span></span> <span data-ttu-id="e9d85-112">Он вызывается, когда поток пробудится из ожидания в окне, или когда происходит визуализация следующего образца.</span><span class="sxs-lookup"><span data-stu-id="e9d85-112">It is called when the thread is awoken from waiting in the window, or when the next sample is due to be rendered.</span></span> <span data-ttu-id="e9d85-113">В конечном итоге он может использоваться для сбора информации, управляющей синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="e9d85-113">It could eventually be used to gather information that controls synchronization.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d85-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e9d85-114">Requirements</span></span>



| <span data-ttu-id="e9d85-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e9d85-115">Requirement</span></span> | <span data-ttu-id="e9d85-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e9d85-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d85-117">Header</span><span class="sxs-lookup"><span data-stu-id="e9d85-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e9d85-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9d85-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9d85-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e9d85-119">Library</span></span><br/> | <dl> <span data-ttu-id="e9d85-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e9d85-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9d85-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9d85-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9d85-122">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="e9d85-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




