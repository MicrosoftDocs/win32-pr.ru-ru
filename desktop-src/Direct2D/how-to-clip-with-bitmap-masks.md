---
title: Использование точечного рисунка в качестве маски непрозрачности
description: Показывает, как обрезать область с растровыми масками.
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2106f43a6845cd724204fbf3e5aa1ec2b866bf46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987754"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a>Использование точечного рисунка в качестве маски непрозрачности

В этом разделе описывается использование точечного рисунка в качестве маски опакти путем вызова метода [**ID2D1Factory:: филлопаЦитимаск**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) . Маска непрозрачности — это битовая карта, которая предоставляет сведения о покрытии, представленные альфа-каналом, который управляет прозрачностью отображаемого содержимого. Этот подход более эффективен, чем использование слоев с маской непрозрачности. Дополнительные сведения см. в разделе [Общие сведения о слоях](direct2d-layers-overview.md).

**Обрезка области**

1.  Загрузка исходного растрового изображения из ресурса. Сведения о загрузке точечного рисунка см. в разделе [Загрузка растрового изображения из ресурса](how-to-load-a-bitmap-from-a-resource.md).
2.  Загрузка маски точечного рисунка из ресурса.
3.  Создайте растровую кисть с исходным точечным рисунком. Сведения о том, как создать растровую кисть, см. в разделе [Создание растровой кисти](how-to-create-a-bitmap-brush.md).
4.  Вызовите [**ID2D1Factory:: сетантиалиасмоде**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) , чтобы установить режим сглаживания для целевого объекта прорисовки в \_ режим сглаживания D2D1, \_ \_ псевдоним для [**ID2D1Factory:: филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) для работы.
5.  Вызовите [**филлопаЦитимаск**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) , используя битовую маску и растровую кисть на целевом объекте прорисовки для заполнения клипа.

На следующем рисунке показана исходная битовая карта слева, битовая маска в центре и битовая карта, обрезанная до маски справа.

![Иллюстрация точечного рисунка Голдфиш, маски в форме рыбы, созданной из растрового изображения, и итогового точечного рисунка в форме рыбы после маски](images/cliparegion-opacitymask.png)

В следующем коде показано, как обрезать область с маской, показанной на предыдущем рисунке. Сначала загружается исходное растровое изображение и битовая маска. А затем создает растровую кисть с исходным точечным рисунком.


```C++
// Create the bitmap to be used by the bitmap brush
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFish",
        L"Image",
        &m_pOrigBitmap
        );
}

if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFishMask",
        L"Image",
        &m_pBitmapMask
        );
}

if (SUCCEEDED(hr))
{
    D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = D2D1::BitmapBrushProperties(
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
        );

    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pOrigBitmap,
        propertiesXClampYClamp,
        &m_pOriginalBitmapBrush
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateBitmapBrush(
            m_pBitmapMask,
            propertiesXClampYClamp,
            &m_pBitmapMaskBrush
            );
    }
}
```



Затем он вызывает [**сетантиалиасмоде**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) для установки режима сглаживания. Вызовите [**филлопаЦитимаск**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) , чтобы использовать битовую маску для обрезки исходного точечного рисунка.


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



Дополнительные сведения о масках непрозрачности см. в статье [Общие сведения о масках непрозрачности](opacity-masks-overview.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по Direct2D](reference.md)
</dt> </dl>

 

 