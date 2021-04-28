---
description: 'Кбасепин. notify, метод notify уведомляет ПИН-код о том, что запрошено изменение качества. Этот метод реализует метод Икуалитиконтрол:: notify.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Метод Кбасепин. notify (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35e751fb583010402df53e1a85eca11f751eda24
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096022"
---
# <a name="cbasepinnotify-method"></a><span data-ttu-id="de00f-104">Кбасепин. notify, метод</span><span class="sxs-lookup"><span data-stu-id="de00f-104">CBasePin.Notify method</span></span>

<span data-ttu-id="de00f-105">`Notify`Метод уведомляет ПИН-код о том, что запрошено изменение качества.</span><span class="sxs-lookup"><span data-stu-id="de00f-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="de00f-106">Этот метод реализует метод [**икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="de00f-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de00f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de00f-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="de00f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="de00f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de00f-109">*пселф*</span><span class="sxs-lookup"><span data-stu-id="de00f-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="de00f-110">Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра, который доставил сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="de00f-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="de00f-111">*формате*</span><span class="sxs-lookup"><span data-stu-id="de00f-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="de00f-112">Задает структуру [**качества**](/windows/win32/api/strmif/ns-strmif-quality) , содержащую сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="de00f-112">Specifies a [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de00f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de00f-113">Return value</span></span>

<span data-ttu-id="de00f-114">Базовый класс возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="de00f-114">The base class returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="de00f-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="de00f-115">Remarks</span></span>

<span data-ttu-id="de00f-116">Выходные сигналы должны переопределять этот метод, чтобы принимать сообщения контроля качества.</span><span class="sxs-lookup"><span data-stu-id="de00f-116">Output pins should override this method to accept quality-control messages.</span></span>

<span data-ttu-id="de00f-117">Если установлен внешний диспетчер качества (см. раздел [**кбасепин:: сетсинк**](cbasepin-setsink.md)), передайте сообщение в Диспетчер качества.</span><span class="sxs-lookup"><span data-stu-id="de00f-117">If an external quality manager was installed (see [**CBasePin::SetSink**](cbasepin-setsink.md)), pass the message to that quality manager.</span></span> <span data-ttu-id="de00f-118">В противном случае фильтр должен обрабатывать само сообщение или передавать поток сообщений.</span><span class="sxs-lookup"><span data-stu-id="de00f-118">Otherwise, the filter should handle the message itself, or pass the message upstream.</span></span> <span data-ttu-id="de00f-119">Дополнительные сведения см. в разделе [Управление качеством](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="de00f-119">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de00f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="de00f-120">Requirements</span></span>



| <span data-ttu-id="de00f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="de00f-121">Requirement</span></span> | <span data-ttu-id="de00f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="de00f-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de00f-123">Header</span><span class="sxs-lookup"><span data-stu-id="de00f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="de00f-124"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de00f-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="de00f-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="de00f-125">Library</span></span><br/> | <dl> <span data-ttu-id="de00f-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="de00f-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de00f-127">См. также</span><span class="sxs-lookup"><span data-stu-id="de00f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de00f-128">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="de00f-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




