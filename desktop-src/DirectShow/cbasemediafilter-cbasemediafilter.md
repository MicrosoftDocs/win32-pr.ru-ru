---
description: Метод конструктора Кбасемедиафилтер. Кбасемедиафилтер.
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Конструктор Кбасемедиафилтер. Кбасемедиафилтер (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f123c7af29c6420de6004132180eba8dbf33fa72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096322"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a><span data-ttu-id="e6b2e-103">Кбасемедиафилтер. Кбасемедиафилтер, конструктор</span><span class="sxs-lookup"><span data-stu-id="e6b2e-103">CBaseMediaFilter.CBaseMediaFilter constructor</span></span>

<span data-ttu-id="e6b2e-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6b2e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6b2e-105">Syntax</span></span>


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="e6b2e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6b2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6b2e-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="e6b2e-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e6b2e-108">Указатель на строку, содержащую имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-108">Pointer to a string containing the name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="e6b2e-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="e6b2e-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e6b2e-110">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="e6b2e-111">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="e6b2e-112">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e6b2e-113">*плокк*</span><span class="sxs-lookup"><span data-stu-id="e6b2e-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="e6b2e-114">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="e6b2e-115">*этому*</span><span class="sxs-lookup"><span data-stu-id="e6b2e-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="e6b2e-116">Идентификатор класса объекта.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-116">Class identifier of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6b2e-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="e6b2e-117">Remarks</span></span>

<span data-ttu-id="e6b2e-118">Если другой объект содержит или выполняет статистическую обработку `CBaseMediaFilter` объекта, блокировка **ккритсек** может быть внешней по отношению к `CBaseMediaFilter` объекту.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-118">If another object contains or aggregates the `CBaseMediaFilter` object, the **CCritSec** lock might be external to the `CBaseMediaFilter` object.</span></span> <span data-ttu-id="e6b2e-119">В этом случае передайте указатель на блокировку в *плокк*.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-119">In that case, pass a pointer to the lock in *pLock*.</span></span>

<span data-ttu-id="e6b2e-120">В противном случае можно:</span><span class="sxs-lookup"><span data-stu-id="e6b2e-120">Otherwise, you can:</span></span>

-   <span data-ttu-id="e6b2e-121">Создайте производный класс, который наследует `CBaseMediaFilter` и **ккритсек**.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-121">Derive a class that inherits both `CBaseMediaFilter` and **CCritSec**.</span></span> <span data-ttu-id="e6b2e-122">Для *плокк* передайте этот указатель.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-122">For *pLock*, pass the this pointer.</span></span>
-   <span data-ttu-id="e6b2e-123">Создайте производный класс, который наследует `CBaseMediaFilter` и содержит переменную-член **ккритсек** .</span><span class="sxs-lookup"><span data-stu-id="e6b2e-123">Derive a class that inherits `CBaseMediaFilter` and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="e6b2e-124">Для *плокк* передайте адрес этой переменной.</span><span class="sxs-lookup"><span data-stu-id="e6b2e-124">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6b2e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e6b2e-125">Requirements</span></span>



| <span data-ttu-id="e6b2e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e6b2e-126">Requirement</span></span> | <span data-ttu-id="e6b2e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e6b2e-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b2e-128">Header</span><span class="sxs-lookup"><span data-stu-id="e6b2e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e6b2e-129"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6b2e-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e6b2e-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e6b2e-130">Library</span></span><br/> | <dl> <span data-ttu-id="e6b2e-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e6b2e-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6b2e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e6b2e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6b2e-133">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="e6b2e-133">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




