---
description: Метод Unlock разблокирует объект критической секции.
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: Метод Ккритсек. Unlock (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca84ce452d71d0d3111039d7a95d8f5dd3155058
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657594"
---
# <a name="ccritsecunlock-method"></a><span data-ttu-id="8afe1-103">Ккритсек. Unlock, метод</span><span class="sxs-lookup"><span data-stu-id="8afe1-103">CCritSec.Unlock method</span></span>

<span data-ttu-id="8afe1-104">Метод **Unlock** разблокирует объект критической секции.</span><span class="sxs-lookup"><span data-stu-id="8afe1-104">The **Unlock** method unlocks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8afe1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8afe1-105">Syntax</span></span>


```C++
void Unlock();
```



## <a name="parameters"></a><span data-ttu-id="8afe1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8afe1-106">Parameters</span></span>

<span data-ttu-id="8afe1-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8afe1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8afe1-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8afe1-108">Return value</span></span>

<span data-ttu-id="8afe1-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8afe1-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8afe1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8afe1-110">Remarks</span></span>

<span data-ttu-id="8afe1-111">Этот метод вызывает функцию [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) .</span><span class="sxs-lookup"><span data-stu-id="8afe1-111">This method calls the [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) function.</span></span> <span data-ttu-id="8afe1-112">Вызывайте этот метод один раз для каждого вызова метода [**ккритсек:: Lock**](ccritsec-lock.md) .</span><span class="sxs-lookup"><span data-stu-id="8afe1-112">Call this method once for each call to the [**CCritSec::Lock**](ccritsec-lock.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8afe1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8afe1-113">Requirements</span></span>



| <span data-ttu-id="8afe1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8afe1-114">Requirement</span></span> | <span data-ttu-id="8afe1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8afe1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8afe1-116">Header</span><span class="sxs-lookup"><span data-stu-id="8afe1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8afe1-117"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8afe1-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8afe1-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8afe1-118">Library</span></span><br/> | <dl> <span data-ttu-id="8afe1-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8afe1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8afe1-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8afe1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8afe1-121">**Класс Ккритсек**</span><span class="sxs-lookup"><span data-stu-id="8afe1-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

