---
description: Метод конструктора Квидеотрансформфилтер. Квидеотрансформфилтер.
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: Конструктор Квидеотрансформфилтер. Квидеотрансформфилтер (Втранс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.CVideoTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59609e09b252e56aded1669264bb98cdbe823e89
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084592"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a><span data-ttu-id="8aa16-103">Квидеотрансформфилтер. Квидеотрансформфилтер, конструктор</span><span class="sxs-lookup"><span data-stu-id="8aa16-103">CVideoTransformFilter.CVideoTransformFilter constructor</span></span>

<span data-ttu-id="8aa16-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="8aa16-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aa16-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8aa16-105">Syntax</span></span>


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="8aa16-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8aa16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aa16-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="8aa16-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="8aa16-108">Строка, содержащая имя отладки фильтра.</span><span class="sxs-lookup"><span data-stu-id="8aa16-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="8aa16-109">Дополнительные сведения см. в разделе [**кбасеобжект:: кбасеобжект**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="8aa16-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="8aa16-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="8aa16-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="8aa16-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="8aa16-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="8aa16-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="8aa16-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="8aa16-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8aa16-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8aa16-114">*этому*</span><span class="sxs-lookup"><span data-stu-id="8aa16-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="8aa16-115">Идентификатор класса фильтра.</span><span class="sxs-lookup"><span data-stu-id="8aa16-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8aa16-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8aa16-116">Requirements</span></span>



| <span data-ttu-id="8aa16-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8aa16-117">Requirement</span></span> | <span data-ttu-id="8aa16-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8aa16-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa16-119">Header</span><span class="sxs-lookup"><span data-stu-id="8aa16-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8aa16-120"><dt>Втранс. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8aa16-120"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8aa16-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8aa16-121">Library</span></span><br/> | <dl> <span data-ttu-id="8aa16-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8aa16-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa16-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8aa16-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa16-124">**Класс Квидеотрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="8aa16-124">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




