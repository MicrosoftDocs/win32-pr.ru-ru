---
description: Метод GetIDsOfNames сопоставляет набор имен с соответствующим набором идентификаторов DISPID.
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
ms.openlocfilehash: dc2c7eee4304bb32ac1af2759bc2f094aca1d592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679830"
---
# <a name="cmediapositiongetidsofnames-method"></a><span data-ttu-id="120d7-103">Кмедиапоситион. GetIDsOfNames, метод</span><span class="sxs-lookup"><span data-stu-id="120d7-103">CMediaPosition.GetIDsOfNames method</span></span>

<span data-ttu-id="120d7-104">`GetIDsOfNames`Метод сопоставляет набор имен с соответствующим набором идентификаторов DISPID.</span><span class="sxs-lookup"><span data-stu-id="120d7-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="120d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="120d7-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="120d7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="120d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="120d7-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="120d7-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="120d7-108">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="120d7-108">Reserved.</span></span> <span data-ttu-id="120d7-109">Используйте IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="120d7-109">Use IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="120d7-110">*ргсзнамес*</span><span class="sxs-lookup"><span data-stu-id="120d7-110">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="120d7-111">Адрес массива строк расширенных символов, содержащих имена для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="120d7-111">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="120d7-112">*Записи CNAME*</span><span class="sxs-lookup"><span data-stu-id="120d7-112">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="120d7-113">Размер массива, заданного параметром *ргсзнамес* .</span><span class="sxs-lookup"><span data-stu-id="120d7-113">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="120d7-114">*lcid*</span><span class="sxs-lookup"><span data-stu-id="120d7-114">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="120d7-115">Контекст языкового стандарта, в котором следует интерпретировать имена.</span><span class="sxs-lookup"><span data-stu-id="120d7-115">Locale context in which to interpret the names.</span></span> <span data-ttu-id="120d7-116">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="120d7-116">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="120d7-117">*ргдиспид*</span><span class="sxs-lookup"><span data-stu-id="120d7-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="120d7-118">Указатель на массив, который получает идентификаторы DISPID.</span><span class="sxs-lookup"><span data-stu-id="120d7-118">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="120d7-119">Каждый элемент получает идентификатор, соответствующий одному из имен, переданных в параметре *ргсзнамес* .</span><span class="sxs-lookup"><span data-stu-id="120d7-119">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="120d7-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="120d7-120">Return value</span></span>

<span data-ttu-id="120d7-121">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="120d7-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="120d7-122">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="120d7-122">Possible values include the following.</span></span>



| <span data-ttu-id="120d7-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="120d7-123">Return code</span></span>                                                                                         | <span data-ttu-id="120d7-124">Описание</span><span class="sxs-lookup"><span data-stu-id="120d7-124">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="120d7-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="120d7-125"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="120d7-126">Успешно.</span><span class="sxs-lookup"><span data-stu-id="120d7-126">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="120d7-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="120d7-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="120d7-128">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="120d7-128">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="120d7-129"><dt>**\_выункновннаме E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="120d7-129"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="120d7-130">Одно или несколько имен не были известны.</span><span class="sxs-lookup"><span data-stu-id="120d7-130">One or more of the names were not known.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="120d7-131">Требования</span><span class="sxs-lookup"><span data-stu-id="120d7-131">Requirements</span></span>



| <span data-ttu-id="120d7-132">Требование</span><span class="sxs-lookup"><span data-stu-id="120d7-132">Requirement</span></span> | <span data-ttu-id="120d7-133">Значение</span><span class="sxs-lookup"><span data-stu-id="120d7-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="120d7-134">Header</span><span class="sxs-lookup"><span data-stu-id="120d7-134">Header</span></span><br/>  | <dl> <span data-ttu-id="120d7-135"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="120d7-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="120d7-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="120d7-136">Library</span></span><br/> | <dl> <span data-ttu-id="120d7-137"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="120d7-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="120d7-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="120d7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="120d7-139">**Класс Кмедиапоситион**</span><span class="sxs-lookup"><span data-stu-id="120d7-139">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




