---
description: Кмедиаевент. GetTypeInfo метод — получает объект сведений о типе, который может получать сведения о типе для интерфейса.
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Кмедиаевент. GetTypeInfo, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f93e3227051729f9d16e1f9ef8de464a14cca33b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095572"
---
# <a name="cmediaeventgettypeinfo-method"></a><span data-ttu-id="cb178-103">Кмедиаевент. GetTypeInfo, метод</span><span class="sxs-lookup"><span data-stu-id="cb178-103">CMediaEvent.GetTypeInfo method</span></span>

<span data-ttu-id="cb178-104">Извлекает объект сведений о типе, который может получить сведения о типе для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cb178-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb178-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb178-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="cb178-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb178-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb178-107">*итинфо*</span><span class="sxs-lookup"><span data-stu-id="cb178-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="cb178-108">Возвращаемые сведения о типе.</span><span class="sxs-lookup"><span data-stu-id="cb178-108">Type information to return.</span></span> <span data-ttu-id="cb178-109">Передайте ноль, чтобы получить сведения о типе для реализации **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="cb178-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="cb178-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="cb178-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="cb178-111">КОД локали для сведений о типе.</span><span class="sxs-lookup"><span data-stu-id="cb178-111">Locale ID for the type information.</span></span> <span data-ttu-id="cb178-112">Для классов, поддерживающих локализованные имена членов, объект может возвращать различные сведения о типе для разных языков.</span><span class="sxs-lookup"><span data-stu-id="cb178-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="cb178-113">Для классов, не поддерживающих локализованные имена членов, этот параметр можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="cb178-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="cb178-114">*пптинфо*</span><span class="sxs-lookup"><span data-stu-id="cb178-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="cb178-115">Адрес указателя на запрошенный объект Type-Information.</span><span class="sxs-lookup"><span data-stu-id="cb178-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb178-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb178-116">Return value</span></span>

<span data-ttu-id="cb178-117">Возвращает указатель E, \_ Если *пптинфо* является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="cb178-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="cb178-118">Возвращает тип \_ E \_ елементнотфаунд, если *итинфо* не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="cb178-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="cb178-119">\_При успешном завершении возвращает значение S ОК.</span><span class="sxs-lookup"><span data-stu-id="cb178-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="cb178-120">В противном случае возвращает **значение HRESULT** из одного из вызовов для получения типа.</span><span class="sxs-lookup"><span data-stu-id="cb178-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb178-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cb178-121">Requirements</span></span>



| <span data-ttu-id="cb178-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cb178-122">Requirement</span></span> | <span data-ttu-id="cb178-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cb178-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb178-124">Header</span><span class="sxs-lookup"><span data-stu-id="cb178-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cb178-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb178-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cb178-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb178-126">Library</span></span><br/> | <dl> <span data-ttu-id="cb178-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cb178-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb178-128">См. также</span><span class="sxs-lookup"><span data-stu-id="cb178-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb178-129">**Класс Кмедиаевент**</span><span class="sxs-lookup"><span data-stu-id="cb178-129">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




