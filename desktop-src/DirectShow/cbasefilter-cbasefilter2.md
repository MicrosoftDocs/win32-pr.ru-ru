---
description: Метод конструктора конструктора Кбасефилтер. Кбасефилтер (const TCHAR \* , лпункновн, ккритсек \* , рефклсид).
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: Конструктор Кбасефилтер. Кбасефилтер (const TCHAR *, лпункновн, ккритсек*, рефклсид) (амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b621bdb3f6a15ae950959a65eba8841bde399b81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099832"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a><span data-ttu-id="21fc4-103">Конструктор Кбасефилтер. Кбасефилтер (const TCHAR \* , лпункновн, ккритсек \* , рефклсид)</span><span class="sxs-lookup"><span data-stu-id="21fc4-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID) constructor</span></span>

<span data-ttu-id="21fc4-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="21fc4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="21fc4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21fc4-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="21fc4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="21fc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21fc4-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="21fc4-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="21fc4-108">Указатель на строку, содержащую имя фильтра, для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="21fc4-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="21fc4-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="21fc4-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="21fc4-110">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="21fc4-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="21fc4-111">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="21fc4-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="21fc4-112">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="21fc4-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="21fc4-113">*плокк*</span><span class="sxs-lookup"><span data-stu-id="21fc4-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="21fc4-114">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="21fc4-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="21fc4-115">*этому*</span><span class="sxs-lookup"><span data-stu-id="21fc4-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="21fc4-116">Идентификатор класса (CLSID) фильтра.</span><span class="sxs-lookup"><span data-stu-id="21fc4-116">Class identifier (CLSID) of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21fc4-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="21fc4-117">Remarks</span></span>

<span data-ttu-id="21fc4-118">Для объекта критического раздела, как правило, необходимо выполнить одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="21fc4-118">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="21fc4-119">Создайте производный класс, который наследует как **кбасефилтер** , так и **ккритсек**.</span><span class="sxs-lookup"><span data-stu-id="21fc4-119">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="21fc4-120">Для *плокк* передайте `this` указатель.</span><span class="sxs-lookup"><span data-stu-id="21fc4-120">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="21fc4-121">Создайте производный класс, который наследует **кбасефилтер** и содержит переменную-член **ккритсек** .</span><span class="sxs-lookup"><span data-stu-id="21fc4-121">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="21fc4-122">Для *плокк* передайте адрес этой переменной.</span><span class="sxs-lookup"><span data-stu-id="21fc4-122">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="21fc4-123">Требования</span><span class="sxs-lookup"><span data-stu-id="21fc4-123">Requirements</span></span>



| <span data-ttu-id="21fc4-124">Требование</span><span class="sxs-lookup"><span data-stu-id="21fc4-124">Requirement</span></span> | <span data-ttu-id="21fc4-125">Значение</span><span class="sxs-lookup"><span data-stu-id="21fc4-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21fc4-126">Header</span><span class="sxs-lookup"><span data-stu-id="21fc4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="21fc4-127"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21fc4-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="21fc4-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21fc4-128">Library</span></span><br/> | <dl> <span data-ttu-id="21fc4-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="21fc4-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21fc4-130">См. также</span><span class="sxs-lookup"><span data-stu-id="21fc4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21fc4-131">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="21fc4-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




