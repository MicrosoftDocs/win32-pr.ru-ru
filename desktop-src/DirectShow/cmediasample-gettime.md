---
description: 'Метод Times получает время, в течение которого этот пример должен начинаться и заканчиваться. Этот метод реализует метод Имедиасампле:: Time.'
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: Метод Кмедиасампле. Time (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ff2035ede3e49feb2bc14a7aa31cfc18f2e7d23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665215"
---
# <a name="cmediasamplegettime-method"></a><span data-ttu-id="9738a-104">Кмедиасампле. метод времени</span><span class="sxs-lookup"><span data-stu-id="9738a-104">CMediaSample.GetTime method</span></span>

<span data-ttu-id="9738a-105">`GetTime`Метод получает время, в течение которого этот пример должен начинаться и заканчиваться.</span><span class="sxs-lookup"><span data-stu-id="9738a-105">The `GetTime` method retrieves the stream times at which this sample should begin and finish.</span></span> <span data-ttu-id="9738a-106">Этот метод реализует метод [**имедиасампле:: Time**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) .</span><span class="sxs-lookup"><span data-stu-id="9738a-106">This method implements the [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9738a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9738a-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="9738a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9738a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9738a-109">*птиместарт*</span><span class="sxs-lookup"><span data-stu-id="9738a-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="9738a-110">Указатель на переменную, которая получает начальное время потока в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="9738a-110">Pointer to a variable that receives the beginning stream time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="9738a-111">*птиминд*</span><span class="sxs-lookup"><span data-stu-id="9738a-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="9738a-112">Указатель на переменную, которая получает конечное время потока в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="9738a-112">Pointer to a variable that receives the ending stream time, in 100-nanosecond units.</span></span> <span data-ttu-id="9738a-113">Если в образце не указано время прекращения, то для него задается значение времени начала плюс единица.</span><span class="sxs-lookup"><span data-stu-id="9738a-113">If the sample has no stop time, the value is set to the start time plus one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9738a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9738a-114">Return value</span></span>

<span data-ttu-id="9738a-115">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9738a-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="9738a-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9738a-116">Return code</span></span>                                                                                                   | <span data-ttu-id="9738a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9738a-117">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="9738a-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9738a-118"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="9738a-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="9738a-119">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="9738a-120"><dt>**VFW \_ S \_ \_ время прекращения \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9738a-120"><dt>**VFW\_S\_NO\_STOP\_TIME**</dt></span></span> </dl>         | <span data-ttu-id="9738a-121">Пример имеет допустимое время начала, но не время окончания.</span><span class="sxs-lookup"><span data-stu-id="9738a-121">Sample has a valid start time, but no stop time.</span></span><br/> |
| <dl> <span data-ttu-id="9738a-122"><dt>**в \_ VFW \_ E \_ время выборки \_ не \_ задано**</dt></span><span class="sxs-lookup"><span data-stu-id="9738a-122"><dt>**VFW\_E\_SAMPLE\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="9738a-123">Образец не имеет допустимых меток времени.</span><span class="sxs-lookup"><span data-stu-id="9738a-123">Sample does not have valid time stamps.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="9738a-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9738a-124">Remarks</span></span>

<span data-ttu-id="9738a-125">Переменные конечного элемента [**кмедиасампле:: m \_ Start**](cmediasample-m-start.md) и [**кмедиасампле: \_ : m**](cmediasample-m-end.md) определяют метки времени.</span><span class="sxs-lookup"><span data-stu-id="9738a-125">The [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables specify the time stamps.</span></span> <span data-ttu-id="9738a-126">Переменная члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) указывает, являются ли отметки времени допустимыми.</span><span class="sxs-lookup"><span data-stu-id="9738a-126">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="9738a-127">Дополнительные сведения о метках времени см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="9738a-127">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9738a-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9738a-128">Requirements</span></span>



| <span data-ttu-id="9738a-129">Требование</span><span class="sxs-lookup"><span data-stu-id="9738a-129">Requirement</span></span> | <span data-ttu-id="9738a-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9738a-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9738a-131">Header</span><span class="sxs-lookup"><span data-stu-id="9738a-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9738a-132"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9738a-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9738a-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9738a-133">Library</span></span><br/> | <dl> <span data-ttu-id="9738a-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9738a-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9738a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9738a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9738a-136">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="9738a-136">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




