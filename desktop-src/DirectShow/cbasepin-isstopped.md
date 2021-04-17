---
description: Метод Stopped определяет, остановлен ли фильтр, содержащий этот ПИН-код.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Метод Кбасепин. Stopped (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657976"
---
# <a name="cbasepinisstopped-method"></a><span data-ttu-id="4096e-103">Кбасепин. метод Stopped</span><span class="sxs-lookup"><span data-stu-id="4096e-103">CBasePin.IsStopped method</span></span>

<span data-ttu-id="4096e-104">`IsStopped`Метод определяет, остановлен ли фильтр, содержащий этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="4096e-104">The `IsStopped` method determines whether the filter containing this pin is stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="4096e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4096e-105">Syntax</span></span>


```C++
BOOL IsStopped();
```



## <a name="parameters"></a><span data-ttu-id="4096e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4096e-106">Parameters</span></span>

<span data-ttu-id="4096e-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4096e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4096e-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4096e-108">Return value</span></span>

<span data-ttu-id="4096e-109">Возвращает **значение true** , если фильтр остановлен.</span><span class="sxs-lookup"><span data-stu-id="4096e-109">Returns **TRUE** if the filter is stopped.</span></span> <span data-ttu-id="4096e-110">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="4096e-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4096e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4096e-111">Remarks</span></span>

<span data-ttu-id="4096e-112">Не вызывайте этот метод из в методе конструктора **кбасепин** , так как фильтр, возможно, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="4096e-112">Do not call this method from within in the **CBasePin** constructor method, because the filter might not be initialized yet.</span></span>

## <a name="requirements"></a><span data-ttu-id="4096e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4096e-113">Requirements</span></span>



| <span data-ttu-id="4096e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4096e-114">Requirement</span></span> | <span data-ttu-id="4096e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4096e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4096e-116">Header</span><span class="sxs-lookup"><span data-stu-id="4096e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4096e-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4096e-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4096e-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4096e-118">Library</span></span><br/> | <dl> <span data-ttu-id="4096e-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4096e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4096e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4096e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4096e-121">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="4096e-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




