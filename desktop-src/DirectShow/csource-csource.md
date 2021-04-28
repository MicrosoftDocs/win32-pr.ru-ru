---
description: Метод конструктора Ксаурце. Ксаурце.
ms.assetid: 94a92c1e-9768-4293-8290-a2b1938cd196
title: Конструктор Ксаурце. Ксаурце (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fab398f3f4e3fdd8c23ce1e1c08f5c130478dfb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085362"
---
# <a name="csourcecsource-constructor"></a><span data-ttu-id="0e890-103">Ксаурце. Ксаурце, конструктор</span><span class="sxs-lookup"><span data-stu-id="0e890-103">CSource.CSource constructor</span></span>

<span data-ttu-id="0e890-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="0e890-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e890-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e890-105">Syntax</span></span>


```C++
CSource(
   TCHAR     *pName,
   LPUNKNOWN lpunk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="0e890-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e890-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e890-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="0e890-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0e890-108">Указатель на строку, содержащую имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0e890-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="0e890-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="0e890-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e890-110">*лпунк*</span><span class="sxs-lookup"><span data-stu-id="0e890-110">*lpunk*</span></span> 
</dt> <dd>

<span data-ttu-id="0e890-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="0e890-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="0e890-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="0e890-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="0e890-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0e890-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0e890-114">*этому*</span><span class="sxs-lookup"><span data-stu-id="0e890-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="0e890-115">Идентификатор класса фильтра.</span><span class="sxs-lookup"><span data-stu-id="0e890-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e890-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0e890-116">Requirements</span></span>



| <span data-ttu-id="0e890-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0e890-117">Requirement</span></span> | <span data-ttu-id="0e890-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0e890-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e890-119">Header</span><span class="sxs-lookup"><span data-stu-id="0e890-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0e890-120"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e890-120"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0e890-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0e890-121">Library</span></span><br/> | <dl> <span data-ttu-id="0e890-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0e890-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e890-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0e890-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e890-124">**Класс Ксаурце**</span><span class="sxs-lookup"><span data-stu-id="0e890-124">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




