---
description: 'Следующий метод извлекает указанное число типов мультимедиа. Этот метод реализует метод Иенуммедиатипес:: Next.'
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Метод Ценуммедиатипес. Next (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657590"
---
# <a name="cenummediatypesnext-method"></a><span data-ttu-id="06118-104">Ценуммедиатипес. Next, метод</span><span class="sxs-lookup"><span data-stu-id="06118-104">CEnumMediaTypes.Next method</span></span>

<span data-ttu-id="06118-105">`Next`Метод извлекает указанное число типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="06118-105">The `Next` method retrieves a specified number of media types.</span></span> <span data-ttu-id="06118-106">Этот метод реализует метод [**иенуммедиатипес:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) .</span><span class="sxs-lookup"><span data-stu-id="06118-106">This method implements the [**IEnumMediaTypes::Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06118-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06118-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="06118-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="06118-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06118-109">*кмедиатипес*</span><span class="sxs-lookup"><span data-stu-id="06118-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="06118-110">Число извлекаемых типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="06118-110">Number of media types to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="06118-111">*ппмедиатипес*</span><span class="sxs-lookup"><span data-stu-id="06118-111">*ppMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="06118-112">Массив указателей на [**структуры \_ \_ типов мультимедиа**](/windows/win32/api/strmif/ns-strmif-am_media_type) *кпинс* размера.</span><span class="sxs-lookup"><span data-stu-id="06118-112">Array of pointers to [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structures, of size *cPins*.</span></span>

</dd> <dt>

<span data-ttu-id="06118-113">*пкфетчед*</span><span class="sxs-lookup"><span data-stu-id="06118-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="06118-114">Указатель на переменную, которая получает число типов мультимедиа, возвращаемых методом.</span><span class="sxs-lookup"><span data-stu-id="06118-114">Pointer to a variable that receives the number of media types the method returned.</span></span> <span data-ttu-id="06118-115">Может иметь **значение NULL** , если *кмедиатипес* равен 1.</span><span class="sxs-lookup"><span data-stu-id="06118-115">Can be **NULL** if *cMediaTypes* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06118-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06118-116">Return value</span></span>

<span data-ttu-id="06118-117">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="06118-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="06118-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="06118-118">Return code</span></span>                                                                                                | <span data-ttu-id="06118-119">Описание</span><span class="sxs-lookup"><span data-stu-id="06118-119">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06118-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="06118-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="06118-121">Не удалось получить столько типов носителей, сколько запрошено.</span><span class="sxs-lookup"><span data-stu-id="06118-121">Did not retrieve as many media types as requested.</span></span><br/>                       |
| <dl> <span data-ttu-id="06118-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="06118-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="06118-123">Успешно.</span><span class="sxs-lookup"><span data-stu-id="06118-123">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="06118-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="06118-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="06118-125">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="06118-125">Invalid argument.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="06118-126"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="06118-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="06118-127">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="06118-127">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="06118-128"><dt>**VFW \_ E \_ перечисление не \_ \_ \_ синхронизировано**</dt></span><span class="sxs-lookup"><span data-stu-id="06118-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="06118-129">Состояние ПИН-кода изменилось и теперь не согласуется с перечислителем.</span><span class="sxs-lookup"><span data-stu-id="06118-129">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="06118-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06118-130">Remarks</span></span>

<span data-ttu-id="06118-131">Если метод выполнен, массив, заданный параметром *ппмедиатипес* , содержит указатели \_ на \_ структуры типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="06118-131">If the method succeeds, the array specified by *ppMediaTypes* contains pointers to AM\_MEDIA\_TYPE structures.</span></span> <span data-ttu-id="06118-132">Число структур равно *\* пкфетчед*.</span><span class="sxs-lookup"><span data-stu-id="06118-132">The number of structures is equal to *\*pcFetched*.</span></span> <span data-ttu-id="06118-133">Освободите каждый тип мультимедиа, вызвав функцию [**делетемедиатипе**](deletemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="06118-133">Free each media type by calling the [**DeleteMediaType**](deletemediatype.md) function.</span></span>

<span data-ttu-id="06118-134">Этот метод вызывает метод [**кбасепин:: жетмедиатипе**](cbasepin-getmediatype.md) ПИН-кода для получения типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="06118-134">This method calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to retrieve the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="06118-135">Требования</span><span class="sxs-lookup"><span data-stu-id="06118-135">Requirements</span></span>



| <span data-ttu-id="06118-136">Требование</span><span class="sxs-lookup"><span data-stu-id="06118-136">Requirement</span></span> | <span data-ttu-id="06118-137">Значение</span><span class="sxs-lookup"><span data-stu-id="06118-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06118-138">Header</span><span class="sxs-lookup"><span data-stu-id="06118-138">Header</span></span><br/>  | <dl> <span data-ttu-id="06118-139"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06118-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="06118-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="06118-140">Library</span></span><br/> | <dl> <span data-ttu-id="06118-141"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="06118-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06118-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06118-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06118-143">**Класс Ценуммедиатипес**</span><span class="sxs-lookup"><span data-stu-id="06118-143">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




