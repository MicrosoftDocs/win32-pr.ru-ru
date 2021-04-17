---
description: Метод Сетдефаулттаржетрект задает целевой видеопрямоугольник по умолчанию (чистый виртуальный). Это внутренняя функция-член, которая вызывается при сбросе исходного прямоугольника.
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: Кбасеконтролвидео. Сетдефаулттаржетрект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54b31268935cb296543b3992bf67b7a2193c1a92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657377"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a><span data-ttu-id="44770-104">Кбасеконтролвидео. Сетдефаулттаржетрект, метод</span><span class="sxs-lookup"><span data-stu-id="44770-104">CBaseControlVideo.SetDefaultTargetRect method</span></span>

<span data-ttu-id="44770-105">`SetDefaultTargetRect`Метод задает целевой видеопрямоугольник по умолчанию (чистый виртуальный).</span><span class="sxs-lookup"><span data-stu-id="44770-105">The `SetDefaultTargetRect` method sets the default target video rectangle (pure virtual).</span></span> <span data-ttu-id="44770-106">Это внутренняя функция-член, которая вызывается при сбросе исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="44770-106">This is an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="44770-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44770-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="44770-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="44770-108">Parameters</span></span>

<span data-ttu-id="44770-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="44770-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44770-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44770-110">Return value</span></span>

<span data-ttu-id="44770-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="44770-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44770-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44770-112">Remarks</span></span>

<span data-ttu-id="44770-113">Производные классы должны переопределять этот параметр, чтобы сбросить конечный прямоугольник видео.</span><span class="sxs-lookup"><span data-stu-id="44770-113">Derived classes should override this to reset the destination video rectangle.</span></span> <span data-ttu-id="44770-114">Он вызывается из функции-члена [**кбасеконтролвидео:: сетдефаултдестинатионпоситион**](cbasecontrolvideo-setdefaultdestinationposition.md) .</span><span class="sxs-lookup"><span data-stu-id="44770-114">It is called from the [**CBaseControlVideo::SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) member function.</span></span>

<span data-ttu-id="44770-115">В следующем примере демонстрируется реализация этой функции в производном классе.</span><span class="sxs-lookup"><span data-stu-id="44770-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// This is called when you reset the default target rectangle.
HRESULT CVideoText::SetDefaultTargetRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT TargetRect = {0,0,m_Size.cx,m_Size.cy};
    m_pRenderer->m_DrawImage.SetTargetRect(&TargetRect);
    return NOERROR;
}
```



<span data-ttu-id="44770-116">В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="44770-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="44770-117">\_Элемент данных m мтин, также определенный в производном классе, содержит объект [**кмедиатипе**](cmediatype.md) с типом носителя для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="44770-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with the media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="44770-118">Требования</span><span class="sxs-lookup"><span data-stu-id="44770-118">Requirements</span></span>



| <span data-ttu-id="44770-119">Требование</span><span class="sxs-lookup"><span data-stu-id="44770-119">Requirement</span></span> | <span data-ttu-id="44770-120">Значение</span><span class="sxs-lookup"><span data-stu-id="44770-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44770-121">Header</span><span class="sxs-lookup"><span data-stu-id="44770-121">Header</span></span><br/>  | <dl> <span data-ttu-id="44770-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44770-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="44770-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="44770-123">Library</span></span><br/> | <dl> <span data-ttu-id="44770-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="44770-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44770-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44770-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44770-126">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="44770-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




