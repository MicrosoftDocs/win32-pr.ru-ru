---
description: 'Кбасеинпутпин. notify, метод notify уведомляет ПИН-код о том, что запрошено изменение качества. Этот метод реализует метод Икуалитиконтрол:: notify.'
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
ms.openlocfilehash: 610888193762618d427a0329a27d3019bd625e69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120002"
---
# <a name="cbaseinputpinnotify-method"></a><span data-ttu-id="d060a-104">Кбасеинпутпин. notify, метод</span><span class="sxs-lookup"><span data-stu-id="d060a-104">CBaseInputPin.Notify method</span></span>

<span data-ttu-id="d060a-105">`Notify`Метод уведомляет ПИН-код о том, что запрошено изменение качества.</span><span class="sxs-lookup"><span data-stu-id="d060a-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="d060a-106">Этот метод реализует метод [**икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="d060a-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d060a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d060a-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="d060a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d060a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d060a-109">*пселф*</span><span class="sxs-lookup"><span data-stu-id="d060a-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="d060a-110">Указатель на фильтр, отправляющий сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="d060a-110">Pointer to the filter that is sending the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="d060a-111">*формате*</span><span class="sxs-lookup"><span data-stu-id="d060a-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="d060a-112">Структура [**качества**](/windows/win32/api/strmif/ns-strmif-quality) , содержащая сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="d060a-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d060a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d060a-113">Return value</span></span>

<span data-ttu-id="d060a-114">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d060a-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d060a-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="d060a-115">Remarks</span></span>

<span data-ttu-id="d060a-116">Фильтры обычно передают сообщения контроля качества в закрепление выходного потока, а не на входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="d060a-116">Filters usually pass quality-control messages to an upstream output pin, not to an input pin.</span></span> <span data-ttu-id="d060a-117">Таким образом, этот метод возвращает значение \_ ОК, не делая ничего.</span><span class="sxs-lookup"><span data-stu-id="d060a-117">Therefore, this method returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="d060a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d060a-118">Requirements</span></span>



| <span data-ttu-id="d060a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d060a-119">Requirement</span></span> | <span data-ttu-id="d060a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d060a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d060a-121">Header</span><span class="sxs-lookup"><span data-stu-id="d060a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d060a-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d060a-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d060a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d060a-123">Library</span></span><br/> | <dl> <span data-ttu-id="d060a-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d060a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d060a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d060a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d060a-126">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="d060a-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="d060a-127">Управление качеством</span><span class="sxs-lookup"><span data-stu-id="d060a-127">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




