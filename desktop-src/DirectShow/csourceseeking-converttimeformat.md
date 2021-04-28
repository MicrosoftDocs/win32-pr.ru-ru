---
description: 'Ксаурцесикинг. Конверттимеформат, метод Конверттимеформат преобразует из одного формата времени в другой. Этот метод реализует метод Имедиасикинг:: Конверттимеформат.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Ксаурцесикинг. Конверттимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba5c6808e091f48baac7d8928e327f45773e13a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085252"
---
# <a name="csourceseekingconverttimeformat-method"></a><span data-ttu-id="cafcd-104">Ксаурцесикинг. Конверттимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="cafcd-104">CSourceSeeking.ConvertTimeFormat method</span></span>

<span data-ttu-id="cafcd-105">`ConvertTimeFormat`Метод преобразует из одного формата времени в другой.</span><span class="sxs-lookup"><span data-stu-id="cafcd-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="cafcd-106">Этот метод реализует метод [**имедиасикинг:: конверттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="cafcd-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cafcd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cafcd-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="cafcd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cafcd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cafcd-109">*птаржет*</span><span class="sxs-lookup"><span data-stu-id="cafcd-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="cafcd-110">Указатель на переменную, которая получает преобразованное время.</span><span class="sxs-lookup"><span data-stu-id="cafcd-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="cafcd-111">*птаржетформат*</span><span class="sxs-lookup"><span data-stu-id="cafcd-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="cafcd-112">Указатель на идентификатор GUID целевого формата.</span><span class="sxs-lookup"><span data-stu-id="cafcd-112">Pointer to the GUID of the target format.</span></span> <span data-ttu-id="cafcd-113">Если **значение равно NULL**, используется текущий формат.</span><span class="sxs-lookup"><span data-stu-id="cafcd-113">If **NULL**, the current format is used.</span></span> <span data-ttu-id="cafcd-114">См. раздел [**идентификаторы GUID формата времени**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="cafcd-114">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafcd-115">*Источник*</span><span class="sxs-lookup"><span data-stu-id="cafcd-115">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="cafcd-116">Значение времени, которое необходимо преобразовать.</span><span class="sxs-lookup"><span data-stu-id="cafcd-116">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="cafcd-117">*псаурцеформат*</span><span class="sxs-lookup"><span data-stu-id="cafcd-117">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="cafcd-118">Указатель на идентификатор GUID формата времени для преобразования.</span><span class="sxs-lookup"><span data-stu-id="cafcd-118">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="cafcd-119">Если **значение равно NULL**, используется текущий формат.</span><span class="sxs-lookup"><span data-stu-id="cafcd-119">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cafcd-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cafcd-120">Return value</span></span>

<span data-ttu-id="cafcd-121">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cafcd-121">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="cafcd-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cafcd-122">Return code</span></span>                                                                                  | <span data-ttu-id="cafcd-123">Описание</span><span class="sxs-lookup"><span data-stu-id="cafcd-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="cafcd-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cafcd-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="cafcd-125">Успешное завершение</span><span class="sxs-lookup"><span data-stu-id="cafcd-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="cafcd-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cafcd-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="cafcd-127">Недопустимый аргумент</span><span class="sxs-lookup"><span data-stu-id="cafcd-127">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="cafcd-128"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="cafcd-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="cafcd-129">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="cafcd-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cafcd-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="cafcd-130">Remarks</span></span>

<span data-ttu-id="cafcd-131">Единственный формат времени, поддерживаемый базовым классом, — это \_ \_ время носителя формата времени \_ (100-наносекундных единиц).</span><span class="sxs-lookup"><span data-stu-id="cafcd-131">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span> <span data-ttu-id="cafcd-132">Этот метод возвращает E \_ INVALIDARG, за исключением тривиальных случаев, где *Птаржетформат* и *псаурцеформат* УКАЗЫВАЮТ время хранения в \_ формате времени \_ носителя \_ .</span><span class="sxs-lookup"><span data-stu-id="cafcd-132">This method returns E\_INVALIDARG, except in the trivial case where *pTargetFormat* and *pSourceFormat* both specify TIME\_FORMAT\_MEDIA\_TIME.</span></span>

## <a name="requirements"></a><span data-ttu-id="cafcd-133">Требования</span><span class="sxs-lookup"><span data-stu-id="cafcd-133">Requirements</span></span>



| <span data-ttu-id="cafcd-134">Требование</span><span class="sxs-lookup"><span data-stu-id="cafcd-134">Requirement</span></span> | <span data-ttu-id="cafcd-135">Значение</span><span class="sxs-lookup"><span data-stu-id="cafcd-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cafcd-136">Header</span><span class="sxs-lookup"><span data-stu-id="cafcd-136">Header</span></span><br/>  | <dl> <span data-ttu-id="cafcd-137"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cafcd-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cafcd-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cafcd-138">Library</span></span><br/> | <dl> <span data-ttu-id="cafcd-139"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cafcd-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cafcd-140">См. также</span><span class="sxs-lookup"><span data-stu-id="cafcd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cafcd-141">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="cafcd-141">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




