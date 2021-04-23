---
description: Метод Сенднотифивиндов сообщает о вышестоящем фильтре обработчика окна видео.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Кбасерендерер. Сенднотифивиндов, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657106"
---
# <a name="cbaserenderersendnotifywindow-method"></a><span data-ttu-id="dcbbf-103">Кбасерендерер. Сенднотифивиндов, метод</span><span class="sxs-lookup"><span data-stu-id="dcbbf-103">CBaseRenderer.SendNotifyWindow method</span></span>

<span data-ttu-id="dcbbf-104">`SendNotifyWindow`Метод уведомляет вышестоящий фильтр обработчика окна видео.</span><span class="sxs-lookup"><span data-stu-id="dcbbf-104">The `SendNotifyWindow` method notifies the upstream filter of the video window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcbbf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcbbf-105">Syntax</span></span>


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="dcbbf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcbbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcbbf-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="dcbbf-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="dcbbf-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) выходного ПИН-кода вышестоящего фильтра.</span><span class="sxs-lookup"><span data-stu-id="dcbbf-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the upstream filter's output pin.</span></span>

</dd> <dt>

<span data-ttu-id="dcbbf-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="dcbbf-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="dcbbf-110">Указатель на окно видео или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dcbbf-110">Handle to the video window, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcbbf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcbbf-111">Return value</span></span>

<span data-ttu-id="dcbbf-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dcbbf-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcbbf-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcbbf-113">Remarks</span></span>

<span data-ttu-id="dcbbf-114">Если выходной ПИН-код вышестоящего фильтра поддерживает интерфейс [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) , этот метод отправляет ему код события [**\_ \_ окна уведомления EC**](ec-notify-window.md) вместе с маркером окна.</span><span class="sxs-lookup"><span data-stu-id="dcbbf-114">If the output pin of the upstream filter supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, this method sends it the [**EC\_NOTIFY\_WINDOW**](ec-notify-window.md) event code along with the window handle.</span></span>

<span data-ttu-id="dcbbf-115">Модули подготовки видео могут переопределять методы [**кбасерендерер:: комплетеконнект**](cbaserenderer-completeconnect.md) для вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="dcbbf-115">Video renderers can override their [**CBaseRenderer::CompleteConnect**](cbaserenderer-completeconnect.md) methods to call this method.</span></span> <span data-ttu-id="dcbbf-116">Он предоставляет механизм для формирования вышестоящего фильтра маркера окна.</span><span class="sxs-lookup"><span data-stu-id="dcbbf-116">It provides a mechanism for informing the upstream filter of the window handle.</span></span> <span data-ttu-id="dcbbf-117">В этом случае Переопределите метод [**кбасерендерер:: бреакконнект**](cbaserenderer-breakconnect.md) и вызовите `SendNotifyWindow` его с помощью маркера **null** .</span><span class="sxs-lookup"><span data-stu-id="dcbbf-117">If you do this, override the [**CBaseRenderer::BreakConnect**](cbaserenderer-breakconnect.md) method as well, and call `SendNotifyWindow` with a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcbbf-118">Требования</span><span class="sxs-lookup"><span data-stu-id="dcbbf-118">Requirements</span></span>



| <span data-ttu-id="dcbbf-119">Требование</span><span class="sxs-lookup"><span data-stu-id="dcbbf-119">Requirement</span></span> | <span data-ttu-id="dcbbf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="dcbbf-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcbbf-121">Header</span><span class="sxs-lookup"><span data-stu-id="dcbbf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dcbbf-122"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcbbf-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dcbbf-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dcbbf-123">Library</span></span><br/> | <dl> <span data-ttu-id="dcbbf-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dcbbf-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcbbf-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcbbf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcbbf-126">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="dcbbf-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




