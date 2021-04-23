---
description: 'Метод Кбасеинпутпин начинает операцию очистки. Этот метод реализует метод Ипин:: Бегинфлуш.'
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Кбасеинпутпин. Бегинфлуш, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c0f687daf65e91443f4f59896d641b9b0cfd43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657295"
---
# <a name="cbaseinputpinbeginflush-method"></a><span data-ttu-id="dfc15-104">Кбасеинпутпин. Бегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="dfc15-104">CBaseInputPin.BeginFlush method</span></span>

<span data-ttu-id="dfc15-105">`CBaseInputPin`Метод начинает операцию записи на диск.</span><span class="sxs-lookup"><span data-stu-id="dfc15-105">The `CBaseInputPin` method begins a flush operation.</span></span> <span data-ttu-id="dfc15-106">Этот метод реализует метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="dfc15-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc15-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfc15-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="dfc15-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfc15-108">Parameters</span></span>

<span data-ttu-id="dfc15-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="dfc15-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dfc15-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfc15-110">Return value</span></span>

<span data-ttu-id="dfc15-111">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="dfc15-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfc15-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfc15-112">Remarks</span></span>

<span data-ttu-id="dfc15-113">Этот метод задает для флага [**кбасеинпутпин:: m \_ Бфлушинг**](cbaseinputpin-m-bflushing.md) **значение true**, что приводит к тому, что метод [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) отклоняет любые другие выборки.</span><span class="sxs-lookup"><span data-stu-id="dfc15-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which causes the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to reject any more samples.</span></span>

<span data-ttu-id="dfc15-114">Производный класс должен переопределить этот метод и выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="dfc15-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="dfc15-115">Вызовите метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) для подчиненных входных контактов.</span><span class="sxs-lookup"><span data-stu-id="dfc15-115">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on downstream input pins.</span></span> <span data-ttu-id="dfc15-116">Если ПИН-код еще не доставил никаких образцов мультимедиа, этот шаг можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="dfc15-116">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="dfc15-117">Если выходные контакты являются производными от класса [**кбасеаутпутпин**](cbaseoutputpin.md) , можно вызвать метод [**Кбасеаутпутпин::D еливербегинфлуш**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="dfc15-117">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>
2.  <span data-ttu-id="dfc15-118">Вызовите метод базового класса.</span><span class="sxs-lookup"><span data-stu-id="dfc15-118">Call the base class method.</span></span>
3.  <span data-ttu-id="dfc15-119">Начинает отменять данные в очереди.</span><span class="sxs-lookup"><span data-stu-id="dfc15-119">Begin discarding queued data.</span></span>
4.  <span data-ttu-id="dfc15-120">Возврат из всех заблокированных вызовов метода **Receive** .</span><span class="sxs-lookup"><span data-stu-id="dfc15-120">Return from any blocked calls to the **Receive** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfc15-121">Требования</span><span class="sxs-lookup"><span data-stu-id="dfc15-121">Requirements</span></span>



| <span data-ttu-id="dfc15-122">Требование</span><span class="sxs-lookup"><span data-stu-id="dfc15-122">Requirement</span></span> | <span data-ttu-id="dfc15-123">Значение</span><span class="sxs-lookup"><span data-stu-id="dfc15-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfc15-124">Header</span><span class="sxs-lookup"><span data-stu-id="dfc15-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dfc15-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfc15-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dfc15-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dfc15-126">Library</span></span><br/> | <dl> <span data-ttu-id="dfc15-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dfc15-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfc15-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfc15-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfc15-129">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="dfc15-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




