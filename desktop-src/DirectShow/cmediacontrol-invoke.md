---
description: Предоставляет доступ к открытым свойствам и методам объекта.
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: Метод Кмедиаконтрол. Invoke (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b9a29d163180ffc609ca44f2bbbfb2870c5faef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675627"
---
# <a name="cmediacontrolinvoke-method"></a><span data-ttu-id="da8dd-103">Кмедиаконтрол. Invoke, метод</span><span class="sxs-lookup"><span data-stu-id="da8dd-103">CMediaControl.Invoke method</span></span>

<span data-ttu-id="da8dd-104">Предоставляет доступ к открытым свойствам и методам объекта.</span><span class="sxs-lookup"><span data-stu-id="da8dd-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="da8dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da8dd-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="da8dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da8dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da8dd-107">*диспидмембер*</span><span class="sxs-lookup"><span data-stu-id="da8dd-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="da8dd-108">Идентификатор элемента.</span><span class="sxs-lookup"><span data-stu-id="da8dd-108">Identifier of the member.</span></span> <span data-ttu-id="da8dd-109">Чтобы получить идентификатор диспетчеризации, используйте [**кмедиаконтрол:: GetIdsOfNames**](cmediacontrol-getidsofnames.md) или документацию объекта.</span><span class="sxs-lookup"><span data-stu-id="da8dd-109">Use [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="da8dd-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="da8dd-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="da8dd-111">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="da8dd-111">Reserved for future use.</span></span> <span data-ttu-id="da8dd-112">Должен иметь \_ значение IID null.</span><span class="sxs-lookup"><span data-stu-id="da8dd-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="da8dd-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="da8dd-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="da8dd-114">Контекст языкового стандарта, в котором следует интерпретировать аргументы.</span><span class="sxs-lookup"><span data-stu-id="da8dd-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="da8dd-115">*вфлагс*</span><span class="sxs-lookup"><span data-stu-id="da8dd-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="da8dd-116">Флаги, описывающие контекст `CMediaControl::Invoke` вызова.</span><span class="sxs-lookup"><span data-stu-id="da8dd-116">Flags describing the context of the `CMediaControl::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="da8dd-117">*пдисппарамс*</span><span class="sxs-lookup"><span data-stu-id="da8dd-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="da8dd-118">Указатель на структуру, содержащую массив аргументов, массив идентификаторов диспетчеризации аргументов для именованных аргументов и количество элементов в массивах.</span><span class="sxs-lookup"><span data-stu-id="da8dd-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="da8dd-119">*пварресулт*</span><span class="sxs-lookup"><span data-stu-id="da8dd-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="da8dd-120">Указатель на место хранения результата или **значение NULL** , если вызывающий объект не ждет результата.</span><span class="sxs-lookup"><span data-stu-id="da8dd-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="da8dd-121">*пексцепинфо*</span><span class="sxs-lookup"><span data-stu-id="da8dd-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="da8dd-122">Указатель на структуру, содержащую сведения об исключении.</span><span class="sxs-lookup"><span data-stu-id="da8dd-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="da8dd-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="da8dd-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="da8dd-124">Указатель на индекс первого аргумента в массиве **rgvarg** структуры **DISPPARAMS** , который содержит ошибку.</span><span class="sxs-lookup"><span data-stu-id="da8dd-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="da8dd-125">Дополнительные сведения о **DISPPARAMS** см. в разделе пакет SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="da8dd-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da8dd-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da8dd-126">Return value</span></span>

<span data-ttu-id="da8dd-127">Возвращает \_ \_ значение ункновнинтерфаце E, если *RIID* не является IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="da8dd-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="da8dd-128">Возвращает один из кодов ошибок из [**кмедиаконтрол:: GetTypeInfo**](cmediacontrol-gettypeinfo.md) , если вызов завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="da8dd-128">Returns one of the error codes from [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="da8dd-129">В противном случае возвращает **значение HRESULT** из вызова **IDispatch:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="da8dd-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="da8dd-130">Требования</span><span class="sxs-lookup"><span data-stu-id="da8dd-130">Requirements</span></span>



| <span data-ttu-id="da8dd-131">Требование</span><span class="sxs-lookup"><span data-stu-id="da8dd-131">Requirement</span></span> | <span data-ttu-id="da8dd-132">Значение</span><span class="sxs-lookup"><span data-stu-id="da8dd-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da8dd-133">Header</span><span class="sxs-lookup"><span data-stu-id="da8dd-133">Header</span></span><br/>  | <dl> <span data-ttu-id="da8dd-134"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da8dd-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="da8dd-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="da8dd-135">Library</span></span><br/> | <dl> <span data-ttu-id="da8dd-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="da8dd-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da8dd-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da8dd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da8dd-138">**Класс Кмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="da8dd-138">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




