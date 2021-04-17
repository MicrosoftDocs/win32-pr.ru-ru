---
description: Метод Препаререндер вызывается до того, как фильтр отрисовывает пример.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Кбасерендерер. Препаререндер, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669402"
---
# <a name="cbaserendererpreparerender-method"></a><span data-ttu-id="28636-103">Кбасерендерер. Препаререндер, метод</span><span class="sxs-lookup"><span data-stu-id="28636-103">CBaseRenderer.PrepareRender method</span></span>

<span data-ttu-id="28636-104">`PrepareRender`Метод вызывается до того, как фильтр отрисовывает пример.</span><span class="sxs-lookup"><span data-stu-id="28636-104">The `PrepareRender` method is called before the filter renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="28636-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28636-105">Syntax</span></span>


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a><span data-ttu-id="28636-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28636-106">Parameters</span></span>

<span data-ttu-id="28636-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="28636-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28636-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28636-108">Return value</span></span>

<span data-ttu-id="28636-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="28636-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28636-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28636-110">Remarks</span></span>

<span data-ttu-id="28636-111">Фильтр вызывает этот метод перед вызовом метода [**кбасерендерер:: онрецеивефирстсампле**](cbaserenderer-onreceivefirstsample.md) или метода [**Кбасерендерер:: Render**](cbaserenderer-render.md) .</span><span class="sxs-lookup"><span data-stu-id="28636-111">The filter calls this method before it calls the [**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) method or the [**CBaseRenderer::Render**](cbaserenderer-render.md) method.</span></span> <span data-ttu-id="28636-112">`PrepareRender` не выполняет никаких действий в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="28636-112">`PrepareRender` does not do anything in the base class.</span></span> <span data-ttu-id="28636-113">Производный класс может переопределить его для выполнения любых действий, необходимых перед отрисовкой.</span><span class="sxs-lookup"><span data-stu-id="28636-113">The derived class can override it to perform any actions required before rendering.</span></span> <span data-ttu-id="28636-114">Например, модуль подготовки видео может переопределить этот метод, чтобы реализовать его палитру.</span><span class="sxs-lookup"><span data-stu-id="28636-114">For example, a video renderer can override this method to realize its palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="28636-115">Требования</span><span class="sxs-lookup"><span data-stu-id="28636-115">Requirements</span></span>



| <span data-ttu-id="28636-116">Требование</span><span class="sxs-lookup"><span data-stu-id="28636-116">Requirement</span></span> | <span data-ttu-id="28636-117">Значение</span><span class="sxs-lookup"><span data-stu-id="28636-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28636-118">Header</span><span class="sxs-lookup"><span data-stu-id="28636-118">Header</span></span><br/>  | <dl> <span data-ttu-id="28636-119"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28636-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="28636-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="28636-120">Library</span></span><br/> | <dl> <span data-ttu-id="28636-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="28636-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28636-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28636-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28636-123">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="28636-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




