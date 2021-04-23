---
description: 'Метод notify уведомляет ПИН-код о том, что запрошено изменение качества. Этот метод реализует метод Икуалитиконтрол:: notify.'
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
ms.openlocfilehash: f34ea630a461226c32b9d827b2b91dcd0874cac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668578"
---
# <a name="cbasepinnotify-method"></a><span data-ttu-id="34301-104">Кбасепин. notify, метод</span><span class="sxs-lookup"><span data-stu-id="34301-104">CBasePin.Notify method</span></span>

<span data-ttu-id="34301-105">`Notify`Метод уведомляет ПИН-код о том, что запрошено изменение качества.</span><span class="sxs-lookup"><span data-stu-id="34301-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="34301-106">Этот метод реализует метод [**икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="34301-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="34301-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34301-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="34301-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="34301-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34301-109">*пселф*</span><span class="sxs-lookup"><span data-stu-id="34301-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="34301-110">Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра, который доставил сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="34301-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="34301-111">*формате*</span><span class="sxs-lookup"><span data-stu-id="34301-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="34301-112">Задает структуру [**качества**](/windows/win32/api/strmif/ns-strmif-quality) , содержащую сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="34301-112">Specifies a [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34301-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34301-113">Return value</span></span>

<span data-ttu-id="34301-114">Базовый класс возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="34301-114">The base class returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="34301-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34301-115">Remarks</span></span>

<span data-ttu-id="34301-116">Выходные сигналы должны переопределять этот метод, чтобы принимать сообщения контроля качества.</span><span class="sxs-lookup"><span data-stu-id="34301-116">Output pins should override this method to accept quality-control messages.</span></span>

<span data-ttu-id="34301-117">Если установлен внешний диспетчер качества (см. раздел [**кбасепин:: сетсинк**](cbasepin-setsink.md)), передайте сообщение в Диспетчер качества.</span><span class="sxs-lookup"><span data-stu-id="34301-117">If an external quality manager was installed (see [**CBasePin::SetSink**](cbasepin-setsink.md)), pass the message to that quality manager.</span></span> <span data-ttu-id="34301-118">В противном случае фильтр должен обрабатывать само сообщение или передавать поток сообщений.</span><span class="sxs-lookup"><span data-stu-id="34301-118">Otherwise, the filter should handle the message itself, or pass the message upstream.</span></span> <span data-ttu-id="34301-119">Дополнительные сведения см. в разделе [Управление качеством](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="34301-119">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34301-120">Требования</span><span class="sxs-lookup"><span data-stu-id="34301-120">Requirements</span></span>



| <span data-ttu-id="34301-121">Требование</span><span class="sxs-lookup"><span data-stu-id="34301-121">Requirement</span></span> | <span data-ttu-id="34301-122">Значение</span><span class="sxs-lookup"><span data-stu-id="34301-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34301-123">Header</span><span class="sxs-lookup"><span data-stu-id="34301-123">Header</span></span><br/>  | <dl> <span data-ttu-id="34301-124"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34301-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="34301-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34301-125">Library</span></span><br/> | <dl> <span data-ttu-id="34301-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="34301-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34301-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34301-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34301-128">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="34301-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




