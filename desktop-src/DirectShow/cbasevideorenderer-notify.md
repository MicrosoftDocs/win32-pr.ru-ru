---
description: Метод notify получает уведомление о том, что запрошено изменение качества.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Метод Кбасевидеорендерер. notify (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd2b894bf78163a7b2d2387e43ecb5cec76ffdf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657118"
---
# <a name="cbasevideorenderernotify-method"></a><span data-ttu-id="ce955-103">Кбасевидеорендерер. notify, метод</span><span class="sxs-lookup"><span data-stu-id="ce955-103">CBaseVideoRenderer.Notify method</span></span>

<span data-ttu-id="ce955-104">`Notify`Метод получает уведомление о том, что запрошено изменение качества.</span><span class="sxs-lookup"><span data-stu-id="ce955-104">The `Notify` method receives a notification that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce955-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce955-105">Syntax</span></span>


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="ce955-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce955-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce955-107">*пселф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce955-107">*pSelf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce955-108">Указатель на фильтр, отправляющий уведомление.</span><span class="sxs-lookup"><span data-stu-id="ce955-108">Pointer to the filter that is sending the quality notification.</span></span>

</dd> <dt>

<span data-ttu-id="ce955-109">*вопросы* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ce955-109">*q* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce955-110">Структура уведомления об изменении качества.</span><span class="sxs-lookup"><span data-stu-id="ce955-110">Quality notification structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce955-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce955-111">Return value</span></span>

<span data-ttu-id="ce955-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce955-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce955-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce955-113">Remarks</span></span>

<span data-ttu-id="ce955-114">Эта функция члена реализует метод [**икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) в модуле подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="ce955-114">This member function implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method on the video renderer.</span></span> <span data-ttu-id="ce955-115">Этот метод вызывается, как правило, диспетчером графа фильтров, когда необходимо вырезать качество.</span><span class="sxs-lookup"><span data-stu-id="ce955-115">This is called, typically by the filter graph manager, when the quality must be cut back.</span></span> <span data-ttu-id="ce955-116">Это может произойти, когда качество воспроизведения звука увеличилось до момента, когда необходимо уменьшить качество воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="ce955-116">This might occur when the quality of audio playback has been increased to the point that the video playback quality must be decreased.</span></span>

<span data-ttu-id="ce955-117">`Notify` Задает для элемента данных **m \_ трсроттле** значение задержки, которое должно быть вставлено между кадрами [**сроттлеваит**](cbasevideorenderer-throttlewait.md).</span><span class="sxs-lookup"><span data-stu-id="ce955-117">`Notify` sets the **m\_trThrottle** data member to a delay value to be inserted between frames by [**ThrottleWait**](cbasevideorenderer-throttlewait.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce955-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ce955-118">Requirements</span></span>



| <span data-ttu-id="ce955-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ce955-119">Requirement</span></span> | <span data-ttu-id="ce955-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ce955-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce955-121">Header</span><span class="sxs-lookup"><span data-stu-id="ce955-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ce955-122"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce955-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce955-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ce955-123">Library</span></span><br/> | <dl> <span data-ttu-id="ce955-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ce955-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce955-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce955-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce955-126">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="ce955-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




