---
description: Критическая секция, защищающая состояние потоковой передачи. Дополнительные сведения см. в разделе поток данных для разработчиков фильтров.
ms.assetid: f77c3129-ca25-47b8-8a6e-3a07169701af
title: 'Элемент Ктрансформфилтер:: m_csReceive (Трансфрм. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csReceive
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 542f108cee8dbe761040ef8474ae7cec565e0b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679641"
---
# <a name="ctransformfilterm_csreceive-member"></a><span data-ttu-id="03d69-104">Элемент Ктрансформфилтер:: m \_ ксрецеиве</span><span class="sxs-lookup"><span data-stu-id="03d69-104">CTransformFilter::m\_csReceive member</span></span>

<span data-ttu-id="03d69-105">Критическая секция, защищающая состояние потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="03d69-105">Critical section that protects the streaming state.</span></span> <span data-ttu-id="03d69-106">Дополнительные сведения см. в разделе [поток данных для разработчиков фильтров](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="03d69-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="03d69-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03d69-107">Syntax</span></span>


```C++
CCritSec m_csReceive;
```



## <a name="requirements"></a><span data-ttu-id="03d69-108">Требования</span><span class="sxs-lookup"><span data-stu-id="03d69-108">Requirements</span></span>



| <span data-ttu-id="03d69-109">Требование</span><span class="sxs-lookup"><span data-stu-id="03d69-109">Requirement</span></span> | <span data-ttu-id="03d69-110">Значение</span><span class="sxs-lookup"><span data-stu-id="03d69-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d69-111">Header</span><span class="sxs-lookup"><span data-stu-id="03d69-111">Header</span></span><br/>  | <dl> <span data-ttu-id="03d69-112"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03d69-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="03d69-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03d69-113">Library</span></span><br/> | <dl> <span data-ttu-id="03d69-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="03d69-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03d69-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03d69-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d69-116">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="03d69-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




