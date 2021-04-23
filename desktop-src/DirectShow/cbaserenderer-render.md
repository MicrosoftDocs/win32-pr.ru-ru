---
description: Метод Render визуализирует образец.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Метод Кбасерендерер. Render (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658046"
---
# <a name="cbaserendererrender-method"></a><span data-ttu-id="860a9-103">Кбасерендерер. Render, метод</span><span class="sxs-lookup"><span data-stu-id="860a9-103">CBaseRenderer.Render method</span></span>

<span data-ttu-id="860a9-104">`Render`Метод подготавливает к просмотру пример.</span><span class="sxs-lookup"><span data-stu-id="860a9-104">The `Render` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="860a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="860a9-105">Syntax</span></span>


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="860a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="860a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="860a9-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="860a9-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="860a9-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="860a9-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="860a9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="860a9-109">Return value</span></span>

<span data-ttu-id="860a9-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="860a9-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="860a9-111">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="860a9-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="860a9-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="860a9-112">Return code</span></span>                                                                             | <span data-ttu-id="860a9-113">Описание</span><span class="sxs-lookup"><span data-stu-id="860a9-113">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="860a9-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="860a9-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="860a9-115">Фильтр остановлен или *пмедиасампле* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="860a9-115">The filter is stopped, or *pMediaSample* is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="860a9-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="860a9-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="860a9-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="860a9-117">Success.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="860a9-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="860a9-118">Remarks</span></span>

<span data-ttu-id="860a9-119">Этот метод вызывает чистый виртуальный метод [**кбасерендерер::D орендерсампле**](cbaserenderer-dorendersample.md), который выполняет реальную работу.</span><span class="sxs-lookup"><span data-stu-id="860a9-119">This method calls the pure virtual method [**CBaseRenderer::DoRenderSample**](cbaserenderer-dorendersample.md), which does the real work.</span></span> <span data-ttu-id="860a9-120">Производный класс должен реализовывать **дорендерсампле**.</span><span class="sxs-lookup"><span data-stu-id="860a9-120">The derived class must implement **DoRenderSample**.</span></span>

<span data-ttu-id="860a9-121">Непосредственно перед вызовом **дорендерсампле** этот метод вызывает метод [**Кбасерендерер:: онрендерстарт**](cbaserenderer-onrenderstart.md) .</span><span class="sxs-lookup"><span data-stu-id="860a9-121">Immediately before calling **DoRenderSample**, this method calls the [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md) method.</span></span> <span data-ttu-id="860a9-122">Сразу же после этого вызывается метод [**кбасерендерер:: онрендеренд**](cbaserenderer-onrenderend.md) .</span><span class="sxs-lookup"><span data-stu-id="860a9-122">Immediately after, it calls the [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md) method.</span></span> <span data-ttu-id="860a9-123">Производный класс может переопределить эти два метода по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="860a9-123">The derived class can override those two methods as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="860a9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="860a9-124">Requirements</span></span>



| <span data-ttu-id="860a9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="860a9-125">Requirement</span></span> | <span data-ttu-id="860a9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="860a9-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="860a9-127">Header</span><span class="sxs-lookup"><span data-stu-id="860a9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="860a9-128"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="860a9-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="860a9-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="860a9-129">Library</span></span><br/> | <dl> <span data-ttu-id="860a9-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="860a9-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="860a9-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="860a9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="860a9-132">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="860a9-132">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




