---
description: Метод конструктора.
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: Конструктор Кбасеаутпутпин. Кбасеаутпутпин (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0461c5056ee48caa19f21d1fcb8fcf1636157d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669182"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a><span data-ttu-id="0a069-103">Кбасеаутпутпин. Кбасеаутпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="0a069-103">CBaseOutputPin.CBaseOutputPin constructor</span></span>

<span data-ttu-id="0a069-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="0a069-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a069-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a069-105">Syntax</span></span>


```C++
CBaseOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="0a069-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a069-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a069-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="0a069-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="0a069-108">Строка, содержащая имя отладки объекта.</span><span class="sxs-lookup"><span data-stu-id="0a069-108">String containing the debug name of the object.</span></span> <span data-ttu-id="0a069-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="0a069-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a069-110">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="0a069-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="0a069-111">Указатель на фильтр, создавший этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="0a069-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="0a069-112">*плокк*</span><span class="sxs-lookup"><span data-stu-id="0a069-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="0a069-113">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="0a069-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="0a069-114">Это может быть тот же критический раздел, что и для блокировки фильтра, [**кбасефилтер:: m \_ плокк**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="0a069-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a069-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="0a069-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0a069-116">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="0a069-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="0a069-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="0a069-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0a069-118">Строка расширенных символов, содержащая имя ПИН-кода (также используемое в качестве идентификатора ПИН-кода).</span><span class="sxs-lookup"><span data-stu-id="0a069-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a069-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a069-119">Remarks</span></span>

<span data-ttu-id="0a069-120">Все параметры передаются непосредственно в конструктор [**кбасепин**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="0a069-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a069-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0a069-121">Requirements</span></span>



| <span data-ttu-id="0a069-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0a069-122">Requirement</span></span> | <span data-ttu-id="0a069-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0a069-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a069-124">Header</span><span class="sxs-lookup"><span data-stu-id="0a069-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0a069-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a069-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0a069-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0a069-126">Library</span></span><br/> | <dl> <span data-ttu-id="0a069-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0a069-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a069-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a069-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a069-129">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="0a069-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




