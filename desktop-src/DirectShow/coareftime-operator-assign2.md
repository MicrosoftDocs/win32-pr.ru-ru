---
description: Оператор назначает новое время ссылки и использует параметр "RT [ref]".
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: Коарефтиме. operator = метод (Ктлутил. h)-RT [ref] параметр
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105674767"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a><span data-ttu-id="13b7d-103">Коарефтиме. operator = метод (Ктлутил. h)-RT [ref] параметр</span><span class="sxs-lookup"><span data-stu-id="13b7d-103">COARefTime.operator= method (Ctlutil.h) - rt [ref] parameter</span></span>

<span data-ttu-id="13b7d-104">Этот оператор назначает новое время ссылки.</span><span class="sxs-lookup"><span data-stu-id="13b7d-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b7d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13b7d-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a><span data-ttu-id="13b7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="13b7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13b7d-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="13b7d-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="13b7d-108">Ссылка на значение [**\_ времени ссылки**](reference-time.md) , указывающее новое время ссылки в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="13b7d-108">Reference to a [**REFERENCE\_TIME**](reference-time.md) value that specifies the new reference time in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13b7d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13b7d-109">Return value</span></span>

<span data-ttu-id="13b7d-110">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="13b7d-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="13b7d-111">Требования</span><span class="sxs-lookup"><span data-stu-id="13b7d-111">Requirements</span></span>

| <span data-ttu-id="13b7d-112">Требование</span><span class="sxs-lookup"><span data-stu-id="13b7d-112">Requirement</span></span>                    | <span data-ttu-id="13b7d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="13b7d-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13b7d-114">Header</span><span class="sxs-lookup"><span data-stu-id="13b7d-114">Header</span></span>  | <span data-ttu-id="13b7d-115">Ктлутил. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="13b7d-115">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="13b7d-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13b7d-116">Library</span></span> | <span data-ttu-id="13b7d-117">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="13b7d-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="13b7d-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13b7d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13b7d-119">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="13b7d-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




