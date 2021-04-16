---
description: Метод Динамикреконнект выполняет динамическое повторное подключение с новым типом носителя. Повторное подключение может произойти во время выполнения графа фильтра.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Кдинамикаутпутпин. Динамикреконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656849"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a><span data-ttu-id="125e2-104">Кдинамикаутпутпин. Динамикреконнект, метод</span><span class="sxs-lookup"><span data-stu-id="125e2-104">CDynamicOutputPin.DynamicReconnect method</span></span>

<span data-ttu-id="125e2-105">`DynamicReconnect`Метод выполняет динамическое повторное подключение с новым типом носителя.</span><span class="sxs-lookup"><span data-stu-id="125e2-105">The `DynamicReconnect` method performs a dynamic reconnection with a new media type.</span></span> <span data-ttu-id="125e2-106">Повторное подключение может произойти во время выполнения графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="125e2-106">The reconnection can occur while the filter graph is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="125e2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="125e2-107">Syntax</span></span>


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="125e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="125e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="125e2-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="125e2-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="125e2-110">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , указывающую тип носителя.</span><span class="sxs-lookup"><span data-stu-id="125e2-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="125e2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="125e2-111">Return value</span></span>

<span data-ttu-id="125e2-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="125e2-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="125e2-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="125e2-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="125e2-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="125e2-114">Return code</span></span>                                                                            | <span data-ttu-id="125e2-115">Описание</span><span class="sxs-lookup"><span data-stu-id="125e2-115">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="125e2-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="125e2-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="125e2-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="125e2-117">Success.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="125e2-118"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="125e2-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="125e2-119">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="125e2-119">Failure.</span></span> <span data-ttu-id="125e2-120">Возможно, фильтр-владелец не вызывал метод [**кдинамикаутпутпин:: сетконфигинфо**](cdynamicoutputpin-setconfiginfo.md) .</span><span class="sxs-lookup"><span data-stu-id="125e2-120">Possibly the owning filter did not call the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="125e2-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="125e2-121">Remarks</span></span>

<span data-ttu-id="125e2-122">Этот метод должен вызываться из того же потока, который доставляет данные в ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="125e2-122">This method must be called from the same thread that delivers data to the pin.</span></span> <span data-ttu-id="125e2-123">После вызова этого метода не удается доставить образцы со старым типом носителя.</span><span class="sxs-lookup"><span data-stu-id="125e2-123">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="125e2-124">Вызывающий объект должен гарантировать, что старые примеры не ожидаются.</span><span class="sxs-lookup"><span data-stu-id="125e2-124">The caller must ensure that no old samples are pending.</span></span>

<span data-ttu-id="125e2-125">Перед вызовом этого метода вызовите метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="125e2-125">Call [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="125e2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="125e2-126">Requirements</span></span>



| <span data-ttu-id="125e2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="125e2-127">Requirement</span></span> | <span data-ttu-id="125e2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="125e2-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="125e2-129">Header</span><span class="sxs-lookup"><span data-stu-id="125e2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="125e2-130"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="125e2-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="125e2-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="125e2-131">Library</span></span><br/> | <dl> <span data-ttu-id="125e2-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="125e2-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="125e2-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="125e2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="125e2-134">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="125e2-134">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




