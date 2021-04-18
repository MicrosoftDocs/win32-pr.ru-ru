---
description: 'Метод Receive получает следующий образец носителя в потоке. Этот метод реализует метод Имеминпутпин:: Receive.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Метод Кбасеинпутпин. Receive (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10306d5568ae1754105a4367952cef82f931be99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656913"
---
# <a name="cbaseinputpinreceive-method"></a><span data-ttu-id="4724a-104">Кбасеинпутпин. Receive, метод</span><span class="sxs-lookup"><span data-stu-id="4724a-104">CBaseInputPin.Receive method</span></span>

<span data-ttu-id="4724a-105">`Receive`Метод получает следующий пример носителя в потоке.</span><span class="sxs-lookup"><span data-stu-id="4724a-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="4724a-106">Этот метод реализует метод [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="4724a-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4724a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4724a-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="4724a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4724a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4724a-109">*псампле*</span><span class="sxs-lookup"><span data-stu-id="4724a-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="4724a-110">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="4724a-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4724a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4724a-111">Return value</span></span>

<span data-ttu-id="4724a-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4724a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4724a-113">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4724a-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="4724a-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4724a-114">Return code</span></span>                                                                                             | <span data-ttu-id="4724a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4724a-115">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="4724a-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4724a-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="4724a-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="4724a-117">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="4724a-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4724a-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="4724a-119">ПИН-код в данный момент очищается; Пример отклонен.</span><span class="sxs-lookup"><span data-stu-id="4724a-119">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="4724a-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4724a-120"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="4724a-121">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="4724a-121">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="4724a-122"><dt>**VFW \_ E \_ инвалидмедиатипе**</dt></span><span class="sxs-lookup"><span data-stu-id="4724a-122"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="4724a-123">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="4724a-123">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="4724a-124"><dt>**\_ \_ ошибка среды выполнения VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4724a-124"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="4724a-125">Произошла ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="4724a-125">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="4724a-126"><dt>**VFW \_ E — \_ неправильное \_ состояние**</dt></span><span class="sxs-lookup"><span data-stu-id="4724a-126"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="4724a-127">ПИН-код остановлен.</span><span class="sxs-lookup"><span data-stu-id="4724a-127">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="4724a-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4724a-128">Remarks</span></span>

<span data-ttu-id="4724a-129">Входной ПИН-код вышестоящего выхода вызывает этот метод для доставки образца на входный ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="4724a-129">The upstream output pin calls this method to deliver a sample to the input pin.</span></span> <span data-ttu-id="4724a-130">Входной ПИН-код должен выполнять одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="4724a-130">The input pin must do one of the following:</span></span>

-   <span data-ttu-id="4724a-131">Обработайте пример перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="4724a-131">Process the sample before returning.</span></span>
-   <span data-ttu-id="4724a-132">Верните и обработайте пример в рабочем потоке.</span><span class="sxs-lookup"><span data-stu-id="4724a-132">Return, and process the sample in a worker thread.</span></span>
-   <span data-ttu-id="4724a-133">Отклонить пример.</span><span class="sxs-lookup"><span data-stu-id="4724a-133">Reject the sample.</span></span>

<span data-ttu-id="4724a-134">Если ПИН-код использует рабочий поток для обработки образца, добавьте счетчик ссылок в образец внутри этого метода.</span><span class="sxs-lookup"><span data-stu-id="4724a-134">If the pin uses a worker thread to process the sample, add a reference count to the sample inside this method.</span></span> <span data-ttu-id="4724a-135">После возврата метода вышестоящий ПИН-код освобождает пример.</span><span class="sxs-lookup"><span data-stu-id="4724a-135">After the method returns, the upstream pin releases the sample.</span></span> <span data-ttu-id="4724a-136">Когда число ссылок в образце достигает нуля, пример возвращается к распределителю для повторного использования.</span><span class="sxs-lookup"><span data-stu-id="4724a-136">When the sample's reference count reaches zero, the sample returns to the allocator for re-use.</span></span>

<span data-ttu-id="4724a-137">Этот метод является синхронным и может блокироваться.</span><span class="sxs-lookup"><span data-stu-id="4724a-137">This method is synchronous and can block.</span></span> <span data-ttu-id="4724a-138">Если метод может блокироваться, метод [**кбасеинпутпин:: рецеивеканблокк**](cbaseinputpin-receivecanblock.md) в ПИН-коде должен вернуть значение s \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4724a-138">If the method might block, the pin's [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) method should return S\_OK.</span></span>

<span data-ttu-id="4724a-139">В базовом классе этот метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4724a-139">In the base class, this method performs the following steps:</span></span>

1.  <span data-ttu-id="4724a-140">Вызывает метод [**кбасеинпутпин:: чеккстреаминг**](cbaseinputpin-checkstreaming.md) , чтобы убедиться, что ПИН-код может обработать образцы сейчас.</span><span class="sxs-lookup"><span data-stu-id="4724a-140">Calls the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method to verify that the pin can process samples now.</span></span> <span data-ttu-id="4724a-141">Если это невозможно, например, если ПИН-код остановлен, метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4724a-141">If it cannot for example, if the pin is stopped the method fails.</span></span>
2.  <span data-ttu-id="4724a-142">Извлекает пример свойств и проверяет, был ли изменен формат (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="4724a-142">Retrieves the sample properties and checks whether the format has changed (see below).</span></span>
3.  <span data-ttu-id="4724a-143">Если формат изменился, метод вызывает метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) , чтобы определить, приемлем ли новый формат.</span><span class="sxs-lookup"><span data-stu-id="4724a-143">If the format has changed, the method calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the new format is acceptable.</span></span>
4.  <span data-ttu-id="4724a-144">Если новый формат неприемлем, метод вызывает метод [**кбасепин:: EndOfStream**](cbasepin-endofstream.md) , ОТПРАВЛЯЕТ \_ событие EC еррораборт и возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="4724a-144">If the new format is not acceptable, the method calls the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method, posts an EC\_ERRORABORT event, and returns an error code.</span></span>
5.  <span data-ttu-id="4724a-145">Если ошибок нет, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4724a-145">Assuming there were no errors, the method returns S\_OK.</span></span>

<span data-ttu-id="4724a-146">Проверьте формат, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4724a-146">Test for a format change as follows:</span></span>

-   <span data-ttu-id="4724a-147">Если образец поддерживает интерфейс [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) , проверьте элемент **двсамплефлагс** структуры [**\_ \_ свойств SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="4724a-147">If the sample supports the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface, check the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span> <span data-ttu-id="4724a-148">Если установлен \_ \_ флаг типечанжед для примера, формат изменился.</span><span class="sxs-lookup"><span data-stu-id="4724a-148">If the AM\_SAMPLE\_TYPECHANGED flag is present, the format has changed.</span></span>
-   <span data-ttu-id="4724a-149">В противном случае, если образец не поддерживает **IMediaSample2**, вызовите метод [**Имедиасампле:: жетмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .</span><span class="sxs-lookup"><span data-stu-id="4724a-149">Otherwise, if the sample does not support **IMediaSample2**, call the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span> <span data-ttu-id="4724a-150">Если метод возвращает значение, отличное от **null** , формат изменился.</span><span class="sxs-lookup"><span data-stu-id="4724a-150">If the method returns a non-**NULL** value, the format has changed.</span></span>

<span data-ttu-id="4724a-151">В базовом классе этот метод не обрабатывает пример.</span><span class="sxs-lookup"><span data-stu-id="4724a-151">In the base class, this method does not process the sample.</span></span> <span data-ttu-id="4724a-152">Производный класс должен переопределить этот метод для выполнения обработки.</span><span class="sxs-lookup"><span data-stu-id="4724a-152">The derived class must override this method to perform the processing.</span></span> <span data-ttu-id="4724a-153">(То, что это влечет, полностью зависит от фильтра.) Производный класс должен вызвать метод базового класса, чтобы проверить наличие ошибок, описанных выше.</span><span class="sxs-lookup"><span data-stu-id="4724a-153">(What this entails depends entirely on the filter.) The derived class should call the base-class method, to check for the errors described previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="4724a-154">Требования</span><span class="sxs-lookup"><span data-stu-id="4724a-154">Requirements</span></span>



| <span data-ttu-id="4724a-155">Требование</span><span class="sxs-lookup"><span data-stu-id="4724a-155">Requirement</span></span> | <span data-ttu-id="4724a-156">Значение</span><span class="sxs-lookup"><span data-stu-id="4724a-156">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4724a-157">Header</span><span class="sxs-lookup"><span data-stu-id="4724a-157">Header</span></span><br/>  | <dl> <span data-ttu-id="4724a-158"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4724a-158"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4724a-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4724a-159">Library</span></span><br/> | <dl> <span data-ttu-id="4724a-160"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4724a-160"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4724a-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4724a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4724a-162">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="4724a-162">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




