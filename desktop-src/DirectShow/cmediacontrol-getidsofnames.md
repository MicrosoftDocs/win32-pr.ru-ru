---
description: 'Сопоставляет одну функцию-член и необязательный набор параметров с соответствующим набором целочисленных идентификаторов диспетчеризации (DISPID), которые могут использоваться при последующих вызовах функции-члена Кмедиаконтрол:: Invoke.'
ms.assetid: 9ce1b1aa-ea03-4a65-bff7-e46771cd0772
title: Кмедиаконтрол. GetIDsOfNames, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f906db9540f0429e1e7831284e55edf8c29b6a03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668557"
---
# <a name="cmediacontrolgetidsofnames-method"></a><span data-ttu-id="335f6-103">Кмедиаконтрол. GetIDsOfNames, метод</span><span class="sxs-lookup"><span data-stu-id="335f6-103">CMediaControl.GetIDsOfNames method</span></span>

<span data-ttu-id="335f6-104">Сопоставляет одну функцию-член и необязательный набор параметров с соответствующим набором целочисленных идентификаторов диспетчеризации (DISPID), которые могут использоваться при последующих вызовах функции-члена [**кмедиаконтрол:: Invoke**](cmediacontrol-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="335f6-104">Maps a single member function and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used upon subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="335f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="335f6-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="335f6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="335f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="335f6-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="335f6-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="335f6-108">Идентификатор ссылки.</span><span class="sxs-lookup"><span data-stu-id="335f6-108">Reference identifier.</span></span> <span data-ttu-id="335f6-109">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="335f6-109">Reserved for future use.</span></span> <span data-ttu-id="335f6-110">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="335f6-110">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="335f6-111">*ргсзнамес*</span><span class="sxs-lookup"><span data-stu-id="335f6-111">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="335f6-112">Адрес указателя на переданный массив сопоставляемых имен.</span><span class="sxs-lookup"><span data-stu-id="335f6-112">Address of a pointer to a passed-in array of names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="335f6-113">*Записи CNAME*</span><span class="sxs-lookup"><span data-stu-id="335f6-113">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="335f6-114">Количество сопоставляемых имен.</span><span class="sxs-lookup"><span data-stu-id="335f6-114">Count of the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="335f6-115">*lcid*</span><span class="sxs-lookup"><span data-stu-id="335f6-115">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="335f6-116">Контекст языкового стандарта, в котором следует интерпретировать имена.</span><span class="sxs-lookup"><span data-stu-id="335f6-116">Locale context in which to interpret the names.</span></span>

</dd> <dt>

<span data-ttu-id="335f6-117">*ргдиспид*</span><span class="sxs-lookup"><span data-stu-id="335f6-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="335f6-118">Указатель на выделенный вызывающим объектом массив, каждый элемент которого содержит идентификатор, соответствующий одному из имен, переданных в массиве *ргсзнамес* .</span><span class="sxs-lookup"><span data-stu-id="335f6-118">Pointer to a caller-allocated array, each element of which contains an ID corresponding to one of the names passed in the *rgszNames* array.</span></span> <span data-ttu-id="335f6-119">Первый элемент представляет имя элемента; последующие элементы представляют каждый из параметров элемента.</span><span class="sxs-lookup"><span data-stu-id="335f6-119">The first element represents the member name; the subsequent elements represent each of the member's parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="335f6-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="335f6-120">Return value</span></span>

<span data-ttu-id="335f6-121">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="335f6-121">Returns one of the following values.</span></span>



| <span data-ttu-id="335f6-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="335f6-122">Return code</span></span>                                                                                            | <span data-ttu-id="335f6-123">Описание</span><span class="sxs-lookup"><span data-stu-id="335f6-123">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="335f6-124"><dt>**из \_ \_ неизвестного \_ идентификатора CLSID**</dt></span><span class="sxs-lookup"><span data-stu-id="335f6-124"><dt>**DISP\_E\_UNKNOWN\_CLSID**</dt></span></span> </dl> | <span data-ttu-id="335f6-125">Идентификатор CLSID не распознан.</span><span class="sxs-lookup"><span data-stu-id="335f6-125">The CLSID was not recognized.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="335f6-126"><dt>**\_выункновннаме E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="335f6-126"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl>    | <span data-ttu-id="335f6-127">Одно или несколько имен не были известны.</span><span class="sxs-lookup"><span data-stu-id="335f6-127">One or more of the names were not known.</span></span> <span data-ttu-id="335f6-128">Возвращаемые идентификаторы DISPID содержат \_ неизвестный идентификатор DISPID для каждой записи, соответствующей неизвестному имени.</span><span class="sxs-lookup"><span data-stu-id="335f6-128">The returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span><br/> |
| <dl> <span data-ttu-id="335f6-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="335f6-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="335f6-130">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="335f6-130">Out of memory.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="335f6-131"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="335f6-131"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="335f6-132">Успешно.</span><span class="sxs-lookup"><span data-stu-id="335f6-132">Success.</span></span><br/>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="335f6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="335f6-133">Requirements</span></span>



| <span data-ttu-id="335f6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="335f6-134">Requirement</span></span> | <span data-ttu-id="335f6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="335f6-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="335f6-136">Header</span><span class="sxs-lookup"><span data-stu-id="335f6-136">Header</span></span><br/>  | <dl> <span data-ttu-id="335f6-137"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="335f6-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="335f6-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="335f6-138">Library</span></span><br/> | <dl> <span data-ttu-id="335f6-139"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="335f6-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="335f6-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="335f6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="335f6-141">**Класс Кмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="335f6-141">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




