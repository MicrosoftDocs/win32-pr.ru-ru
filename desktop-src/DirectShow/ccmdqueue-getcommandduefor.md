---
description: Метод Жеткомманддуефор извлекает отложенную команду, которая запланирована в указанное время.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Ккмдкуеуе. Жеткомманддуефор, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674869"
---
# <a name="ccmdqueuegetcommandduefor-method"></a><span data-ttu-id="cd73c-103">Ккмдкуеуе. Жеткомманддуефор, метод</span><span class="sxs-lookup"><span data-stu-id="cd73c-103">CCmdQueue.GetCommandDueFor method</span></span>

<span data-ttu-id="cd73c-104">`GetCommandDueFor`Метод получает отложенную команду, которая запланирована в указанное время.</span><span class="sxs-lookup"><span data-stu-id="cd73c-104">The `GetCommandDueFor` method retrieves a deferred command that is scheduled at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd73c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd73c-105">Syntax</span></span>


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="cd73c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd73c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd73c-107">*тстреам*</span><span class="sxs-lookup"><span data-stu-id="cd73c-107">*tStream*</span></span> 
</dt> <dd>

<span data-ttu-id="cd73c-108">Время, для которого запланирована команда.</span><span class="sxs-lookup"><span data-stu-id="cd73c-108">Time for which the command is scheduled.</span></span>

</dd> <dt>

<span data-ttu-id="cd73c-109">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="cd73c-109">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="cd73c-110">Адрес указателя на отложенную команду, которая должна быть выполнена в момент, указанный в параметре *тстреам* .</span><span class="sxs-lookup"><span data-stu-id="cd73c-110">Address of a pointer to the deferred command to be carried out at the time specified in the *tStream* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd73c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd73c-111">Return value</span></span>

<span data-ttu-id="cd73c-112">Возвращает VFW \_ E \_ не \_ найдено, если нет ни одной команды; в противном случае возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cd73c-112">Returns VFW\_E\_NOT\_FOUND if no commands are due; otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd73c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd73c-113">Remarks</span></span>

<span data-ttu-id="cd73c-114">Эта функция-член принимает потоковое время и возвращает отложенную команду, запланированную в это время.</span><span class="sxs-lookup"><span data-stu-id="cd73c-114">This member function takes a stream time and returns the deferred command scheduled at that time.</span></span> <span data-ttu-id="cd73c-115">Фактическое смещение времени потока вычисляется при выполнении очереди команд.</span><span class="sxs-lookup"><span data-stu-id="cd73c-115">The actual stream-time offset is calculated when the command queue is run.</span></span> <span data-ttu-id="cd73c-116">Команды остаются в очереди до выполнения или отмены.</span><span class="sxs-lookup"><span data-stu-id="cd73c-116">Commands remain queued until run or canceled.</span></span> <span data-ttu-id="cd73c-117">Эта функция члена не будет блокироваться.</span><span class="sxs-lookup"><span data-stu-id="cd73c-117">This member function will not block.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd73c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cd73c-118">Requirements</span></span>



| <span data-ttu-id="cd73c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cd73c-119">Requirement</span></span> | <span data-ttu-id="cd73c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cd73c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd73c-121">Header</span><span class="sxs-lookup"><span data-stu-id="cd73c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cd73c-122"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd73c-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cd73c-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cd73c-123">Library</span></span><br/> | <dl> <span data-ttu-id="cd73c-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cd73c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd73c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd73c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd73c-126">**Класс Ккмдкуеуе**</span><span class="sxs-lookup"><span data-stu-id="cd73c-126">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




