---
description: Метод Онстопстреаминг вызывается в конце потоковой передачи, чтобы исправить время для отчета страницы свойств.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Кбасевидеорендерер. Онстопстреаминг, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675009"
---
# <a name="cbasevideorendereronstopstreaming-method"></a><span data-ttu-id="bbebf-103">Кбасевидеорендерер. Онстопстреаминг, метод</span><span class="sxs-lookup"><span data-stu-id="bbebf-103">CBaseVideoRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="bbebf-104">`OnStopStreaming`Метод вызывается в конце потоковой передачи, чтобы исправить время для отчета страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="bbebf-104">The `OnStopStreaming` method is called at the end of streaming to fix times for the property page report.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbebf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbebf-105">Syntax</span></span>


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="bbebf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbebf-106">Parameters</span></span>

<span data-ttu-id="bbebf-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bbebf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbebf-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbebf-108">Return value</span></span>

<span data-ttu-id="bbebf-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bbebf-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbebf-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbebf-110">Remarks</span></span>

<span data-ttu-id="bbebf-111">Эта функция-член вызывается дважды, один раз при приостановке и снова, когда поток фактически останавливается.</span><span class="sxs-lookup"><span data-stu-id="bbebf-111">This member function is called twice, once when pausing and again when the stream is actually stopped.</span></span>

<span data-ttu-id="bbebf-112">Эта функция члена переопределяет [**кбасерендерер:: онстопстреаминг**](cbaserenderer-onstopstreaming.md).</span><span class="sxs-lookup"><span data-stu-id="bbebf-112">This member function overrides [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbebf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bbebf-113">Requirements</span></span>



| <span data-ttu-id="bbebf-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bbebf-114">Requirement</span></span> | <span data-ttu-id="bbebf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bbebf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbebf-116">Header</span><span class="sxs-lookup"><span data-stu-id="bbebf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bbebf-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbebf-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bbebf-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bbebf-118">Library</span></span><br/> | <dl> <span data-ttu-id="bbebf-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bbebf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbebf-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbebf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbebf-121">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="bbebf-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




