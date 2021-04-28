---
description: 'Ктрансформаутпутпин. notify, метод notify уведомляет ПИН-код о том, что запрошено изменение качества. Этот метод реализует метод Икуалитиконтрол:: notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Метод Ктрансформаутпутпин. notify (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a55e493c737b5a5864ec0a8dd38eee3abbfa586
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084812"
---
# <a name="ctransformoutputpinnotify-method"></a><span data-ttu-id="36d22-104">Ктрансформаутпутпин. notify, метод</span><span class="sxs-lookup"><span data-stu-id="36d22-104">CTransformOutputPin.Notify method</span></span>

<span data-ttu-id="36d22-105">`Notify`Метод уведомляет ПИН-код о том, что запрошено изменение качества.</span><span class="sxs-lookup"><span data-stu-id="36d22-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="36d22-106">Этот метод реализует метод [**икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="36d22-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d22-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36d22-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="36d22-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="36d22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36d22-109">*пселф*</span><span class="sxs-lookup"><span data-stu-id="36d22-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="36d22-110">Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра, который доставил сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="36d22-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality control message.</span></span>

</dd> <dt>

<span data-ttu-id="36d22-111">*формате*</span><span class="sxs-lookup"><span data-stu-id="36d22-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="36d22-112">Структура [**качества**](/windows/win32/api/strmif/ns-strmif-quality) , содержащая сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="36d22-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36d22-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36d22-113">Return value</span></span>

<span data-ttu-id="36d22-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="36d22-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="36d22-115">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="36d22-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="36d22-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="36d22-116">Return code</span></span>                                                                                       | <span data-ttu-id="36d22-117">Описание</span><span class="sxs-lookup"><span data-stu-id="36d22-117">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="36d22-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="36d22-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="36d22-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="36d22-119">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="36d22-120"><dt>**VFW \_ E \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="36d22-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="36d22-121">Не удалось найти объект для приема сообщения.</span><span class="sxs-lookup"><span data-stu-id="36d22-121">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36d22-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="36d22-122">Remarks</span></span>

<span data-ttu-id="36d22-123">Этот метод вызывает метод [**ктрансформфилтер:: алтеркуалити**](ctransformfilter-alterquality.md) фильтра.</span><span class="sxs-lookup"><span data-stu-id="36d22-123">This method calls the filter's [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span> <span data-ttu-id="36d22-124">Если фильтр не обрабатывает сообщение качества, этот метод вызывает метод [**кбасеинпутпин::P асснотифи**](cbaseinputpin-passnotify.md) для входного ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="36d22-124">If the filter does not handle the quality message, this method calls the [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md) method on the filter's input pin.</span></span> <span data-ttu-id="36d22-125">Метод **пасснотифи** передает исходящий текст сообщения (или в пользовательский диспетчер качества, если он был установлен).</span><span class="sxs-lookup"><span data-stu-id="36d22-125">The **PassNotify** method passes the quality message upstream (or to a custom quality manager, if one was installed).</span></span>

## <a name="requirements"></a><span data-ttu-id="36d22-126">Требования</span><span class="sxs-lookup"><span data-stu-id="36d22-126">Requirements</span></span>



| <span data-ttu-id="36d22-127">Требование</span><span class="sxs-lookup"><span data-stu-id="36d22-127">Requirement</span></span> | <span data-ttu-id="36d22-128">Значение</span><span class="sxs-lookup"><span data-stu-id="36d22-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36d22-129">Header</span><span class="sxs-lookup"><span data-stu-id="36d22-129">Header</span></span><br/>  | <dl> <span data-ttu-id="36d22-130"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36d22-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="36d22-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36d22-131">Library</span></span><br/> | <dl> <span data-ttu-id="36d22-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="36d22-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




