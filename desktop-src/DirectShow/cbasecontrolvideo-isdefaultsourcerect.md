---
description: Метод Исдефаултсаурцерект определяет, использует ли модуль подготовки отчетов исходный прямоугольник по умолчанию (чисто виртуальный).
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: Кбасеконтролвидео. Исдефаултсаурцерект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390ae779eaa7d640d23b40a7e6f6579e158bf6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669184"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a><span data-ttu-id="1d3c4-103">Кбасеконтролвидео. Исдефаултсаурцерект, метод</span><span class="sxs-lookup"><span data-stu-id="1d3c4-103">CBaseControlVideo.IsDefaultSourceRect method</span></span>

<span data-ttu-id="1d3c4-104">`IsDefaultSourceRect`Метод определяет, использует ли модуль подготовки отчетов исходный прямоугольник по умолчанию (чисто виртуальный).</span><span class="sxs-lookup"><span data-stu-id="1d3c4-104">The `IsDefaultSourceRect` method determines if the renderer is using the default source rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d3c4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d3c4-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="1d3c4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d3c4-106">Parameters</span></span>

<span data-ttu-id="1d3c4-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1d3c4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d3c4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d3c4-108">Return value</span></span>

<span data-ttu-id="1d3c4-109">Возвращает \_ ОК, если модуль подготовки отчетов использует источник по умолчанию; в противном случае возвращает \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="1d3c4-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d3c4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d3c4-110">Remarks</span></span>

<span data-ttu-id="1d3c4-111">Эта функция члена должна быть реализована в производном классе.</span><span class="sxs-lookup"><span data-stu-id="1d3c4-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="1d3c4-112">Он вызывается функцией-членом [**кбасеконтролвидео:: исусингдефаултсаурце**](cbasecontrolvideo-isusingdefaultsource.md) .</span><span class="sxs-lookup"><span data-stu-id="1d3c4-112">It is called by the [**CBaseControlVideo::IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) member function.</span></span>

<span data-ttu-id="1d3c4-113">В следующем примере демонстрируется реализация этой функции в производном классе.</span><span class="sxs-lookup"><span data-stu-id="1d3c4-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="1d3c4-114">В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="1d3c4-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="1d3c4-115">\_Элемент данных m мтин, также определенный в производном классе, содержит объект [**кмедиатипе**](cmediatype.md) с типом носителя для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="1d3c4-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with the media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d3c4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1d3c4-116">Requirements</span></span>



| <span data-ttu-id="1d3c4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1d3c4-117">Requirement</span></span> | <span data-ttu-id="1d3c4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1d3c4-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d3c4-119">Header</span><span class="sxs-lookup"><span data-stu-id="1d3c4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1d3c4-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d3c4-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1d3c4-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1d3c4-121">Library</span></span><br/> | <dl> <span data-ttu-id="1d3c4-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1d3c4-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d3c4-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d3c4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d3c4-124">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="1d3c4-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




