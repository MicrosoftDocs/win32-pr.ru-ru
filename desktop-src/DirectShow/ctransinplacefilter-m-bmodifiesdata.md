---
description: '\_Переменная-член m бмодифиесдата указывает, изменяет ли фильтр демонстрационные данные, которые получают. Значение задается в конструкторе Ктрансинплацефилтер, но значением по умолчанию является TRUE.'
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Элемент Ктрансинплацефилтер:: m_bModifiesData (Трансип. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5bc0d630fd0eda6e9915f8c11f5b15d21b725ce8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657329"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a><span data-ttu-id="81dfa-104">Элемент Ктрансинплацефилтер:: m \_ бмодифиесдата</span><span class="sxs-lookup"><span data-stu-id="81dfa-104">CTransInPlaceFilter::m\_bModifiesData member</span></span>

<span data-ttu-id="81dfa-105">`m_bModifiesData`Переменная-член указывает, изменяет ли фильтр получаемый образец данных.</span><span class="sxs-lookup"><span data-stu-id="81dfa-105">The `m_bModifiesData` member variable indicates whether the filter modifies the sample data that is receives.</span></span> <span data-ttu-id="81dfa-106">Значение задается в конструкторе **ктрансинплацефилтер** , но значением по умолчанию является **true**.</span><span class="sxs-lookup"><span data-stu-id="81dfa-106">The value is set in the **CTransInPlaceFilter** constructor, but defaults to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="81dfa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81dfa-107">Syntax</span></span>


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a><span data-ttu-id="81dfa-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="81dfa-108">Remarks</span></span>

<span data-ttu-id="81dfa-109">Эта переменная влияет на то, как фильтр согласовывает распределитель.</span><span class="sxs-lookup"><span data-stu-id="81dfa-109">This variable affects how the filter negotiates the allocator.</span></span> <span data-ttu-id="81dfa-110">Если значение равно **true**, фильтр не может использовать распределитель только для чтения для обоих подключений.</span><span class="sxs-lookup"><span data-stu-id="81dfa-110">If the value is **TRUE**, the filter cannot use a read-only allocator for both pin connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="81dfa-111">Требования</span><span class="sxs-lookup"><span data-stu-id="81dfa-111">Requirements</span></span>



| <span data-ttu-id="81dfa-112">Требование</span><span class="sxs-lookup"><span data-stu-id="81dfa-112">Requirement</span></span> | <span data-ttu-id="81dfa-113">Значение</span><span class="sxs-lookup"><span data-stu-id="81dfa-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81dfa-114">Header</span><span class="sxs-lookup"><span data-stu-id="81dfa-114">Header</span></span><br/>  | <dl> <span data-ttu-id="81dfa-115"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81dfa-115"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81dfa-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81dfa-116">Library</span></span><br/> | <dl> <span data-ttu-id="81dfa-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="81dfa-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81dfa-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81dfa-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81dfa-119">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="81dfa-119">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




