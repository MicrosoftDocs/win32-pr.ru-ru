---
description: Кмедиапоситион. GetIDsOfNames, метод GetIDsOfNames сопоставляет набор имен с соответствующим набором идентификаторов DISPID.
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Кмедиапоситион. GetIDsOfNames, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26a348e58fa84aa4134ce9f2ea756874b9ce2724
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095532"
---
# <a name="cmediapositiongetidsofnames-method"></a><span data-ttu-id="040fa-103">Кмедиапоситион. GetIDsOfNames, метод</span><span class="sxs-lookup"><span data-stu-id="040fa-103">CMediaPosition.GetIDsOfNames method</span></span>

<span data-ttu-id="040fa-104">`GetIDsOfNames`Метод сопоставляет набор имен с соответствующим набором идентификаторов DISPID.</span><span class="sxs-lookup"><span data-stu-id="040fa-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="040fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="040fa-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="040fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="040fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="040fa-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="040fa-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="040fa-108">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="040fa-108">Reserved.</span></span> <span data-ttu-id="040fa-109">Используйте IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="040fa-109">Use IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="040fa-110">*ргсзнамес*</span><span class="sxs-lookup"><span data-stu-id="040fa-110">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="040fa-111">Адрес массива строк расширенных символов, содержащих имена для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="040fa-111">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="040fa-112">*Записи CNAME*</span><span class="sxs-lookup"><span data-stu-id="040fa-112">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="040fa-113">Размер массива, заданного параметром *ргсзнамес* .</span><span class="sxs-lookup"><span data-stu-id="040fa-113">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="040fa-114">*lcid*</span><span class="sxs-lookup"><span data-stu-id="040fa-114">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="040fa-115">Контекст языкового стандарта, в котором следует интерпретировать имена.</span><span class="sxs-lookup"><span data-stu-id="040fa-115">Locale context in which to interpret the names.</span></span> <span data-ttu-id="040fa-116">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="040fa-116">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="040fa-117">*ргдиспид*</span><span class="sxs-lookup"><span data-stu-id="040fa-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="040fa-118">Указатель на массив, который получает идентификаторы DISPID.</span><span class="sxs-lookup"><span data-stu-id="040fa-118">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="040fa-119">Каждый элемент получает идентификатор, соответствующий одному из имен, переданных в параметре *ргсзнамес* .</span><span class="sxs-lookup"><span data-stu-id="040fa-119">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="040fa-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="040fa-120">Return value</span></span>

<span data-ttu-id="040fa-121">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="040fa-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="040fa-122">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="040fa-122">Possible values include the following.</span></span>



| <span data-ttu-id="040fa-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="040fa-123">Return code</span></span>                                                                                         | <span data-ttu-id="040fa-124">Описание</span><span class="sxs-lookup"><span data-stu-id="040fa-124">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="040fa-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="040fa-125"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="040fa-126">Успешно.</span><span class="sxs-lookup"><span data-stu-id="040fa-126">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="040fa-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="040fa-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="040fa-128">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="040fa-128">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="040fa-129"><dt>**\_выункновннаме E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="040fa-129"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="040fa-130">Одно или несколько имен не были известны.</span><span class="sxs-lookup"><span data-stu-id="040fa-130">One or more of the names were not known.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="040fa-131">Требования</span><span class="sxs-lookup"><span data-stu-id="040fa-131">Requirements</span></span>



| <span data-ttu-id="040fa-132">Требование</span><span class="sxs-lookup"><span data-stu-id="040fa-132">Requirement</span></span> | <span data-ttu-id="040fa-133">Значение</span><span class="sxs-lookup"><span data-stu-id="040fa-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="040fa-134">Header</span><span class="sxs-lookup"><span data-stu-id="040fa-134">Header</span></span><br/>  | <dl> <span data-ttu-id="040fa-135"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="040fa-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="040fa-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="040fa-136">Library</span></span><br/> | <dl> <span data-ttu-id="040fa-137"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="040fa-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="040fa-138">См. также</span><span class="sxs-lookup"><span data-stu-id="040fa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="040fa-139">**Класс Кмедиапоситион**</span><span class="sxs-lookup"><span data-stu-id="040fa-139">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




