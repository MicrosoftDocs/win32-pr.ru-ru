---
description: Включает или отключает ведение журнала отладки для данного критического раздела.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: Функция Дбглокктраце (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657223"
---
# <a name="dbglocktrace-function"></a><span data-ttu-id="21191-103">Функция Дбглокктраце</span><span class="sxs-lookup"><span data-stu-id="21191-103">DbgLockTrace function</span></span>

<span data-ttu-id="21191-104">Включает или отключает ведение журнала отладки для данного критического раздела.</span><span class="sxs-lookup"><span data-stu-id="21191-104">Enables or disables debug logging of a given critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="21191-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21191-105">Syntax</span></span>


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a><span data-ttu-id="21191-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="21191-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21191-107">*пккрит*</span><span class="sxs-lookup"><span data-stu-id="21191-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="21191-108">Указатель на критический раздел [**ккритсек**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="21191-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> <dt>

<span data-ttu-id="21191-109">*фтраце*</span><span class="sxs-lookup"><span data-stu-id="21191-109">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="21191-110">Значение, указывающее, включено ли ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="21191-110">Value specifying whether logging is enabled.</span></span> <span data-ttu-id="21191-111">Используйте **значение true** , чтобы включить ведение журнала, или **false** , чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="21191-111">Use **TRUE** to enable logging or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21191-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21191-112">Return value</span></span>

<span data-ttu-id="21191-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="21191-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21191-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21191-114">Remarks</span></span>

<span data-ttu-id="21191-115">Эта функция используется для трассировки определенной критической секции.</span><span class="sxs-lookup"><span data-stu-id="21191-115">Use this function to trace a specific critical section.</span></span> <span data-ttu-id="21191-116">По умолчанию ведение журнала отладки критических разделов отключено из-за большого количества критических разделов.</span><span class="sxs-lookup"><span data-stu-id="21191-116">By default, debug logging of critical sections is disabled, because of the large number of critical sections.</span></span>

<span data-ttu-id="21191-117">Чтобы выполнить трассировку критической секции, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="21191-117">To trace a critical section, perform the following steps:</span></span>

1.  <span data-ttu-id="21191-118">Определите ОТЛАДКу или \_ отладку перед включением заголовков DirectShow.</span><span class="sxs-lookup"><span data-stu-id="21191-118">Define DEBUG or \_DEBUG before you include the DirectShow headers.</span></span>
2.  <span data-ttu-id="21191-119">Включите ведение журнала отладки для критически важных разделов, вызвав [**дбгсетмодулелевел**](dbgsetmodulelevel.md) с \_ флагом блокировки журнала.</span><span class="sxs-lookup"><span data-stu-id="21191-119">Enable debug logging for critical sections, by calling [**DbgSetModuleLevel**](dbgsetmodulelevel.md) with the LOG\_LOCKING flag.</span></span>
3.  <span data-ttu-id="21191-120">Вызовите **дбглокктраце** в критическом разделе, который необходимо отследить.</span><span class="sxs-lookup"><span data-stu-id="21191-120">Call **DbgLockTrace** on the critical section you want to trace.</span></span>

<span data-ttu-id="21191-121">В розничных сборках функция **дбглокктраце** не действует.</span><span class="sxs-lookup"><span data-stu-id="21191-121">In retail builds, the **DbgLockTrace** function has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="21191-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="21191-122">Examples</span></span>

<span data-ttu-id="21191-123">В следующем примере кода показано, как отслеживать критическую секцию.</span><span class="sxs-lookup"><span data-stu-id="21191-123">The following code example shows how to trace a critical section.</span></span>


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
```



## <a name="requirements"></a><span data-ttu-id="21191-124">Требования</span><span class="sxs-lookup"><span data-stu-id="21191-124">Requirements</span></span>



| <span data-ttu-id="21191-125">Требование</span><span class="sxs-lookup"><span data-stu-id="21191-125">Requirement</span></span> | <span data-ttu-id="21191-126">Значение</span><span class="sxs-lookup"><span data-stu-id="21191-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21191-127">Header</span><span class="sxs-lookup"><span data-stu-id="21191-127">Header</span></span><br/>  | <dl> <span data-ttu-id="21191-128"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21191-128"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="21191-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21191-129">Library</span></span><br/> | <dl> <span data-ttu-id="21191-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="21191-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21191-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21191-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21191-132">Функции отладки критического раздела</span><span class="sxs-lookup"><span data-stu-id="21191-132">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




