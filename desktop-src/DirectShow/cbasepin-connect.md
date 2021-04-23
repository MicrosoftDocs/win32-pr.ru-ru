---
description: 'Метод Connect подключает ПИН-код к другому ПИН-коду. Этот метод реализует метод Ипин:: Connect.'
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: Метод Кбасепин. Connect (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed8bcdab7e0909e59e7d9ec00645786f8ce48c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657995"
---
# <a name="cbasepinconnect-method"></a><span data-ttu-id="79ca6-104">Кбасепин. Connect, метод</span><span class="sxs-lookup"><span data-stu-id="79ca6-104">CBasePin.Connect method</span></span>

<span data-ttu-id="79ca6-105">`Connect`Метод подключает ПИН-код к другому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="79ca6-105">The `Connect` method connects the pin to another pin.</span></span> <span data-ttu-id="79ca6-106">Этот метод реализует метод [**Ипин:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) .</span><span class="sxs-lookup"><span data-stu-id="79ca6-106">This method implements the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="79ca6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79ca6-107">Syntax</span></span>


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="79ca6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="79ca6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79ca6-109">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="79ca6-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="79ca6-110">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) получающий ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="79ca6-110">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="79ca6-111">*состоит*</span><span class="sxs-lookup"><span data-stu-id="79ca6-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="79ca6-112">Указатель на структуру [**\_ \_ типа файлов мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , указывающую тип носителя для соединения.</span><span class="sxs-lookup"><span data-stu-id="79ca6-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type for the connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79ca6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79ca6-113">Return value</span></span>

<span data-ttu-id="79ca6-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="79ca6-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="79ca6-115">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="79ca6-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="79ca6-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="79ca6-116">Return code</span></span>                                                                                                  | <span data-ttu-id="79ca6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="79ca6-117">Description</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="79ca6-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="79ca6-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="79ca6-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="79ca6-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="79ca6-120"><dt>**VFW \_ E \_ уже \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="79ca6-120"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>    | <span data-ttu-id="79ca6-121">ПИН-код уже подключен.</span><span class="sxs-lookup"><span data-stu-id="79ca6-121">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="79ca6-122"><dt>**VFW \_ E \_ нет \_ приемлемых \_ типов**</dt></span><span class="sxs-lookup"><span data-stu-id="79ca6-122"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="79ca6-123">Не удалось найти допустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="79ca6-123">Could not find an acceptable media type.</span></span><br/>                                |
| <dl> <span data-ttu-id="79ca6-124"><dt>**VFW \_ E \_ не \_ остановлен**</dt></span><span class="sxs-lookup"><span data-stu-id="79ca6-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>          | <span data-ttu-id="79ca6-125">Фильтр активен, и ПИН-код не поддерживает динамическое повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="79ca6-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="79ca6-126"><dt>**\_тип VFW \_ E \_ не \_ принят**</dt></span><span class="sxs-lookup"><span data-stu-id="79ca6-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl>   | <span data-ttu-id="79ca6-127">Указан недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="79ca6-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="79ca6-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79ca6-128">Remarks</span></span>

<span data-ttu-id="79ca6-129">Параметр *ПЛТ* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="79ca6-129">The *pmt* parameter can be **NULL**.</span></span> <span data-ttu-id="79ca6-130">Также можно указать частичный тип носителя со значением GUID \_ null для основного типа, подтипа или формата.</span><span class="sxs-lookup"><span data-stu-id="79ca6-130">It can also specify a partial media type, with a value of GUID\_NULL for the major type, subtype, or format.</span></span>

<span data-ttu-id="79ca6-131">В базовом классе этот метод проверяет, подключен ли ПИН-код и был ли остановлен фильтр.</span><span class="sxs-lookup"><span data-stu-id="79ca6-131">In the base class, this method tests whether the pin is already connected and whether the filter is stopped.</span></span> <span data-ttu-id="79ca6-132">Он делегирует оставшуюся часть процесса подключения методу [**кбасепин:: агримедиатипе**](cbasepin-agreemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="79ca6-132">It delegates the rest of the connection process to the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="79ca6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="79ca6-133">Requirements</span></span>



| <span data-ttu-id="79ca6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="79ca6-134">Requirement</span></span> | <span data-ttu-id="79ca6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="79ca6-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79ca6-136">Header</span><span class="sxs-lookup"><span data-stu-id="79ca6-136">Header</span></span><br/>  | <dl> <span data-ttu-id="79ca6-137"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79ca6-137"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="79ca6-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="79ca6-138">Library</span></span><br/> | <dl> <span data-ttu-id="79ca6-139"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="79ca6-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79ca6-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79ca6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79ca6-141">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="79ca6-141">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




