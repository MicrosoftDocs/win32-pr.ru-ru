---
description: Метод конструктора.
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
ms.openlocfilehash: ee1ec8944d56d2aa6f46e59ac5034969ca77ea19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657472"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="d8551-103">Крендерединпутпин. Крендерединпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="d8551-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="d8551-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="d8551-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8551-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8551-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="d8551-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8551-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8551-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="d8551-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="d8551-108">Строка, содержащая имя отладки объекта.</span><span class="sxs-lookup"><span data-stu-id="d8551-108">String containing the debug name of the object.</span></span> <span data-ttu-id="d8551-109">Дополнительные сведения см. в разделе [**класс кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="d8551-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8551-110">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="d8551-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="d8551-111">Указатель на фильтр, создавший этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="d8551-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="d8551-112">*плокк*</span><span class="sxs-lookup"><span data-stu-id="d8551-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="d8551-113">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="d8551-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="d8551-114">Это может быть тот же критический раздел, что и для блокировки фильтра, [**кбасефилтер:: m \_ плокк**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="d8551-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8551-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="d8551-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d8551-116">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="d8551-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="d8551-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="d8551-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d8551-118">Строка расширенных символов, содержащая имя ПИН-кода (также используемое в качестве идентификатора ПИН-кода).</span><span class="sxs-lookup"><span data-stu-id="d8551-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8551-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d8551-119">Requirements</span></span>



| <span data-ttu-id="d8551-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d8551-120">Requirement</span></span> | <span data-ttu-id="d8551-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d8551-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8551-122">Header</span><span class="sxs-lookup"><span data-stu-id="d8551-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d8551-123"><dt>Амекстра. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8551-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8551-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d8551-124">Library</span></span><br/> | <dl> <span data-ttu-id="d8551-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d8551-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8551-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8551-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8551-127">**Класс Крендерединпутпин**</span><span class="sxs-lookup"><span data-stu-id="d8551-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




