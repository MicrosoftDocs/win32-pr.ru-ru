---
description: Метод Онрендеренд выполняет сглаживание для случаев, когда время отрисовки меняется из-за прерываний.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Кбасевидеорендерер. Онрендеренд, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656895"
---
# <a name="cbasevideorendereronrenderend-method"></a><span data-ttu-id="66ae1-103">Кбасевидеорендерер. Онрендеренд, метод</span><span class="sxs-lookup"><span data-stu-id="66ae1-103">CBaseVideoRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="66ae1-104">`OnRenderEnd`Метод выполняет сглаживание для случаев, когда время отрисовки меняется из-за прерываний.</span><span class="sxs-lookup"><span data-stu-id="66ae1-104">The `OnRenderEnd` method performs smoothing for cases where the rendering time varies due to interruptions.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ae1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66ae1-105">Syntax</span></span>


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="66ae1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="66ae1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ae1-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="66ae1-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="66ae1-108">Указатель на пример носителя.</span><span class="sxs-lookup"><span data-stu-id="66ae1-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ae1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66ae1-109">Return value</span></span>

<span data-ttu-id="66ae1-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="66ae1-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66ae1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66ae1-111">Remarks</span></span>

<span data-ttu-id="66ae1-112">Эту функцию члена следует вызывать сразу после рисования изображения.</span><span class="sxs-lookup"><span data-stu-id="66ae1-112">This member function should be called just after drawing an image.</span></span>

<span data-ttu-id="66ae1-113">Эта функция члена переопределяет [**кбасерендерер:: онрендеренд**](cbaserenderer-onrenderend.md).</span><span class="sxs-lookup"><span data-stu-id="66ae1-113">This member function overrides [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66ae1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="66ae1-114">Requirements</span></span>



| <span data-ttu-id="66ae1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="66ae1-115">Requirement</span></span> | <span data-ttu-id="66ae1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="66ae1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66ae1-117">Header</span><span class="sxs-lookup"><span data-stu-id="66ae1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="66ae1-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66ae1-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="66ae1-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="66ae1-119">Library</span></span><br/> | <dl> <span data-ttu-id="66ae1-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="66ae1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66ae1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66ae1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ae1-122">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="66ae1-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




