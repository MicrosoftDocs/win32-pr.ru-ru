---
description: Кмедиаконтрол. GetTypeInfo метод — получает объект сведений о типе, который может получать сведения о типе для интерфейса.
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: Кмедиаконтрол. GetTypeInfo, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857dbdeee9a2add9ab77cae0ff97d69699d2dd2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099132"
---
# <a name="cmediacontrolgettypeinfo-method"></a><span data-ttu-id="098af-103">Кмедиаконтрол. GetTypeInfo, метод</span><span class="sxs-lookup"><span data-stu-id="098af-103">CMediaControl.GetTypeInfo method</span></span>

<span data-ttu-id="098af-104">Извлекает объект сведений о типе, который может получить сведения о типе для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="098af-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="098af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="098af-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="098af-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="098af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="098af-107">*итинфо*</span><span class="sxs-lookup"><span data-stu-id="098af-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="098af-108">Возвращаемые сведения о типе.</span><span class="sxs-lookup"><span data-stu-id="098af-108">Type information to return.</span></span> <span data-ttu-id="098af-109">Передайте ноль, чтобы получить сведения о типе для реализации **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="098af-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="098af-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="098af-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="098af-111">КОД локали для сведений о типе.</span><span class="sxs-lookup"><span data-stu-id="098af-111">Locale ID for the type information.</span></span> <span data-ttu-id="098af-112">Для классов, поддерживающих локализованные имена членов, объект может возвращать различные сведения о типе для разных языков.</span><span class="sxs-lookup"><span data-stu-id="098af-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="098af-113">Для классов, не поддерживающих локализованные имена членов, этот параметр можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="098af-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="098af-114">*пптинфо*</span><span class="sxs-lookup"><span data-stu-id="098af-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="098af-115">Адрес указателя на запрошенный объект Type-Information.</span><span class="sxs-lookup"><span data-stu-id="098af-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="098af-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="098af-116">Return value</span></span>

<span data-ttu-id="098af-117">Возвращает указатель E, \_ Если *пптинфо* является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="098af-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="098af-118">Возвращает тип \_ E \_ елементнотфаунд, если *итинфо* не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="098af-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="098af-119">\_При успешном завершении возвращает значение S ОК.</span><span class="sxs-lookup"><span data-stu-id="098af-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="098af-120">В противном случае возвращает **значение HRESULT** из одного из вызовов для получения типа.</span><span class="sxs-lookup"><span data-stu-id="098af-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="098af-121">Требования</span><span class="sxs-lookup"><span data-stu-id="098af-121">Requirements</span></span>



| <span data-ttu-id="098af-122">Требование</span><span class="sxs-lookup"><span data-stu-id="098af-122">Requirement</span></span> | <span data-ttu-id="098af-123">Значение</span><span class="sxs-lookup"><span data-stu-id="098af-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="098af-124">Header</span><span class="sxs-lookup"><span data-stu-id="098af-124">Header</span></span><br/>  | <dl> <span data-ttu-id="098af-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="098af-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="098af-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="098af-126">Library</span></span><br/> | <dl> <span data-ttu-id="098af-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="098af-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="098af-128">См. также</span><span class="sxs-lookup"><span data-stu-id="098af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="098af-129">**Класс Кмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="098af-129">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




