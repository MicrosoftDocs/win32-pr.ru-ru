---
description: Ожидает сигнала для всех (или всех) указанных объектов.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Функция Дбгваитформултиплеобжектс (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658031"
---
# <a name="dbgwaitformultipleobjects-function"></a><span data-ttu-id="d8931-103">Функция Дбгваитформултиплеобжектс</span><span class="sxs-lookup"><span data-stu-id="d8931-103">DbgWaitForMultipleObjects function</span></span>

<span data-ttu-id="d8931-104">Ожидает сигнала для всех (или всех) указанных объектов.</span><span class="sxs-lookup"><span data-stu-id="d8931-104">Waits for any (or all) of the specified objects to be signaled.</span></span>

<span data-ttu-id="d8931-105">В отладочной сборке эта функция активирует утверждение, если интервал времени ожидания истекает до того, как объекты будут сигнальными.</span><span class="sxs-lookup"><span data-stu-id="d8931-105">In a debug build, this function triggers an assert if the time-out interval expires before the objects are signaled.</span></span> <span data-ttu-id="d8931-106">Чтобы установить интервал времени ожидания, вызовите функцию [**дбгсетваиттимеаут**](dbgsetwaittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="d8931-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="d8931-107">В розничной сборке эта функция эквивалентна функции **WaitForMultipleObjects** с интервалом времени ожидания, равным бесконечности.</span><span class="sxs-lookup"><span data-stu-id="d8931-107">In a retail build, this function is equivalent to the **WaitForMultipleObjects** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8931-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8931-108">Syntax</span></span>


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a><span data-ttu-id="d8931-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8931-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8931-110">*нкаунт*</span><span class="sxs-lookup"><span data-stu-id="d8931-110">*nCount*</span></span> 
</dt> <dd>

<span data-ttu-id="d8931-111">Число объектов.</span><span class="sxs-lookup"><span data-stu-id="d8931-111">Number of objects.</span></span>

</dd> <dt>

<span data-ttu-id="d8931-112">*лфандлес*</span><span class="sxs-lookup"><span data-stu-id="d8931-112">*lpHandles*</span></span> 
</dt> <dd>

<span data-ttu-id="d8931-113">Массив дескрипторов объектов размером *нкаунт*.</span><span class="sxs-lookup"><span data-stu-id="d8931-113">Array of handles to objects, of size *nCount*.</span></span>

</dd> <dt>

<span data-ttu-id="d8931-114">*бваиталл*</span><span class="sxs-lookup"><span data-stu-id="d8931-114">*bWaitAll*</span></span> 
</dt> <dd>

<span data-ttu-id="d8931-115">Логическое значение, указывающее, следует ли ожидать все объекты.</span><span class="sxs-lookup"><span data-stu-id="d8931-115">Boolean value that specifies whether to wait for all of the objects.</span></span> <span data-ttu-id="d8931-116">Если **значение равно true**, функция ожидает получения сигнала для всех объектов.</span><span class="sxs-lookup"><span data-stu-id="d8931-116">If **TRUE**, the function waits for all of the objects to be signaled.</span></span> <span data-ttu-id="d8931-117">В противном случае он ожидает сигнала хотя бы для одного объекта.</span><span class="sxs-lookup"><span data-stu-id="d8931-117">Otherwise, it waits for at least one object to be signaled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8931-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d8931-118">Requirements</span></span>



| <span data-ttu-id="d8931-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d8931-119">Requirement</span></span> | <span data-ttu-id="d8931-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d8931-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8931-121">Header</span><span class="sxs-lookup"><span data-stu-id="d8931-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d8931-122"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8931-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8931-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d8931-123">Library</span></span><br/> | <dl> <span data-ttu-id="d8931-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d8931-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8931-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8931-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8931-126">Функции ожидания отладки</span><span class="sxs-lookup"><span data-stu-id="d8931-126">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




