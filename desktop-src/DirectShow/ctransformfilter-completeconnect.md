---
description: Метод Комплетеконнект завершает подключение ПИН-кода.
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
ms.openlocfilehash: 630950cf9b05c08412394bf9270f2369b3f3b94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657452"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="fe5e9-103">Ктрансформфилтер. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="fe5e9-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="fe5e9-104">`CompleteConnect`Метод завершает соединение с закреплением.</span><span class="sxs-lookup"><span data-stu-id="fe5e9-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe5e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe5e9-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="fe5e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe5e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe5e9-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="fe5e9-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="fe5e9-108">Член перечисленного типа с [**\_ направлением ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывающий, какой ПИН-код фильтра делает соединение.</span><span class="sxs-lookup"><span data-stu-id="fe5e9-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="fe5e9-109">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="fe5e9-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="fe5e9-110">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода в этой попытке подключения.</span><span class="sxs-lookup"><span data-stu-id="fe5e9-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe5e9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe5e9-111">Return value</span></span>

<span data-ttu-id="fe5e9-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fe5e9-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe5e9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe5e9-113">Remarks</span></span>

<span data-ttu-id="fe5e9-114">Методы [**ктрансформинпутпин:: комплетеконнект**](ctransforminputpin-completeconnect.md) и [**Ктрансформаутпутпин:: комплетеконнект**](ctransformoutputpin-completeconnect.md) вызывают этот метод во время процесса подключения ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="fe5e9-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="fe5e9-115">Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="fe5e9-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe5e9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fe5e9-116">Requirements</span></span>



| <span data-ttu-id="fe5e9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fe5e9-117">Requirement</span></span> | <span data-ttu-id="fe5e9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fe5e9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe5e9-119">Header</span><span class="sxs-lookup"><span data-stu-id="fe5e9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fe5e9-120"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe5e9-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fe5e9-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe5e9-121">Library</span></span><br/> | <dl> <span data-ttu-id="fe5e9-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fe5e9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe5e9-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe5e9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe5e9-124">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="fe5e9-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




