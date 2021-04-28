---
description: Кдинамикаутпутпин. Деливербегинфлуш, метод Деливербегинфлуш запрашивает подключенный входной ПИН-код для начала операции очистки.
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: Кдинамикаутпутпин. Деливербегинфлуш, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4158a3d6191325e8b647e4551133952d623f795
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099322"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="205f8-103">Кдинамикаутпутпин. Деливербегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="205f8-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="205f8-104">`DeliverBeginFlush`Метод запрашивает подключенный входной ПИН-код для начала операции очистки.</span><span class="sxs-lookup"><span data-stu-id="205f8-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="205f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="205f8-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="205f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="205f8-106">Parameters</span></span>

<span data-ttu-id="205f8-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="205f8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="205f8-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="205f8-108">Return value</span></span>

<span data-ttu-id="205f8-109">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="205f8-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="205f8-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="205f8-110">Remarks</span></span>

<span data-ttu-id="205f8-111">Этот метод переопределяет метод [**кбасеаутпутпин::D еливербегинфлуш**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="205f8-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="205f8-112">Он устанавливает событие [**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="205f8-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="205f8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="205f8-113">Requirements</span></span>



| <span data-ttu-id="205f8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="205f8-114">Requirement</span></span> | <span data-ttu-id="205f8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="205f8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="205f8-116">Header</span><span class="sxs-lookup"><span data-stu-id="205f8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="205f8-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="205f8-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="205f8-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="205f8-118">Library</span></span><br/> | <dl> <span data-ttu-id="205f8-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="205f8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="205f8-120">См. также</span><span class="sxs-lookup"><span data-stu-id="205f8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205f8-121">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="205f8-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




