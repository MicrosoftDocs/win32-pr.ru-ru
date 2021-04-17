---
description: Метод Free вызывается во время операции дефиксации.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: Метод Кмемаллокатор. Free (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679968"
---
# <a name="cmemallocatorfree-method"></a><span data-ttu-id="7e5f2-103">Кмемаллокатор. Free, метод</span><span class="sxs-lookup"><span data-stu-id="7e5f2-103">CMemAllocator.Free method</span></span>

<span data-ttu-id="7e5f2-104">`Free`Метод вызывается во время операции дефиксации.</span><span class="sxs-lookup"><span data-stu-id="7e5f2-104">The `Free` method is called during a decommit operation.</span></span> <span data-ttu-id="7e5f2-105">Этот метод реализует чистый виртуальный метод [**кбасеаллокатор:: Free**](cbaseallocator-free.md) , но не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="7e5f2-105">This method implements the pure virtual [**CBaseAllocator::Free**](cbaseallocator-free.md) method, but does nothing.</span></span> <span data-ttu-id="7e5f2-106">Буферная память фактически не освобождается до тех пор, пока не будет уничтожен объект **кмемаллокатор** .</span><span class="sxs-lookup"><span data-stu-id="7e5f2-106">The buffer memory is not actually released until the **CMemAllocator** object is destroyed.</span></span> <span data-ttu-id="7e5f2-107">Метод деструктора вызывает [**кмемаллокатор:: реаллифри**](cmemallocator-reallyfree.md) для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="7e5f2-107">The destructor method calls [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md) to release the memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e5f2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e5f2-108">Syntax</span></span>


```C++
void Free();
```



## <a name="parameters"></a><span data-ttu-id="7e5f2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e5f2-109">Parameters</span></span>

<span data-ttu-id="7e5f2-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7e5f2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e5f2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e5f2-111">Return value</span></span>

<span data-ttu-id="7e5f2-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7e5f2-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e5f2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7e5f2-113">Requirements</span></span>



| <span data-ttu-id="7e5f2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7e5f2-114">Requirement</span></span> | <span data-ttu-id="7e5f2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7e5f2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e5f2-116">Header</span><span class="sxs-lookup"><span data-stu-id="7e5f2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7e5f2-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e5f2-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7e5f2-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7e5f2-118">Library</span></span><br/> | <dl> <span data-ttu-id="7e5f2-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7e5f2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e5f2-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e5f2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e5f2-121">**Класс Кмемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="7e5f2-121">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




