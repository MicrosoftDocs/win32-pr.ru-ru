---
description: 'Метод Receive получает пример носителя, обрабатывает его и доставляет образец вывода в нисходящий фильтр. Этот метод переопределяет метод Ктрансформфилтер:: Receive.'
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: Метод Квидеотрансформфилтер. Receive (Втранс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675626"
---
# <a name="cvideotransformfilterreceive-method"></a><span data-ttu-id="d3b51-104">Квидеотрансформфилтер. Receive, метод</span><span class="sxs-lookup"><span data-stu-id="d3b51-104">CVideoTransformFilter.Receive method</span></span>

<span data-ttu-id="d3b51-105">`Receive`Метод получает пример носителя, обрабатывает его и доставляет образец вывода в нисходящий фильтр.</span><span class="sxs-lookup"><span data-stu-id="d3b51-105">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> <span data-ttu-id="d3b51-106">Этот метод переопределяет метод [**ктрансформфилтер:: Receive**](ctransformfilter-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="d3b51-106">This method overrides the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b51-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3b51-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="d3b51-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3b51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b51-109">*псампле*</span><span class="sxs-lookup"><span data-stu-id="d3b51-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="d3b51-110">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) в образце входных данных.</span><span class="sxs-lookup"><span data-stu-id="d3b51-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b51-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3b51-111">Return value</span></span>

<span data-ttu-id="d3b51-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3b51-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d3b51-113">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="d3b51-113">Possible values include the following:</span></span>



| <span data-ttu-id="d3b51-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d3b51-114">Return code</span></span>                                                                             | <span data-ttu-id="d3b51-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d3b51-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="d3b51-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d3b51-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d3b51-117">Вышестоящий фильтр должен закончить отправку образцов.</span><span class="sxs-lookup"><span data-stu-id="d3b51-117">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="d3b51-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d3b51-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d3b51-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="d3b51-119">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="d3b51-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3b51-120">Remarks</span></span>

<span data-ttu-id="d3b51-121">Этот метод вызывает [**квидеотрансформфилтер:: шаулдскипфраме**](cvideotransformfilter-shouldskipframe.md) , чтобы определить, должен ли он доставлять этот пример или просто отбросить его.</span><span class="sxs-lookup"><span data-stu-id="d3b51-121">This method calls [**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) to determine whether it should deliver this sample or simply discard it.</span></span> <span data-ttu-id="d3b51-122">Если **шаулдскипфраме** возвращает **значение false** (что означает, что выбор должен быть доставлен), метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d3b51-122">If **ShouldSkipFrame** returns **FALSE** (indicating the sample should be delivered), the method does the following:</span></span>

1.  <span data-ttu-id="d3b51-123">Вызывает [**ктрансформфилтер:: инитиализеаутпутсампле**](ctransformfilter-initializeoutputsample.md) для подготовки примера вывода</span><span class="sxs-lookup"><span data-stu-id="d3b51-123">Calls [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) to prepare the output sample</span></span>
2.  <span data-ttu-id="d3b51-124">Вызывает метод [**ктрансформфилтер:: Transform**](ctransformfilter-transform.md) для обработки входного примера.</span><span class="sxs-lookup"><span data-stu-id="d3b51-124">Calls [**CTransformFilter::Transform**](ctransformfilter-transform.md) to process the input sample.</span></span> <span data-ttu-id="d3b51-125">Этот метод является чисто виртуальным и должен быть реализован в производном классе.</span><span class="sxs-lookup"><span data-stu-id="d3b51-125">This method is pure virtual, and must be implemented in the derived class.</span></span>
3.  <span data-ttu-id="d3b51-126">Вызывает [**кбасеаутпутпин::D еливер**](cbaseoutputpin-deliver.md) для доставки примера Output.</span><span class="sxs-lookup"><span data-stu-id="d3b51-126">Calls [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) to deliver the output sample.</span></span>

<span data-ttu-id="d3b51-127">Кроме того, этот метод проверяет изменения формата во входном или выходном примере путем вызова [**имедиасампле:: жетмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="d3b51-127">Also, this method checks for format changes on the input or output sample, by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="d3b51-128">При изменении формата метод задает тип соединения для соответствующего ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d3b51-128">If there is a format change, the method sets the connection type on the corresponding pin.</span></span> <span data-ttu-id="d3b51-129">Прежде чем задается новый тип, он вызывает **стопстреаминг**.</span><span class="sxs-lookup"><span data-stu-id="d3b51-129">Before it sets the new type, it calls **StopStreaming**.</span></span> <span data-ttu-id="d3b51-130">После установки нового типа он вызывает **стартстреаминг**.</span><span class="sxs-lookup"><span data-stu-id="d3b51-130">After it sets the new type, it calls **StartStreaming**.</span></span> <span data-ttu-id="d3b51-131">Производный класс может использовать эти методы для обновления своего внутреннего состояния.</span><span class="sxs-lookup"><span data-stu-id="d3b51-131">The derived class can use these methods to update its internal state.</span></span> <span data-ttu-id="d3b51-132">Производному классу также может потребоваться проверить новый формат в его методе **Transform** .</span><span class="sxs-lookup"><span data-stu-id="d3b51-132">The derived class might also need to check for the new format in its **Transform** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b51-133">Требования</span><span class="sxs-lookup"><span data-stu-id="d3b51-133">Requirements</span></span>



| <span data-ttu-id="d3b51-134">Требование</span><span class="sxs-lookup"><span data-stu-id="d3b51-134">Requirement</span></span> | <span data-ttu-id="d3b51-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d3b51-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b51-136">Header</span><span class="sxs-lookup"><span data-stu-id="d3b51-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d3b51-137"><dt>Втранс. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3b51-137"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d3b51-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d3b51-138">Library</span></span><br/> | <dl> <span data-ttu-id="d3b51-139"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d3b51-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3b51-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3b51-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b51-141">**Класс Квидеотрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="d3b51-141">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




