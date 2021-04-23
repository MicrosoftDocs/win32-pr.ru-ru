---
description: Создает поток.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Метод Кмсгсреад. CreateThread (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8951995de18158fe4d1e5f84b1d98da701067ab6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668659"
---
# <a name="cmsgthreadcreatethread-method"></a><span data-ttu-id="8c74a-103">Кмсгсреад. CreateThread, метод</span><span class="sxs-lookup"><span data-stu-id="8c74a-103">CMsgThread.CreateThread method</span></span>

<span data-ttu-id="8c74a-104">Создает поток.</span><span class="sxs-lookup"><span data-stu-id="8c74a-104">Creates a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c74a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c74a-105">Syntax</span></span>


```C++
BOOL CreateThread();
```



## <a name="parameters"></a><span data-ttu-id="8c74a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c74a-106">Parameters</span></span>

<span data-ttu-id="8c74a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8c74a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c74a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c74a-108">Return value</span></span>

<span data-ttu-id="8c74a-109">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8c74a-109">Returns one of the following values.</span></span>



| <span data-ttu-id="8c74a-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8c74a-110">Return code</span></span>                                                                              | <span data-ttu-id="8c74a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8c74a-111">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="8c74a-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="8c74a-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="8c74a-113">Поток успешно создан.</span><span class="sxs-lookup"><span data-stu-id="8c74a-113">Thread was successfully created.</span></span><br/>     |
| <dl> <span data-ttu-id="8c74a-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="8c74a-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="8c74a-115">Не удалось создать поток.</span><span class="sxs-lookup"><span data-stu-id="8c74a-115">Thread was not successfully created.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8c74a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c74a-116">Remarks</span></span>

<span data-ttu-id="8c74a-117">Поток выполняет цикл, блокируется до постановки запроса в очередь (с помощью функции-члена [**кмсгсреад::P утсреадмсг**](cmsgthread-putthreadmsg.md) ), а затем вызывает функцию-член [**Кмсгсреад:: среадмессажепрок**](cmsgthread-threadmessageproc.md) с каждым сообщением.</span><span class="sxs-lookup"><span data-stu-id="8c74a-117">The thread will loop, blocking until a request is queued (through the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then calling the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function with each message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c74a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8c74a-118">Requirements</span></span>



| <span data-ttu-id="8c74a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8c74a-119">Requirement</span></span> | <span data-ttu-id="8c74a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8c74a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c74a-121">Header</span><span class="sxs-lookup"><span data-stu-id="8c74a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8c74a-122"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c74a-122"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8c74a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c74a-123">Library</span></span><br/> | <dl> <span data-ttu-id="8c74a-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8c74a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c74a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c74a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c74a-126">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="8c74a-126">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




