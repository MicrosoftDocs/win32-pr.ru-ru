---
description: Метод Реконнектпин прерывает существующее подключение к заданному ПИН-коду и повторно подключает его к тому же ПИН-коду, используя указанный тип носителя.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Кбасефилтер. Реконнектпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22507995621d708e40437175d7004d10f68fedb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656870"
---
# <a name="cbasefilterreconnectpin-method"></a><span data-ttu-id="2ecb0-103">Кбасефилтер. Реконнектпин, метод</span><span class="sxs-lookup"><span data-stu-id="2ecb0-103">CBaseFilter.ReconnectPin method</span></span>

<span data-ttu-id="2ecb0-104">`ReconnectPin`Метод прерывает существующее подключение к заданному ПИН-коду и повторно подключает его к тому же ПИН-коду, используя указанный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="2ecb0-104">The `ReconnectPin` method breaks an existing pin connection and reconnects it to the same pin, using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ecb0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ecb0-105">Syntax</span></span>


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="2ecb0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ecb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ecb0-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="2ecb0-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="2ecb0-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="2ecb0-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2ecb0-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="2ecb0-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2ecb0-110">Указатель на структуру [**\_ \_ типа файлов мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , указывающую тип носителя, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2ecb0-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ecb0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ecb0-111">Return value</span></span>

<span data-ttu-id="2ecb0-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ecb0-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2ecb0-113">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2ecb0-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="2ecb0-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2ecb0-114">Return code</span></span>                                                                                   | <span data-ttu-id="2ecb0-115">Описание</span><span class="sxs-lookup"><span data-stu-id="2ecb0-115">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ecb0-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2ecb0-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2ecb0-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2ecb0-117">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="2ecb0-118"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="2ecb0-118"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="2ecb0-119">Переменная-член [**m \_ Пграф**](cbasefilter-m-pgraph.md) имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2ecb0-119">[**m\_pGraph**](cbasefilter-m-pgraph.md) member variable is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2ecb0-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ecb0-120">Remarks</span></span>

<span data-ttu-id="2ecb0-121">Этот метод вызывает метод [**IFilterGraph2:: реконнектекс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="2ecb0-121">This method calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span> <span data-ttu-id="2ecb0-122">Если интерфейс [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) недоступен, метод вызывает [**ифилтерграф:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span><span class="sxs-lookup"><span data-stu-id="2ecb0-122">If the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface is not available, the method calls [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ecb0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="2ecb0-123">Requirements</span></span>



| <span data-ttu-id="2ecb0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="2ecb0-124">Requirement</span></span> | <span data-ttu-id="2ecb0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="2ecb0-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ecb0-126">Header</span><span class="sxs-lookup"><span data-stu-id="2ecb0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2ecb0-127"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ecb0-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2ecb0-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ecb0-128">Library</span></span><br/> | <dl> <span data-ttu-id="2ecb0-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2ecb0-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ecb0-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ecb0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ecb0-131">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="2ecb0-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




