---
description: Чистый виртуальный метод, переопределяемый производными классами.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Кбасеконтролвидео. ЖетстатиЦимаже, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13b0515e20202373954050b6fa18f10a20a76a6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657437"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a><span data-ttu-id="c366d-103">Кбасеконтролвидео. ЖетстатиЦимаже, метод</span><span class="sxs-lookup"><span data-stu-id="c366d-103">CBaseControlVideo.GetStaticImage method</span></span>

<span data-ttu-id="c366d-104">Чистый виртуальный метод, переопределяемый производными классами.</span><span class="sxs-lookup"><span data-stu-id="c366d-104">Pure virtual method that derived classes override.</span></span>

## <a name="syntax"></a><span data-ttu-id="c366d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c366d-105">Syntax</span></span>


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c366d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c366d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c366d-107">*пбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="c366d-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c366d-108">Указатель на размер выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="c366d-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c366d-109">*пдибимаже*</span><span class="sxs-lookup"><span data-stu-id="c366d-109">*pDIBImage*</span></span> 
</dt> <dd>

<span data-ttu-id="c366d-110">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="c366d-110">Pointer to the output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c366d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c366d-111">Return value</span></span>

<span data-ttu-id="c366d-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c366d-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c366d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c366d-113">Remarks</span></span>

<span data-ttu-id="c366d-114">С помощью интерфейса [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) приложение может запрашивать, что ему предоставляется копия текущего изображения в буфере памяти (некоторые модули подготовки отчетов могут возвращать в него значение E \_ нотимпл, если они не поддерживаются).</span><span class="sxs-lookup"><span data-stu-id="c366d-114">Through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface, an application can request that it be given a copy of the current image in a memory buffer (some renderers can return E\_NOTIMPL to this if they do not support it).</span></span> <span data-ttu-id="c366d-115">Производный класс определяет способ получения изображения.</span><span class="sxs-lookup"><span data-stu-id="c366d-115">The derived class determines how to retrieve the image.</span></span> <span data-ttu-id="c366d-116">Когда приложение вызывает **кбасеконтролвидео:: жетстатиЦимаже**, оно вызывает чистый виртуальный метод, который производный класс должен переопределить для его реализации.</span><span class="sxs-lookup"><span data-stu-id="c366d-116">When the application calls **CBaseControlVideo::GetStaticImage**, it calls this pure virtual method that the derived class should override to implement it.</span></span> <span data-ttu-id="c366d-117">Это также вызывается функцией-членом [**кбасеконтролвидео:: жеткуррентимаже**](cbasecontrolvideo-getcurrentimage.md) .</span><span class="sxs-lookup"><span data-stu-id="c366d-117">This is also called by the [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) member function.</span></span>

<span data-ttu-id="c366d-118">Класс предоставляет вспомогательную функцию-член [**кбасеконтролвидео:: копимаже**](cbasecontrolvideo-copyimage.md), которой можно предоставить образец, содержащий изображение, а функция-член скопирует соответствующий раздел (на основе текущего исходного прямоугольника) в выходной буфер, предоставленный приложением.</span><span class="sxs-lookup"><span data-stu-id="c366d-118">The class provides a helper member function, [**CBaseControlVideo::CopyImage**](cbasecontrolvideo-copyimage.md), that can be given a sample that contains an image, and the member function will copy the relevant section of it (based on the current source rectangle) into the output buffer supplied by the application.</span></span>

<span data-ttu-id="c366d-119">В следующем примере демонстрируется реализация этой функции-члена в производном классе.</span><span class="sxs-lookup"><span data-stu-id="c366d-119">The following example demonstrates an implementation of this member function in a derived class.</span></span> <span data-ttu-id="c366d-120">В этом примере m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md).</span><span class="sxs-lookup"><span data-stu-id="c366d-120">In this example, m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md).</span></span>


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c366d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c366d-121">Requirements</span></span>



| <span data-ttu-id="c366d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c366d-122">Requirement</span></span> | <span data-ttu-id="c366d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c366d-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c366d-124">Header</span><span class="sxs-lookup"><span data-stu-id="c366d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c366d-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c366d-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c366d-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c366d-126">Library</span></span><br/> | <dl> <span data-ttu-id="c366d-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c366d-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c366d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c366d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c366d-129">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="c366d-129">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




