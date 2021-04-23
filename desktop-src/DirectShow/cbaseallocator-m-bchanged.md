---
description: Флаг, указывающий, изменились ли требования к буферу.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Элемент Кбасеаллокатор:: m_bChanged (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669119"
---
# <a name="cbaseallocatorm_bchanged-member"></a><span data-ttu-id="22445-103">Элемент Кбасеаллокатор:: m \_ бчанжед</span><span class="sxs-lookup"><span data-stu-id="22445-103">CBaseAllocator::m\_bChanged member</span></span>

<span data-ttu-id="22445-104">Флаг, указывающий, изменились ли требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="22445-104">Flag indicating whether the buffer requirements have changed.</span></span> <span data-ttu-id="22445-105">Метод [**кбасеаллокатор:: SetProperties**](cbaseallocator-setproperties.md) устанавливает значение **true**.</span><span class="sxs-lookup"><span data-stu-id="22445-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets the value to **TRUE**.</span></span> <span data-ttu-id="22445-106">В производном классе чистый виртуальный метод [**кбасеаллокатор:: Alloc**](cbaseallocator-alloc.md) должен вернуть значение **false**.</span><span class="sxs-lookup"><span data-stu-id="22445-106">In a derived class, the pure virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) should set the value back to **FALSE**.</span></span> <span data-ttu-id="22445-107">После выделения буферов нет необходимости их повторного выделения, пока *m \_ Бчанжед* имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="22445-107">Once buffers have been allocated, there is no need to re-allocate them while *m\_bChanged* is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="22445-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22445-108">Syntax</span></span>


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a><span data-ttu-id="22445-109">Требования</span><span class="sxs-lookup"><span data-stu-id="22445-109">Requirements</span></span>



| <span data-ttu-id="22445-110">Требование</span><span class="sxs-lookup"><span data-stu-id="22445-110">Requirement</span></span> | <span data-ttu-id="22445-111">Значение</span><span class="sxs-lookup"><span data-stu-id="22445-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22445-112">Header</span><span class="sxs-lookup"><span data-stu-id="22445-112">Header</span></span><br/>  | <dl> <span data-ttu-id="22445-113"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22445-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="22445-114">Библиотека</span><span class="sxs-lookup"><span data-stu-id="22445-114">Library</span></span><br/> | <dl> <span data-ttu-id="22445-115"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="22445-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22445-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22445-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22445-117">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="22445-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




