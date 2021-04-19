---
description: 'Метод Жеткуррентпоситион извлекает текущую точку относительно общей продолжительности потока. Этот метод реализует метод Имедиасикинг:: Жеткуррентпоситион.'
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Кпоспасссру. Жеткуррентпоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5cdbd93edf7630499f6585fbbf6e34a70bed68c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675769"
---
# <a name="cpospassthrugetcurrentposition-method"></a><span data-ttu-id="14023-104">Кпоспасссру. Жеткуррентпоситион, метод</span><span class="sxs-lookup"><span data-stu-id="14023-104">CPosPassThru.GetCurrentPosition method</span></span>

<span data-ttu-id="14023-105">`GetCurrentPosition`Метод получает текущую координату относительно общей продолжительности потока.</span><span class="sxs-lookup"><span data-stu-id="14023-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="14023-106">Этот метод реализует метод [**имедиасикинг:: жеткуррентпоситион**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) .</span><span class="sxs-lookup"><span data-stu-id="14023-106">This method implements the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="14023-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14023-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="14023-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="14023-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14023-109">*пкуррент*</span><span class="sxs-lookup"><span data-stu-id="14023-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="14023-110">Указатель на переменную, которая получает текущую координату в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="14023-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14023-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14023-111">Return value</span></span>

<span data-ttu-id="14023-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14023-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="14023-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="14023-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="14023-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="14023-114">Return code</span></span>                                                                               | <span data-ttu-id="14023-115">Описание</span><span class="sxs-lookup"><span data-stu-id="14023-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="14023-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="14023-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="14023-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="14023-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="14023-118"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="14023-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="14023-119">Метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="14023-119">Method is not supported.</span></span><br/>   |
| <dl> <span data-ttu-id="14023-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="14023-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="14023-121">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="14023-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14023-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14023-122">Remarks</span></span>

<span data-ttu-id="14023-123">Этот метод вызывает метод [**кпоспасссру:: жетмедиатиме**](cpospassthru-getmediatime.md) для получения самой последней вакансии.</span><span class="sxs-lookup"><span data-stu-id="14023-123">This method calls the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method to retrieve the most recent position.</span></span> <span data-ttu-id="14023-124">Если **жетмедиатиме** завершается сбоем, метод вызывает **Имедиасикинг:: жеткуррентпоситион** на подключенном ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="14023-124">If **GetMediaTime** fails, the method calls **IMediaSeeking::GetCurrentPosition** on the connected pin.</span></span>

<span data-ttu-id="14023-125">Метод **жетмедиатиме** по умолчанию завершается сбоем в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="14023-125">The **GetMediaTime** method fails by default in the base class.</span></span> <span data-ttu-id="14023-126">Если фильтр кэширует текущую точку, переопределите **жетмедиатиме** , чтобы вернуть кэшированное значение.</span><span class="sxs-lookup"><span data-stu-id="14023-126">If your filter caches the current position, override **GetMediaTime** to return the cached value.</span></span>

## <a name="requirements"></a><span data-ttu-id="14023-127">Требования</span><span class="sxs-lookup"><span data-stu-id="14023-127">Requirements</span></span>



| <span data-ttu-id="14023-128">Требование</span><span class="sxs-lookup"><span data-stu-id="14023-128">Requirement</span></span> | <span data-ttu-id="14023-129">Значение</span><span class="sxs-lookup"><span data-stu-id="14023-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14023-130">Header</span><span class="sxs-lookup"><span data-stu-id="14023-130">Header</span></span><br/>  | <dl> <span data-ttu-id="14023-131"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14023-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="14023-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14023-132">Library</span></span><br/> | <dl> <span data-ttu-id="14023-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="14023-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14023-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14023-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14023-135">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="14023-135">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




