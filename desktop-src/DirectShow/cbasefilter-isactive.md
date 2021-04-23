---
description: Метод «onactive» определяет, активен ли фильтр (выполняется или приостановлен).
ms.assetid: 3bbb50d5-6a07-4932-940c-4466b95e6412
title: Метод Кбасефилтер. onactive (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63cf2cd78bb61562c9b4d6a09de3d88c88d4c643
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657800"
---
# <a name="cbasefilterisactive-method"></a><span data-ttu-id="78b69-103">Кбасефилтер. on, метод</span><span class="sxs-lookup"><span data-stu-id="78b69-103">CBaseFilter.IsActive method</span></span>

<span data-ttu-id="78b69-104">`IsActive`Метод определяет, активен ли фильтр (выполняется или приостановлен).</span><span class="sxs-lookup"><span data-stu-id="78b69-104">The `IsActive` method determines whether the filter is currently active (running or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="78b69-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78b69-105">Syntax</span></span>


```C++
BOOL IsActive();
```



## <a name="parameters"></a><span data-ttu-id="78b69-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78b69-106">Parameters</span></span>

<span data-ttu-id="78b69-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="78b69-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="78b69-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78b69-108">Return value</span></span>

<span data-ttu-id="78b69-109">Возвращает **значение true** , если фильтр приостановлен или выполняется, или **значение false** , если он остановлен.</span><span class="sxs-lookup"><span data-stu-id="78b69-109">Returns **TRUE** if the filter is paused or running, or **FALSE** if it is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="78b69-110">Требования</span><span class="sxs-lookup"><span data-stu-id="78b69-110">Requirements</span></span>



| <span data-ttu-id="78b69-111">Требование</span><span class="sxs-lookup"><span data-stu-id="78b69-111">Requirement</span></span> | <span data-ttu-id="78b69-112">Значение</span><span class="sxs-lookup"><span data-stu-id="78b69-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78b69-113">Header</span><span class="sxs-lookup"><span data-stu-id="78b69-113">Header</span></span><br/>  | <dl> <span data-ttu-id="78b69-114"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78b69-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="78b69-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="78b69-115">Library</span></span><br/> | <dl> <span data-ttu-id="78b69-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="78b69-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78b69-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78b69-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78b69-118">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="78b69-118">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




