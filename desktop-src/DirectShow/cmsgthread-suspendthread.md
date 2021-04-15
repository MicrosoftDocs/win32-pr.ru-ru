---
description: Использует функцию Microsoft Win32 Суспендсреад для приостановки работы выполняющегося потока.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Кмсгсреад. Суспендсреад, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669394"
---
# <a name="cmsgthreadsuspendthread-method"></a><span data-ttu-id="c64fd-103">Кмсгсреад. Суспендсреад, метод</span><span class="sxs-lookup"><span data-stu-id="c64fd-103">CMsgThread.SuspendThread method</span></span>

<span data-ttu-id="c64fd-104">Использует функцию Microsoft Win32 **суспендсреад** для приостановки работы выполняющегося потока.</span><span class="sxs-lookup"><span data-stu-id="c64fd-104">Uses the Microsoft Win32 **SuspendThread** function to suspend the operation of a running thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="c64fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c64fd-105">Syntax</span></span>


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a><span data-ttu-id="c64fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c64fd-106">Parameters</span></span>

<span data-ttu-id="c64fd-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c64fd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c64fd-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c64fd-108">Return value</span></span>

<span data-ttu-id="c64fd-109">Если функция-член выполнена, возвращаемое значение является предыдущим счетчиком приостановок потока.</span><span class="sxs-lookup"><span data-stu-id="c64fd-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="c64fd-110">Если функция-член завершается ошибкой, возвращается значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c64fd-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="c64fd-111">Чтобы получить расширенные сведения об ошибке, вызовите функцию Microsoft Win32 **GetLastError** .</span><span class="sxs-lookup"><span data-stu-id="c64fd-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="c64fd-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c64fd-112">Remarks</span></span>

<span data-ttu-id="c64fd-113">Клиентский поток вызывает эту функцию члена для приостановки работы рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="c64fd-113">The client thread calls this member function to suspend the operation of the worker thread.</span></span> <span data-ttu-id="c64fd-114">Рабочий поток остается приостановленным и не будет выполняться до выполнения дополнительного вызова функции-члена [**кмсгсреад:: ресумесреад**](cmsgthread-resumethread.md) .</span><span class="sxs-lookup"><span data-stu-id="c64fd-114">The worker thread remains suspended and will not execute until an additional call to the [**CMsgThread::ResumeThread**](cmsgthread-resumethread.md) member function is made.</span></span>

## <a name="requirements"></a><span data-ttu-id="c64fd-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c64fd-115">Requirements</span></span>



| <span data-ttu-id="c64fd-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c64fd-116">Requirement</span></span> | <span data-ttu-id="c64fd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c64fd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c64fd-118">Header</span><span class="sxs-lookup"><span data-stu-id="c64fd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c64fd-119"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c64fd-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c64fd-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c64fd-120">Library</span></span><br/> | <dl> <span data-ttu-id="c64fd-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c64fd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c64fd-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c64fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c64fd-123">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="c64fd-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




