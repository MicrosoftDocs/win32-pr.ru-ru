---
description: 'Метод Жетмедиатипе Извлекает тип мультимедиа, если тип мультимедиа отличается от предыдущего примера. Этот метод реализует метод Имедиасампле:: Жетмедиатипе.'
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Кмедиасампле. Жетмедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665405"
---
# <a name="cmediasamplegetmediatype-method"></a><span data-ttu-id="635e3-104">Кмедиасампле. Жетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="635e3-104">CMediaSample.GetMediaType method</span></span>

<span data-ttu-id="635e3-105">`GetMediaType`Метод извлекает тип мультимедиа, если тип мультимедиа отличается от предыдущего примера.</span><span class="sxs-lookup"><span data-stu-id="635e3-105">The `GetMediaType` method retrieves the media type, if the media type differs from the previous sample.</span></span> <span data-ttu-id="635e3-106">Этот метод реализует метод [**имедиасампле:: жетмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .</span><span class="sxs-lookup"><span data-stu-id="635e3-106">This method implements the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="635e3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="635e3-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="635e3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="635e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="635e3-109">*ппмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="635e3-109">*ppMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="635e3-110">Адрес переменной, которая получает указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="635e3-110">Address of a variable that receives a pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="635e3-111">Если тип носителя не изменился с предыдущего примера, *\* ппмедиатипе* имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="635e3-111">If the media type has not changed from the previous sample, *\*ppMediaType* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="635e3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="635e3-112">Return value</span></span>

<span data-ttu-id="635e3-113">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="635e3-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="635e3-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="635e3-114">Return code</span></span>                                                                                   | <span data-ttu-id="635e3-115">Описание</span><span class="sxs-lookup"><span data-stu-id="635e3-115">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="635e3-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="635e3-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="635e3-117">Тип носителя не изменился по сравнению с предыдущим примером.</span><span class="sxs-lookup"><span data-stu-id="635e3-117">The media type has not changed from the previous sample.</span></span><br/> |
| <dl> <span data-ttu-id="635e3-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="635e3-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="635e3-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="635e3-119">Success.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="635e3-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="635e3-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="635e3-121">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="635e3-121">Insufficient memory.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="635e3-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="635e3-122">Remarks</span></span>

<span data-ttu-id="635e3-123">По завершении работы с типом мультимедиа освободите блок памяти, вызвав функцию служебной программы [**делетемедиатипе**](deletemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="635e3-123">When you are done with the media type, free the memory block by calling the [**DeleteMediaType**](deletemediatype.md) utility function.</span></span>

<span data-ttu-id="635e3-124">Переменная члена [**кмедиасампле:: m \_ пмедиатипе**](cmediasample-m-pmediatype.md) указывает тип носителя.</span><span class="sxs-lookup"><span data-stu-id="635e3-124">The [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable specifies the media type.</span></span> <span data-ttu-id="635e3-125">Переменная члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) указывает, изменился ли тип носителя.</span><span class="sxs-lookup"><span data-stu-id="635e3-125">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the media type has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="635e3-126">Требования</span><span class="sxs-lookup"><span data-stu-id="635e3-126">Requirements</span></span>



| <span data-ttu-id="635e3-127">Требование</span><span class="sxs-lookup"><span data-stu-id="635e3-127">Requirement</span></span> | <span data-ttu-id="635e3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="635e3-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="635e3-129">Header</span><span class="sxs-lookup"><span data-stu-id="635e3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="635e3-130"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="635e3-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="635e3-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="635e3-131">Library</span></span><br/> | <dl> <span data-ttu-id="635e3-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="635e3-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="635e3-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="635e3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="635e3-134">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="635e3-134">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




