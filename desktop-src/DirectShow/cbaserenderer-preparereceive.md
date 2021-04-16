---
description: Метод Препаререцеиве готовит фильтр для подготовки к просмотру примера.
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: Кбасерендерер. Препаререцеиве, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658051"
---
# <a name="cbaserendererpreparereceive-method"></a><span data-ttu-id="56faf-103">Кбасерендерер. Препаререцеиве, метод</span><span class="sxs-lookup"><span data-stu-id="56faf-103">CBaseRenderer.PrepareReceive method</span></span>

<span data-ttu-id="56faf-104">`PrepareReceive`Метод подготавливает фильтр для подготовки к просмотру примера.</span><span class="sxs-lookup"><span data-stu-id="56faf-104">The `PrepareReceive` method prepares the filter to render a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="56faf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56faf-105">Syntax</span></span>


```C++
virtual HRESULT PrepareReceive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="56faf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="56faf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56faf-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="56faf-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="56faf-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="56faf-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56faf-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56faf-109">Return value</span></span>

<span data-ttu-id="56faf-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56faf-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="56faf-111">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="56faf-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="56faf-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="56faf-112">Return code</span></span>                                                                                             | <span data-ttu-id="56faf-113">Описание</span><span class="sxs-lookup"><span data-stu-id="56faf-113">Description</span></span>                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="56faf-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="56faf-114"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="56faf-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="56faf-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="56faf-116"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="56faf-116"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="56faf-117">сбой.</span><span class="sxs-lookup"><span data-stu-id="56faf-117">Failed.</span></span><br/>                         |
| <dl> <span data-ttu-id="56faf-118"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="56faf-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="56faf-119">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="56faf-119">Unexpected error.</span></span><br/>               |
| <dl> <span data-ttu-id="56faf-120"><dt>**Пример с VFW \_ E \_ \_ отклонен**</dt></span><span class="sxs-lookup"><span data-stu-id="56faf-120"><dt>**VFW\_E\_SAMPLE\_REJECTED**</dt></span></span> </dl> | <span data-ttu-id="56faf-121">Фильтр удаляет этот пример.</span><span class="sxs-lookup"><span data-stu-id="56faf-121">Filter is dropping this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="56faf-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56faf-122">Remarks</span></span>

<span data-ttu-id="56faf-123">Фильтр вызывает этот метод из метода [**кбасерендерер:: Receive**](cbaserenderer-receive.md) перед отрисовкой примера.</span><span class="sxs-lookup"><span data-stu-id="56faf-123">The filter calls this method from inside the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, before it renders a sample.</span></span> <span data-ttu-id="56faf-124">Если фильтр работает, этот метод планирует пример для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="56faf-124">If the filter is running, this method schedules the sample for rendering.</span></span>

<span data-ttu-id="56faf-125">Если у фильтра уже есть образец, ожидающий выполнения, или если конец потока уже достигнут, метод возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="56faf-125">If the filter already has a pending sample, or if the end-of-stream was already reached, the method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="56faf-126">Возможно, вышестоящий фильтр не сериализует вызовы потоковой передачи правильно.</span><span class="sxs-lookup"><span data-stu-id="56faf-126">Possibly the upstream filter is not serializing its streaming calls correctly.</span></span>

<span data-ttu-id="56faf-127">Если алгоритм планирования определяет, что этот пример следует удалить (см. раздел [**кбасерендерер:: счедулесампле**](cbaserenderer-schedulesample.md)), метод возвращает пример "VFW E", который был \_ \_ \_ отклонен.</span><span class="sxs-lookup"><span data-stu-id="56faf-127">If the scheduling algorithm determines that the sample should be dropped (see [**CBaseRenderer::ScheduleSample**](cbaserenderer-schedulesample.md)), the method returns VFW\_E\_SAMPLE\_REJECTED.</span></span> <span data-ttu-id="56faf-128">Однако метод [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) входного контакта не передает этот код ошибки в вышестоящий фильтр, так как удаление образца не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="56faf-128">However, the input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method does not pass this error code to the upstream filter, because dropping a sample is not an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="56faf-129">Требования</span><span class="sxs-lookup"><span data-stu-id="56faf-129">Requirements</span></span>



| <span data-ttu-id="56faf-130">Требование</span><span class="sxs-lookup"><span data-stu-id="56faf-130">Requirement</span></span> | <span data-ttu-id="56faf-131">Значение</span><span class="sxs-lookup"><span data-stu-id="56faf-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56faf-132">Header</span><span class="sxs-lookup"><span data-stu-id="56faf-132">Header</span></span><br/>  | <dl> <span data-ttu-id="56faf-133"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56faf-133"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="56faf-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="56faf-134">Library</span></span><br/> | <dl> <span data-ttu-id="56faf-135"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="56faf-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56faf-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56faf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56faf-137">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="56faf-137">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




