---
description: Метод Канреконнектвхенактиве запрашивает, поддерживает ли ПИН-код динамическое повторное подключение.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Кбасепин. Канреконнектвхенактиве, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669014"
---
# <a name="cbasepincanreconnectwhenactive-method"></a><span data-ttu-id="d5d5a-103">Кбасепин. Канреконнектвхенактиве, метод</span><span class="sxs-lookup"><span data-stu-id="d5d5a-103">CBasePin.CanReconnectWhenActive method</span></span>

<span data-ttu-id="d5d5a-104">`CanReconnectWhenActive`Метод запрашивает, поддерживает ли ПИН-код динамическое повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="d5d5a-104">The `CanReconnectWhenActive` method queries whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d5a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5d5a-105">Syntax</span></span>


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a><span data-ttu-id="d5d5a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5d5a-106">Parameters</span></span>

<span data-ttu-id="d5d5a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d5d5a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5d5a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5d5a-108">Return value</span></span>

<span data-ttu-id="d5d5a-109">Возвращает логическое значение, указывающее, может ли ПИН-код динамически переподключаться.</span><span class="sxs-lookup"><span data-stu-id="d5d5a-109">Returns a Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="d5d5a-110">Если **значение — true**, ПИН-код может динамически переподключаться.</span><span class="sxs-lookup"><span data-stu-id="d5d5a-110">If **TRUE**, the pin can dynamically reconnect.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5d5a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5d5a-111">Remarks</span></span>

<span data-ttu-id="d5d5a-112">По умолчанию перед повторным подключением к любому из его ПИН-кодов необходимо отключить фильтр.</span><span class="sxs-lookup"><span data-stu-id="d5d5a-112">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="d5d5a-113">Однако если ПИН-код поддерживает динамическое повторное подключение, он может подключиться, пока фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="d5d5a-113">If a pin supports dynamic reconnection, however, it can reconnect while the filter is active.</span></span> <span data-ttu-id="d5d5a-114">Дополнительные сведения см. в разделе [динамическое построение графа](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="d5d5a-114">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5d5a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d5d5a-115">Requirements</span></span>



| <span data-ttu-id="d5d5a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d5d5a-116">Requirement</span></span> | <span data-ttu-id="d5d5a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d5d5a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d5a-118">Header</span><span class="sxs-lookup"><span data-stu-id="d5d5a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d5d5a-119"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5d5a-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d5d5a-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5d5a-120">Library</span></span><br/> | <dl> <span data-ttu-id="d5d5a-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d5d5a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d5a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5d5a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d5a-123">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="d5d5a-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




