---
description: 'Метод Сетмедиатипе задает тип носителя для образца. Этот метод реализует метод Имедиасампле:: Сетмедиатипе.'
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Кмедиасампле. Сетмедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f46fc4e8c348b1d03d19e815f658e0f637b8f880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674980"
---
# <a name="cmediasamplesetmediatype-method"></a><span data-ttu-id="b14cb-104">Кмедиасампле. Сетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="b14cb-104">CMediaSample.SetMediaType method</span></span>

<span data-ttu-id="b14cb-105">`SetMediaType`Метод задает тип носителя для образца.</span><span class="sxs-lookup"><span data-stu-id="b14cb-105">The `SetMediaType` method sets the media type for the sample.</span></span> <span data-ttu-id="b14cb-106">Этот метод реализует метод [**имедиасампле:: сетмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) .</span><span class="sxs-lookup"><span data-stu-id="b14cb-106">This method implements the [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b14cb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b14cb-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="b14cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b14cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b14cb-109">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="b14cb-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="b14cb-110">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="b14cb-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b14cb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b14cb-111">Return value</span></span>

<span data-ttu-id="b14cb-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b14cb-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="b14cb-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b14cb-113">Return code</span></span>                                                                                   | <span data-ttu-id="b14cb-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b14cb-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="b14cb-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b14cb-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b14cb-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="b14cb-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="b14cb-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b14cb-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b14cb-118">Недостаточно памяти</span><span class="sxs-lookup"><span data-stu-id="b14cb-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b14cb-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b14cb-119">Remarks</span></span>

<span data-ttu-id="b14cb-120">Этот метод задает переменную члена [**кмедиасампле:: m \_ пмедиатипе**](cmediasample-m-pmediatype.md) , которая указывает тип мультимедиа, и переменную элемента [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) , которая указывает, изменился ли тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b14cb-120">This method sets the [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable, which specifies the media type, and the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the media type has changed.</span></span>

<span data-ttu-id="b14cb-121">Этот метод создает копию \_ \_ структуры типа мультимедиа AM.</span><span class="sxs-lookup"><span data-stu-id="b14cb-121">This method makes a copy of the AM\_MEDIA\_TYPE structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b14cb-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b14cb-122">Requirements</span></span>



| <span data-ttu-id="b14cb-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b14cb-123">Requirement</span></span> | <span data-ttu-id="b14cb-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b14cb-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b14cb-125">Header</span><span class="sxs-lookup"><span data-stu-id="b14cb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b14cb-126"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b14cb-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b14cb-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b14cb-127">Library</span></span><br/> | <dl> <span data-ttu-id="b14cb-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b14cb-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b14cb-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b14cb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b14cb-130">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="b14cb-130">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




