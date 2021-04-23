---
description: Префикс каждого буфера в байтах.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Элемент Кбасеаллокатор:: m_lPrefix (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657047"
---
# <a name="cbaseallocatorm_lprefix-member"></a><span data-ttu-id="337fe-103">Элемент Кбасеаллокатор:: m \_ лпрефикс</span><span class="sxs-lookup"><span data-stu-id="337fe-103">CBaseAllocator::m\_lPrefix member</span></span>

<span data-ttu-id="337fe-104">Префикс каждого буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="337fe-104">Prefix of each buffer, in bytes.</span></span> <span data-ttu-id="337fe-105">Если значение не равно нулю, то каждый указатель буфера, возвращенный методом [**кбасеаллокатор::**](cbaseallocator-getbuffer.md) GetBytes, предшествует блоку байтов размером *m \_ лпрефикс*.</span><span class="sxs-lookup"><span data-stu-id="337fe-105">If the value is non-zero, each buffer pointer returned by the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method is preceded by a block of bytes of size *m\_lPrefix*.</span></span> <span data-ttu-id="337fe-106">Этот блок памяти называется *префиксом*.</span><span class="sxs-lookup"><span data-stu-id="337fe-106">This memory block is called the *prefix*.</span></span> <span data-ttu-id="337fe-107">Переменная члена [**кбасеаллокатор:: m \_ лсизе**](cbaseallocator-m-lsize.md) не включает значение префикса.</span><span class="sxs-lookup"><span data-stu-id="337fe-107">The [**CBaseAllocator::m\_lSize**](cbaseallocator-m-lsize.md) member variable does not include the prefix value.</span></span>

## <a name="syntax"></a><span data-ttu-id="337fe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="337fe-108">Syntax</span></span>


```C++
long m_lPrefix;
```



## <a name="requirements"></a><span data-ttu-id="337fe-109">Требования</span><span class="sxs-lookup"><span data-stu-id="337fe-109">Requirements</span></span>



| <span data-ttu-id="337fe-110">Требование</span><span class="sxs-lookup"><span data-stu-id="337fe-110">Requirement</span></span> | <span data-ttu-id="337fe-111">Значение</span><span class="sxs-lookup"><span data-stu-id="337fe-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="337fe-112">Header</span><span class="sxs-lookup"><span data-stu-id="337fe-112">Header</span></span><br/>  | <dl> <span data-ttu-id="337fe-113"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="337fe-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="337fe-114">Библиотека</span><span class="sxs-lookup"><span data-stu-id="337fe-114">Library</span></span><br/> | <dl> <span data-ttu-id="337fe-115"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="337fe-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="337fe-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="337fe-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="337fe-117">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="337fe-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




