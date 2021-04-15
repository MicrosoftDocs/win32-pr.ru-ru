---
description: Метод Receive получает следующий образец носителя в потоке.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Метод Кбасерендерер. Receive (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669514"
---
# <a name="cbaserendererreceive-method"></a><span data-ttu-id="36ddd-103">Кбасерендерер. Receive, метод</span><span class="sxs-lookup"><span data-stu-id="36ddd-103">CBaseRenderer.Receive method</span></span>

<span data-ttu-id="36ddd-104">`Receive`Метод получает следующий пример носителя в потоке.</span><span class="sxs-lookup"><span data-stu-id="36ddd-104">The `Receive` method receives the next media sample in the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="36ddd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36ddd-105">Syntax</span></span>


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="36ddd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36ddd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36ddd-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="36ddd-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="36ddd-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="36ddd-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36ddd-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36ddd-109">Return value</span></span>

<span data-ttu-id="36ddd-110">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="36ddd-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="36ddd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36ddd-111">Remarks</span></span>

<span data-ttu-id="36ddd-112">Входной ПИН-код вызывает этот метод при получении примера из вышестоящего фильтра.</span><span class="sxs-lookup"><span data-stu-id="36ddd-112">The input pin calls this method when it receives a sample from the upstream filter.</span></span>

<span data-ttu-id="36ddd-113">Если фильтр выполняется, этот метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="36ddd-113">If the filter is running, this method performs the following steps:</span></span>

1.  <span data-ttu-id="36ddd-114">Планирует пример для подготовки к просмотру ([**кбасерендерер::P репаререцеиве**](cbaserenderer-preparereceive.md)).</span><span class="sxs-lookup"><span data-stu-id="36ddd-114">Schedules the sample for rendering ([**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md)).</span></span>
2.  <span data-ttu-id="36ddd-115">Ожидает запланированное время ([**кбасерендерер:: ваитфоррендертиме**](cbaserenderer-waitforrendertime.md)).</span><span class="sxs-lookup"><span data-stu-id="36ddd-115">Waits for the scheduled time ([**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).</span></span>
3.  <span data-ttu-id="36ddd-116">Визуализирует образец ([**кбасерендерер:: Render**](cbaserenderer-render.md)).</span><span class="sxs-lookup"><span data-stu-id="36ddd-116">Renders the sample ([**CBaseRenderer::Render**](cbaserenderer-render.md)).</span></span>
4.  <span data-ttu-id="36ddd-117">Освобождает образец ([**кбасерендерер:: клеарпендингсампле**](cbaserenderer-clearpendingsample.md)).</span><span class="sxs-lookup"><span data-stu-id="36ddd-117">Releases the sample ([**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md)).</span></span>

<span data-ttu-id="36ddd-118">Если фильтр приостановлен, метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="36ddd-118">If the filter is paused, the method performs the following steps:</span></span>

1.  <span data-ttu-id="36ddd-119">Уведомляет производный класс о том, что образец доступен ([**кбасерендерер:: онрецеивефирстсампле**](cbaserenderer-onreceivefirstsample.md)).</span><span class="sxs-lookup"><span data-stu-id="36ddd-119">Notifies the derived class that a sample is available ([**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).</span></span>
2.  <span data-ttu-id="36ddd-120">Ожидает запланированное время.</span><span class="sxs-lookup"><span data-stu-id="36ddd-120">Waits for the scheduled time.</span></span>
3.  <span data-ttu-id="36ddd-121">Подготавливает к просмотру образец.</span><span class="sxs-lookup"><span data-stu-id="36ddd-121">Renders the sample.</span></span>
4.  <span data-ttu-id="36ddd-122">Освобождает пример.</span><span class="sxs-lookup"><span data-stu-id="36ddd-122">Releases the sample.</span></span>

<span data-ttu-id="36ddd-123">При приостановке метод ожидает на шаге 2, пока фильтр не переключится в состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="36ddd-123">While paused, the method waits in step 2 until the filter switches to a running state.</span></span> <span data-ttu-id="36ddd-124">На этом этапе фильтр планирует пример.</span><span class="sxs-lookup"><span data-stu-id="36ddd-124">At that point, the filter schedules the sample.</span></span>

<span data-ttu-id="36ddd-125">В базовом классе метод **онрецеивефирстсампле** не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="36ddd-125">In the base class, the **OnReceiveFirstSample** method does nothing.</span></span> <span data-ttu-id="36ddd-126">Производный класс может переопределить его.</span><span class="sxs-lookup"><span data-stu-id="36ddd-126">The derived class can override it.</span></span> <span data-ttu-id="36ddd-127">Например, когда модуль подготовки видео приостанавливается, он отображает первый пример в виде изображения по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="36ddd-127">For example, when a video renderer is paused, it displays the first sample as a still image.</span></span>

## <a name="requirements"></a><span data-ttu-id="36ddd-128">Требования</span><span class="sxs-lookup"><span data-stu-id="36ddd-128">Requirements</span></span>



| <span data-ttu-id="36ddd-129">Требование</span><span class="sxs-lookup"><span data-stu-id="36ddd-129">Requirement</span></span> | <span data-ttu-id="36ddd-130">Значение</span><span class="sxs-lookup"><span data-stu-id="36ddd-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ddd-131">Header</span><span class="sxs-lookup"><span data-stu-id="36ddd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="36ddd-132"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36ddd-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="36ddd-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36ddd-133">Library</span></span><br/> | <dl> <span data-ttu-id="36ddd-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="36ddd-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36ddd-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36ddd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36ddd-136">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="36ddd-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




