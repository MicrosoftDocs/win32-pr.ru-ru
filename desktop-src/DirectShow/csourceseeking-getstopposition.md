---
description: 'Метод Жетстоппоситион извлекает время, когда воспроизведение останавливается, относительно длительности потока. Этот метод реализует метод Имедиасикинг:: Жетстоппоситион.'
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Ксаурцесикинг. Жетстоппоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688976"
---
# <a name="csourceseekinggetstopposition-method"></a><span data-ttu-id="62459-104">Ксаурцесикинг. Жетстоппоситион, метод</span><span class="sxs-lookup"><span data-stu-id="62459-104">CSourceSeeking.GetStopPosition method</span></span>

<span data-ttu-id="62459-105">`GetStopPosition`Метод получает время, когда воспроизведение будет прервано относительно длительности потока.</span><span class="sxs-lookup"><span data-stu-id="62459-105">The `GetStopPosition` method retrieves the time when playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="62459-106">Этот метод реализует метод [**имедиасикинг:: жетстоппоситион**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .</span><span class="sxs-lookup"><span data-stu-id="62459-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="62459-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62459-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="62459-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="62459-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62459-109">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="62459-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="62459-110">Указатель на переменную, которая получает время окончания в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="62459-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62459-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62459-111">Return value</span></span>

<span data-ttu-id="62459-112">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="62459-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="62459-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="62459-113">Return code</span></span>                                                                               | <span data-ttu-id="62459-114">Описание</span><span class="sxs-lookup"><span data-stu-id="62459-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="62459-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="62459-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="62459-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="62459-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="62459-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="62459-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="62459-118">Значение указателя **null**</span><span class="sxs-lookup"><span data-stu-id="62459-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62459-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62459-119">Remarks</span></span>

<span data-ttu-id="62459-120">Время окончания задается переменной-членом [**ксаурцесикинг:: m \_ ртстоп**](csourceseeking-m-rtstop.md) .</span><span class="sxs-lookup"><span data-stu-id="62459-120">The stop time is specified by the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="62459-121">Требования</span><span class="sxs-lookup"><span data-stu-id="62459-121">Requirements</span></span>



| <span data-ttu-id="62459-122">Требование</span><span class="sxs-lookup"><span data-stu-id="62459-122">Requirement</span></span> | <span data-ttu-id="62459-123">Значение</span><span class="sxs-lookup"><span data-stu-id="62459-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62459-124">Header</span><span class="sxs-lookup"><span data-stu-id="62459-124">Header</span></span><br/>  | <dl> <span data-ttu-id="62459-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62459-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="62459-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="62459-126">Library</span></span><br/> | <dl> <span data-ttu-id="62459-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="62459-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62459-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62459-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62459-129">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="62459-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




