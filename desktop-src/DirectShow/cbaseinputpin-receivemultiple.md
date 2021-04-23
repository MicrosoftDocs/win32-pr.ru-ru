---
description: 'Метод Рецеивемултипле получает массив выборок. Этот метод реализует метод Имеминпутпин:: Рецеивемултипле.'
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Кбасеинпутпин. Рецеивемултипле, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669381"
---
# <a name="cbaseinputpinreceivemultiple-method"></a><span data-ttu-id="4c642-104">Кбасеинпутпин. Рецеивемултипле, метод</span><span class="sxs-lookup"><span data-stu-id="4c642-104">CBaseInputPin.ReceiveMultiple method</span></span>

<span data-ttu-id="4c642-105">`ReceiveMultiple`Метод получает массив выборок.</span><span class="sxs-lookup"><span data-stu-id="4c642-105">The `ReceiveMultiple` method receives an array of samples.</span></span> <span data-ttu-id="4c642-106">Этот метод реализует метод [**имеминпутпин:: рецеивемултипле**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .</span><span class="sxs-lookup"><span data-stu-id="4c642-106">This method implements the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c642-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c642-107">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="4c642-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c642-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c642-109">*псамплес*</span><span class="sxs-lookup"><span data-stu-id="4c642-109">*pSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="4c642-110">Адрес массива указателей [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) , размером *нсамплес*.</span><span class="sxs-lookup"><span data-stu-id="4c642-110">Address of an array of [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers, of size *nSamples*.</span></span>

</dd> <dt>

<span data-ttu-id="4c642-111">*нсамплес*</span><span class="sxs-lookup"><span data-stu-id="4c642-111">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="4c642-112">Количество выборок для обработки.</span><span class="sxs-lookup"><span data-stu-id="4c642-112">Number of samples to process.</span></span>

</dd> <dt>

<span data-ttu-id="4c642-113">*нсамплеспроцессед*</span><span class="sxs-lookup"><span data-stu-id="4c642-113">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="4c642-114">Указатель на переменную, которая получает количество обработанных выборок.</span><span class="sxs-lookup"><span data-stu-id="4c642-114">Pointer to a variable that receives the number of samples that were processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c642-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c642-115">Return value</span></span>

<span data-ttu-id="4c642-116">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c642-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4c642-117">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4c642-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="4c642-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4c642-118">Return code</span></span>                                                                                             | <span data-ttu-id="4c642-119">Описание</span><span class="sxs-lookup"><span data-stu-id="4c642-119">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="4c642-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4c642-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="4c642-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="4c642-121">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="4c642-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4c642-122"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="4c642-123">ПИН-код в данный момент очищается; Пример отклонен.</span><span class="sxs-lookup"><span data-stu-id="4c642-123">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="4c642-124"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4c642-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="4c642-125">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="4c642-125">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="4c642-126"><dt>**VFW \_ E \_ инвалидмедиатипе**</dt></span><span class="sxs-lookup"><span data-stu-id="4c642-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="4c642-127">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="4c642-127">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="4c642-128"><dt>**\_ \_ ошибка среды выполнения VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4c642-128"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="4c642-129">Произошла ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="4c642-129">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="4c642-130"><dt>**VFW \_ E — \_ неправильное \_ состояние**</dt></span><span class="sxs-lookup"><span data-stu-id="4c642-130"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="4c642-131">ПИН-код остановлен.</span><span class="sxs-lookup"><span data-stu-id="4c642-131">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="4c642-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c642-132">Remarks</span></span>

<span data-ttu-id="4c642-133">Этот метод ведет себя как метод [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) , но получает массив выборок.</span><span class="sxs-lookup"><span data-stu-id="4c642-133">This method behaves like the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, but receives an array of samples.</span></span> <span data-ttu-id="4c642-134">В базовом классе метод циклически перебирает массив и вызывает **Receive** с каждым образцом.</span><span class="sxs-lookup"><span data-stu-id="4c642-134">In the base class, the method loops through the array and calls **Receive** with each sample.</span></span> <span data-ttu-id="4c642-135">Переопределите эту функцию, если фильтр может обрабатывать пакеты образцов более эффективно, чем по одному за раз.</span><span class="sxs-lookup"><span data-stu-id="4c642-135">Override this function if your filter can process batches of samples more efficiently than processing them one at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c642-136">Требования</span><span class="sxs-lookup"><span data-stu-id="4c642-136">Requirements</span></span>



| <span data-ttu-id="4c642-137">Требование</span><span class="sxs-lookup"><span data-stu-id="4c642-137">Requirement</span></span> | <span data-ttu-id="4c642-138">Значение</span><span class="sxs-lookup"><span data-stu-id="4c642-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c642-139">Header</span><span class="sxs-lookup"><span data-stu-id="4c642-139">Header</span></span><br/>  | <dl> <span data-ttu-id="4c642-140"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c642-140"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4c642-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4c642-141">Library</span></span><br/> | <dl> <span data-ttu-id="4c642-142"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4c642-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c642-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c642-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c642-144">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="4c642-144">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




