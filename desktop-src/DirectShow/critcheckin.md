---
description: Возвращает значение TRUE, если текущий поток является владельцем указанной критической секции.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Функция Критчеккин (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff31707dc409db1e72c36866150c5a0b24c53f9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657171"
---
# <a name="critcheckin-function"></a><span data-ttu-id="a20b9-103">Функция Критчеккин</span><span class="sxs-lookup"><span data-stu-id="a20b9-103">CritCheckIn function</span></span>

<span data-ttu-id="a20b9-104">Возвращает **значение true** , если текущий поток является владельцем указанной критической секции.</span><span class="sxs-lookup"><span data-stu-id="a20b9-104">Returns **TRUE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="a20b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a20b9-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="a20b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a20b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a20b9-107">*пккрит*</span><span class="sxs-lookup"><span data-stu-id="a20b9-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="a20b9-108">Указатель на критический раздел [**ккритсек**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="a20b9-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a20b9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a20b9-109">Return value</span></span>

<span data-ttu-id="a20b9-110">В отладочных сборках возвращает **значение true** , если текущий поток является владельцем этой критической секции, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a20b9-110">In debug builds, returns **TRUE** if the current thread is the owner of this critical section, or **FALSE** otherwise.</span></span> <span data-ttu-id="a20b9-111">В розничных сборках всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a20b9-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a20b9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a20b9-112">Remarks</span></span>

<span data-ttu-id="a20b9-113">Эта функция особенно полезна в макросе [**Assert**](assert.md) , чтобы проверить, владеет ли поток заданной блокировкой.</span><span class="sxs-lookup"><span data-stu-id="a20b9-113">This function is especially useful within the [**ASSERT**](assert.md) macro, to test whether a thread owns a given lock.</span></span>

## <a name="examples"></a><span data-ttu-id="a20b9-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="a20b9-114">Examples</span></span>

<span data-ttu-id="a20b9-115">В следующем примере кода показано, как использовать эту функцию:</span><span class="sxs-lookup"><span data-stu-id="a20b9-115">The following code example shows how to use this function:</span></span>


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a><span data-ttu-id="a20b9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a20b9-116">Requirements</span></span>



| <span data-ttu-id="a20b9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a20b9-117">Requirement</span></span> | <span data-ttu-id="a20b9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a20b9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a20b9-119">Header</span><span class="sxs-lookup"><span data-stu-id="a20b9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a20b9-120"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a20b9-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a20b9-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a20b9-121">Library</span></span><br/> | <dl> <span data-ttu-id="a20b9-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a20b9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a20b9-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a20b9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a20b9-124">Функции отладки критического раздела</span><span class="sxs-lookup"><span data-stu-id="a20b9-124">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




