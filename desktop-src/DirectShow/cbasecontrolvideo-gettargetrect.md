---
description: Метод Жеттаржетрект извлекает прямоугольник назначения. Это внутренняя вспомогательная функция-член.
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: Кбасеконтролвидео. Жеттаржетрект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d59a12e134edf37c8ab0a63f46f77923b112605d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668481"
---
# <a name="cbasecontrolvideogettargetrect-method"></a><span data-ttu-id="0fb3c-104">Кбасеконтролвидео. Жеттаржетрект, метод</span><span class="sxs-lookup"><span data-stu-id="0fb3c-104">CBaseControlVideo.GetTargetRect method</span></span>

<span data-ttu-id="0fb3c-105">`GetTargetRect`Метод извлекает прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="0fb3c-105">The `GetTargetRect` method retrieves the destination rectangle.</span></span> <span data-ttu-id="0fb3c-106">Это внутренняя вспомогательная функция-член.</span><span class="sxs-lookup"><span data-stu-id="0fb3c-106">This is an internal helper member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb3c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fb3c-107">Syntax</span></span>


```C++
virtual HRESULT GetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="0fb3c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fb3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fb3c-109">*птаржетрект*</span><span class="sxs-lookup"><span data-stu-id="0fb3c-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="0fb3c-110">Указатель на прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="0fb3c-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fb3c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fb3c-111">Return value</span></span>

<span data-ttu-id="0fb3c-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0fb3c-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fb3c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0fb3c-113">Remarks</span></span>

<span data-ttu-id="0fb3c-114">Эта функция члена должна быть переопределена в производном классе для возврата целевого прямоугольника, удерживаемого модулем подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="0fb3c-114">This member function must be overridden in the derived class to return the target rectangle held by the video renderer.</span></span> <span data-ttu-id="0fb3c-115">Он вызывается из следующих функций-членов [**кбасеконтролвидео**](cbasecontrolvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="0fb3c-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="0fb3c-116">**Кбасеконтролвидео:: Жетдестинатионпоситион**</span><span class="sxs-lookup"><span data-stu-id="0fb3c-116">**CBaseControlVideo::GetDestinationPosition**</span></span>](cbasecontrolvideo-getdestinationposition.md)
-   [<span data-ttu-id="0fb3c-117">**Кбасеконтролвидео::p UT \_ дестинатионлефт**</span><span class="sxs-lookup"><span data-stu-id="0fb3c-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="0fb3c-118">**Кбасеконтролвидео:: Get \_ дестинатионлефт**</span><span class="sxs-lookup"><span data-stu-id="0fb3c-118">**CBaseControlVideo::get\_DestinationLeft**</span></span>](cbasecontrolvideo-get-destinationleft.md)
-   [<span data-ttu-id="0fb3c-119">**Кбасеконтролвидео::p UT \_ дестинатионвидс**</span><span class="sxs-lookup"><span data-stu-id="0fb3c-119">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="0fb3c-120">**Кбасеконтролвидео:: Get \_ дестинатионвидс**</span><span class="sxs-lookup"><span data-stu-id="0fb3c-120">**CBaseControlVideo::get\_DestinationWidth**</span></span>](cbasecontrolvideo-get-destinationwidth.md)
-   [<span data-ttu-id="0fb3c-121">**Кбасеконтролвидео::p UT \_ дестинатионтоп**</span><span class="sxs-lookup"><span data-stu-id="0fb3c-121">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="0fb3c-122">**Кбасеконтролвидео:: Get \_ дестинатионтоп**</span><span class="sxs-lookup"><span data-stu-id="0fb3c-122">**CBaseControlVideo::get\_DestinationTop**</span></span>](cbasecontrolvideo-get-destinationtop.md)
-   [<span data-ttu-id="0fb3c-123">**Кбасеконтролвидео::p UT \_ дестинатионхеигхт**</span><span class="sxs-lookup"><span data-stu-id="0fb3c-123">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)
-   [<span data-ttu-id="0fb3c-124">**Кбасеконтролвидео:: Get \_ дестинатионхеигхт**</span><span class="sxs-lookup"><span data-stu-id="0fb3c-124">**CBaseControlVideo::get\_DestinationHeight**</span></span>](cbasecontrolvideo-get-destinationheight.md)

<span data-ttu-id="0fb3c-125">В следующем примере демонстрируется реализация этой функции в производном классе.</span><span class="sxs-lookup"><span data-stu-id="0fb3c-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="0fb3c-126">В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="0fb3c-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb3c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0fb3c-127">Requirements</span></span>



| <span data-ttu-id="0fb3c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0fb3c-128">Requirement</span></span> | <span data-ttu-id="0fb3c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0fb3c-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb3c-130">Header</span><span class="sxs-lookup"><span data-stu-id="0fb3c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0fb3c-131"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fb3c-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0fb3c-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0fb3c-132">Library</span></span><br/> | <dl> <span data-ttu-id="0fb3c-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0fb3c-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fb3c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fb3c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fb3c-135">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="0fb3c-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




