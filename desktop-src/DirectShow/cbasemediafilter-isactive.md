---
description: Метод «GetObject» определяет, является ли объект активным (запущен или приостановлен).
ms.assetid: 6531cf1f-e057-4094-9354-d5a32371c83c
title: Метод Кбасемедиафилтер. onactive (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6438850b90309b47fbe1fb76b1fd4f7baea8f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665277"
---
# <a name="cbasemediafilterisactive-method"></a><span data-ttu-id="1cb46-103">Кбасемедиафилтер. on, метод</span><span class="sxs-lookup"><span data-stu-id="1cb46-103">CBaseMediaFilter.IsActive method</span></span>

<span data-ttu-id="1cb46-104">`IsActive`Метод определяет, является ли объект активным (запущен или приостановлен).</span><span class="sxs-lookup"><span data-stu-id="1cb46-104">The `IsActive` method determines whether the object is active (running or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="1cb46-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cb46-105">Syntax</span></span>


```C++
BOOL IsActive();
```



## <a name="parameters"></a><span data-ttu-id="1cb46-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cb46-106">Parameters</span></span>

<span data-ttu-id="1cb46-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1cb46-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cb46-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1cb46-108">Return value</span></span>

<span data-ttu-id="1cb46-109">Возвращает **значение true** , если объект приостановлен или запущен, или **значение false** , если он остановлен.</span><span class="sxs-lookup"><span data-stu-id="1cb46-109">Returns **TRUE** if the object is paused or running, or **FALSE** if it is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cb46-110">Требования</span><span class="sxs-lookup"><span data-stu-id="1cb46-110">Requirements</span></span>



| <span data-ttu-id="1cb46-111">Требование</span><span class="sxs-lookup"><span data-stu-id="1cb46-111">Requirement</span></span> | <span data-ttu-id="1cb46-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1cb46-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb46-113">Header</span><span class="sxs-lookup"><span data-stu-id="1cb46-113">Header</span></span><br/>  | <dl> <span data-ttu-id="1cb46-114"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cb46-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1cb46-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1cb46-115">Library</span></span><br/> | <dl> <span data-ttu-id="1cb46-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1cb46-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cb46-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1cb46-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb46-118">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="1cb46-118">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




