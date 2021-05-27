---
title: Сбой очистки D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Сбой вызова записи на диск для целевого объекта прорисовки
keywords:
- Сбой D1110 Flush Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 721fb27e8cfd5e83f94b93079ee66e4a1c35992d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549929"
---
# <a name="d1110-flush-failure"></a><span data-ttu-id="0ebb0-104">D1110: сбой записи на диск</span><span class="sxs-lookup"><span data-stu-id="0ebb0-104">D1110: Flush Failure</span></span>

<span data-ttu-id="0ebb0-105">Неудачный вызов операции записи на диск в целевом \[ *ресурсе* прорисовки \] .</span><span class="sxs-lookup"><span data-stu-id="0ebb0-105">A Flush call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="0ebb0-106">Теги \[ *TAG1*, *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="0ebb0-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="0ebb0-107">Заполнители</span><span class="sxs-lookup"><span data-stu-id="0ebb0-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="0ebb0-108"><span id="resource"></span><span id="RESOURCE"></span>*ресурсов*</span><span class="sxs-lookup"><span data-stu-id="0ebb0-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="0ebb0-109">Адрес целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="0ebb0-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="0ebb0-110"><span id="tag1"></span><span id="TAG1"></span>*TAG1*</span><span class="sxs-lookup"><span data-stu-id="0ebb0-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="0ebb0-111">Первое значение тега.</span><span class="sxs-lookup"><span data-stu-id="0ebb0-111">The first tag value.</span></span> <span data-ttu-id="0ebb0-112">Дополнительные сведения см. в разделе [**сеттагс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="0ebb0-112">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="0ebb0-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="0ebb0-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="0ebb0-114">Второе значение тега.</span><span class="sxs-lookup"><span data-stu-id="0ebb0-114">The second tag value.</span></span> <span data-ttu-id="0ebb0-115">Дополнительные сведения см. в разделе [**сеттагс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="0ebb0-115">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="0ebb0-116">Уровень ошибки</span><span class="sxs-lookup"><span data-stu-id="0ebb0-116">Error Level</span></span> | <span data-ttu-id="0ebb0-117">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="0ebb0-117">Warning</span></span> |



 

## <a name="examples"></a><span data-ttu-id="0ebb0-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="0ebb0-118">Examples</span></span>

<span data-ttu-id="0ebb0-119">**Пример 1.** В следующем коде показано, что вызов Draw находится в недопустимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="0ebb0-119">**Example 1:** The following code shows that a draw call is in an invalid state.</span></span> <span data-ttu-id="0ebb0-120">Чтобы избежать предупреждающего сообщения, используйте [**сетантиалиасмоде**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) , чтобы задать \_ режим сглаживания \_ D2D1 \_ перед вызовом [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) .</span><span class="sxs-lookup"><span data-stu-id="0ebb0-120">To avoid the warning message, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set D2D1\_ANTIALIAS\_MODE\_ANTIALIASED before a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) call.</span></span>


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





<span data-ttu-id="0ebb0-121">В этом примере создается следующее сообщение отладки:</span><span class="sxs-lookup"><span data-stu-id="0ebb0-121">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

<span data-ttu-id="0ebb0-122">**Пример 2:** В следующем коде показано, что [**Сброс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) вызывается после вызова [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="0ebb0-122">**Example 2:** The following code shows that the [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called after the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call.</span></span>


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



<span data-ttu-id="0ebb0-123">В этом примере создается следующее сообщение отладки:</span><span class="sxs-lookup"><span data-stu-id="0ebb0-123">This example produces the following debug message:</span></span>

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a><span data-ttu-id="0ebb0-124">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="0ebb0-124">Possible Causes</span></span>

<span data-ttu-id="0ebb0-125">Вызов функции [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) может завершиться ошибкой по одной из двух причин.</span><span class="sxs-lookup"><span data-stu-id="0ebb0-125">The [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call can fail for one of two reasons.</span></span> <span data-ttu-id="0ebb0-126">Может произойти сбой, поскольку метод вызывался за пределами вызова [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) / [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или может завершиться ошибкой из-за ошибки, вызванной одной из операций целевого объекта прорисовки, которые были обработаны с момента последнего вызова метода **flush** или **EndDraw** .</span><span class="sxs-lookup"><span data-stu-id="0ebb0-126">It may fail because the method was called outside of the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)/[**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call, or it may fail because there was an error produced by one of the render target operations that have been processed since the last **Flush** call or **EndDraw** call.</span></span> <span data-ttu-id="0ebb0-127">Чтобы устранить эту проблему, приложение должно определить причину ошибки и выполнить соответствующее действие.</span><span class="sxs-lookup"><span data-stu-id="0ebb0-127">To fix the issue, the application should determine the cause of the error and take the appropriate action.</span></span>

## <a name="fixes"></a><span data-ttu-id="0ebb0-128">Исправления</span><span class="sxs-lookup"><span data-stu-id="0ebb0-128">Fixes</span></span>

<span data-ttu-id="0ebb0-129">Вызов [**очистки**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) может завершиться неудачей по нескольким причинам.</span><span class="sxs-lookup"><span data-stu-id="0ebb0-129">There are many reasons that a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call might fail.</span></span> <span data-ttu-id="0ebb0-130">Приложение должно определить причину ошибки и предпринять соответствующие действия.</span><span class="sxs-lookup"><span data-stu-id="0ebb0-130">The application should determine the cause of the error and take the appropriate action.</span></span>

 

 