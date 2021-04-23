---
description: Метод Онрендерстарт вызывается, когда подготовка готовится к запуску.
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: Кбасерендерер. Онрендерстарт, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7838b0ba43c1e570b745541882a2f2f815dd948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668489"
---
# <a name="cbaserendereronrenderstart-method"></a><span data-ttu-id="26036-103">Кбасерендерер. Онрендерстарт, метод</span><span class="sxs-lookup"><span data-stu-id="26036-103">CBaseRenderer.OnRenderStart method</span></span>

<span data-ttu-id="26036-104">`OnRenderStart`Метод вызывается, когда подготовка готовится к запуску.</span><span class="sxs-lookup"><span data-stu-id="26036-104">The `OnRenderStart` method is called when rendering is about to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="26036-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26036-105">Syntax</span></span>


```C++
virtual void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="26036-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26036-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26036-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="26036-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="26036-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="26036-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26036-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26036-109">Return value</span></span>

<span data-ttu-id="26036-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="26036-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26036-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26036-111">Remarks</span></span>

<span data-ttu-id="26036-112">Метод [**кбасерендерер:: Render**](cbaserenderer-render.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="26036-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="26036-113">Он не выполняет никаких действий в базовом классе, но производный класс может его переопределить. Например, для накопления данных контроля качества.</span><span class="sxs-lookup"><span data-stu-id="26036-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="26036-114">Требования</span><span class="sxs-lookup"><span data-stu-id="26036-114">Requirements</span></span>



| <span data-ttu-id="26036-115">Требование</span><span class="sxs-lookup"><span data-stu-id="26036-115">Requirement</span></span> | <span data-ttu-id="26036-116">Значение</span><span class="sxs-lookup"><span data-stu-id="26036-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26036-117">Header</span><span class="sxs-lookup"><span data-stu-id="26036-117">Header</span></span><br/>  | <dl> <span data-ttu-id="26036-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26036-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="26036-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="26036-119">Library</span></span><br/> | <dl> <span data-ttu-id="26036-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="26036-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26036-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26036-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26036-122">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="26036-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




