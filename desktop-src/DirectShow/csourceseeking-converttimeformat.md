---
description: 'Метод Конверттимеформат преобразует из одного формата времени в другой. Этот метод реализует метод Имедиасикинг:: Конверттимеформат.'
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
ms.openlocfilehash: 3869ef5bc9656414ca5b465a04d04a4ca4be41e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685248"
---
# <a name="csourceseekingconverttimeformat-method"></a><span data-ttu-id="4ecb8-104">Ксаурцесикинг. Конверттимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="4ecb8-104">CSourceSeeking.ConvertTimeFormat method</span></span>

<span data-ttu-id="4ecb8-105">`ConvertTimeFormat`Метод преобразует из одного формата времени в другой.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="4ecb8-106">Этот метод реализует метод [**имедиасикинг:: конверттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="4ecb8-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ecb8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ecb8-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="4ecb8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ecb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ecb8-109">*птаржет*</span><span class="sxs-lookup"><span data-stu-id="4ecb8-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="4ecb8-110">Указатель на переменную, которая получает преобразованное время.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="4ecb8-111">*птаржетформат*</span><span class="sxs-lookup"><span data-stu-id="4ecb8-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="4ecb8-112">Указатель на идентификатор GUID целевого формата.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-112">Pointer to the GUID of the target format.</span></span> <span data-ttu-id="4ecb8-113">Если **значение равно NULL**, используется текущий формат.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-113">If **NULL**, the current format is used.</span></span> <span data-ttu-id="4ecb8-114">См. раздел [**идентификаторы GUID формата времени**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="4ecb8-114">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ecb8-115">*Источник*</span><span class="sxs-lookup"><span data-stu-id="4ecb8-115">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="4ecb8-116">Значение времени, которое необходимо преобразовать.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-116">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="4ecb8-117">*псаурцеформат*</span><span class="sxs-lookup"><span data-stu-id="4ecb8-117">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="4ecb8-118">Указатель на идентификатор GUID формата времени для преобразования.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-118">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="4ecb8-119">Если **значение равно NULL**, используется текущий формат.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-119">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ecb8-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ecb8-120">Return value</span></span>

<span data-ttu-id="4ecb8-121">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-121">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="4ecb8-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4ecb8-122">Return code</span></span>                                                                                  | <span data-ttu-id="4ecb8-123">Описание</span><span class="sxs-lookup"><span data-stu-id="4ecb8-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="4ecb8-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4ecb8-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4ecb8-125">Успешно</span><span class="sxs-lookup"><span data-stu-id="4ecb8-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="4ecb8-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4ecb8-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4ecb8-127">Недопустимый аргумент</span><span class="sxs-lookup"><span data-stu-id="4ecb8-127">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="4ecb8-128"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4ecb8-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="4ecb8-129">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="4ecb8-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4ecb8-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ecb8-130">Remarks</span></span>

<span data-ttu-id="4ecb8-131">Единственный формат времени, поддерживаемый базовым классом, — это \_ \_ время носителя формата времени \_ (100-наносекундных единиц).</span><span class="sxs-lookup"><span data-stu-id="4ecb8-131">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span> <span data-ttu-id="4ecb8-132">Этот метод возвращает E \_ INVALIDARG, за исключением тривиальных случаев, где *Птаржетформат* и *псаурцеформат* УКАЗЫВАЮТ время хранения в \_ формате времени \_ носителя \_ .</span><span class="sxs-lookup"><span data-stu-id="4ecb8-132">This method returns E\_INVALIDARG, except in the trivial case where *pTargetFormat* and *pSourceFormat* both specify TIME\_FORMAT\_MEDIA\_TIME.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ecb8-133">Требования</span><span class="sxs-lookup"><span data-stu-id="4ecb8-133">Requirements</span></span>



| <span data-ttu-id="4ecb8-134">Требование</span><span class="sxs-lookup"><span data-stu-id="4ecb8-134">Requirement</span></span> | <span data-ttu-id="4ecb8-135">Значение</span><span class="sxs-lookup"><span data-stu-id="4ecb8-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ecb8-136">Header</span><span class="sxs-lookup"><span data-stu-id="4ecb8-136">Header</span></span><br/>  | <dl> <span data-ttu-id="4ecb8-137"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ecb8-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4ecb8-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4ecb8-138">Library</span></span><br/> | <dl> <span data-ttu-id="4ecb8-139"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4ecb8-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ecb8-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ecb8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ecb8-141">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="4ecb8-141">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




