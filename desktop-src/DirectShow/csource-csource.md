---
description: Метод конструктора.
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
ms.openlocfilehash: 992775659d5f9838ef63b15c5395998f1faf6200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685114"
---
# <a name="csourcecsource-constructor"></a><span data-ttu-id="a0942-103">Ксаурце. Ксаурце, конструктор</span><span class="sxs-lookup"><span data-stu-id="a0942-103">CSource.CSource constructor</span></span>

<span data-ttu-id="a0942-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="a0942-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0942-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0942-105">Syntax</span></span>


```C++
CSource(
   TCHAR     *pName,
   LPUNKNOWN lpunk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="a0942-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0942-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0942-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="a0942-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a0942-108">Указатель на строку, содержащую имя объекта.</span><span class="sxs-lookup"><span data-stu-id="a0942-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="a0942-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="a0942-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0942-110">*лпунк*</span><span class="sxs-lookup"><span data-stu-id="a0942-110">*lpunk*</span></span> 
</dt> <dd>

<span data-ttu-id="a0942-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="a0942-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="a0942-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="a0942-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="a0942-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a0942-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0942-114">*этому*</span><span class="sxs-lookup"><span data-stu-id="a0942-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="a0942-115">Идентификатор класса фильтра.</span><span class="sxs-lookup"><span data-stu-id="a0942-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0942-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a0942-116">Requirements</span></span>



| <span data-ttu-id="a0942-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a0942-117">Requirement</span></span> | <span data-ttu-id="a0942-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a0942-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0942-119">Header</span><span class="sxs-lookup"><span data-stu-id="a0942-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a0942-120"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0942-120"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a0942-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a0942-121">Library</span></span><br/> | <dl> <span data-ttu-id="a0942-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a0942-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0942-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0942-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0942-124">**Класс Ксаурце**</span><span class="sxs-lookup"><span data-stu-id="a0942-124">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




