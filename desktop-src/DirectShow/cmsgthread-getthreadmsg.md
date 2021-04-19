---
description: Извлекает объект КМСГ в очереди, содержащий запрос.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Кмсгсреад. Жетсреадмсг, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675659"
---
# <a name="cmsgthreadgetthreadmsg-method"></a><span data-ttu-id="78882-103">Кмсгсреад. Жетсреадмсг, метод</span><span class="sxs-lookup"><span data-stu-id="78882-103">CMsgThread.GetThreadMsg method</span></span>

<span data-ttu-id="78882-104">Извлекает объект [**КМСГ**](cmsg.md) в очереди, содержащий запрос.</span><span class="sxs-lookup"><span data-stu-id="78882-104">Retrieves a queued [**CMsg**](cmsg.md) object containing a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="78882-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78882-105">Syntax</span></span>


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a><span data-ttu-id="78882-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78882-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78882-107">*msg*</span><span class="sxs-lookup"><span data-stu-id="78882-107">*msg*</span></span> 
</dt> <dd>

<span data-ttu-id="78882-108">Указатель на выделенный объект [**КМСГ**](cmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="78882-108">Pointer to an allocated [**CMsg**](cmsg.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78882-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78882-109">Return value</span></span>

<span data-ttu-id="78882-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="78882-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78882-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78882-111">Remarks</span></span>

<span data-ttu-id="78882-112">Эта функция-член вызывается из закрытой функции [**среадпрок**](camthread-threadproc.md) рабочего потока для получения следующей функции-члена.</span><span class="sxs-lookup"><span data-stu-id="78882-112">This member function is called from the worker thread's private [**ThreadProc**](camthread-threadproc.md) function to retrieve the next member function.</span></span> <span data-ttu-id="78882-113">Параметр *MSG* должен указывать на выделенный объект [**КМСГ**](cmsg.md) , который будет заполнен параметрами для следующего запроса в очереди.</span><span class="sxs-lookup"><span data-stu-id="78882-113">The *msg* parameter should point to an allocated [**CMsg**](cmsg.md) object that will be filled with the parameters to the next request in the queue.</span></span> <span data-ttu-id="78882-114">Если нет запросов в очереди, эта функция-член блокируется до постановки следующего запроса в очередь (путем вызова функции-члена [**кмсгсреад::P утсреадмсг**](cmsgthread-putthreadmsg.md) ).</span><span class="sxs-lookup"><span data-stu-id="78882-114">If there are no queued requests, this member function blocks until the next request is queued (by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function).</span></span>

## <a name="requirements"></a><span data-ttu-id="78882-115">Требования</span><span class="sxs-lookup"><span data-stu-id="78882-115">Requirements</span></span>



| <span data-ttu-id="78882-116">Требование</span><span class="sxs-lookup"><span data-stu-id="78882-116">Requirement</span></span> | <span data-ttu-id="78882-117">Значение</span><span class="sxs-lookup"><span data-stu-id="78882-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78882-118">Header</span><span class="sxs-lookup"><span data-stu-id="78882-118">Header</span></span><br/>  | <dl> <span data-ttu-id="78882-119"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78882-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="78882-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="78882-120">Library</span></span><br/> | <dl> <span data-ttu-id="78882-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="78882-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78882-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78882-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78882-123">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="78882-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




