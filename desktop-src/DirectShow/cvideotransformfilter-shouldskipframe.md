---
description: Метод Шаулдскипфраме определяет, должен ли фильтр удалить указанный образец.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Квидеотрансформфилтер. Шаулдскипфраме, метод (Втранс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656997"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a><span data-ttu-id="3eebd-103">Квидеотрансформфилтер. Шаулдскипфраме, метод</span><span class="sxs-lookup"><span data-stu-id="3eebd-103">CVideoTransformFilter.ShouldSkipFrame method</span></span>

<span data-ttu-id="3eebd-104">`ShouldSkipFrame`Метод определяет, должен ли фильтр удалить указанный образец.</span><span class="sxs-lookup"><span data-stu-id="3eebd-104">The `ShouldSkipFrame` method determines whether the filter should drop a specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eebd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3eebd-105">Syntax</span></span>


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="3eebd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3eebd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eebd-107">*ПИН*</span><span class="sxs-lookup"><span data-stu-id="3eebd-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="3eebd-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="3eebd-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eebd-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3eebd-109">Return value</span></span>

<span data-ttu-id="3eebd-110">Возвращает **значение true** , если фильтр должен удалить этот образец, или **значение false** , если фильтр должен обработать этот пример.</span><span class="sxs-lookup"><span data-stu-id="3eebd-110">Returns **TRUE** if the filter should drop this sample, or **FALSE** if the filter should process this sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eebd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3eebd-111">Remarks</span></span>

<span data-ttu-id="3eebd-112">Этот метод возвращает **значение true** , если выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="3eebd-112">This method returns **TRUE** if the following conditions are met:</span></span>

-   <span data-ttu-id="3eebd-113">В образце есть отметки времени.</span><span class="sxs-lookup"><span data-stu-id="3eebd-113">The sample has time stamps.</span></span>
-   <span data-ttu-id="3eebd-114">Среднее время декодирования составляет не менее 25% от длительности кадра.</span><span class="sxs-lookup"><span data-stu-id="3eebd-114">The average decoding time is at least 25% of the frame duration.</span></span>
-   <span data-ttu-id="3eebd-115">Модуль подготовки отчетов в настоящий момент является по крайней мере одним кадром в конце, как указано в сообщениях качества.</span><span class="sxs-lookup"><span data-stu-id="3eebd-115">The renderer is currently at least one frame late, as reported through quality messages.</span></span>
-   <span data-ttu-id="3eebd-116">Пропуск к следующему ключевому кадру не приведет к тому, что кадр получит более одного кадра на ранних этапах.</span><span class="sxs-lookup"><span data-stu-id="3eebd-116">Skipping to the next key frame would not cause the frame to arrive more than one frame early.</span></span>

<span data-ttu-id="3eebd-117">Для целей этого вычисления фильтр записывает следующие сведения при обработке данных:</span><span class="sxs-lookup"><span data-stu-id="3eebd-117">For purposes of this calculation, the filter records the following information as it processes data:</span></span>

-   <span data-ttu-id="3eebd-118">Среднее время декодирования за последние 20 кадров (**m \_ итравгдекоде**)</span><span class="sxs-lookup"><span data-stu-id="3eebd-118">The average decoding time over the past 20 frames (**m\_itrAvgDecode**)</span></span>
-   <span data-ttu-id="3eebd-119">Число кадров с момента последнего ключевого кадра (**m \_ нфрамессинцекэйфраме**)</span><span class="sxs-lookup"><span data-stu-id="3eebd-119">The number of frames since the last key frame (**m\_nFramesSinceKeyFrame**)</span></span>
-   <span data-ttu-id="3eebd-120">Оценка количества кадров между ключевыми кадрами (**m \_ нкэйфрамепериод**)</span><span class="sxs-lookup"><span data-stu-id="3eebd-120">An estimate of how many frames there are between key frames (**m\_nKeyFramePeriod**)</span></span>

<span data-ttu-id="3eebd-121">После того как фильтр удалит кадр, он по-своему будет удалять кадры, пока не достигнет следующего ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="3eebd-121">Once the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="3eebd-122">Если этот метод возвращает **значение true**, он также отправляет [**событие \_ \_ изменения качества EC**](ec-quality-change.md) в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="3eebd-122">If this method returns **TRUE**, it also sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the Filter Graph Manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eebd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3eebd-123">Requirements</span></span>



| <span data-ttu-id="3eebd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3eebd-124">Requirement</span></span> | <span data-ttu-id="3eebd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3eebd-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eebd-126">Header</span><span class="sxs-lookup"><span data-stu-id="3eebd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3eebd-127"><dt>Втранс. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3eebd-127"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3eebd-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3eebd-128">Library</span></span><br/> | <dl> <span data-ttu-id="3eebd-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3eebd-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eebd-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3eebd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eebd-131">**Класс Квидеотрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="3eebd-131">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




