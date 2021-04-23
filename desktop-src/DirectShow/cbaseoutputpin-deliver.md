---
description: Метод доставки предоставляет пример носителя для подключенного входного контакта.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: Метод Кбасеаутпутпин. доставки (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669179"
---
# <a name="cbaseoutputpindeliver-method"></a><span data-ttu-id="031c0-103">Метод Кбасеаутпутпин. доставки</span><span class="sxs-lookup"><span data-stu-id="031c0-103">CBaseOutputPin.Deliver method</span></span>

<span data-ttu-id="031c0-104">`Deliver`Метод доставляет пример носителя в подключенный входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="031c0-104">The `Deliver` method delivers a media sample to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="031c0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="031c0-105">Syntax</span></span>


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="031c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="031c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="031c0-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="031c0-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="031c0-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="031c0-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="031c0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="031c0-109">Return value</span></span>

<span data-ttu-id="031c0-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="031c0-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="031c0-111">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="031c0-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="031c0-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="031c0-112">Return code</span></span>                                                                                           | <span data-ttu-id="031c0-113">Описание</span><span class="sxs-lookup"><span data-stu-id="031c0-113">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="031c0-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="031c0-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="031c0-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="031c0-115">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="031c0-116"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="031c0-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="031c0-117">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="031c0-117">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="031c0-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="031c0-118">Remarks</span></span>

<span data-ttu-id="031c0-119">Этот метод вызывает метод [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="031c0-119">This method calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input pin.</span></span> <span data-ttu-id="031c0-120">**Receive** может блокироваться, если метод [**Имеминпутпин:: Рецеивеканблокк**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="031c0-120">**Receive** can block if the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method returns S\_OK.</span></span>

<span data-ttu-id="031c0-121">Выпустите пример после вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="031c0-121">Release the sample after calling this method.</span></span> <span data-ttu-id="031c0-122">Входной ПИН-код может содержать счетчик ссылок для образца, поэтому не используйте этот пример повторно.</span><span class="sxs-lookup"><span data-stu-id="031c0-122">The input pin might hold a reference count on the sample, so do not reuse the sample.</span></span> <span data-ttu-id="031c0-123">Всегда вызывайте метод [**кбасеаутпутпин:: жетделиверибуффер**](cbaseoutputpin-getdeliverybuffer.md) , чтобы получить новый пример.</span><span class="sxs-lookup"><span data-stu-id="031c0-123">Always call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain a new sample.</span></span>

<span data-ttu-id="031c0-124">Перед вызовом этого метода удерживайте критическую секцию фильтра.</span><span class="sxs-lookup"><span data-stu-id="031c0-124">Hold the filter's critical section before calling this method.</span></span> <span data-ttu-id="031c0-125">В противном случае ПИН-код может быть отключен во время вызова метода.</span><span class="sxs-lookup"><span data-stu-id="031c0-125">Otherwise, the pin might get disconnected during the method call.</span></span> <span data-ttu-id="031c0-126">Если фильтр использует рабочий поток для доставки образцов, задержите критическую секцию, когда фильтр готов к доставке примера.</span><span class="sxs-lookup"><span data-stu-id="031c0-126">If the filter uses a worker thread to deliver samples, hold the critical section when the filter is ready to deliver a sample.</span></span> <span data-ttu-id="031c0-127">В противном случае можно хранить критическую секцию в методе [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) фильтра, где фильтры обрабатывают образцы.</span><span class="sxs-lookup"><span data-stu-id="031c0-127">Otherwise, you can hold the critical section in the filter's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, where the filter processes samples.</span></span>

<span data-ttu-id="031c0-128">Рабочие потоки могут создавать потенциальные взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="031c0-128">Worker threads can create a potential deadlock.</span></span> <span data-ttu-id="031c0-129">Когда поток удерживает критическую секцию, он может ожидать изменения состояния в фильтре.</span><span class="sxs-lookup"><span data-stu-id="031c0-129">When the thread holds the critical section, it might wait on a state change in the filter.</span></span> <span data-ttu-id="031c0-130">В то же время изменение состояния может ожидать завершения потока.</span><span class="sxs-lookup"><span data-stu-id="031c0-130">At the same time, the state change might be waiting for the thread to complete.</span></span> <span data-ttu-id="031c0-131">Чтобы избежать этого, код изменения состояния должен сигнализировать о событии, завершающем поток, а затем ожидать завершения потока.</span><span class="sxs-lookup"><span data-stu-id="031c0-131">To prevent this, the state-change code should signal an event that terminates the thread, and then wait for the thread to signal completion.</span></span>

## <a name="requirements"></a><span data-ttu-id="031c0-132">Требования</span><span class="sxs-lookup"><span data-stu-id="031c0-132">Requirements</span></span>



| <span data-ttu-id="031c0-133">Требование</span><span class="sxs-lookup"><span data-stu-id="031c0-133">Requirement</span></span> | <span data-ttu-id="031c0-134">Значение</span><span class="sxs-lookup"><span data-stu-id="031c0-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="031c0-135">Header</span><span class="sxs-lookup"><span data-stu-id="031c0-135">Header</span></span><br/>  | <dl> <span data-ttu-id="031c0-136"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="031c0-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="031c0-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="031c0-137">Library</span></span><br/> | <dl> <span data-ttu-id="031c0-138"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="031c0-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="031c0-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="031c0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="031c0-140">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="031c0-140">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




