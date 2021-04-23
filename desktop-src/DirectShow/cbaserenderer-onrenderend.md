---
description: Метод Онрендеренд вызывается после отрисовки образца.
ms.assetid: c9b3a3b2-a5c0-4a08-9e55-53c27a4d1032
title: Кбасерендерер. Онрендеренд, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5859cf81a5fd0306f3470ee0fc6d54476e99833d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658054"
---
# <a name="cbaserendereronrenderend-method"></a><span data-ttu-id="1d814-103">Кбасерендерер. Онрендеренд, метод</span><span class="sxs-lookup"><span data-stu-id="1d814-103">CBaseRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="1d814-104">`OnRenderEnd`Метод вызывается после отрисовки образца.</span><span class="sxs-lookup"><span data-stu-id="1d814-104">The `OnRenderEnd` method is called after a sample is rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d814-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d814-105">Syntax</span></span>


```C++
virtual void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="1d814-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d814-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d814-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="1d814-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="1d814-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="1d814-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d814-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d814-109">Return value</span></span>

<span data-ttu-id="1d814-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1d814-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d814-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d814-111">Remarks</span></span>

<span data-ttu-id="1d814-112">Метод [**кбасерендерер:: Render**](cbaserenderer-render.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="1d814-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="1d814-113">Он не выполняет никаких действий в базовом классе, но производный класс может его переопределить. Например, для накопления данных контроля качества.</span><span class="sxs-lookup"><span data-stu-id="1d814-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d814-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1d814-114">Requirements</span></span>



| <span data-ttu-id="1d814-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1d814-115">Requirement</span></span> | <span data-ttu-id="1d814-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1d814-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d814-117">Header</span><span class="sxs-lookup"><span data-stu-id="1d814-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1d814-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d814-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1d814-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1d814-119">Library</span></span><br/> | <dl> <span data-ttu-id="1d814-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1d814-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d814-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d814-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d814-122">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="1d814-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




