---
description: Метод конструктора.
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
ms.openlocfilehash: 554c768f2cb99fda77aa87cfc916580b948da0ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657819"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a><span data-ttu-id="8bf4a-103">Кбасеинпутпин. Кбасеинпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="8bf4a-103">CBaseInputPin.CBaseInputPin constructor</span></span>

<span data-ttu-id="8bf4a-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="8bf4a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf4a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bf4a-105">Syntax</span></span>


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
);
```



## <a name="parameters"></a><span data-ttu-id="8bf4a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bf4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf4a-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="8bf4a-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf4a-108">Строка, содержащая имя отладки объекта.</span><span class="sxs-lookup"><span data-stu-id="8bf4a-108">String containing the debug name of the object.</span></span> <span data-ttu-id="8bf4a-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="8bf4a-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bf4a-110">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="8bf4a-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf4a-111">Указатель на фильтр, создавший этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="8bf4a-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="8bf4a-112">*плокк*</span><span class="sxs-lookup"><span data-stu-id="8bf4a-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf4a-113">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="8bf4a-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="8bf4a-114">Это может быть тот же критический раздел, что и для блокировки фильтра, [**кбасефилтер:: m \_ плокк**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="8bf4a-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bf4a-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="8bf4a-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf4a-116">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="8bf4a-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="8bf4a-117">*ппиннаме*</span><span class="sxs-lookup"><span data-stu-id="8bf4a-117">*pPinName*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf4a-118">Строка расширенных символов, содержащая имя ПИН-кода (также используемое в качестве идентификатора ПИН-кода).</span><span class="sxs-lookup"><span data-stu-id="8bf4a-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bf4a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8bf4a-119">Remarks</span></span>

<span data-ttu-id="8bf4a-120">Все параметры передаются непосредственно в конструктор [**кбасепин**](cbasepin-cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="8bf4a-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin-cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf4a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8bf4a-121">Requirements</span></span>



| <span data-ttu-id="8bf4a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8bf4a-122">Requirement</span></span> | <span data-ttu-id="8bf4a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf4a-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf4a-124">Header</span><span class="sxs-lookup"><span data-stu-id="8bf4a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8bf4a-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8bf4a-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8bf4a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8bf4a-126">Library</span></span><br/> | <dl> <span data-ttu-id="8bf4a-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8bf4a-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf4a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bf4a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf4a-129">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="8bf4a-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




