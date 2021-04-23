---
description: Метод Асинчронаусблоккаутпутпин блокирует ПИН-код. Метод может быть возвращен до того, как ПИН-код будет заблокирован.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Кдинамикаутпутпин. Асинчронаусблоккаутпутпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658084"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a><span data-ttu-id="8632b-104">Кдинамикаутпутпин. Асинчронаусблоккаутпутпин, метод</span><span class="sxs-lookup"><span data-stu-id="8632b-104">CDynamicOutputPin.AsynchronousBlockOutputPin method</span></span>

<span data-ttu-id="8632b-105">`AsynchronousBlockOutputPin`Метод блокирует ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="8632b-105">The `AsynchronousBlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="8632b-106">Метод может быть возвращен до того, как ПИН-код будет заблокирован.</span><span class="sxs-lookup"><span data-stu-id="8632b-106">The method might return before the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="8632b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8632b-107">Syntax</span></span>


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a><span data-ttu-id="8632b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8632b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8632b-109">*хнотификаллерпинблоккедевент*</span><span class="sxs-lookup"><span data-stu-id="8632b-109">*hNotifyCallerPinBlockedEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="8632b-110">Дескриптор события.</span><span class="sxs-lookup"><span data-stu-id="8632b-110">Handle to an event.</span></span> <span data-ttu-id="8632b-111">Событие получает сигнал, когда закрепление вывода блокируется или если вызывающий объект отменяет операцию блокировки.</span><span class="sxs-lookup"><span data-stu-id="8632b-111">The event is signaled when the output pin is blocked, or if the caller cancels the block operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8632b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8632b-112">Return value</span></span>

<span data-ttu-id="8632b-113">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8632b-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8632b-114">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8632b-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="8632b-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8632b-115">Return code</span></span>                                                                                                                    | <span data-ttu-id="8632b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8632b-116">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="8632b-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8632b-117"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="8632b-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="8632b-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="8632b-119"><dt>**\_ \_ ПИН-код VFW E \_ уже \_ заблокирован**</dt></span><span class="sxs-lookup"><span data-stu-id="8632b-119"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="8632b-120">ПИН-код уже заблокирован в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="8632b-120">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="8632b-121"><dt>**\_ \_ ПИН-код VFW E \_ уже \_ заблокирован \_ в \_ этом \_ потоке**</dt></span><span class="sxs-lookup"><span data-stu-id="8632b-121"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="8632b-122">ПИН-код уже заблокирован в вызывающем потоке.</span><span class="sxs-lookup"><span data-stu-id="8632b-122">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8632b-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8632b-123">Remarks</span></span>

<span data-ttu-id="8632b-124">Не вызывайте этот метод из потока потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="8632b-124">Do not call this method from the streaming thread.</span></span>

<span data-ttu-id="8632b-125">Если поток потоковой передачи не использует ПИН-код, этот метод немедленно блокирует ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="8632b-125">If no streaming thread is using the pin, this method immediately blocks the pin.</span></span> <span data-ttu-id="8632b-126">В противном случае он устанавливает состояние ПИН-кода "Pending" и возвращает.</span><span class="sxs-lookup"><span data-stu-id="8632b-126">Otherwise, it sets the pin status to "pending" and returns.</span></span> <span data-ttu-id="8632b-127">После завершения операции потоковой передачи поток потоковой передачи вызывает метод [**кдинамикаутпутпин:: стопусингаутпутпин**](cdynamicoutputpin-stopusingoutputpin.md) , который блокирует ПИН-код и сигнализирует о событии **хнотификаллерпинблоккедевент** .</span><span class="sxs-lookup"><span data-stu-id="8632b-127">When the streaming operation completes, the streaming thread calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, which blocks the pin and signals the **hNotifyCallerPinBlockedEvent** event.</span></span> <span data-ttu-id="8632b-128">Чтобы отменить незавершенный блок, вызовите метод [**кдинамикаутпутпин:: унблоккаутпутпин**](cdynamicoutputpin-unblockoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="8632b-128">To cancel a pending block, call the [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8632b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="8632b-129">Requirements</span></span>



| <span data-ttu-id="8632b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="8632b-130">Requirement</span></span> | <span data-ttu-id="8632b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8632b-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8632b-132">Header</span><span class="sxs-lookup"><span data-stu-id="8632b-132">Header</span></span><br/>  | <dl> <span data-ttu-id="8632b-133"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8632b-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8632b-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8632b-134">Library</span></span><br/> | <dl> <span data-ttu-id="8632b-135"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8632b-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8632b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8632b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8632b-137">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="8632b-137">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




