---
description: Флаг, указывающий, был ли удален последний пример. Если метод Receive удаляет пример, он устанавливает значение TRUE.
ms.assetid: 6143f948-75b0-47c6-9951-4c18c0773857
title: 'Элемент Ктрансформфилтер:: m_bSampleSkipped (Трансфрм. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSampleSkipped
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 61d8ceda20fed4c8ec89538cbe9675ad1f3e4549
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657753"
---
# <a name="ctransformfilterm_bsampleskipped-member"></a><span data-ttu-id="958cf-104">Элемент Ктрансформфилтер:: m \_ бсамплескиппед</span><span class="sxs-lookup"><span data-stu-id="958cf-104">CTransformFilter::m\_bSampleSkipped member</span></span>

<span data-ttu-id="958cf-105">Флаг, указывающий, был ли удален последний пример.</span><span class="sxs-lookup"><span data-stu-id="958cf-105">Flag that indicates whether the most recent sample was dropped.</span></span> <span data-ttu-id="958cf-106">Если метод [**Receive**](ctransformfilter-receive.md) удаляет пример, он устанавливает значение **true**.</span><span class="sxs-lookup"><span data-stu-id="958cf-106">If the [**Receive**](ctransformfilter-receive.md) method drops a sample, it sets the value to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="958cf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="958cf-107">Syntax</span></span>


```C++
BOOL m_bSampleSkipped;
```



## <a name="requirements"></a><span data-ttu-id="958cf-108">Требования</span><span class="sxs-lookup"><span data-stu-id="958cf-108">Requirements</span></span>



| <span data-ttu-id="958cf-109">Требование</span><span class="sxs-lookup"><span data-stu-id="958cf-109">Requirement</span></span> | <span data-ttu-id="958cf-110">Значение</span><span class="sxs-lookup"><span data-stu-id="958cf-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="958cf-111">Header</span><span class="sxs-lookup"><span data-stu-id="958cf-111">Header</span></span><br/>  | <dl> <span data-ttu-id="958cf-112"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="958cf-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="958cf-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="958cf-113">Library</span></span><br/> | <dl> <span data-ttu-id="958cf-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="958cf-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="958cf-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="958cf-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="958cf-116">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="958cf-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




