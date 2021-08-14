---
title: Поворот объекта
description: Показывает, как повернуть объект.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babc84c08af759d8484c8ba85db40780f68570d93a0a8b9442e93b960ecac39c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003539"
---
# <a name="how-to-rotate-an-object"></a>Поворот объекта

В этом разделе описывается, как повернуть объект относительно заданной точки. Чтобы повернуть объект, вызовите метод [**Matrix3x2F:: вращение**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) . Этот метод принимает два параметра: заданный угол и Центральная точка. Угол — это угол поворота по часовой стрелке в градусах, а центральная точка — это точка, на которую поворачивается объект. Центральная точка выражается в системе координат объекта, который преобразуется.

Например, следующий код поворачивает квадрат по часовой стрелке 45 градусов относительно центра квадрата.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



На следующем рисунке показан результат применения предыдущего преобразования вращения к квадрату. Исходный квадрат является пунктирным контуром, а повернутый квадрат — сплошной контур.

![Иллюстрация квадрата, повернутого по часовой стрелке 45 градусов относительно центра исходного квадрата](images/rotate-ovw.png)

На следующем рисунке показан результат поворота на один и тот же угол относительно другой центральной точки. Обратите внимание, что повернутые объекты находятся в разных позициях относительно исходного объекта. Левый контур квадрата является результатом поворота по центру исходного квадрата, а правый контурный квадрат — результат поворота левого верхнего угла исходного квадрата.

![Иллюстрация квадрата, повернутого по часовой стрелке 45 градусов относительно другой центральной точки](images/translate-rotationcompare.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по Direct2D](reference.md)
</dt> <dt>

[Общие сведения о преобразованиях Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 