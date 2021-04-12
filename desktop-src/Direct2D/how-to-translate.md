---
title: Преобразование объекта
description: Показывает, как преобразовать объект.
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338745"
---
# <a name="how-to-translate-an-object"></a>Преобразование объекта

Для преобразования двухмерного объекта необходимо переместить объект вдоль оси x, оси y или обоих объектов. Для создания преобразования преобразования можно вызвать один из двух следующих методов.

-   [**Translation (размер \_ D2D1 \_ F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): принимает упорядоченную пару, определяющую расстояние, которое будет переводиться вдоль оси x и оси y.
-   [**Преобразование (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): принимает расстояние для перемещения вдоль оси x и расстояния, которое необходимо преобразовать вдоль оси y.

В следующем коде создается матрица преобразования перевода, которая перемещает квадратные 20 единиц вправо вдоль оси x и 10 единиц вниз вдоль оси y.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 80.5f, 186.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the translation transform to the render target.
    m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(20, 10));

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



На следующем рисунке показан результат применения преобразования «Преобразование» к квадрату, где исходный квадрат является пунктирным контуром, а преобразованный квадрат — сплошной.

![Иллюстрация квадрата, на которую перемещается 20 единиц вправо по оси x и 10 единиц вниз по оси y](images/translation-ovw.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по Direct2D](reference.md)
</dt> <dt>

[Общие сведения о преобразованиях Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 