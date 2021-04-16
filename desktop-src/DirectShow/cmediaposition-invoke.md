---
description: Метод Invoke предоставляет доступ к свойствам и методам, предоставляемым объектом.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: Метод Кмедиапоситион. Invoke (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669225"
---
# <a name="cmediapositioninvoke-method"></a><span data-ttu-id="b0da5-103">Кмедиапоситион. Invoke, метод</span><span class="sxs-lookup"><span data-stu-id="b0da5-103">CMediaPosition.Invoke method</span></span>

<span data-ttu-id="b0da5-104">`Invoke`Метод предоставляет доступ к свойствам и методам, предоставляемым объектом.</span><span class="sxs-lookup"><span data-stu-id="b0da5-104">The `Invoke` method provides access to properties and methods exposed by the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0da5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0da5-105">Syntax</span></span>


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a><span data-ttu-id="b0da5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0da5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0da5-107">*диспидмембер*</span><span class="sxs-lookup"><span data-stu-id="b0da5-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="b0da5-108">Идентификатор элемента.</span><span class="sxs-lookup"><span data-stu-id="b0da5-108">Identifier of the member.</span></span> <span data-ttu-id="b0da5-109">Чтобы получить идентификатор диспетчеризации, используйте [**кмедиапоситион:: GetIdsOfNames**](cmediaposition-getidsofnames.md) .</span><span class="sxs-lookup"><span data-stu-id="b0da5-109">Use [**CMediaPosition::GetIDsOfNames**](cmediaposition-getidsofnames.md) to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b0da5-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="b0da5-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="b0da5-111">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="b0da5-111">Reserved for future use.</span></span> <span data-ttu-id="b0da5-112">Должен иметь \_ значение IID null.</span><span class="sxs-lookup"><span data-stu-id="b0da5-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="b0da5-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="b0da5-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="b0da5-114">Контекст языкового стандарта, в котором следует интерпретировать аргументы.</span><span class="sxs-lookup"><span data-stu-id="b0da5-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="b0da5-115">*вфлагс*</span><span class="sxs-lookup"><span data-stu-id="b0da5-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b0da5-116">Флаги, описывающие контекст вызова.</span><span class="sxs-lookup"><span data-stu-id="b0da5-116">Flags describing the context of the call.</span></span>

</dd> <dt>

<span data-ttu-id="b0da5-117">*пдисппарамс*</span><span class="sxs-lookup"><span data-stu-id="b0da5-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="b0da5-118">Указатель на структуру **диппарамс** , содержащую аргументы.</span><span class="sxs-lookup"><span data-stu-id="b0da5-118">Pointer to a **DIPPARAMS** structure that contains the arguments.</span></span>

</dd> <dt>

<span data-ttu-id="b0da5-119">*пварресулт*</span><span class="sxs-lookup"><span data-stu-id="b0da5-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="b0da5-120">Указатель на **вариант** , который получает результат, или **значение NULL** , если вызывающий объект не ждет результата.</span><span class="sxs-lookup"><span data-stu-id="b0da5-120">Pointer to a **VARIANT** that receives the result, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="b0da5-121">*пексцепинфо*</span><span class="sxs-lookup"><span data-stu-id="b0da5-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b0da5-122">Указатель на структуру, которая получает сведения об исключении.</span><span class="sxs-lookup"><span data-stu-id="b0da5-122">Pointer to a structure that receives exception information.</span></span>

</dd> <dt>

<span data-ttu-id="b0da5-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="b0da5-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="b0da5-124">Указатель на переменную, которая получает индекс первого аргумента, который вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="b0da5-124">Pointer to a variable that receives the index of the first argument that causes an error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0da5-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0da5-125">Return value</span></span>

<span data-ttu-id="b0da5-126">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b0da5-126">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b0da5-127">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="b0da5-127">Possible values include the following.</span></span>



| <span data-ttu-id="b0da5-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b0da5-128">Return code</span></span>                                                                                              | <span data-ttu-id="b0da5-129">Описание</span><span class="sxs-lookup"><span data-stu-id="b0da5-129">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="b0da5-130"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b0da5-130"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="b0da5-131">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b0da5-131">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="b0da5-132"><dt>**\_выункновнинтерфаце E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0da5-132"><dt>**DISP\_E\_UNKNOWNINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="b0da5-133">Параметр *riid* не является идентификатором \_ null</span><span class="sxs-lookup"><span data-stu-id="b0da5-133">The *riid* parameter is not IID\_NULL</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b0da5-134">Требования</span><span class="sxs-lookup"><span data-stu-id="b0da5-134">Requirements</span></span>



| <span data-ttu-id="b0da5-135">Требование</span><span class="sxs-lookup"><span data-stu-id="b0da5-135">Requirement</span></span> | <span data-ttu-id="b0da5-136">Значение</span><span class="sxs-lookup"><span data-stu-id="b0da5-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0da5-137">Header</span><span class="sxs-lookup"><span data-stu-id="b0da5-137">Header</span></span><br/>  | <dl> <span data-ttu-id="b0da5-138"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0da5-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b0da5-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b0da5-139">Library</span></span><br/> | <dl> <span data-ttu-id="b0da5-140"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b0da5-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0da5-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0da5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0da5-142">**Класс Кмедиапоситион**</span><span class="sxs-lookup"><span data-stu-id="b0da5-142">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




