---
description: Кбаседиспатч. GetIDsOfNames, метод GetIDsOfNames сопоставляет набор имен с соответствующим набором идентификаторов DISPID.
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: Кбаседиспатч. GetIDsOfNames, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f3b718c95d588ffdc7fa63902e6b26ffbf11fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099922"
---
# <a name="cbasedispatchgetidsofnames-method"></a><span data-ttu-id="3b583-103">Кбаседиспатч. GetIDsOfNames, метод</span><span class="sxs-lookup"><span data-stu-id="3b583-103">CBaseDispatch.GetIDsOfNames method</span></span>

<span data-ttu-id="3b583-104">`GetIDsOfNames`Метод сопоставляет набор имен с соответствующим набором идентификаторов DISPID.</span><span class="sxs-lookup"><span data-stu-id="3b583-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b583-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b583-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="3b583-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b583-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b583-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="3b583-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="3b583-108">Ссылка на идентификатор интерфейса (IID), указывающий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="3b583-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="3b583-109">*ргсзнамес*</span><span class="sxs-lookup"><span data-stu-id="3b583-109">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="3b583-110">Адрес массива строк расширенных символов, содержащих имена для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="3b583-110">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="3b583-111">*Записи CNAME*</span><span class="sxs-lookup"><span data-stu-id="3b583-111">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="3b583-112">Размер массива, заданного параметром *ргсзнамес* .</span><span class="sxs-lookup"><span data-stu-id="3b583-112">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3b583-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="3b583-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="3b583-114">Контекст языкового стандарта, в котором следует интерпретировать имена.</span><span class="sxs-lookup"><span data-stu-id="3b583-114">Locale context in which to interpret the names.</span></span> <span data-ttu-id="3b583-115">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3b583-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3b583-116">*ргдиспид*</span><span class="sxs-lookup"><span data-stu-id="3b583-116">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="3b583-117">Указатель на массив, который получает идентификаторы DISPID.</span><span class="sxs-lookup"><span data-stu-id="3b583-117">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="3b583-118">Каждый элемент получает идентификатор, соответствующий одному из имен, переданных в параметре *ргсзнамес* .</span><span class="sxs-lookup"><span data-stu-id="3b583-118">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b583-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b583-119">Return value</span></span>

<span data-ttu-id="3b583-120">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b583-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3b583-121">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="3b583-121">Possible values include the following.</span></span>



| <span data-ttu-id="3b583-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3b583-122">Return code</span></span>                                                                                         | <span data-ttu-id="3b583-123">Описание</span><span class="sxs-lookup"><span data-stu-id="3b583-123">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="3b583-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3b583-124"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="3b583-125">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3b583-125">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="3b583-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3b583-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="3b583-127">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="3b583-127">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="3b583-128"><dt>**\_выункновннаме E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3b583-128"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="3b583-129">Одно или несколько имен не были известны.</span><span class="sxs-lookup"><span data-stu-id="3b583-129">One or more of the names were not known.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b583-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="3b583-130">Remarks</span></span>

<span data-ttu-id="3b583-131">Этот метод ведет себя как метод **IDispatch:: GetIdsOfNames** , но параметр *riid* указывает интерфейс для получения идентификаторов DISPID.</span><span class="sxs-lookup"><span data-stu-id="3b583-131">This method behaves like the **IDispatch::GetIDsOfNames** method, but the *riid* parameter specifies the interface on which to retrieve DISPIDs.</span></span> <span data-ttu-id="3b583-132">(В версии **IDispatch** параметр *riid* зарезервирован.)</span><span class="sxs-lookup"><span data-stu-id="3b583-132">(In the **IDispatch** version, the *riid* parameter is reserved.)</span></span>

<span data-ttu-id="3b583-133">Если метод возвращает представление \_ E \_ ункновннаме, ВОЗВРАЩАЕМые идентификаторы DISPID содержат \_ неизвестный идентификатор DISPID для каждой записи, соответствующей неизвестному имени.</span><span class="sxs-lookup"><span data-stu-id="3b583-133">If the method returns DISP\_E\_UNKNOWNNAME, the returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b583-134">Требования</span><span class="sxs-lookup"><span data-stu-id="3b583-134">Requirements</span></span>



| <span data-ttu-id="3b583-135">Требование</span><span class="sxs-lookup"><span data-stu-id="3b583-135">Requirement</span></span> | <span data-ttu-id="3b583-136">Значение</span><span class="sxs-lookup"><span data-stu-id="3b583-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b583-137">Header</span><span class="sxs-lookup"><span data-stu-id="3b583-137">Header</span></span><br/>  | <dl> <span data-ttu-id="3b583-138"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b583-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3b583-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3b583-139">Library</span></span><br/> | <dl> <span data-ttu-id="3b583-140"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3b583-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b583-141">См. также</span><span class="sxs-lookup"><span data-stu-id="3b583-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b583-142">**Класс Кбаседиспатч**</span><span class="sxs-lookup"><span data-stu-id="3b583-142">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




