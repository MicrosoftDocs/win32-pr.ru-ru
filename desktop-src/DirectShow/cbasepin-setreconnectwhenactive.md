---
description: Метод Сетреконнектвхенактиве указывает, поддерживает ли ПИН-код динамическое повторное подключение.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Кбасепин. Сетреконнектвхенактиве, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665085"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a><span data-ttu-id="7a635-103">Кбасепин. Сетреконнектвхенактиве, метод</span><span class="sxs-lookup"><span data-stu-id="7a635-103">CBasePin.SetReconnectWhenActive method</span></span>

<span data-ttu-id="7a635-104">`SetReconnectWhenActive`Метод указывает, поддерживает ли ПИН-код динамическое повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="7a635-104">The `SetReconnectWhenActive` method specifies whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a635-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a635-105">Syntax</span></span>


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a><span data-ttu-id="7a635-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a635-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a635-107">*бканреконнект*</span><span class="sxs-lookup"><span data-stu-id="7a635-107">*bCanReconnect*</span></span> 
</dt> <dd>

<span data-ttu-id="7a635-108">Логическое значение, указывающее, может ли ПИН-код динамически переподключаться.</span><span class="sxs-lookup"><span data-stu-id="7a635-108">Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="7a635-109">Если **значение — true**, ПИН-код может динамически переподключаться.</span><span class="sxs-lookup"><span data-stu-id="7a635-109">If **TRUE**, the pin can dynamically reconnect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a635-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a635-110">Return value</span></span>

<span data-ttu-id="7a635-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7a635-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a635-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a635-112">Remarks</span></span>

<span data-ttu-id="7a635-113">По умолчанию перед повторным подключением к любому из его ПИН-кодов необходимо отключить фильтр.</span><span class="sxs-lookup"><span data-stu-id="7a635-113">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="7a635-114">Если ПИН-код может повторно подключиться, пока фильтр активен, вызовите этот метод со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="7a635-114">If the pin can reconnect while the filter is active, call this method with a value of **TRUE**.</span></span> <span data-ttu-id="7a635-115">Дополнительные сведения см. в разделе [динамическое построение графа](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="7a635-115">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a635-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7a635-116">Requirements</span></span>



| <span data-ttu-id="7a635-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7a635-117">Requirement</span></span> | <span data-ttu-id="7a635-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7a635-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a635-119">Header</span><span class="sxs-lookup"><span data-stu-id="7a635-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7a635-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a635-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7a635-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7a635-121">Library</span></span><br/> | <dl> <span data-ttu-id="7a635-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7a635-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a635-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a635-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a635-124">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="7a635-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




