---
description: 'Метод Рецеивеконнектион принимает соединение из другого ПИН-кода. Этот метод реализует метод Ипин:: Рецеивеконнектион.'
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: Кбасепин. Рецеивеконнектион, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657667"
---
# <a name="cbasepinreceiveconnection-method"></a><span data-ttu-id="89268-104">Кбасепин. Рецеивеконнектион, метод</span><span class="sxs-lookup"><span data-stu-id="89268-104">CBasePin.ReceiveConnection method</span></span>

<span data-ttu-id="89268-105">`ReceiveConnection`Метод принимает соединение с другого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="89268-105">The `ReceiveConnection` method accepts a connection from another pin.</span></span> <span data-ttu-id="89268-106">Этот метод реализует метод [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) .</span><span class="sxs-lookup"><span data-stu-id="89268-106">This method implements the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="89268-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89268-107">Syntax</span></span>


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="89268-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="89268-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89268-109">*пконнектор*</span><span class="sxs-lookup"><span data-stu-id="89268-109">*pConnector*</span></span> 
</dt> <dd>

<span data-ttu-id="89268-110">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) соединительного контакта.</span><span class="sxs-lookup"><span data-stu-id="89268-110">Pointer to the connecting pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="89268-111">*состоит*</span><span class="sxs-lookup"><span data-stu-id="89268-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="89268-112">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , указывающую тип носителя.</span><span class="sxs-lookup"><span data-stu-id="89268-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89268-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89268-113">Return value</span></span>

<span data-ttu-id="89268-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89268-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="89268-115">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="89268-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="89268-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="89268-116">Return code</span></span>                                                                                                | <span data-ttu-id="89268-117">Описание</span><span class="sxs-lookup"><span data-stu-id="89268-117">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89268-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="89268-118"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="89268-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="89268-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="89268-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="89268-120"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="89268-121">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="89268-121">**NULL** pointer argument.</span></span><br/>                                              |
| <dl> <span data-ttu-id="89268-122"><dt>**VFW \_ E \_ уже \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="89268-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="89268-123">ПИН-код уже подключен.</span><span class="sxs-lookup"><span data-stu-id="89268-123">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="89268-124"><dt>**VFW \_ E \_ не \_ остановлен**</dt></span><span class="sxs-lookup"><span data-stu-id="89268-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>        | <span data-ttu-id="89268-125">Фильтр активен, и ПИН-код не поддерживает динамическое повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="89268-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="89268-126"><dt>**\_тип VFW \_ E \_ не \_ принят**</dt></span><span class="sxs-lookup"><span data-stu-id="89268-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="89268-127">Указан недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="89268-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="89268-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89268-128">Remarks</span></span>

<span data-ttu-id="89268-129">Закрепление вывода вызывает этот метод для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="89268-129">The output pin calls this method on the input pin.</span></span> <span data-ttu-id="89268-130">Если закрепление ввода возвращает код ошибки, соединение завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="89268-130">If the input pin returns an error code, the connection fails.</span></span>

<span data-ttu-id="89268-131">В базовом классе этот метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="89268-131">In the base class, this method performs the following steps:</span></span>

-   <span data-ttu-id="89268-132">Проверяет, подключен ли ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="89268-132">Checks whether the pin is already connected.</span></span>
-   <span data-ttu-id="89268-133">Проверяет, остановлен ли фильтр.</span><span class="sxs-lookup"><span data-stu-id="89268-133">Checks whether the filter is stopped.</span></span>
-   <span data-ttu-id="89268-134">Вызывает метод [**кбасепин:: чеккконнект**](cbasepin-checkconnect.md) , чтобы проверить, подходит ли соединительный ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="89268-134">Calls the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method to test whether the connecting pin is suitable.</span></span>
-   <span data-ttu-id="89268-135">Вызывает метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) , чтобы проверить, является ли тип мультимедиа допустимым.</span><span class="sxs-lookup"><span data-stu-id="89268-135">Calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to test whether the media type is acceptable.</span></span>

<span data-ttu-id="89268-136">Если все эти шаги выполнены, метод вызывает методы [**кбасепин:: комплетеконнект**](cbasepin-completeconnect.md) и [**сетмедиатипе**](cbasepin-setmediatype.md) для завершения соединения.</span><span class="sxs-lookup"><span data-stu-id="89268-136">If all of these steps succeed, the method calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) and [**SetMediaType**](cbasepin-setmediatype.md) methods to complete the connection.</span></span> <span data-ttu-id="89268-137">Эти методы хранят тип мультимедиа и указатель на выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="89268-137">These methods store the media type and a pointer to the output pin.</span></span>

<span data-ttu-id="89268-138">При сбое **чеккконнект** или **чеккмедиатипе** базовый класс вызывает метод [**кбасепин:: бреакконнект**](cbasepin-breakconnect.md) , чтобы разорвать соединение, а затем возвращает код ошибки из `ReceiveConnection` .</span><span class="sxs-lookup"><span data-stu-id="89268-138">If **CheckConnect** or **CheckMediaType** fail, the base class calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method to break the connection and then returns an error code from `ReceiveConnection`.</span></span>

## <a name="requirements"></a><span data-ttu-id="89268-139">Требования</span><span class="sxs-lookup"><span data-stu-id="89268-139">Requirements</span></span>



| <span data-ttu-id="89268-140">Требование</span><span class="sxs-lookup"><span data-stu-id="89268-140">Requirement</span></span> | <span data-ttu-id="89268-141">Значение</span><span class="sxs-lookup"><span data-stu-id="89268-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89268-142">Header</span><span class="sxs-lookup"><span data-stu-id="89268-142">Header</span></span><br/>  | <dl> <span data-ttu-id="89268-143"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89268-143"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="89268-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89268-144">Library</span></span><br/> | <dl> <span data-ttu-id="89268-145"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="89268-145"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89268-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89268-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89268-147">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="89268-147">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




