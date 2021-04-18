---
description: 'Метод notify уведомляет ПИН-код о том, что запрошено изменение качества. Этот метод реализует метод Икуалитиконтрол:: notify.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Метод Кбасеинпутпин. notify (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae7ca47c5adc11c87a739e8736ba327dc0b65f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669023"
---
# <a name="cbaseinputpinnotify-method"></a><span data-ttu-id="89a04-104">Кбасеинпутпин. notify, метод</span><span class="sxs-lookup"><span data-stu-id="89a04-104">CBaseInputPin.Notify method</span></span>

<span data-ttu-id="89a04-105">`Notify`Метод уведомляет ПИН-код о том, что запрошено изменение качества.</span><span class="sxs-lookup"><span data-stu-id="89a04-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="89a04-106">Этот метод реализует метод [**икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="89a04-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="89a04-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89a04-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="89a04-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="89a04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89a04-109">*пселф*</span><span class="sxs-lookup"><span data-stu-id="89a04-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="89a04-110">Указатель на фильтр, отправляющий сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="89a04-110">Pointer to the filter that is sending the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="89a04-111">*формате*</span><span class="sxs-lookup"><span data-stu-id="89a04-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="89a04-112">Структура [**качества**](/windows/win32/api/strmif/ns-strmif-quality) , содержащая сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="89a04-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89a04-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89a04-113">Return value</span></span>

<span data-ttu-id="89a04-114">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="89a04-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="89a04-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89a04-115">Remarks</span></span>

<span data-ttu-id="89a04-116">Фильтры обычно передают сообщения контроля качества в закрепление выходного потока, а не на входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="89a04-116">Filters usually pass quality-control messages to an upstream output pin, not to an input pin.</span></span> <span data-ttu-id="89a04-117">Таким образом, этот метод возвращает значение \_ ОК, не делая ничего.</span><span class="sxs-lookup"><span data-stu-id="89a04-117">Therefore, this method returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="89a04-118">Требования</span><span class="sxs-lookup"><span data-stu-id="89a04-118">Requirements</span></span>



| <span data-ttu-id="89a04-119">Требование</span><span class="sxs-lookup"><span data-stu-id="89a04-119">Requirement</span></span> | <span data-ttu-id="89a04-120">Значение</span><span class="sxs-lookup"><span data-stu-id="89a04-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a04-121">Header</span><span class="sxs-lookup"><span data-stu-id="89a04-121">Header</span></span><br/>  | <dl> <span data-ttu-id="89a04-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89a04-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="89a04-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89a04-123">Library</span></span><br/> | <dl> <span data-ttu-id="89a04-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="89a04-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89a04-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89a04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a04-126">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="89a04-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="89a04-127">Управление качеством</span><span class="sxs-lookup"><span data-stu-id="89a04-127">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




