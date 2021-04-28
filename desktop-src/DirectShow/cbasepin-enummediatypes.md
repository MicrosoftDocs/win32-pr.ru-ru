---
description: 'Кбасепин. Енуммедиатипес, метод Енуммедиатипес перечисляет предпочтительные типы мультимедиа для ПИН-кода. Этот метод реализует метод Ипин:: Енуммедиатипес.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Кбасепин. Енуммедиатипес, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c68fe1ab83724149dcd2fb58a60e9c6950d887ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099392"
---
# <a name="cbasepinenummediatypes-method"></a><span data-ttu-id="62ae7-104">Кбасепин. Енуммедиатипес, метод</span><span class="sxs-lookup"><span data-stu-id="62ae7-104">CBasePin.EnumMediaTypes method</span></span>

<span data-ttu-id="62ae7-105">`EnumMediaTypes`Метод перечисляет предпочтительные типы мультимедиа для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="62ae7-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="62ae7-106">Этот метод реализует метод [**Ипин:: енуммедиатипес**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="62ae7-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ae7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62ae7-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="62ae7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="62ae7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62ae7-109">*ппенум*</span><span class="sxs-lookup"><span data-stu-id="62ae7-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="62ae7-110">Адрес переменной, которая получает указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="62ae7-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62ae7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62ae7-111">Return value</span></span>

<span data-ttu-id="62ae7-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62ae7-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="62ae7-113">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="62ae7-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="62ae7-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="62ae7-114">Return code</span></span>                                                                                   | <span data-ttu-id="62ae7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="62ae7-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="62ae7-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="62ae7-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="62ae7-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="62ae7-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="62ae7-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="62ae7-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="62ae7-119">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="62ae7-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="62ae7-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="62ae7-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="62ae7-121">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="62ae7-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62ae7-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="62ae7-122">Remarks</span></span>

<span data-ttu-id="62ae7-123">Входные сигналы не требуются для перечисления каких-либо предпочтительных типов.</span><span class="sxs-lookup"><span data-stu-id="62ae7-123">Input pins are not required to enumerate any preferred types.</span></span> <span data-ttu-id="62ae7-124">Выходные контакты должны перечислить по крайней мере один предпочтительный тип.</span><span class="sxs-lookup"><span data-stu-id="62ae7-124">Output pins must enumerate at least one preferred type.</span></span> <span data-ttu-id="62ae7-125">В противном случае у обоих ПИН-кодов может не быть предпочтительного типа, что делает соединение невозможным.</span><span class="sxs-lookup"><span data-stu-id="62ae7-125">Otherwise, both pins could lack a preferred type, making a connection impossible.</span></span>

<span data-ttu-id="62ae7-126">Интерфейс **иенуммедиатипес** работает как стандартный перечислитель com.</span><span class="sxs-lookup"><span data-stu-id="62ae7-126">The **IEnumMediaTypes** interface works like a standard COM enumerator.</span></span> <span data-ttu-id="62ae7-127">Дополнительные сведения см. [в разделе Перечисление объектов в графе фильтра](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="62ae7-127">For more information, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span> <span data-ttu-id="62ae7-128">Если метод выполнен успешно, то интерфейс **иенуммедиатипес** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="62ae7-128">If the method succeeds, the **IEnumMediaTypes** interface has an outstanding reference count.</span></span> <span data-ttu-id="62ae7-129">Не забудьте освободить его по завершении.</span><span class="sxs-lookup"><span data-stu-id="62ae7-129">Be sure to release it when you are done.</span></span>

<span data-ttu-id="62ae7-130">Базовый класс [**ценуммедиатипес**](cenummediatypes.md) реализует **иенуммедиатипес**.</span><span class="sxs-lookup"><span data-stu-id="62ae7-130">The [**CEnumMediaTypes**](cenummediatypes.md) base class implements **IEnumMediaTypes**.</span></span> <span data-ttu-id="62ae7-131">Он вызывает метод [**кбасепин:: жетмедиатипе**](cbasepin-getmediatype.md) ПИН-кода для перечисления типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="62ae7-131">It calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to enumerate the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ae7-132">Требования</span><span class="sxs-lookup"><span data-stu-id="62ae7-132">Requirements</span></span>



| <span data-ttu-id="62ae7-133">Требование</span><span class="sxs-lookup"><span data-stu-id="62ae7-133">Requirement</span></span> | <span data-ttu-id="62ae7-134">Значение</span><span class="sxs-lookup"><span data-stu-id="62ae7-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ae7-135">Header</span><span class="sxs-lookup"><span data-stu-id="62ae7-135">Header</span></span><br/>  | <dl> <span data-ttu-id="62ae7-136"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62ae7-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="62ae7-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="62ae7-137">Library</span></span><br/> | <dl> <span data-ttu-id="62ae7-138"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="62ae7-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62ae7-139">См. также</span><span class="sxs-lookup"><span data-stu-id="62ae7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ae7-140">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="62ae7-140">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




