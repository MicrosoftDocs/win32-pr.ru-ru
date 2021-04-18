---
description: Метод Жетдуехандле извлекает дескриптор события для получения сигнала.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Ккмдкуеуе. Жетдуехандле, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb7c8c965c72abe6343a8a75863e0e6969dc5c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674865"
---
# <a name="ccmdqueuegetduehandle-method"></a><span data-ttu-id="15a7d-103">Ккмдкуеуе. Жетдуехандле, метод</span><span class="sxs-lookup"><span data-stu-id="15a7d-103">CCmdQueue.GetDueHandle method</span></span>

<span data-ttu-id="15a7d-104">`GetDueHandle`Метод получает дескриптор события для получения сигнала.</span><span class="sxs-lookup"><span data-stu-id="15a7d-104">The `GetDueHandle` method retrieves the event handle to be signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a7d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15a7d-105">Syntax</span></span>


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a><span data-ttu-id="15a7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="15a7d-106">Parameters</span></span>

<span data-ttu-id="15a7d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="15a7d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15a7d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15a7d-108">Return value</span></span>

<span data-ttu-id="15a7d-109">Возвращает маркер события.</span><span class="sxs-lookup"><span data-stu-id="15a7d-109">Returns the event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="15a7d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15a7d-110">Remarks</span></span>

<span data-ttu-id="15a7d-111">Возвращают обработчики событий при наличии отложенных команд, которые должны быть вызваны выполнением (когда [**ккмдкуеуе:: жетдуекомманд**](ccmdqueue-getduecommand.md) не будет блокироваться).</span><span class="sxs-lookup"><span data-stu-id="15a7d-111">Return the event handle whenever there are deferred commands that are due for execution (when [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md) will not block).</span></span>

## <a name="requirements"></a><span data-ttu-id="15a7d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="15a7d-112">Requirements</span></span>



| <span data-ttu-id="15a7d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="15a7d-113">Requirement</span></span> | <span data-ttu-id="15a7d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="15a7d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15a7d-115">Header</span><span class="sxs-lookup"><span data-stu-id="15a7d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="15a7d-116"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15a7d-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15a7d-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="15a7d-117">Library</span></span><br/> | <dl> <span data-ttu-id="15a7d-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="15a7d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a7d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15a7d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a7d-120">**Класс Ккмдкуеуе**</span><span class="sxs-lookup"><span data-stu-id="15a7d-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




