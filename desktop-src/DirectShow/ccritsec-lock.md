---
description: Метод Lock блокирует объект критической секции.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: Метод Ккритсек. Lock (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680083"
---
# <a name="ccritseclock-method"></a><span data-ttu-id="1a4ea-103">Ккритсек. Lock, метод</span><span class="sxs-lookup"><span data-stu-id="1a4ea-103">CCritSec.Lock method</span></span>

<span data-ttu-id="1a4ea-104">Метод **Lock** блокирует объект критической секции.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-104">The **Lock** method locks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a4ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a4ea-105">Syntax</span></span>


```C++
void Lock();
```



## <a name="parameters"></a><span data-ttu-id="1a4ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a4ea-106">Parameters</span></span>

<span data-ttu-id="1a4ea-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a4ea-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a4ea-108">Return value</span></span>

<span data-ttu-id="1a4ea-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a4ea-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a4ea-110">Remarks</span></span>

<span data-ttu-id="1a4ea-111">Этот метод вызывает функцию [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) .</span><span class="sxs-lookup"><span data-stu-id="1a4ea-111">This method calls the [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) function.</span></span>

<span data-ttu-id="1a4ea-112">Вызовите функцию члена [**ккритсек:: Unlock**](ccritsec-unlock.md) , чтобы разблокировать критическую секцию.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-112">Call the [**CCritSec::Unlock**](ccritsec-unlock.md) member function to unlock the critical section.</span></span> <span data-ttu-id="1a4ea-113">В одном потоке можно выполнить несколько вызовов метода **Lock** . не забудьте вызвать **разблокировку** соответствующего числа раз.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-113">You can make multiple calls to the **Lock** method on the same thread; be sure to call **Unlock** a corresponding number of times.</span></span>

<span data-ttu-id="1a4ea-114">Если объект уже заблокирован другим потоком, метод **ккритсек:: Lock** блокируется до освобождения объекта или до возникновения возможного исключения взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-114">If the object is already locked by another thread, the **CCritSec::Lock** method blocks until the object is released, or until a possible-deadlock exception occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a4ea-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1a4ea-115">Requirements</span></span>



| <span data-ttu-id="1a4ea-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1a4ea-116">Requirement</span></span> | <span data-ttu-id="1a4ea-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1a4ea-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4ea-118">Header</span><span class="sxs-lookup"><span data-stu-id="1a4ea-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1a4ea-119"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a4ea-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1a4ea-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1a4ea-120">Library</span></span><br/> | <dl> <span data-ttu-id="1a4ea-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1a4ea-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a4ea-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a4ea-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a4ea-123">**Класс Ккритсек**</span><span class="sxs-lookup"><span data-stu-id="1a4ea-123">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

