---
description: 'Метод Жетмедиатиме извлекает значения времени носителя для этого образца. Этот метод реализует метод Имедиасампле:: Жетмедиатиме.'
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Кмедиасампле. Жетмедиатиме, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675202"
---
# <a name="cmediasamplegetmediatime-method"></a><span data-ttu-id="925ee-104">Кмедиасампле. Жетмедиатиме, метод</span><span class="sxs-lookup"><span data-stu-id="925ee-104">CMediaSample.GetMediaTime method</span></span>

<span data-ttu-id="925ee-105">`GetMediaTime`Метод извлекает значения времени носителя для этого образца.</span><span class="sxs-lookup"><span data-stu-id="925ee-105">The `GetMediaTime` method retrieves the media times for this sample.</span></span> <span data-ttu-id="925ee-106">Этот метод реализует метод [**имедиасампле:: жетмедиатиме**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) .</span><span class="sxs-lookup"><span data-stu-id="925ee-106">This method implements the [**IMediaSample::GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="925ee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="925ee-107">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="925ee-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="925ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="925ee-109">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="925ee-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="925ee-110">Указатель на переменную, которая получает время начала воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="925ee-110">Pointer to a variable that receives the media start time.</span></span>

</dd> <dt>

<span data-ttu-id="925ee-111">*Ожидаем*</span><span class="sxs-lookup"><span data-stu-id="925ee-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="925ee-112">Указатель на переменную, которая получает время окончания воспроизведения носителя.</span><span class="sxs-lookup"><span data-stu-id="925ee-112">Pointer to a variable that receives the media stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="925ee-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="925ee-113">Return value</span></span>

<span data-ttu-id="925ee-114">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="925ee-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="925ee-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="925ee-115">Return code</span></span>                                                                                                  | <span data-ttu-id="925ee-116">Описание</span><span class="sxs-lookup"><span data-stu-id="925ee-116">Description</span></span>                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="925ee-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="925ee-117"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="925ee-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="925ee-118">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="925ee-119"><dt>**\_ \_ \_ \_ не задано время в \_ подключении к VFW E Media**</dt></span><span class="sxs-lookup"><span data-stu-id="925ee-119"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="925ee-120">Для этого образца не заданы времена носителя.</span><span class="sxs-lookup"><span data-stu-id="925ee-120">No media times were set for this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="925ee-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="925ee-121">Remarks</span></span>

<span data-ttu-id="925ee-122">Переменная-член [**кмедиасампле:: m \_ медиаенд**](cmediasample-m-mediaend.md) указывает смещение от [**кмедиасампле:: m \_ медиастарт**](cmediasample-m-mediastart.md), но значение, полученное параметром *"пересчитать* ", является абсолютным временем носителя, вычисленным как **m \_ медиастарт**  +  **m \_ медиаенд**.</span><span class="sxs-lookup"><span data-stu-id="925ee-122">The [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable specifies an offset from [**CMediaSample::m\_MediaStart**](cmediasample-m-mediastart.md), but the value received by the *pEnd* parameter is an absolute media time, calculated as **m\_MediaStart** + **m\_MediaEnd**.</span></span>

<span data-ttu-id="925ee-123">Дополнительные сведения о времени мультимедиа см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="925ee-123">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="925ee-124">Требования</span><span class="sxs-lookup"><span data-stu-id="925ee-124">Requirements</span></span>



| <span data-ttu-id="925ee-125">Требование</span><span class="sxs-lookup"><span data-stu-id="925ee-125">Requirement</span></span> | <span data-ttu-id="925ee-126">Значение</span><span class="sxs-lookup"><span data-stu-id="925ee-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="925ee-127">Header</span><span class="sxs-lookup"><span data-stu-id="925ee-127">Header</span></span><br/>  | <dl> <span data-ttu-id="925ee-128"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="925ee-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="925ee-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="925ee-129">Library</span></span><br/> | <dl> <span data-ttu-id="925ee-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="925ee-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="925ee-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="925ee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="925ee-132">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="925ee-132">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




