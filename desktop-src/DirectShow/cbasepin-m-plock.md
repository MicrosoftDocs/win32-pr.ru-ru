---
description: Указатель на объект критической секции, защищающий состояние фильтра.
ms.assetid: e733360d-ed95-493f-a85b-53d584681f60
title: 'Элемент Кбасепин:: m_pLock (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0a18755c1ea1c5c29b9839ecaf8803a84f8c8f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669112"
---
# <a name="cbasepinm_plock-member"></a><span data-ttu-id="ac4bc-103">Элемент Кбасепин:: m \_ плокк</span><span class="sxs-lookup"><span data-stu-id="ac4bc-103">CBasePin::m\_pLock member</span></span>

<span data-ttu-id="ac4bc-104">Указатель на объект критической секции, защищающий состояние фильтра.</span><span class="sxs-lookup"><span data-stu-id="ac4bc-104">Pointer to a critical section object that protects the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac4bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac4bc-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="ac4bc-106">Требования</span><span class="sxs-lookup"><span data-stu-id="ac4bc-106">Requirements</span></span>



| <span data-ttu-id="ac4bc-107">Требование</span><span class="sxs-lookup"><span data-stu-id="ac4bc-107">Requirement</span></span> | <span data-ttu-id="ac4bc-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ac4bc-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4bc-109">Header</span><span class="sxs-lookup"><span data-stu-id="ac4bc-109">Header</span></span><br/>  | <dl> <span data-ttu-id="ac4bc-110"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac4bc-110"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ac4bc-111">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac4bc-111">Library</span></span><br/> | <dl> <span data-ttu-id="ac4bc-112"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ac4bc-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac4bc-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac4bc-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac4bc-114">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="ac4bc-114">**CBasePin Class**</span></span>](cbasepin.md)
</dt> <dt>

[<span data-ttu-id="ac4bc-115">Потоки и критические разделы</span><span class="sxs-lookup"><span data-stu-id="ac4bc-115">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




