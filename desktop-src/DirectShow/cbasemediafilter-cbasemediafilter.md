---
description: Метод конструктора.
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
ms.openlocfilehash: 8498e9da88804291fc5cdb900ff1dbda212e8b0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665325"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a><span data-ttu-id="51f2d-103">Кбасемедиафилтер. Кбасемедиафилтер, конструктор</span><span class="sxs-lookup"><span data-stu-id="51f2d-103">CBaseMediaFilter.CBaseMediaFilter constructor</span></span>

<span data-ttu-id="51f2d-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="51f2d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51f2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51f2d-105">Syntax</span></span>


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="51f2d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="51f2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51f2d-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="51f2d-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="51f2d-108">Указатель на строку, содержащую имя объекта.</span><span class="sxs-lookup"><span data-stu-id="51f2d-108">Pointer to a string containing the name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="51f2d-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="51f2d-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="51f2d-110">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="51f2d-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="51f2d-111">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="51f2d-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="51f2d-112">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="51f2d-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="51f2d-113">*плокк*</span><span class="sxs-lookup"><span data-stu-id="51f2d-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="51f2d-114">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="51f2d-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="51f2d-115">*этому*</span><span class="sxs-lookup"><span data-stu-id="51f2d-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="51f2d-116">Идентификатор класса объекта.</span><span class="sxs-lookup"><span data-stu-id="51f2d-116">Class identifier of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51f2d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51f2d-117">Remarks</span></span>

<span data-ttu-id="51f2d-118">Если другой объект содержит или выполняет статистическую обработку `CBaseMediaFilter` объекта, блокировка **ккритсек** может быть внешней по отношению к `CBaseMediaFilter` объекту.</span><span class="sxs-lookup"><span data-stu-id="51f2d-118">If another object contains or aggregates the `CBaseMediaFilter` object, the **CCritSec** lock might be external to the `CBaseMediaFilter` object.</span></span> <span data-ttu-id="51f2d-119">В этом случае передайте указатель на блокировку в *плокк*.</span><span class="sxs-lookup"><span data-stu-id="51f2d-119">In that case, pass a pointer to the lock in *pLock*.</span></span>

<span data-ttu-id="51f2d-120">В противном случае можно:</span><span class="sxs-lookup"><span data-stu-id="51f2d-120">Otherwise, you can:</span></span>

-   <span data-ttu-id="51f2d-121">Создайте производный класс, который наследует `CBaseMediaFilter` и **ккритсек**.</span><span class="sxs-lookup"><span data-stu-id="51f2d-121">Derive a class that inherits both `CBaseMediaFilter` and **CCritSec**.</span></span> <span data-ttu-id="51f2d-122">Для *плокк* передайте этот указатель.</span><span class="sxs-lookup"><span data-stu-id="51f2d-122">For *pLock*, pass the this pointer.</span></span>
-   <span data-ttu-id="51f2d-123">Создайте производный класс, который наследует `CBaseMediaFilter` и содержит переменную-член **ккритсек** .</span><span class="sxs-lookup"><span data-stu-id="51f2d-123">Derive a class that inherits `CBaseMediaFilter` and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="51f2d-124">Для *плокк* передайте адрес этой переменной.</span><span class="sxs-lookup"><span data-stu-id="51f2d-124">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="51f2d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="51f2d-125">Requirements</span></span>



| <span data-ttu-id="51f2d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="51f2d-126">Requirement</span></span> | <span data-ttu-id="51f2d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="51f2d-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f2d-128">Header</span><span class="sxs-lookup"><span data-stu-id="51f2d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="51f2d-129"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51f2d-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="51f2d-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="51f2d-130">Library</span></span><br/> | <dl> <span data-ttu-id="51f2d-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="51f2d-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51f2d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51f2d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f2d-133">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="51f2d-133">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




