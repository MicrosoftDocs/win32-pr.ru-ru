---
description: Метод Бреакконнект освобождает ПИН-код из соединения.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Ктрансформфилтер. Бреакконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657025"
---
# <a name="ctransformfilterbreakconnect-method"></a><span data-ttu-id="82c72-103">Ктрансформфилтер. Бреакконнект, метод</span><span class="sxs-lookup"><span data-stu-id="82c72-103">CTransformFilter.BreakConnect method</span></span>

<span data-ttu-id="82c72-104">`BreakConnect`Метод освобождает ПИН-код из соединения.</span><span class="sxs-lookup"><span data-stu-id="82c72-104">The `BreakConnect` method releases a pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="82c72-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82c72-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="82c72-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82c72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82c72-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="82c72-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="82c72-108">Член перечислимого [**типа \_ направления ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывающий, какое подключение к закреплению было разорвано (входные или выходные данные).</span><span class="sxs-lookup"><span data-stu-id="82c72-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin connection was broken (input or output).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82c72-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82c72-109">Return value</span></span>

<span data-ttu-id="82c72-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="82c72-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="82c72-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82c72-111">Remarks</span></span>

<span data-ttu-id="82c72-112">Методы [**ктрансформинпутпин:: бреакконнект**](ctransforminputpin-breakconnect.md) и [**Ктрансформаутпутпин:: бреакконнект**](ctransformoutputpin-breakconnect.md) вызывают этот метод, если соединение с закреплением разорвано.</span><span class="sxs-lookup"><span data-stu-id="82c72-112">The [**CTransformInputPin::BreakConnect**](ctransforminputpin-breakconnect.md) and [**CTransformOutputPin::BreakConnect**](ctransformoutputpin-breakconnect.md) methods call this method when a pin connection is broken.</span></span> <span data-ttu-id="82c72-113">Этот метод не выполняет никаких действий в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="82c72-113">This method does nothing in the base class.</span></span> <span data-ttu-id="82c72-114">При переопределении метода [**чеккконнект**](ctransformfilter-checkconnect.md) Переопределите этот метод, чтобы освободить все ресурсы, полученные в методе **чеккконнект** , включая указатели интерфейса.</span><span class="sxs-lookup"><span data-stu-id="82c72-114">If you override the [**CheckConnect**](ctransformfilter-checkconnect.md) method, override this method to release any resources obtained in the **CheckConnect** method, including interface pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="82c72-115">Требования</span><span class="sxs-lookup"><span data-stu-id="82c72-115">Requirements</span></span>



| <span data-ttu-id="82c72-116">Требование</span><span class="sxs-lookup"><span data-stu-id="82c72-116">Requirement</span></span> | <span data-ttu-id="82c72-117">Значение</span><span class="sxs-lookup"><span data-stu-id="82c72-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82c72-118">Header</span><span class="sxs-lookup"><span data-stu-id="82c72-118">Header</span></span><br/>  | <dl> <span data-ttu-id="82c72-119"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82c72-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="82c72-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82c72-120">Library</span></span><br/> | <dl> <span data-ttu-id="82c72-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="82c72-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82c72-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82c72-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82c72-123">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="82c72-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




