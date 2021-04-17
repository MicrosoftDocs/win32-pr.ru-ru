---
description: Метод Пстателокк извлекает указатель на объект критической секции фильтра.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: Метод Ксаурце. Пстателокк (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0705584a513d64dfd1cd17075d95617234f7f8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685116"
---
# <a name="csourcepstatelock-method"></a><span data-ttu-id="4cc14-103">Ксаурце. Пстателокк, метод</span><span class="sxs-lookup"><span data-stu-id="4cc14-103">CSource.pStateLock method</span></span>

<span data-ttu-id="4cc14-104">Метод **пстателокк** извлекает указатель на объект критической секции фильтра.</span><span class="sxs-lookup"><span data-stu-id="4cc14-104">The **pStateLock** method retrieves a pointer to the filter's critical section object.</span></span>

> [!Note]  
> <span data-ttu-id="4cc14-105">Несмотря на то, что именование аналогично переменной-члену, **пстателокк** является методом.</span><span class="sxs-lookup"><span data-stu-id="4cc14-105">Although named like a member variable, **pStateLock** is a method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4cc14-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cc14-106">Syntax</span></span>


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a><span data-ttu-id="4cc14-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cc14-107">Parameters</span></span>

<span data-ttu-id="4cc14-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4cc14-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4cc14-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cc14-109">Return value</span></span>

<span data-ttu-id="4cc14-110">Возвращает указатель на переменную-член [**ксаурце:: m \_ кстателокк**](csource-m-cstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="4cc14-110">Returns a pointer to the [**CSource::m\_cStateLock**](csource-m-cstatelock.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cc14-111">Требования</span><span class="sxs-lookup"><span data-stu-id="4cc14-111">Requirements</span></span>



| <span data-ttu-id="4cc14-112">Требование</span><span class="sxs-lookup"><span data-stu-id="4cc14-112">Requirement</span></span> | <span data-ttu-id="4cc14-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4cc14-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc14-114">Header</span><span class="sxs-lookup"><span data-stu-id="4cc14-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4cc14-115"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cc14-115"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4cc14-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4cc14-116">Library</span></span><br/> | <dl> <span data-ttu-id="4cc14-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4cc14-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cc14-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cc14-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc14-119">**Класс Ксаурце**</span><span class="sxs-lookup"><span data-stu-id="4cc14-119">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




