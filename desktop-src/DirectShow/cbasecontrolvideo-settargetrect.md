---
description: Метод Сеттаржетрект задает текущий целевой прямоугольник (чисто виртуальный). Это внутренняя функция-член, которая вызывается при изменении прямоугольника назначения.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Кбасеконтролвидео. Сеттаржетрект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657929"
---
# <a name="cbasecontrolvideosettargetrect-method"></a><span data-ttu-id="6a5b5-104">Кбасеконтролвидео. Сеттаржетрект, метод</span><span class="sxs-lookup"><span data-stu-id="6a5b5-104">CBaseControlVideo.SetTargetRect method</span></span>

<span data-ttu-id="6a5b5-105">`SetTargetRect`Метод задает текущий целевой прямоугольник (чисто виртуальный).</span><span class="sxs-lookup"><span data-stu-id="6a5b5-105">The `SetTargetRect` method sets the current target rectangle (pure virtual).</span></span> <span data-ttu-id="6a5b5-106">Это внутренняя функция-член, которая вызывается при изменении прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-106">This is an internal member function that gets called when the destination rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a5b5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a5b5-107">Syntax</span></span>


```C++
virtual HRESULT SetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="6a5b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a5b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a5b5-109">*птаржетрект*</span><span class="sxs-lookup"><span data-stu-id="6a5b5-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="6a5b5-110">Указатель на прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a5b5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a5b5-111">Return value</span></span>

<span data-ttu-id="6a5b5-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a5b5-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a5b5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a5b5-113">Remarks</span></span>

<span data-ttu-id="6a5b5-114">Производные классы должны переопределять этот параметр, чтобы иметь представление об изменении прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-114">Derived classes should override this to know when the destination rectangle changes.</span></span> <span data-ttu-id="6a5b5-115">Он вызывается из следующих функций-членов.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="6a5b5-116">**Кбасеконтролвидео:: Сетдестинатионпоситион**</span><span class="sxs-lookup"><span data-stu-id="6a5b5-116">**CBaseControlVideo::SetDestinationPosition**</span></span>](cbasecontrolvideo-setdestinationposition.md)
-   [<span data-ttu-id="6a5b5-117">**Кбасеконтролвидео::p UT \_ дестинатионлефт**</span><span class="sxs-lookup"><span data-stu-id="6a5b5-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="6a5b5-118">**Кбасеконтролвидео::p UT \_ дестинатионвидс**</span><span class="sxs-lookup"><span data-stu-id="6a5b5-118">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="6a5b5-119">**Кбасеконтролвидео::p UT \_ дестинатионтоп**</span><span class="sxs-lookup"><span data-stu-id="6a5b5-119">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="6a5b5-120">**Кбасеконтролвидео::p UT \_ дестинатионхеигхт**</span><span class="sxs-lookup"><span data-stu-id="6a5b5-120">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)

<span data-ttu-id="6a5b5-121">В следующем примере демонстрируется реализация этой функции в производном классе.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="6a5b5-122">В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="6a5b5-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a5b5-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6a5b5-123">Requirements</span></span>



| <span data-ttu-id="6a5b5-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6a5b5-124">Requirement</span></span> | <span data-ttu-id="6a5b5-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6a5b5-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a5b5-126">Header</span><span class="sxs-lookup"><span data-stu-id="6a5b5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6a5b5-127"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a5b5-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6a5b5-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6a5b5-128">Library</span></span><br/> | <dl> <span data-ttu-id="6a5b5-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6a5b5-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a5b5-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a5b5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a5b5-131">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="6a5b5-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




