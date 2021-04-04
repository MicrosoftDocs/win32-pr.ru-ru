---
title: Общие сведения о совместимых целевых объектах рендеринга A8
description: Описывает основы совместимых целевых объектов рендеринга A8 и предоставляет примеры их использования.
ms.assetid: 218c0123-8da9-4d73-9882-cbf7f205001f
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 552577283adfa9a440e94b7e04f4056bd6c3ecda
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "103988056"
---
# <a name="compatible-a8-render-targets-overview"></a>Общие сведения о совместимых целевых объектах рендеринга A8

В этом разделе описаны основы совместимого целевого объекта рендеринга A8 и приведены примеры его использования.

Совместимый целевой объект рендеринга A8 — совместимый целевой объект отрисовки ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)), использующий формат пикселей A8 ( \_ Формат DXGI \_ a8 \_ UNORM). Вы можете использовать совместимый целевой объект рендеринга A8, чтобы повысить производительность приложения и обеспечить более плавные переходы во время анимации текста. Совместимый целевой объект рендеринга A8 полезен при попытке улучшить следующее:

-   Частота кадров приложения, которая визуализирует текст или сглаживание с помощью сглаживания, включающее только простые анимации, такие как перевод, вращение, масштабирование или изменение цвета.

-   Непрерывность визуального элемента приложения, которое растягивает и диминшес текст во время анимации.

Чтобы создать совместимый целевой объект рендеринга A8, используйте метод [**ID2D1RenderTarget:: креатекомпатиблерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) вместе с форматом DXGI \_ \_ a8 \_ UNORM пикселей и укажите возвращенный совместимый целевой объект рендеринга. Дополнительные сведения о форматах пикселей см. в разделе [Поддерживаемые форматы пикселей и альфа-режимы](./supported-pixel-formats-and-alpha-modes.md).

Например, чтобы эффективно анимировать текст, показанный на следующем снимке экрана, используйте совместимый целевой объект рендеринга A8 для кэширования текста в качестве маски непрозрачности. Затем примените преобразования к маске непрозрачности для достижения быстрых результатов отрисовки.

![снимок экрана с текстом для анимации](images/a8rendertarget.png)

В следующем примере кода показано, как это сделать: Он создает совместимый целевой объект рендеринга A8, извлекает из него битовую карту, а затем визуализирует растровое изображение с помощью [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md).

```cpp
ID2D1BitmapRenderTarget *m_pOpacityRT;

// Create the compatible render target using desiredPixelSize to avoid
// blurriness issues caused by a fractional-pixel desiredSize.

D2D1_PIXEL_FORMAT alphaOnlyFormat = D2D1::PixelFormat(
    DXGI_FORMAT_A8_UNORM, 
    D2D1_ALPHA_MODE_PREMULTIPLIED);

hr = m_pRT->CreateCompatibleRenderTarget(
    NULL,
    &maskPixelSize,
    &alphaOnlyFormat,
    D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE,
    &m_pOpacityRT
    );

D2D1_RECT_F destinationRect = D2D1::RectF(
    roundedOffset.x,
    roundedOffset.y,
    roundedOffset.x + opacityRTSize.width,
    roundedOffset.y + opacityRTSize.height
    );

ID2D1Bitmap *pBitmap = NULL;
m_pOpacityRT->GetBitmap(&pBitmap);

pBitmap->GetDpi(&dpiX, &dpiY);

// The antialias mode must be set to D2D1_ANTIALIAS_MODE_ALIASED
// for this method to succeed. We've set this mode already though
// so no need to do it again.

m_pRT->FillOpacityMask(
    pBitmap,
    m_pBlackBrush,
    D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL,
    &destinationRect
    );

pBitmap->Release();
```

## <a name="related-topics"></a>См. также

[Справочник по Direct2D](reference.md)