---
description: Указывает, насколько поздние образцы поступают в модуль подготовки отчетов в ссылочных единицах времени. Syntax.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Элемент Квидеотрансформфилтер:: m_itrLate (Втранс. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657649"
---
# <a name="cvideotransformfilterm_itrlate-member"></a><span data-ttu-id="b0bbf-104">Элемент Квидеотрансформфилтер:: m \_ итрлате</span><span class="sxs-lookup"><span data-stu-id="b0bbf-104">CVideoTransformFilter::m\_itrLate member</span></span>

<span data-ttu-id="b0bbf-105">Указывает, насколько поздние образцы поступают в модуль подготовки отчетов в ссылочных единицах времени.</span><span class="sxs-lookup"><span data-stu-id="b0bbf-105">Indicates how late the samples are arriving at the renderer, in reference time units.</span></span> <span data-ttu-id="b0bbf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0bbf-106">Syntax</span></span>

## <a name="syntax"></a><span data-ttu-id="b0bbf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0bbf-107">Syntax</span></span>


```C++
int m_itrLate;
```



## <a name="remarks"></a><span data-ttu-id="b0bbf-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0bbf-108">Remarks</span></span>

<span data-ttu-id="b0bbf-109">Когда фильтр получает сообщение о качестве подчиненного, он сохраняет значение просрочки в этой переменной.</span><span class="sxs-lookup"><span data-stu-id="b0bbf-109">When the filter receives a quality message from downstream, it stores the lateness value in this variable.</span></span> <span data-ttu-id="b0bbf-110">Поскольку фильтр удаляет кадры, он обновляет это значение, вычитая продолжительность каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="b0bbf-110">As the filter drops frames, it updates this value by subtracting the duration of each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0bbf-111">Требования</span><span class="sxs-lookup"><span data-stu-id="b0bbf-111">Requirements</span></span>



| <span data-ttu-id="b0bbf-112">Требование</span><span class="sxs-lookup"><span data-stu-id="b0bbf-112">Requirement</span></span> | <span data-ttu-id="b0bbf-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b0bbf-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0bbf-114">Header</span><span class="sxs-lookup"><span data-stu-id="b0bbf-114">Header</span></span><br/>  | <dl> <span data-ttu-id="b0bbf-115"><dt>Втранс. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0bbf-115"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b0bbf-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b0bbf-116">Library</span></span><br/> | <dl> <span data-ttu-id="b0bbf-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b0bbf-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0bbf-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0bbf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0bbf-119">**Класс Квидеотрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="b0bbf-119">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




