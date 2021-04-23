---
description: Метод Ваитмсг ожидает получения сигнала о событии при диспетчеризации отправленных сообщений.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Каммсжевент. Ваитмсг, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9622e962f130a082a5c1206367f4850cebb6ce02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657160"
---
# <a name="cammsgeventwaitmsg-method"></a><span data-ttu-id="87d20-103">Каммсжевент. Ваитмсг, метод</span><span class="sxs-lookup"><span data-stu-id="87d20-103">CAMMsgEvent.WaitMsg method</span></span>

<span data-ttu-id="87d20-104">`WaitMsg`Метод ожидает получения сигнала о событии при диспетчеризации отправленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="87d20-104">The `WaitMsg` method waits for the event to be signaled, while dispatching sent messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="87d20-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87d20-105">Syntax</span></span>


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="87d20-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87d20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87d20-107">*двтимеаут*</span><span class="sxs-lookup"><span data-stu-id="87d20-107">*dwTimeOut*</span></span> 
</dt> <dd>

<span data-ttu-id="87d20-108">Необязательное значение времени ожидания в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="87d20-108">Optional time-out value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87d20-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87d20-109">Return value</span></span>

<span data-ttu-id="87d20-110">Возвращает **значение true** , если событие является сигнальным, или **значение false** , если истекло время ожидания.</span><span class="sxs-lookup"><span data-stu-id="87d20-110">Returns **TRUE** if the event is signaled, or **FALSE** if the time-out occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d20-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87d20-111">Remarks</span></span>

<span data-ttu-id="87d20-112">Этот метод вызывает функцию PeekMessage для обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="87d20-112">This method calls the PeekMessage function to process messages.</span></span> <span data-ttu-id="87d20-113">Вызовите этот метод вместо [**камевент:: wait**](camevent-wait.md) , если поток должен обрабатывать сообщения при ожидании события.</span><span class="sxs-lookup"><span data-stu-id="87d20-113">Call this method instead of [**CAMEvent::Wait**](camevent-wait.md) if your thread needs to process messages while waiting for an event.</span></span> <span data-ttu-id="87d20-114">Если поток не обрабатывает сообщения и другой поток отправляет сообщение, может произойти взаимоблокировка.</span><span class="sxs-lookup"><span data-stu-id="87d20-114">If the thread does not process messages and another thread sends a message, deadlock could occur.</span></span>

<span data-ttu-id="87d20-115">Например, предположим, что создается поток, а затем блокируется до инициализации потока.</span><span class="sxs-lookup"><span data-stu-id="87d20-115">For example, suppose you create a thread and then block until the thread initializes.</span></span> <span data-ttu-id="87d20-116">Если поток отправляет сообщение в окно с помощью вызова функции SendMessage, это приведет к взаимоблокировке.</span><span class="sxs-lookup"><span data-stu-id="87d20-116">If the thread sends a message to your window by calling the SendMessage function, it will result in a deadlock.</span></span> <span data-ttu-id="87d20-117">Это обусловлено тем, что SendMessage не возвращает значение, пока сообщение не будет обработано.</span><span class="sxs-lookup"><span data-stu-id="87d20-117">This is because SendMessage does not return until the message has been processed.</span></span> <span data-ttu-id="87d20-118">Вызов Ваитмсг позволяет вернуть вызов SendMessage, предотвращая взаимоблокировку.</span><span class="sxs-lookup"><span data-stu-id="87d20-118">Calling WaitMsg allows the SendMessage call to return, preventing the deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d20-119">Требования</span><span class="sxs-lookup"><span data-stu-id="87d20-119">Requirements</span></span>



| <span data-ttu-id="87d20-120">Требование</span><span class="sxs-lookup"><span data-stu-id="87d20-120">Requirement</span></span> | <span data-ttu-id="87d20-121">Значение</span><span class="sxs-lookup"><span data-stu-id="87d20-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87d20-122">Header</span><span class="sxs-lookup"><span data-stu-id="87d20-122">Header</span></span><br/>  | <dl> <span data-ttu-id="87d20-123"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87d20-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="87d20-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87d20-124">Library</span></span><br/> | <dl> <span data-ttu-id="87d20-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="87d20-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87d20-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87d20-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d20-127">**Класс Каммсжевент**</span><span class="sxs-lookup"><span data-stu-id="87d20-127">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




