---
description: Ктрансформфилтер. Чеккконнект, метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Ктрансформфилтер. Чеккконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5927aac2fa58322c93a23489a22dc96a1e2a67f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085102"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="d7a44-103">Ктрансформфилтер. Чеккконнект, метод</span><span class="sxs-lookup"><span data-stu-id="d7a44-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="d7a44-104">`CheckConnect`Метод определяет, подходит ли подключение по ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="d7a44-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7a44-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7a44-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="d7a44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7a44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7a44-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="d7a44-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="d7a44-108">Член перечисленного типа с [**\_ направлением ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывающий, какой ПИН-код фильтра делает соединение.</span><span class="sxs-lookup"><span data-stu-id="d7a44-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="d7a44-109">*ппин*</span><span class="sxs-lookup"><span data-stu-id="d7a44-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d7a44-110">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода в этой попытке подключения.</span><span class="sxs-lookup"><span data-stu-id="d7a44-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7a44-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7a44-111">Return value</span></span>

<span data-ttu-id="d7a44-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d7a44-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7a44-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="d7a44-113">Remarks</span></span>

<span data-ttu-id="d7a44-114">Методы [**ктрансформинпутпин:: чеккконнект**](ctransforminputpin-checkconnect.md) и [**Ктрансформаутпутпин:: чеккконнект**](ctransformoutputpin-checkconnect.md) вызывают этот метод во время процесса подключения ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d7a44-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="d7a44-115">Этот метод не выполняет никаких действий в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="d7a44-115">This method does nothing in the base class.</span></span> <span data-ttu-id="d7a44-116">Производный класс может переопределить его.</span><span class="sxs-lookup"><span data-stu-id="d7a44-116">The derived class can override it.</span></span> <span data-ttu-id="d7a44-117">Например, производный класс может запросить другой ПИН-код для определенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d7a44-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a44-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d7a44-118">Requirements</span></span>



| <span data-ttu-id="d7a44-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d7a44-119">Requirement</span></span> | <span data-ttu-id="d7a44-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d7a44-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a44-121">Header</span><span class="sxs-lookup"><span data-stu-id="d7a44-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d7a44-122"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7a44-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d7a44-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d7a44-123">Library</span></span><br/> | <dl> <span data-ttu-id="d7a44-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d7a44-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7a44-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d7a44-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a44-126">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="d7a44-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




