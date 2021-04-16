---
description: Критическая секция, защищающая состояние фильтра. Дополнительные сведения см. в разделе поток данных для разработчиков фильтров.
ms.assetid: 75b9c8b0-e911-41fd-8d07-b854dbe25551
title: 'Элемент Ктрансформфилтер:: m_csFilter (Трансфрм. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 991b07aa654ce42a651f4fa169e757d8380fdc8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657751"
---
# <a name="ctransformfilterm_csfilter-member"></a><span data-ttu-id="e9286-104">Элемент Ктрансформфилтер:: m \_ ксфилтер</span><span class="sxs-lookup"><span data-stu-id="e9286-104">CTransformFilter::m\_csFilter member</span></span>

<span data-ttu-id="e9286-105">Критическая секция, защищающая состояние фильтра.</span><span class="sxs-lookup"><span data-stu-id="e9286-105">Critical section that protects the filter state.</span></span> <span data-ttu-id="e9286-106">Дополнительные сведения см. в разделе [поток данных для разработчиков фильтров](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="e9286-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9286-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9286-107">Syntax</span></span>


```C++
CCritSec m_csFilter;
```



## <a name="requirements"></a><span data-ttu-id="e9286-108">Требования</span><span class="sxs-lookup"><span data-stu-id="e9286-108">Requirements</span></span>



| <span data-ttu-id="e9286-109">Требование</span><span class="sxs-lookup"><span data-stu-id="e9286-109">Requirement</span></span> | <span data-ttu-id="e9286-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e9286-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9286-111">Header</span><span class="sxs-lookup"><span data-stu-id="e9286-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e9286-112"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9286-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e9286-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e9286-113">Library</span></span><br/> | <dl> <span data-ttu-id="e9286-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e9286-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9286-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9286-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9286-116">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="e9286-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




