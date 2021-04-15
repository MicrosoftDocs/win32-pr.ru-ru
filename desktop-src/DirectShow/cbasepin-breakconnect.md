---
description: Метод Бреакконнект освобождает ПИН-код из соединения.
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
ms.openlocfilehash: 8964ea76e48e4753f42923663ab45962cd672e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669305"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="78c58-103">Кбасепин. Бреакконнект, метод</span><span class="sxs-lookup"><span data-stu-id="78c58-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="78c58-104">`BreakConnect`Метод освобождает ПИН-код из соединения.</span><span class="sxs-lookup"><span data-stu-id="78c58-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c58-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78c58-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="78c58-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78c58-106">Parameters</span></span>

<span data-ttu-id="78c58-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="78c58-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="78c58-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78c58-108">Return value</span></span>

<span data-ttu-id="78c58-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="78c58-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="78c58-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78c58-110">Remarks</span></span>

<span data-ttu-id="78c58-111">Этот метод вызывается при отключении ПИН-кода методом [**кбасепин::D метода соединения**](cbasepin-disconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="78c58-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="78c58-112">Он также вызывается во время попытки соединения, если метод [**кбасепин:: чеккконнект**](cbasepin-checkconnect.md) завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="78c58-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="78c58-113">Этот метод должен освобождать все ресурсы, полученные методом **чеккконнект** .</span><span class="sxs-lookup"><span data-stu-id="78c58-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="78c58-114">Например, если **чеккконнект** выделяет память, `BreakConnect` освободите память.</span><span class="sxs-lookup"><span data-stu-id="78c58-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="78c58-115">Если **чеккконнект** запрашивает соединительный ПИН-код для интерфейса, `BreakConnect` должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="78c58-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="78c58-116">Обратите внимание, что `BreakConnect` может быть вызван без соответствующего вызова **комплетеконнект**.</span><span class="sxs-lookup"><span data-stu-id="78c58-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="78c58-117">Поэтому нельзя предположить, что **комплетеконнект** был вызван ранее.</span><span class="sxs-lookup"><span data-stu-id="78c58-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c58-118">Требования</span><span class="sxs-lookup"><span data-stu-id="78c58-118">Requirements</span></span>



| <span data-ttu-id="78c58-119">Требование</span><span class="sxs-lookup"><span data-stu-id="78c58-119">Requirement</span></span> | <span data-ttu-id="78c58-120">Значение</span><span class="sxs-lookup"><span data-stu-id="78c58-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c58-121">Header</span><span class="sxs-lookup"><span data-stu-id="78c58-121">Header</span></span><br/>  | <dl> <span data-ttu-id="78c58-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78c58-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="78c58-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="78c58-123">Library</span></span><br/> | <dl> <span data-ttu-id="78c58-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="78c58-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78c58-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78c58-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c58-126">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="78c58-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




