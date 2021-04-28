---
description: Метод конструктора Кбасеинпутпин. Кбасеинпутпин.
ms.assetid: a853813d-cdf6-4cb4-8288-62685a883b56
title: Конструктор Кбасеинпутпин. Кбасеинпутпин (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95a6dca29a9bdcaf978a54587035b34959d81719
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120052"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a><span data-ttu-id="7ee06-103">Кбасеинпутпин. Кбасеинпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="7ee06-103">CBaseInputPin.CBaseInputPin constructor</span></span>

<span data-ttu-id="7ee06-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="7ee06-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ee06-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ee06-105">Syntax</span></span>


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
);
```



## <a name="parameters"></a><span data-ttu-id="7ee06-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ee06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ee06-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="7ee06-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee06-108">Строка, содержащая имя отладки объекта.</span><span class="sxs-lookup"><span data-stu-id="7ee06-108">String containing the debug name of the object.</span></span> <span data-ttu-id="7ee06-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="7ee06-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ee06-110">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="7ee06-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee06-111">Указатель на фильтр, создавший этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="7ee06-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="7ee06-112">*плокк*</span><span class="sxs-lookup"><span data-stu-id="7ee06-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee06-113">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="7ee06-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="7ee06-114">Это может быть тот же критический раздел, что и для блокировки фильтра, [**кбасефилтер:: m \_ плокк**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="7ee06-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ee06-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="7ee06-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee06-116">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="7ee06-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="7ee06-117">*ппиннаме*</span><span class="sxs-lookup"><span data-stu-id="7ee06-117">*pPinName*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee06-118">Строка расширенных символов, содержащая имя ПИН-кода (также используемое в качестве идентификатора ПИН-кода).</span><span class="sxs-lookup"><span data-stu-id="7ee06-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ee06-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="7ee06-119">Remarks</span></span>

<span data-ttu-id="7ee06-120">Все параметры передаются непосредственно в конструктор [**кбасепин**](cbasepin-cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="7ee06-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin-cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ee06-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7ee06-121">Requirements</span></span>



| <span data-ttu-id="7ee06-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7ee06-122">Requirement</span></span> | <span data-ttu-id="7ee06-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7ee06-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ee06-124">Header</span><span class="sxs-lookup"><span data-stu-id="7ee06-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7ee06-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ee06-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7ee06-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7ee06-126">Library</span></span><br/> | <dl> <span data-ttu-id="7ee06-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7ee06-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ee06-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7ee06-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ee06-129">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="7ee06-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




