---
description: Логическое значение, указывающее на то, что фильтр в данный момент удаляет кадры. Если это значение равно TRUE, фильтр продолжит удалять кадры до тех пор, пока не достигнет следующего ключевого кадра или пока не получит 30 Дельта-кадров в строке без ключевого кадра.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'Элемент Квидеотрансформфилтер:: m_bSkipping (Втранс. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7beb4073052149e246a55ffbb1ff057e836704c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657650"
---
# <a name="cvideotransformfilterm_bskipping-member"></a><span data-ttu-id="6c3ee-104">Элемент Квидеотрансформфилтер:: m \_ бскиппинг</span><span class="sxs-lookup"><span data-stu-id="6c3ee-104">CVideoTransformFilter::m\_bSkipping member</span></span>

<span data-ttu-id="6c3ee-105">Логическое значение, указывающее на то, что фильтр в данный момент удаляет кадры.</span><span class="sxs-lookup"><span data-stu-id="6c3ee-105">Boolean value that indicates whether the filter is currently dropping frames.</span></span> <span data-ttu-id="6c3ee-106">Если это значение равно **true**, фильтр продолжит удалять кадры до тех пор, пока не достигнет следующего ключевого кадра или пока не получит 30 Дельта-кадров в строке без ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="6c3ee-106">If this value is **TRUE**, the filter continues to drop frames until it reaches the next key frame, or until it receives 30 delta frames in a row without a key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c3ee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c3ee-107">Syntax</span></span>


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a><span data-ttu-id="6c3ee-108">Требования</span><span class="sxs-lookup"><span data-stu-id="6c3ee-108">Requirements</span></span>



| <span data-ttu-id="6c3ee-109">Требование</span><span class="sxs-lookup"><span data-stu-id="6c3ee-109">Requirement</span></span> | <span data-ttu-id="6c3ee-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6c3ee-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3ee-111">Header</span><span class="sxs-lookup"><span data-stu-id="6c3ee-111">Header</span></span><br/>  | <dl> <span data-ttu-id="6c3ee-112"><dt>Втранс. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c3ee-112"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6c3ee-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6c3ee-113">Library</span></span><br/> | <dl> <span data-ttu-id="6c3ee-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6c3ee-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c3ee-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c3ee-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3ee-116">**Класс Квидеотрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="6c3ee-116">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




