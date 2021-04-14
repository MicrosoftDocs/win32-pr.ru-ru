---
description: Метод Сетдефаултсаурцерект задает исходный видеопрямоугольник по умолчанию (чистый виртуальный). Это во внутренней функции-члене, которая вызывается при сбросе исходного прямоугольника.
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: Кбасеконтролвидео. Сетдефаултсаурцерект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fe2001a42ca75fff4f3172c8ce05da18881d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668840"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a><span data-ttu-id="cdd74-104">Кбасеконтролвидео. Сетдефаултсаурцерект, метод</span><span class="sxs-lookup"><span data-stu-id="cdd74-104">CBaseControlVideo.SetDefaultSourceRect method</span></span>

<span data-ttu-id="cdd74-105">`SetDefaultSourceRect`Метод задает исходный видеопрямоугольник по умолчанию (чистый виртуальный).</span><span class="sxs-lookup"><span data-stu-id="cdd74-105">The `SetDefaultSourceRect` method sets the default source video rectangle (pure virtual).</span></span> <span data-ttu-id="cdd74-106">Это во внутренней функции-члене, которая вызывается при сбросе исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="cdd74-106">This in an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd74-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdd74-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="cdd74-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdd74-108">Parameters</span></span>

<span data-ttu-id="cdd74-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cdd74-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cdd74-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cdd74-110">Return value</span></span>

<span data-ttu-id="cdd74-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cdd74-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd74-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdd74-112">Remarks</span></span>

<span data-ttu-id="cdd74-113">Производные классы должны переопределять этот параметр, чтобы сбросить исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="cdd74-113">Derived classes should override this to reset the source rectangle.</span></span> <span data-ttu-id="cdd74-114">Он вызывается из [**кбасеконтролвидео:: сетдефаултсаурцепоситион**](cbasecontrolvideo-setdefaultsourceposition.md).</span><span class="sxs-lookup"><span data-stu-id="cdd74-114">It is called from [**CBaseControlVideo::SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).</span></span>

<span data-ttu-id="cdd74-115">В следующем примере демонстрируется реализация этой функции в производном классе.</span><span class="sxs-lookup"><span data-stu-id="cdd74-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



<span data-ttu-id="cdd74-116">В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="cdd74-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="cdd74-117">\_Элемент данных m мтин, также определенный в производном классе, содержит объект [**кмедиатипе**](cmediatype.md) с типом носителя для входного контакта.</span><span class="sxs-lookup"><span data-stu-id="cdd74-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd74-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cdd74-118">Requirements</span></span>



| <span data-ttu-id="cdd74-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cdd74-119">Requirement</span></span> | <span data-ttu-id="cdd74-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cdd74-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd74-121">Header</span><span class="sxs-lookup"><span data-stu-id="cdd74-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cdd74-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdd74-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cdd74-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cdd74-123">Library</span></span><br/> | <dl> <span data-ttu-id="cdd74-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cdd74-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd74-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdd74-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd74-126">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="cdd74-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




