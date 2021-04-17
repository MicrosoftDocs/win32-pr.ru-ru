---
description: Метод Пасснотифи передает сообщение контроля качества соответствующему объекту.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Кбасеинпутпин. Пасснотифи, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665435"
---
# <a name="cbaseinputpinpassnotify-method"></a><span data-ttu-id="cf9ef-103">Кбасеинпутпин. Пасснотифи, метод</span><span class="sxs-lookup"><span data-stu-id="cf9ef-103">CBaseInputPin.PassNotify method</span></span>

<span data-ttu-id="cf9ef-104">`PassNotify`Метод передает сообщение контроля качества соответствующему объекту.</span><span class="sxs-lookup"><span data-stu-id="cf9ef-104">The `PassNotify` method passes a quality-control message to the appropriate object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf9ef-105">Syntax</span></span>


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="cf9ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf9ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf9ef-107">*формате*</span><span class="sxs-lookup"><span data-stu-id="cf9ef-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="cf9ef-108">Структура [**качества**](/windows/win32/api/strmif/ns-strmif-quality) , содержащая сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="cf9ef-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf9ef-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf9ef-109">Return value</span></span>

<span data-ttu-id="cf9ef-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf9ef-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cf9ef-111">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cf9ef-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="cf9ef-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cf9ef-112">Return code</span></span>                                                                                       | <span data-ttu-id="cf9ef-113">Описание</span><span class="sxs-lookup"><span data-stu-id="cf9ef-113">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="cf9ef-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ef-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="cf9ef-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="cf9ef-115">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="cf9ef-116"><dt>**VFW \_ E \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ef-116"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="cf9ef-117">Не удалось найти объект для приема сообщения.</span><span class="sxs-lookup"><span data-stu-id="cf9ef-117">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf9ef-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf9ef-118">Remarks</span></span>

<span data-ttu-id="cf9ef-119">Вызывайте этот метод, если фильтр не обрабатывает сообщения контроля качества.</span><span class="sxs-lookup"><span data-stu-id="cf9ef-119">Call this method if the filter does not handle quality-control messages.</span></span> <span data-ttu-id="cf9ef-120">Этот метод передает сообщение одному из следующих объектов в порядке предпочтения:</span><span class="sxs-lookup"><span data-stu-id="cf9ef-120">This method passes the message to one of the following objects, in order of preference:</span></span>

-   <span data-ttu-id="cf9ef-121">Внешний диспетчер контроля качества, если был вызван метод [**икуалитиконтрол:: сетсинк**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) .</span><span class="sxs-lookup"><span data-stu-id="cf9ef-121">An external quality-control manager, if the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method was called.</span></span>
-   <span data-ttu-id="cf9ef-122">Закрепление вышестоящего выходного потока.</span><span class="sxs-lookup"><span data-stu-id="cf9ef-122">The upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf9ef-123">Требования</span><span class="sxs-lookup"><span data-stu-id="cf9ef-123">Requirements</span></span>



| <span data-ttu-id="cf9ef-124">Требование</span><span class="sxs-lookup"><span data-stu-id="cf9ef-124">Requirement</span></span> | <span data-ttu-id="cf9ef-125">Значение</span><span class="sxs-lookup"><span data-stu-id="cf9ef-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9ef-126">Header</span><span class="sxs-lookup"><span data-stu-id="cf9ef-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cf9ef-127"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ef-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cf9ef-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cf9ef-128">Library</span></span><br/> | <dl> <span data-ttu-id="cf9ef-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ef-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf9ef-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf9ef-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf9ef-131">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="cf9ef-131">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="cf9ef-132">Управление качеством</span><span class="sxs-lookup"><span data-stu-id="cf9ef-132">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




