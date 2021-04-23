---
description: Приостанавливает работу объекта. Реализует метод Имедиафилтер::P Аусе.
ms.assetid: 4f4cbe7e-3004-4731-864f-737c2f51afff
title: Метод Кбасемедиафилтер. Pause (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a75cbcf1d629b997584cff35ebd4095094fe8607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665239"
---
# <a name="cbasemediafilterpause-method"></a><span data-ttu-id="65fbb-104">Кбасемедиафилтер. Pause, метод</span><span class="sxs-lookup"><span data-stu-id="65fbb-104">CBaseMediaFilter.Pause method</span></span>

<span data-ttu-id="65fbb-105">Приостанавливает работу объекта.</span><span class="sxs-lookup"><span data-stu-id="65fbb-105">Pauses the object.</span></span> <span data-ttu-id="65fbb-106">Реализует метод [**имедиафилтер::P Аусе**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="65fbb-106">Implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="65fbb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65fbb-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="65fbb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="65fbb-108">Parameters</span></span>

<span data-ttu-id="65fbb-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="65fbb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65fbb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65fbb-110">Return value</span></span>

<span data-ttu-id="65fbb-111">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="65fbb-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="65fbb-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65fbb-112">Remarks</span></span>

<span data-ttu-id="65fbb-113">В базовом классе этот метод устанавливает переменную члена [**\_ состояния кбасемедиафилтер:: m**](cbasemediafilter-m-state.md) в состояние \_ приостановки, но не выполняет никаких других действий.</span><span class="sxs-lookup"><span data-stu-id="65fbb-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Paused but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="65fbb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="65fbb-114">Requirements</span></span>



| <span data-ttu-id="65fbb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="65fbb-115">Requirement</span></span> | <span data-ttu-id="65fbb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="65fbb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65fbb-117">Header</span><span class="sxs-lookup"><span data-stu-id="65fbb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="65fbb-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65fbb-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="65fbb-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="65fbb-119">Library</span></span><br/> | <dl> <span data-ttu-id="65fbb-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="65fbb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65fbb-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65fbb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65fbb-122">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="65fbb-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




