---
description: Метод конструктора.
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Конструктор Кбасефилтер. Кбасефилтер (const TCHAR *, лпункновн, ккритсек*, РЕФКЛСИД, HRESULT *) (амфилтер. h)
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
ms.openlocfilehash: b4d8806c9b4103c06eb58e11547e83fc933d5d3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657297"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a><span data-ttu-id="e8f0d-103">Конструктор Кбасефилтер. Кбасефилтер (const TCHAR \* , лпункновн, ккритсек \* , РЕФКЛСИД, HRESULT \* )</span><span class="sxs-lookup"><span data-stu-id="e8f0d-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID, HRESULT\*) constructor</span></span>

<span data-ttu-id="e8f0d-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8f0d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8f0d-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="e8f0d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8f0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8f0d-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="e8f0d-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e8f0d-108">Указатель на строку, содержащую имя фильтра, для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="e8f0d-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="e8f0d-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e8f0d-110">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="e8f0d-111">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="e8f0d-112">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e8f0d-113">*плокк*</span><span class="sxs-lookup"><span data-stu-id="e8f0d-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="e8f0d-114">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="e8f0d-115">*этому*</span><span class="sxs-lookup"><span data-stu-id="e8f0d-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="e8f0d-116">Идентификатор класса (CLSID) фильтра.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-116">Class identifier (CLSID) of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="e8f0d-117">*фр*</span><span class="sxs-lookup"><span data-stu-id="e8f0d-117">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="e8f0d-118">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e8f0d-118">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="e8f0d-119">Конструктор не учитывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-119">The constructor ignores this parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8f0d-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8f0d-120">Remarks</span></span>

<span data-ttu-id="e8f0d-121">Для объекта критического раздела, как правило, необходимо выполнить одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-121">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="e8f0d-122">Создайте производный класс, который наследует как **кбасефилтер** , так и **ккритсек**.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-122">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="e8f0d-123">Для *плокк* передайте `this` указатель.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-123">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="e8f0d-124">Создайте производный класс, который наследует **кбасефилтер** и содержит переменную-член **ккритсек** .</span><span class="sxs-lookup"><span data-stu-id="e8f0d-124">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="e8f0d-125">Для *плокк* передайте адрес этой переменной.</span><span class="sxs-lookup"><span data-stu-id="e8f0d-125">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8f0d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e8f0d-126">Requirements</span></span>



| <span data-ttu-id="e8f0d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e8f0d-127">Requirement</span></span> | <span data-ttu-id="e8f0d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e8f0d-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f0d-129">Header</span><span class="sxs-lookup"><span data-stu-id="e8f0d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e8f0d-130"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8f0d-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e8f0d-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e8f0d-131">Library</span></span><br/> | <dl> <span data-ttu-id="e8f0d-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e8f0d-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8f0d-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8f0d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8f0d-134">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="e8f0d-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




