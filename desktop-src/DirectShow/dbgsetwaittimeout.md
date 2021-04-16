---
description: Задает значение времени ожидания отладки. Игнорируется в розничных сборках.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: Функция Дбгсетваиттимеаут (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657126"
---
# <a name="dbgsetwaittimeout-function"></a><span data-ttu-id="49b12-104">Функция Дбгсетваиттимеаут</span><span class="sxs-lookup"><span data-stu-id="49b12-104">DbgSetWaitTimeout function</span></span>

<span data-ttu-id="49b12-105">Задает значение времени ожидания отладки.</span><span class="sxs-lookup"><span data-stu-id="49b12-105">Sets the debugging time-out value.</span></span> <span data-ttu-id="49b12-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="49b12-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="49b12-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49b12-107">Syntax</span></span>


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="49b12-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="49b12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49b12-109">*двтимеаут*</span><span class="sxs-lookup"><span data-stu-id="49b12-109">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="49b12-110">Значение времени ожидания в миллисекундах или бесконечно, чтобы неограниченное время ожидания.</span><span class="sxs-lookup"><span data-stu-id="49b12-110">Time-out value in milliseconds, or INFINITE to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49b12-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49b12-111">Return value</span></span>

<span data-ttu-id="49b12-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="49b12-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49b12-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49b12-113">Remarks</span></span>

<span data-ttu-id="49b12-114">В отладочных сборках функции [**дбгваитформултиплеобжектс**](dbgwaitformultipleobjects.md) и [**дбгваитфорсинглеобжект**](dbgwaitforsingleobject.md) используют это значение в качестве интервала времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="49b12-114">In debug builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions use this value as the time-out interval.</span></span>

## <a name="requirements"></a><span data-ttu-id="49b12-115">Требования</span><span class="sxs-lookup"><span data-stu-id="49b12-115">Requirements</span></span>



| <span data-ttu-id="49b12-116">Требование</span><span class="sxs-lookup"><span data-stu-id="49b12-116">Requirement</span></span> | <span data-ttu-id="49b12-117">Значение</span><span class="sxs-lookup"><span data-stu-id="49b12-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49b12-118">Header</span><span class="sxs-lookup"><span data-stu-id="49b12-118">Header</span></span><br/>  | <dl> <span data-ttu-id="49b12-119"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49b12-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="49b12-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="49b12-120">Library</span></span><br/> | <dl> <span data-ttu-id="49b12-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="49b12-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49b12-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49b12-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49b12-123">Функции ожидания отладки</span><span class="sxs-lookup"><span data-stu-id="49b12-123">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




