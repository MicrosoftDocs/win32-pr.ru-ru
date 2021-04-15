---
description: Переменная- \_ член m бусингимажеаллокатор указывает, является ли распределитель для соединения с закреплением объектом Цимажеаллокатор. Если значение равно TRUE, распределитель является объектом Цимажеаллокатор (или производным от этого класса).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Элемент Кдравимаже:: m_bUsingImageAllocator (Винутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e08d1e8217f42c6855759cefeef40e56949156fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668986"
---
# <a name="cdrawimagem_busingimageallocator-member"></a><span data-ttu-id="4a1b2-104">Элемент Кдравимаже:: m \_ бусингимажеаллокатор</span><span class="sxs-lookup"><span data-stu-id="4a1b2-104">CDrawImage::m\_bUsingImageAllocator member</span></span>

<span data-ttu-id="4a1b2-105">`m_bUsingImageAllocator`Переменная-член указывает, является ли распределитель для соединения с закреплением объектом **Цимажеаллокатор** .</span><span class="sxs-lookup"><span data-stu-id="4a1b2-105">The `m_bUsingImageAllocator` member variable indicates whether the allocator for the pin connection is a **CImageAllocator** object.</span></span> <span data-ttu-id="4a1b2-106">Если значение равно **true**, распределитель является объектом **Цимажеаллокатор** (или производным от этого класса).</span><span class="sxs-lookup"><span data-stu-id="4a1b2-106">If the value is **TRUE**, the allocator is a **CImageAllocator** object (or is derived from that class).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a1b2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a1b2-107">Syntax</span></span>


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a><span data-ttu-id="4a1b2-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a1b2-108">Remarks</span></span>

<span data-ttu-id="4a1b2-109">Если значение равно **true**, объект **кдравимаже** может использовать функции GDI **BitBlt** и **стретчблт** для отрисовки изображения, а не более медленных функций **сетдибитстодевице** и **стретчдибитс** .</span><span class="sxs-lookup"><span data-stu-id="4a1b2-109">When the value is **TRUE**, the **CDrawImage** object can use the GDI **BitBlt** and **StretchBlt** functions to render the image, rather than the slower **SetDIBitsToDevice** and **StretchDIBits** functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a1b2-110">Требования</span><span class="sxs-lookup"><span data-stu-id="4a1b2-110">Requirements</span></span>



| <span data-ttu-id="4a1b2-111">Требование</span><span class="sxs-lookup"><span data-stu-id="4a1b2-111">Requirement</span></span> | <span data-ttu-id="4a1b2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4a1b2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1b2-113">Header</span><span class="sxs-lookup"><span data-stu-id="4a1b2-113">Header</span></span><br/>  | <dl> <span data-ttu-id="4a1b2-114"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a1b2-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a1b2-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4a1b2-115">Library</span></span><br/> | <dl> <span data-ttu-id="4a1b2-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4a1b2-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a1b2-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a1b2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a1b2-118">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="4a1b2-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="4a1b2-119">**Кдравимаже:: Нотифяллокатор**</span><span class="sxs-lookup"><span data-stu-id="4a1b2-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> <dt>

[<span data-ttu-id="4a1b2-120">**Кдравимаже:: Усингимажеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="4a1b2-120">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




