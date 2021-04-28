---
description: Метод конструктора Крендерединпутпин. Крендерединпутпин.
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: Конструктор Крендерединпутпин. Крендерединпутпин (Амекстра. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4bd8e864531604fb36c2abe0bcd57ac5b3a9c869
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085402"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="05822-103">Крендерединпутпин. Крендерединпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="05822-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="05822-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="05822-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="05822-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05822-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="05822-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05822-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05822-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="05822-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="05822-108">Строка, содержащая имя отладки объекта.</span><span class="sxs-lookup"><span data-stu-id="05822-108">String containing the debug name of the object.</span></span> <span data-ttu-id="05822-109">Дополнительные сведения см. в разделе [**класс кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="05822-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="05822-110">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="05822-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="05822-111">Указатель на фильтр, создавший этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="05822-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="05822-112">*плокк*</span><span class="sxs-lookup"><span data-stu-id="05822-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="05822-113">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="05822-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="05822-114">Это может быть тот же критический раздел, что и для блокировки фильтра, [**кбасефилтер:: m \_ плокк**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="05822-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="05822-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="05822-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="05822-116">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="05822-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="05822-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="05822-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="05822-118">Строка расширенных символов, содержащая имя ПИН-кода (также используемое в качестве идентификатора ПИН-кода).</span><span class="sxs-lookup"><span data-stu-id="05822-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05822-119">Требования</span><span class="sxs-lookup"><span data-stu-id="05822-119">Requirements</span></span>



| <span data-ttu-id="05822-120">Требование</span><span class="sxs-lookup"><span data-stu-id="05822-120">Requirement</span></span> | <span data-ttu-id="05822-121">Значение</span><span class="sxs-lookup"><span data-stu-id="05822-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05822-122">Header</span><span class="sxs-lookup"><span data-stu-id="05822-122">Header</span></span><br/>  | <dl> <span data-ttu-id="05822-123"><dt>Амекстра. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05822-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="05822-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05822-124">Library</span></span><br/> | <dl> <span data-ttu-id="05822-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="05822-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05822-126">См. также</span><span class="sxs-lookup"><span data-stu-id="05822-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05822-127">**Класс Крендерединпутпин**</span><span class="sxs-lookup"><span data-stu-id="05822-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




