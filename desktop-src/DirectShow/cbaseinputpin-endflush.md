---
description: 'Метод Ендфлуш завершает операцию очистки. Реализует метод Ипин:: Ендфлуш.'
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Кбасеинпутпин. Ендфлуш, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403ee5aa100309084090dc241724067f9dd3aa5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657067"
---
# <a name="cbaseinputpinendflush-method"></a><span data-ttu-id="43ccf-104">Кбасеинпутпин. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="43ccf-104">CBaseInputPin.EndFlush method</span></span>

<span data-ttu-id="43ccf-105">`EndFlush`Метод завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="43ccf-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="43ccf-106">Реализует метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="43ccf-106">Implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ccf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43ccf-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="43ccf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="43ccf-108">Parameters</span></span>

<span data-ttu-id="43ccf-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="43ccf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43ccf-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43ccf-110">Return value</span></span>

<span data-ttu-id="43ccf-111">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="43ccf-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="43ccf-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43ccf-112">Remarks</span></span>

<span data-ttu-id="43ccf-113">Этот метод задает для флага [**кбасеинпутпин:: m \_ Бфлушинг**](cbaseinputpin-m-bflushing.md) **значение true**, что позволяет методу [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) принимать выборки.</span><span class="sxs-lookup"><span data-stu-id="43ccf-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which enables the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to accept samples.</span></span>

<span data-ttu-id="43ccf-114">Производный класс должен переопределить этот метод и выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="43ccf-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="43ccf-115">Освободите все буферизованные данные и дождитесь отмены всех примеров в очереди.</span><span class="sxs-lookup"><span data-stu-id="43ccf-115">Free any buffered data and wait for all queued samples to be discarded.</span></span>
2.  <span data-ttu-id="43ccf-116">Удалите все ожидающие уведомления [**EC о \_ завершении**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="43ccf-116">Clear any pending [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>
3.  <span data-ttu-id="43ccf-117">Вызовите метод базового класса.</span><span class="sxs-lookup"><span data-stu-id="43ccf-117">Call the base class method.</span></span>
4.  <span data-ttu-id="43ccf-118">Вызовите [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) на нижестоящих входных контактах.</span><span class="sxs-lookup"><span data-stu-id="43ccf-118">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) on downstream input pins.</span></span> <span data-ttu-id="43ccf-119">Если ПИН-код еще не доставил никаких образцов мультимедиа, этот шаг можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="43ccf-119">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="43ccf-120">Если выходные контакты являются производными от класса [**кбасеаутпутпин**](cbaseoutputpin.md) , можно вызвать метод [**Кбасеаутпутпин::D еливерендфлуш**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="43ccf-120">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="43ccf-121">Требования</span><span class="sxs-lookup"><span data-stu-id="43ccf-121">Requirements</span></span>



| <span data-ttu-id="43ccf-122">Требование</span><span class="sxs-lookup"><span data-stu-id="43ccf-122">Requirement</span></span> | <span data-ttu-id="43ccf-123">Значение</span><span class="sxs-lookup"><span data-stu-id="43ccf-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43ccf-124">Header</span><span class="sxs-lookup"><span data-stu-id="43ccf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="43ccf-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43ccf-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="43ccf-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43ccf-126">Library</span></span><br/> | <dl> <span data-ttu-id="43ccf-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="43ccf-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43ccf-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43ccf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ccf-129">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="43ccf-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




