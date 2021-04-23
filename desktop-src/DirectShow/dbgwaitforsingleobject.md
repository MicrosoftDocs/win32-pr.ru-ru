---
description: Ожидает, пока объект станет сигнальным.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Функция Дбгваитфорсинглеобжект (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679976"
---
# <a name="dbgwaitforsingleobject-function"></a><span data-ttu-id="c3d8d-103">Функция Дбгваитфорсинглеобжект</span><span class="sxs-lookup"><span data-stu-id="c3d8d-103">DbgWaitForSingleObject function</span></span>

<span data-ttu-id="c3d8d-104">Ожидает, пока объект станет сигнальным.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-104">Waits for an object to become signaled.</span></span>

<span data-ttu-id="c3d8d-105">В отладочной сборке эта функция активирует утверждение, если интервал времени ожидания истекает до получения сигнала от объекта.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-105">In a debug build, this function triggers an assert if the time-out interval expires before the object is signaled.</span></span> <span data-ttu-id="c3d8d-106">Чтобы установить интервал времени ожидания, вызовите функцию [**дбгсетваиттимеаут**](dbgsetwaittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="c3d8d-107">В розничной сборке эта функция эквивалентна функции **WaitForSingleObject** с интервалом времени ожидания, равным бесконечности.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-107">In a retail build, this function is equivalent to the **WaitForSingleObject** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d8d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3d8d-108">Syntax</span></span>


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a><span data-ttu-id="c3d8d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3d8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3d8d-110">*h*</span><span class="sxs-lookup"><span data-stu-id="c3d8d-110">*h*</span></span> 
</dt> <dd>

<span data-ttu-id="c3d8d-111">Обработчик для объекта.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-111">Handle to the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3d8d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c3d8d-112">Requirements</span></span>



| <span data-ttu-id="c3d8d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c3d8d-113">Requirement</span></span> | <span data-ttu-id="c3d8d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c3d8d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d8d-115">Header</span><span class="sxs-lookup"><span data-stu-id="c3d8d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c3d8d-116"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d8d-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3d8d-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3d8d-117">Library</span></span><br/> | <dl> <span data-ttu-id="c3d8d-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d8d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3d8d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3d8d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d8d-120">Функции ожидания отладки</span><span class="sxs-lookup"><span data-stu-id="c3d8d-120">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




