---
description: Метод Ондиректрендер собирает сведения о времени, которые управляют синхронизацией и контролем качества.
ms.assetid: ed617fac-b2c6-4a3a-ac91-77e2d7cce981
title: Кбасевидеорендерер. Ондиректрендер, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnDirectRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c117366590c96b63ff4595d4563e92aec542cfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675240"
---
# <a name="cbasevideorendererondirectrender-method"></a><span data-ttu-id="88197-103">Кбасевидеорендерер. Ондиректрендер, метод</span><span class="sxs-lookup"><span data-stu-id="88197-103">CBaseVideoRenderer.OnDirectRender method</span></span>

<span data-ttu-id="88197-104">Метод **ондиректрендер** собирает сведения о времени, которые управляют синхронизацией и контролем качества.</span><span class="sxs-lookup"><span data-stu-id="88197-104">The **OnDirectRender** method collects timing information that controls synchronization and quality control.</span></span>

## <a name="syntax"></a><span data-ttu-id="88197-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88197-105">Syntax</span></span>


```C++
virtual HRESULT OnDirectRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="88197-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88197-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88197-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="88197-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="88197-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) примера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="88197-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88197-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88197-109">Return value</span></span>

<span data-ttu-id="88197-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="88197-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88197-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88197-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88197-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88197-112">Remarks</span></span>

<span data-ttu-id="88197-113">Вызовите этот метод вместо [**онрендерстарт**](cbasevideorenderer-onrenderstart.md) и [**онрендеренд**](cbasevideorenderer-onrenderend.md).</span><span class="sxs-lookup"><span data-stu-id="88197-113">Call this method instead of [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) and [**OnRenderEnd**](cbasevideorenderer-onrenderend.md).</span></span> <span data-ttu-id="88197-114">Этот метод используется модулем подготовки видео DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="88197-114">This method is used by the DirectDraw video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="88197-115">Требования</span><span class="sxs-lookup"><span data-stu-id="88197-115">Requirements</span></span>



| <span data-ttu-id="88197-116">Требование</span><span class="sxs-lookup"><span data-stu-id="88197-116">Requirement</span></span> | <span data-ttu-id="88197-117">Значение</span><span class="sxs-lookup"><span data-stu-id="88197-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88197-118">Header</span><span class="sxs-lookup"><span data-stu-id="88197-118">Header</span></span><br/>  | <dl> <span data-ttu-id="88197-119"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88197-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88197-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="88197-120">Library</span></span><br/> | <dl> <span data-ttu-id="88197-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="88197-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88197-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88197-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88197-123">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="88197-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




