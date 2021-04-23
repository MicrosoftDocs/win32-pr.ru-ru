---
description: Метод Исдефаулттаржетрект определяет, использует ли модуль подготовки отчетов целевой прямоугольник по умолчанию (чистый виртуальный).
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Кбасеконтролвидео. Исдефаулттаржетрект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e267cc65345d18800beccbc80ac7952c89d781d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658127"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a><span data-ttu-id="a0850-103">Кбасеконтролвидео. Исдефаулттаржетрект, метод</span><span class="sxs-lookup"><span data-stu-id="a0850-103">CBaseControlVideo.IsDefaultTargetRect method</span></span>

<span data-ttu-id="a0850-104">`IsDefaultTargetRect`Метод определяет, использует ли модуль подготовки отчетов целевой прямоугольник по умолчанию (чисто виртуальный).</span><span class="sxs-lookup"><span data-stu-id="a0850-104">The `IsDefaultTargetRect` method determines if the renderer is using the default target rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0850-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0850-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="a0850-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0850-106">Parameters</span></span>

<span data-ttu-id="a0850-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a0850-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0850-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0850-108">Return value</span></span>

<span data-ttu-id="a0850-109">Возвращает \_ ОК, если модуль подготовки отчетов использует целевой объект по умолчанию; в противном случае возвращает \_ значение s false.</span><span class="sxs-lookup"><span data-stu-id="a0850-109">Returns S\_OK if the renderer is using the default target; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0850-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0850-110">Remarks</span></span>

<span data-ttu-id="a0850-111">Эта функция члена должна быть реализована в производном классе.</span><span class="sxs-lookup"><span data-stu-id="a0850-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="a0850-112">Он вызывается функцией-членом [**кбасеконтролвидео:: исусингдефаултдестинатион**](cbasecontrolvideo-isusingdefaultdestination.md) .</span><span class="sxs-lookup"><span data-stu-id="a0850-112">It is called by the [**CBaseControlVideo::IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) member function.</span></span>

<span data-ttu-id="a0850-113">В следующем примере демонстрируется реализация этой функции в производном классе.</span><span class="sxs-lookup"><span data-stu-id="a0850-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="a0850-114">В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="a0850-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="a0850-115">\_Элемент данных m мтин, также определенный в производном классе, содержит объект [**кмедиатипе**](cmediatype.md) с типом носителя для входного контакта.</span><span class="sxs-lookup"><span data-stu-id="a0850-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0850-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a0850-116">Requirements</span></span>



| <span data-ttu-id="a0850-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a0850-117">Requirement</span></span> | <span data-ttu-id="a0850-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a0850-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0850-119">Header</span><span class="sxs-lookup"><span data-stu-id="a0850-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a0850-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0850-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0850-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a0850-121">Library</span></span><br/> | <dl> <span data-ttu-id="a0850-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a0850-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0850-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0850-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0850-124">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="a0850-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




