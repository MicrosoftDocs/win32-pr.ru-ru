---
description: 'Метод Коннектионмедиатипе Извлекает тип носителя для текущего соединения ПИН-кода, если таковой имеется. Этот метод реализует метод Ипин:: Коннектионмедиатипе.'
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Кбасепин. Коннектионмедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62bd211b6c93e44c571d822ccc86104a5a6fdcab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665153"
---
# <a name="cbasepinconnectionmediatype-method"></a><span data-ttu-id="33c2c-104">Кбасепин. Коннектионмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="33c2c-104">CBasePin.ConnectionMediaType method</span></span>

<span data-ttu-id="33c2c-105">Метод **коннектионмедиатипе** Извлекает тип носителя для текущего соединения ПИН-кода, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="33c2c-105">The **ConnectionMediaType** method retrieves the media type for the current pin connection, if any.</span></span> <span data-ttu-id="33c2c-106">Этот метод реализует метод [**Ипин:: коннектионмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) .</span><span class="sxs-lookup"><span data-stu-id="33c2c-106">This method implements the [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="33c2c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33c2c-107">Syntax</span></span>


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="33c2c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="33c2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c2c-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="33c2c-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="33c2c-110">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , которая получает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="33c2c-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c2c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33c2c-111">Return value</span></span>

<span data-ttu-id="33c2c-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33c2c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="33c2c-113">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="33c2c-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="33c2c-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="33c2c-114">Return code</span></span>                                                                                           | <span data-ttu-id="33c2c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="33c2c-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="33c2c-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="33c2c-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="33c2c-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="33c2c-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="33c2c-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="33c2c-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="33c2c-119">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="33c2c-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="33c2c-120"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="33c2c-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="33c2c-121">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="33c2c-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="33c2c-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33c2c-122">Remarks</span></span>

<span data-ttu-id="33c2c-123">Если ПИН-код подключен, этот метод копирует тип носителя в структуру [**\_ \_ типа данных AM Media**](/windows/win32/api/strmif/ns-strmif-am_media_type) , заданную функцией *ПЛТ*. Вызывающий объект должен освободить блок формата типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="33c2c-123">If the pin is connected, this method copies the media type into the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specified by *pmt*. The caller must free the media type's format block.</span></span> <span data-ttu-id="33c2c-124">Можно использовать функцию [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) или вспомогательную функцию [**фримедиатипе**](freemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="33c2c-124">You can use the [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function, or the [**FreeMediaType**](freemediatype.md) helper function.</span></span>

<span data-ttu-id="33c2c-125">Если ПИН-код не подключен, этот метод обнуляет блок памяти, заданный функцией *ПЛТ* , и возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="33c2c-125">If the pin is not connected, this method zeroes the memory block specified by *pmt* and returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c2c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="33c2c-126">Requirements</span></span>



| <span data-ttu-id="33c2c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="33c2c-127">Requirement</span></span> | <span data-ttu-id="33c2c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="33c2c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c2c-129">Header</span><span class="sxs-lookup"><span data-stu-id="33c2c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="33c2c-130"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33c2c-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="33c2c-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="33c2c-131">Library</span></span><br/> | <dl> <span data-ttu-id="33c2c-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="33c2c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33c2c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33c2c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c2c-134">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="33c2c-134">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

