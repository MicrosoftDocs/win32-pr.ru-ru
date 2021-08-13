---
title: Масштабирование объекта
description: Показывает, как масштабировать объект.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d833ea44e4a38672729dd7647063e8ed9f8de3574d820a3db40d5a848064ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259153"
---
# <a name="how-to-scale-an-object"></a>Масштабирование объекта

В этом разделе описывается масштабирование объекта с помощью класса [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Чтобы масштабировать объект, можно увеличить или уменьшить объект. Для масштабирования объекта можно вызвать один из следующих двух методов.

-   **Matrix3x2F:: Scale (D2D1 \_ \_ , размер F скалефактор, \_ точка D2D1, \_ 2F центерпоинт)**
-   **Matrix3x2F:: Scale (плавающая точка ScaleX, масштабирование с плавающей точкой, D2D1, \_ \_ 2F центерпоинт)**

Первый метод сохраняет *ScaleX* и *Scale* в виде упорядоченной пары значений с плавающей запятой в структуре [**D2D1 \_ size \_ F**](/windows/desktop/Direct2D/d2d1-size-f) . Второй метод определяет *ScaleX* и *масштабирует* как отдельные параметры.

Независимо от используемого метода необходимо указать как значения *ScaleX* , так и коэффициенты *масштабирования* . Значение *ScaleX* является коэффициентом масштабирования в направлении x. Например, значение *ScaleX* , равное 1,5, растягивает объект на 150 процентов вдоль оси x. Точно так же *масштабное* значение является коэффициентом масштабирования в направлении y. Например, значение *шкалы* 0,5 сжимает высоту объекта на 50 процентов вдоль оси y.

Чтобы указать точку в качестве центра операции масштабирования, используйте параметр *центерпоинт* . По умолчанию объект выравнивается по центру относительно его происхождения (0, 0).

В следующем примере кода создается преобразование «масштаб» для увеличения размера квадрата до 130% от исходного размера. *Центерпоинт* задается в левом верхнем углу исходного квадрата.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 80.5f, 498.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the scale transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Scale(
            D2D1::Size(1.3f, 1.3f),
            D2D1::Point2F(438.0f, 80.5f))
        );

    // Paint the rectangle's interior.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



На следующем рисунке показан результат применения преобразования «масштаб» к квадрату. Исходный квадрат является пунктирным контуром, а масштабируемый квадрат — сплошным контуром.

![Иллюстрация квадратного изменения размера до 130% от исходного размера](images/scale-ovw.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Общие сведения о преобразованиях Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Справочник по Direct2D](reference.md)
</dt> </dl>

 

 