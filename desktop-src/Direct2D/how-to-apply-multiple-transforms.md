---
title: Применение нескольких преобразований к объекту
description: Показывает, как применить к объекту несколько преобразований.
ms.assetid: a3875072-bb73-4698-944e-102ab5539d80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d63db7899b79dd07a6a4a14a4efbbfaeefc5723ad09c71a3462ba5d2fd0c042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259693"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a>Применение нескольких преобразований к объекту

Для выполнения нескольких преобразований объекта означает объединение нескольких преобразований в один. То есть выводить выходные данные каждой матрицы преобразования и использовать их в качестве входных данных для следующего, тем самым получая совокупные эффекты всех матричных преобразований.

Предположим, что две матрицы преобразования, вращение и перевод, умножаются вместе. Результатом является новая матрица, которая выполняет функции вращения и перевода. Поскольку умножение матриц не является коммутативной, преобразование «вращение», умноженное на преобразование «перевод», отличается от преобразования «Преобразование», умноженного на преобразование «вращение».

В следующих примерах кода показано, как применить поворот, а затем перевод, а затем — поворот. Обратите внимание, что результаты отрисовки различны.


```C++
D2D1_RECT_F rectangle = D2D1::RectF(300.0f, 40.0f, 360.0f, 100.0f);

// Draw the rectangle before transforming the render target.

m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(330.0f, 70.0f)
    );


D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

// First rotate about the center of the square and then move
// 20 pixels to the right along the x-axis
// and 10 pixels downward along the y-axis.
m_pRenderTarget->SetTransform(rotation* translation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush, 1.0f);
```




```C++
D2D1_RECT_F rectangle = D2D1::Rect(40.0f, 40.0f, 100.0f, 100.0f);

// Draw a rectangle without transforming it.
m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

m_pRenderTarget->SetTransform(translation);

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(70.0f, 70.0f)
    );

// First move 20 pixels to the right along the x-axis and
// 10 pixels downward along the y-axis,
// and then rotate about the center of the original square.
m_pRenderTarget->SetTransform(translation * rotation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



Код создает выходные данные, показанные на следующем рисунке.

![Иллюстрация одного прямоугольника, который был преобразован, затем повернут, и одного прямоугольника, который был перемещен и затем переведен](images/multipletransforms.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по Direct2D](reference.md)
</dt> <dt>

[Общие сведения о преобразованиях Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 




