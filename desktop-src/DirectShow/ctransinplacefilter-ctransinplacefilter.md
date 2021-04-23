---
description: Метод конструктора.
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Конструктор Ктрансинплацефилтер. Ктрансинплацефилтер (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 091ea6e6a52d4cc9221ddb29db34b4823111a395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657981"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a><span data-ttu-id="8833d-103">Ктрансинплацефилтер. Ктрансинплацефилтер, конструктор</span><span class="sxs-lookup"><span data-stu-id="8833d-103">CTransInPlaceFilter.CTransInPlaceFilter constructor</span></span>

<span data-ttu-id="8833d-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="8833d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8833d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8833d-105">Syntax</span></span>


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a><span data-ttu-id="8833d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8833d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8833d-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="8833d-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="8833d-108">Строка, содержащая имя отладки фильтра.</span><span class="sxs-lookup"><span data-stu-id="8833d-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="8833d-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="8833d-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="8833d-110">*лпунк*</span><span class="sxs-lookup"><span data-stu-id="8833d-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="8833d-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="8833d-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="8833d-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="8833d-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="8833d-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8833d-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8833d-114">*этому*</span><span class="sxs-lookup"><span data-stu-id="8833d-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="8833d-115">Идентификатор класса фильтра.</span><span class="sxs-lookup"><span data-stu-id="8833d-115">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="8833d-116">*фр*</span><span class="sxs-lookup"><span data-stu-id="8833d-116">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8833d-117">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="8833d-117">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="8833d-118">*бмодифиесдата*</span><span class="sxs-lookup"><span data-stu-id="8833d-118">*bModifiesData*</span></span> 
</dt> <dd>

<span data-ttu-id="8833d-119">Логическое значение, указывающее, изменяет ли фильтр входные данные.</span><span class="sxs-lookup"><span data-stu-id="8833d-119">Boolean value that specifies whether the filter modifies the input data.</span></span> <span data-ttu-id="8833d-120">**Значение true** показывает, что фильтр изменяет данные.</span><span class="sxs-lookup"><span data-stu-id="8833d-120">If **TRUE**, the filter modifies the data.</span></span> <span data-ttu-id="8833d-121">В противном случае фильтр передает неизмененные данные.</span><span class="sxs-lookup"><span data-stu-id="8833d-121">Otherwise, the filter passes the data downstream unchanged.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8833d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8833d-122">Requirements</span></span>



| <span data-ttu-id="8833d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8833d-123">Requirement</span></span> | <span data-ttu-id="8833d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8833d-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8833d-125">Header</span><span class="sxs-lookup"><span data-stu-id="8833d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8833d-126"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8833d-126"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8833d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8833d-127">Library</span></span><br/> | <dl> <span data-ttu-id="8833d-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8833d-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8833d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8833d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8833d-130">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="8833d-130">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




