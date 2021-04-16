---
description: 'Использует функцию Microsoft Win32 Ресумесреад для продолжения работы рабочего потока после предыдущего вызова функции-члена Кмсгсреад:: Суспендсреад.'
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: Кмсгсреад. Ресумесреад, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679991"
---
# <a name="cmsgthreadresumethread-method"></a><span data-ttu-id="4ecdf-103">Кмсгсреад. Ресумесреад, метод</span><span class="sxs-lookup"><span data-stu-id="4ecdf-103">CMsgThread.ResumeThread method</span></span>

<span data-ttu-id="4ecdf-104">Использует функцию Microsoft Win32 **ресумесреад** для продолжения работы рабочего потока после предыдущего вызова функции-члена [**Кмсгсреад:: суспендсреад**](cmsgthread-suspendthread.md) .</span><span class="sxs-lookup"><span data-stu-id="4ecdf-104">Uses the Microsoft Win32 **ResumeThread** function to continue the operation of the worker thread after a previous call to the [**CMsgThread::SuspendThread**](cmsgthread-suspendthread.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ecdf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ecdf-105">Syntax</span></span>


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a><span data-ttu-id="4ecdf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ecdf-106">Parameters</span></span>

<span data-ttu-id="4ecdf-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4ecdf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ecdf-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ecdf-108">Return value</span></span>

<span data-ttu-id="4ecdf-109">Если функция-член выполнена, возвращаемое значение является предыдущим счетчиком приостановок потока.</span><span class="sxs-lookup"><span data-stu-id="4ecdf-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="4ecdf-110">Если функция-член завершается ошибкой, возвращается значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="4ecdf-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="4ecdf-111">Чтобы получить расширенные сведения об ошибке, вызовите функцию Microsoft Win32 **GetLastError** .</span><span class="sxs-lookup"><span data-stu-id="4ecdf-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ecdf-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4ecdf-112">Requirements</span></span>



| <span data-ttu-id="4ecdf-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4ecdf-113">Requirement</span></span> | <span data-ttu-id="4ecdf-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4ecdf-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ecdf-115">Header</span><span class="sxs-lookup"><span data-stu-id="4ecdf-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4ecdf-116"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ecdf-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4ecdf-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4ecdf-117">Library</span></span><br/> | <dl> <span data-ttu-id="4ecdf-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4ecdf-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ecdf-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ecdf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ecdf-120">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="4ecdf-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




