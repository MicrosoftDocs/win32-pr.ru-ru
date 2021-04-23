---
description: Метод Чанжемедиатипе динамически изменяет тип носителя для соединения.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Кдинамикаутпутпин. Чанжемедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658079"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a><span data-ttu-id="2b342-103">Кдинамикаутпутпин. Чанжемедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="2b342-103">CDynamicOutputPin.ChangeMediaType method</span></span>

<span data-ttu-id="2b342-104">`ChangeMediaType`Метод динамически изменяет тип носителя для соединения.</span><span class="sxs-lookup"><span data-stu-id="2b342-104">The `ChangeMediaType` method dynamically changes the media type for the connection.</span></span> <span data-ttu-id="2b342-105">Это изменение может произойти при выполнении графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="2b342-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="2b342-106">После вызова этого метода не удается доставить образцы со старым типом носителя.</span><span class="sxs-lookup"><span data-stu-id="2b342-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="2b342-107">Вызывающий объект должен гарантировать, что старые примеры не ожидаются.</span><span class="sxs-lookup"><span data-stu-id="2b342-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b342-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b342-108">Syntax</span></span>


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="2b342-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b342-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b342-110">*состоит*</span><span class="sxs-lookup"><span data-stu-id="2b342-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2b342-111">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , указывающую тип носителя.</span><span class="sxs-lookup"><span data-stu-id="2b342-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b342-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b342-112">Return value</span></span>

<span data-ttu-id="2b342-113">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b342-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2b342-114">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2b342-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2b342-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2b342-115">Return code</span></span>                                                                                           | <span data-ttu-id="2b342-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2b342-116">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2b342-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2b342-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="2b342-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2b342-118">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="2b342-119"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="2b342-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="2b342-120">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="2b342-120">Failure.</span></span> <span data-ttu-id="2b342-121">Возможно, фильтр-владелец не вызывал [**кдинамикаутпутпин:: сетконфигинфо**](cdynamicoutputpin-setconfiginfo.md).</span><span class="sxs-lookup"><span data-stu-id="2b342-121">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="2b342-122"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="2b342-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2b342-123">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="2b342-123">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="2b342-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b342-124">Remarks</span></span>

<span data-ttu-id="2b342-125">Перед вызовом этого метода вызовите метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="2b342-125">Call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

<span data-ttu-id="2b342-126">Этот метод сначала проверяет, может ли нисходящий входной ПИН-код принимать новый формат без повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="2b342-126">This method first checks whether the downstream input pin can accept the new format without reconnecting.</span></span> <span data-ttu-id="2b342-127">Он запрашивает входной ПИН-код для интерфейса [**ипинконнектион**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) .</span><span class="sxs-lookup"><span data-stu-id="2b342-127">It queries the input pin for the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="2b342-128">Если входной ПИН-код поддерживает **ипинконнектион**, метод вызывает метод [**Ипинконнектион::D инамиккуерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) с предложенным типом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2b342-128">If the input pin supports **IPinConnection**, the method calls the [**IPinConnection::DynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) method with the proposed media type.</span></span> <span data-ttu-id="2b342-129">Если входной ПИН-код принимает новый тип мультимедиа, метод вызывает метод [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) и повторно согласовывает требования распределителя.</span><span class="sxs-lookup"><span data-stu-id="2b342-129">If the input pin accepts the new media type, the method calls the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method and renegotiates the allocator requirements.</span></span>

<span data-ttu-id="2b342-130">С другой стороны, если подчиненный ПИН-код не поддерживает **ипинконнектион** или если он отклоняет новый тип мультимедиа, метод вызывает метод [**Кдинамикаутпутпин::D инамикреконнект**](cdynamicoutputpin-dynamicreconnect.md) для выполнения динамического повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="2b342-130">On the other hand, if the downstream pin does not support **IPinConnection**, or if it rejects the new media type, the method calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to perform a dynamic reconnection.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b342-131">Требования</span><span class="sxs-lookup"><span data-stu-id="2b342-131">Requirements</span></span>



| <span data-ttu-id="2b342-132">Требование</span><span class="sxs-lookup"><span data-stu-id="2b342-132">Requirement</span></span> | <span data-ttu-id="2b342-133">Значение</span><span class="sxs-lookup"><span data-stu-id="2b342-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b342-134">Header</span><span class="sxs-lookup"><span data-stu-id="2b342-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2b342-135"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b342-135"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2b342-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b342-136">Library</span></span><br/> | <dl> <span data-ttu-id="2b342-137"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2b342-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b342-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b342-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b342-139">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="2b342-139">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




