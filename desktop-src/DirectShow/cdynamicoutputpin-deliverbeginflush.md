---
description: Метод Деливербегинфлуш запрашивает подключенный входной ПИН-код для начала операции очистки.
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
ms.openlocfilehash: 242394a327b63fcc901b08f572096bf2f42238b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668541"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="8c09b-103">Кдинамикаутпутпин. Деливербегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="8c09b-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="8c09b-104">`DeliverBeginFlush`Метод запрашивает подключенный входной ПИН-код для начала операции очистки.</span><span class="sxs-lookup"><span data-stu-id="8c09b-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c09b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c09b-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="8c09b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c09b-106">Parameters</span></span>

<span data-ttu-id="8c09b-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8c09b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c09b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c09b-108">Return value</span></span>

<span data-ttu-id="8c09b-109">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="8c09b-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c09b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c09b-110">Remarks</span></span>

<span data-ttu-id="8c09b-111">Этот метод переопределяет метод [**кбасеаутпутпин::D еливербегинфлуш**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="8c09b-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="8c09b-112">Он устанавливает событие [**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="8c09b-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c09b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8c09b-113">Requirements</span></span>



| <span data-ttu-id="8c09b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8c09b-114">Requirement</span></span> | <span data-ttu-id="8c09b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8c09b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c09b-116">Header</span><span class="sxs-lookup"><span data-stu-id="8c09b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8c09b-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c09b-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8c09b-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c09b-118">Library</span></span><br/> | <dl> <span data-ttu-id="8c09b-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8c09b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c09b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c09b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c09b-121">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="8c09b-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




