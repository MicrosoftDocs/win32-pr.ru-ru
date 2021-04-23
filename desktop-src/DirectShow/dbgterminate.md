---
description: Функция Дбгтерминате очищает библиотеку отладки. Игнорируется в розничных сборках.
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: Функция Дбгтерминате (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29e5fde86b9573261e39a0dbe2e9d87018ff23c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675265"
---
# <a name="dbgterminate-function"></a><span data-ttu-id="1575d-104">Функция Дбгтерминате</span><span class="sxs-lookup"><span data-stu-id="1575d-104">DbgTerminate function</span></span>

<span data-ttu-id="1575d-105">Функция **дбгтерминате** очищает библиотеку отладки.</span><span class="sxs-lookup"><span data-stu-id="1575d-105">The **DbgTerminate** function cleans up the debug library.</span></span> <span data-ttu-id="1575d-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="1575d-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="1575d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1575d-107">Syntax</span></span>


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a><span data-ttu-id="1575d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1575d-108">Parameters</span></span>

<span data-ttu-id="1575d-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="1575d-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1575d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1575d-110">Return value</span></span>

<span data-ttu-id="1575d-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1575d-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1575d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1575d-112">Remarks</span></span>

<span data-ttu-id="1575d-113">Вызовите эту функцию, если вызывается функция [**дбгинитиалисе**](dbginitialise.md) .</span><span class="sxs-lookup"><span data-stu-id="1575d-113">Call this function if you call the [**DbgInitialise**](dbginitialise.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1575d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1575d-114">Requirements</span></span>



| <span data-ttu-id="1575d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1575d-115">Requirement</span></span> | <span data-ttu-id="1575d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1575d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1575d-117">Header</span><span class="sxs-lookup"><span data-stu-id="1575d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1575d-118"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1575d-118"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1575d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1575d-119">Library</span></span><br/> | <dl> <span data-ttu-id="1575d-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1575d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1575d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1575d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1575d-122">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="1575d-122">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




