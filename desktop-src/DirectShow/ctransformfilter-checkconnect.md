---
description: Метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
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
ms.openlocfilehash: 0d41c50323bae7cb4eaca52a87d8c1b936237ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657024"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="e2129-103">Ктрансформфилтер. Чеккконнект, метод</span><span class="sxs-lookup"><span data-stu-id="e2129-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="e2129-104">`CheckConnect`Метод определяет, подходит ли подключение по ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="e2129-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2129-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2129-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="e2129-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2129-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2129-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="e2129-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="e2129-108">Член перечисленного типа с [**\_ направлением ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывающий, какой ПИН-код фильтра делает соединение.</span><span class="sxs-lookup"><span data-stu-id="e2129-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e2129-109">*ппин*</span><span class="sxs-lookup"><span data-stu-id="e2129-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="e2129-110">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода в этой попытке подключения.</span><span class="sxs-lookup"><span data-stu-id="e2129-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2129-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2129-111">Return value</span></span>

<span data-ttu-id="e2129-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e2129-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2129-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2129-113">Remarks</span></span>

<span data-ttu-id="e2129-114">Методы [**ктрансформинпутпин:: чеккконнект**](ctransforminputpin-checkconnect.md) и [**Ктрансформаутпутпин:: чеккконнект**](ctransformoutputpin-checkconnect.md) вызывают этот метод во время процесса подключения ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="e2129-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="e2129-115">Этот метод не выполняет никаких действий в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="e2129-115">This method does nothing in the base class.</span></span> <span data-ttu-id="e2129-116">Производный класс может переопределить его.</span><span class="sxs-lookup"><span data-stu-id="e2129-116">The derived class can override it.</span></span> <span data-ttu-id="e2129-117">Например, производный класс может запросить другой ПИН-код для определенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e2129-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2129-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e2129-118">Requirements</span></span>



| <span data-ttu-id="e2129-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e2129-119">Requirement</span></span> | <span data-ttu-id="e2129-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e2129-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2129-121">Header</span><span class="sxs-lookup"><span data-stu-id="e2129-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e2129-122"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2129-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e2129-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e2129-123">Library</span></span><br/> | <dl> <span data-ttu-id="e2129-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e2129-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2129-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2129-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2129-126">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="e2129-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




