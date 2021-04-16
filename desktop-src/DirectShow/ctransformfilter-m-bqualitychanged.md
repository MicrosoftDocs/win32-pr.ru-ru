---
description: Флаг, указывающий, изменилось ли качество.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Элемент Ктрансформфилтер:: m_bQualityChanged (Трансфрм. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679643"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a><span data-ttu-id="73a71-103">Элемент Ктрансформфилтер:: m \_ бкуалитичанжед</span><span class="sxs-lookup"><span data-stu-id="73a71-103">CTransformFilter::m\_bQualityChanged member</span></span>

<span data-ttu-id="73a71-104">Флаг, указывающий, изменилось ли качество.</span><span class="sxs-lookup"><span data-stu-id="73a71-104">Flag that indicates whether the quality has changed.</span></span> <span data-ttu-id="73a71-105">В первый раз при удалении образца фильтр отправляет событие [**EC об \_ \_ изменении качества**](ec-quality-change.md) в Диспетчер графа фильтров и устанавливает для этого флага **значение true**.</span><span class="sxs-lookup"><span data-stu-id="73a71-105">The first time that the filter drops a sample, it sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager and sets this flag to **TRUE**.</span></span> <span data-ttu-id="73a71-106">Он не отправляет это событие повторно, пока фильтр не остановится и не перезапускается, даже если он продолжит удалять образцы.</span><span class="sxs-lookup"><span data-stu-id="73a71-106">It does not send this event again until the filter stops and restarts, even if it continues to drop samples in the meantime.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a71-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73a71-107">Syntax</span></span>


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a><span data-ttu-id="73a71-108">Требования</span><span class="sxs-lookup"><span data-stu-id="73a71-108">Requirements</span></span>



| <span data-ttu-id="73a71-109">Требование</span><span class="sxs-lookup"><span data-stu-id="73a71-109">Requirement</span></span> | <span data-ttu-id="73a71-110">Значение</span><span class="sxs-lookup"><span data-stu-id="73a71-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73a71-111">Header</span><span class="sxs-lookup"><span data-stu-id="73a71-111">Header</span></span><br/>  | <dl> <span data-ttu-id="73a71-112"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73a71-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="73a71-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="73a71-113">Library</span></span><br/> | <dl> <span data-ttu-id="73a71-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="73a71-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a71-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73a71-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a71-116">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="73a71-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




