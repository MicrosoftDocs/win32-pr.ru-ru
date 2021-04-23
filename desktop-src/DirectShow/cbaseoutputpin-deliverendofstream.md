---
description: Метод Деливерендофстреам доставляет уведомление в виде конца потока в подключенный входной ПИН-код.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Кбасеаутпутпин. Деливерендофстреам, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 334101c9b61631a35c5da91bd398cb7742d39235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657886"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a><span data-ttu-id="346d4-103">Кбасеаутпутпин. Деливерендофстреам, метод</span><span class="sxs-lookup"><span data-stu-id="346d4-103">CBaseOutputPin.DeliverEndOfStream method</span></span>

<span data-ttu-id="346d4-104">`DeliverEndOfStream`Метод доставляет уведомление о завершении потока в подключенный входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="346d4-104">The `DeliverEndOfStream` method delivers an end-of-stream notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="346d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="346d4-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="346d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="346d4-106">Parameters</span></span>

<span data-ttu-id="346d4-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="346d4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="346d4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="346d4-108">Return value</span></span>

<span data-ttu-id="346d4-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="346d4-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="346d4-110">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="346d4-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="346d4-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="346d4-111">Return code</span></span>                                                                                           | <span data-ttu-id="346d4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="346d4-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="346d4-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="346d4-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="346d4-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="346d4-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="346d4-115"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="346d4-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="346d4-116">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="346d4-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="346d4-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="346d4-117">Remarks</span></span>

<span data-ttu-id="346d4-118">Этот метод вызывает метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="346d4-118">This method calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="346d4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="346d4-119">Requirements</span></span>



| <span data-ttu-id="346d4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="346d4-120">Requirement</span></span> | <span data-ttu-id="346d4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="346d4-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="346d4-122">Header</span><span class="sxs-lookup"><span data-stu-id="346d4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="346d4-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="346d4-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="346d4-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="346d4-124">Library</span></span><br/> | <dl> <span data-ttu-id="346d4-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="346d4-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="346d4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="346d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346d4-127">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="346d4-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




