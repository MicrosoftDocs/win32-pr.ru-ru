---
description: Ктрансформфилтер. Комплетеконнект, метод Комплетеконнект завершает подключение ПИН-кода.
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Ктрансформфилтер. Комплетеконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2251ba45c7a39ec9bf205fdd6643e02392e40e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095172"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="1746e-103">Ктрансформфилтер. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="1746e-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="1746e-104">`CompleteConnect`Метод завершает соединение с закреплением.</span><span class="sxs-lookup"><span data-stu-id="1746e-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1746e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1746e-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="1746e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1746e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1746e-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="1746e-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="1746e-108">Член перечисленного типа с [**\_ направлением ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывающий, какой ПИН-код фильтра делает соединение.</span><span class="sxs-lookup"><span data-stu-id="1746e-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1746e-109">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="1746e-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="1746e-110">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода в этой попытке подключения.</span><span class="sxs-lookup"><span data-stu-id="1746e-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1746e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1746e-111">Return value</span></span>

<span data-ttu-id="1746e-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1746e-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1746e-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="1746e-113">Remarks</span></span>

<span data-ttu-id="1746e-114">Методы [**ктрансформинпутпин:: комплетеконнект**](ctransforminputpin-completeconnect.md) и [**Ктрансформаутпутпин:: комплетеконнект**](ctransformoutputpin-completeconnect.md) вызывают этот метод во время процесса подключения ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="1746e-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="1746e-115">Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="1746e-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="1746e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1746e-116">Requirements</span></span>



| <span data-ttu-id="1746e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1746e-117">Requirement</span></span> | <span data-ttu-id="1746e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1746e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1746e-119">Header</span><span class="sxs-lookup"><span data-stu-id="1746e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1746e-120"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1746e-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1746e-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1746e-121">Library</span></span><br/> | <dl> <span data-ttu-id="1746e-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1746e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1746e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="1746e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1746e-124">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="1746e-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




