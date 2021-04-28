---
description: Кбасепин. Бреакконнект, метод Бреакконнект освобождает ПИН-код из соединения.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Кбасепин. Бреакконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9a099b1001c2b8c30398ca350e05d15562a8bc2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099442"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="80e81-103">Кбасепин. Бреакконнект, метод</span><span class="sxs-lookup"><span data-stu-id="80e81-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="80e81-104">`BreakConnect`Метод освобождает ПИН-код из соединения.</span><span class="sxs-lookup"><span data-stu-id="80e81-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e81-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80e81-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="80e81-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80e81-106">Parameters</span></span>

<span data-ttu-id="80e81-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="80e81-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="80e81-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80e81-108">Return value</span></span>

<span data-ttu-id="80e81-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="80e81-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="80e81-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="80e81-110">Remarks</span></span>

<span data-ttu-id="80e81-111">Этот метод вызывается при отключении ПИН-кода методом [**кбасепин::D метода соединения**](cbasepin-disconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="80e81-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="80e81-112">Он также вызывается во время попытки соединения, если метод [**кбасепин:: чеккконнект**](cbasepin-checkconnect.md) завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="80e81-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="80e81-113">Этот метод должен освобождать все ресурсы, полученные методом **чеккконнект** .</span><span class="sxs-lookup"><span data-stu-id="80e81-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="80e81-114">Например, если **чеккконнект** выделяет память, `BreakConnect` освободите память.</span><span class="sxs-lookup"><span data-stu-id="80e81-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="80e81-115">Если **чеккконнект** запрашивает соединительный ПИН-код для интерфейса, `BreakConnect` должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="80e81-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="80e81-116">Обратите внимание, что `BreakConnect` может быть вызван без соответствующего вызова **комплетеконнект**.</span><span class="sxs-lookup"><span data-stu-id="80e81-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="80e81-117">Поэтому нельзя предположить, что **комплетеконнект** был вызван ранее.</span><span class="sxs-lookup"><span data-stu-id="80e81-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="80e81-118">Требования</span><span class="sxs-lookup"><span data-stu-id="80e81-118">Requirements</span></span>



| <span data-ttu-id="80e81-119">Требование</span><span class="sxs-lookup"><span data-stu-id="80e81-119">Requirement</span></span> | <span data-ttu-id="80e81-120">Значение</span><span class="sxs-lookup"><span data-stu-id="80e81-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e81-121">Header</span><span class="sxs-lookup"><span data-stu-id="80e81-121">Header</span></span><br/>  | <dl> <span data-ttu-id="80e81-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80e81-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="80e81-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80e81-123">Library</span></span><br/> | <dl> <span data-ttu-id="80e81-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="80e81-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80e81-125">См. также</span><span class="sxs-lookup"><span data-stu-id="80e81-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e81-126">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="80e81-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




