---
description: Метод Онрецеивефирстсампле вызывается, когда фильтр получает выборку при приостановке.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Кбасерендерер. Онрецеивефирстсампле, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669409"
---
# <a name="cbaserendereronreceivefirstsample-method"></a><span data-ttu-id="c9ca1-103">Кбасерендерер. Онрецеивефирстсампле, метод</span><span class="sxs-lookup"><span data-stu-id="c9ca1-103">CBaseRenderer.OnReceiveFirstSample method</span></span>

<span data-ttu-id="c9ca1-104">`OnReceiveFirstSample`Метод вызывается, когда фильтр получает выборку при приостановке.</span><span class="sxs-lookup"><span data-stu-id="c9ca1-104">The `OnReceiveFirstSample` method is called when the filter receives a sample while paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9ca1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9ca1-105">Syntax</span></span>


```C++
virtual void OnReceiveFirstSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="c9ca1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9ca1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ca1-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="c9ca1-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c9ca1-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="c9ca1-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9ca1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9ca1-109">Return value</span></span>

<span data-ttu-id="c9ca1-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c9ca1-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9ca1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9ca1-111">Remarks</span></span>

<span data-ttu-id="c9ca1-112">Метод [**кбасерендерер:: Receive**](cbaserenderer-receive.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="c9ca1-112">The [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method calls this method.</span></span> <span data-ttu-id="c9ca1-113">Он не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="c9ca1-113">It does nothing in the base class, but the derived class can override it.</span></span> <span data-ttu-id="c9ca1-114">Этот метод предназначен в первую очередь для модулей подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="c9ca1-114">This method is intended primarily for video renderers.</span></span> <span data-ttu-id="c9ca1-115">Когда модуль подготовки видео приостанавливается, он обычно отображает первый пример в виде изображения по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="c9ca1-115">When a video renderer is paused, it typically displays the first sample as a still image.</span></span>

<span data-ttu-id="c9ca1-116">При поиске графа во время приостановки также вызывается этот метод.</span><span class="sxs-lookup"><span data-stu-id="c9ca1-116">Seeking the graph while paused also causes this method to be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9ca1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c9ca1-117">Requirements</span></span>



| <span data-ttu-id="c9ca1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c9ca1-118">Requirement</span></span> | <span data-ttu-id="c9ca1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c9ca1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ca1-120">Header</span><span class="sxs-lookup"><span data-stu-id="c9ca1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c9ca1-121"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9ca1-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c9ca1-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9ca1-122">Library</span></span><br/> | <dl> <span data-ttu-id="c9ca1-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c9ca1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9ca1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9ca1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9ca1-125">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="c9ca1-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




