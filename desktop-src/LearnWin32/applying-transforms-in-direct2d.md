---
title: Применение преобразований в Direct2D
description: Применение преобразований в Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab83cb9a7981ada944de07e362c2f568889a84a4f90f2171150fbab948ab3a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388494"
---
# <a name="applying-transforms-in-direct2d"></a>Применение преобразований в Direct2D

При [рисовании с помощью Direct2D](drawing-with-direct2d.md)мы видели, что метод [**ID2D1RenderTarget:: филлеллипсе**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) рисует эллипс, выравниваемая по осям x и y. Но предположим, что вы хотите нарисовать эллипс с наклоном на угол?

![изображение, которое показывает наклонный эллипс.](images/graphics16.png)

Используя преобразования, можно изменить форму следующим образом.

-   Поворот вокруг точки.
-   Масштабирование.
-   Преобразование (смещение в направлении X или Y).
-   Асимметрия (также называется *сдвигом*).

Преобразование — это математическая операция, которая сопоставляет набор точек с новым набором точек. Например, на следующей диаграмме показан треугольник, повернутый вокруг точки P3. После применения вращения точка P1 сопоставляется с P1 ", точка P2 сопоставлена с P2", а точка P3 сопоставляется с самой собой.

![Диаграмма, показывающая поворот вокруг точки.](images/graphics17.png)

Преобразования реализуются с помощью матриц. Однако вам не нужно понимать математику матриц, чтобы использовать их. Дополнительные сведения о математических вычислениях см. в разделе [приложение. Преобразование матрицы](appendix--matrix-transforms.md).

Чтобы применить преобразование в Direct2D, вызовите метод [**ID2D1RenderTarget:: сеттрансформ**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) . Этот метод принимает структуру [**D2D1 \_ Matrix \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) , определяющую преобразование. Эту структуру можно инициализировать, вызвав методы класса [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Этот класс содержит статические методы, возвращающие матрицу для каждого типа преобразования:

-   [**Matrix3x2F:: вращение**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   [**Matrix3x2F:: Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))
-   [**Matrix3x2F:: Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))
-   [**Matrix3x2F:: асимметрия**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

Например, следующий код применяет поворот на 20 градусов вокруг точки (100, 100).


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

Преобразование применяется ко всем последующим операциям рисования до повторного вызова [**сеттрансформ**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) . Чтобы удалить текущее преобразование, вызовите **сеттрансформ** с помощью матрицы идентификаторов. Чтобы создать матрицу идентификаторов, вызовите функцию [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) .


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a>Рисование часов

Перейдем преобразования, чтобы преобразовать нашу программу Circle в аналоговые часы. Это можно сделать, добавив линии для стрелок.

![снимок экрана программы аналогового времени.](images/graphics18.png)

Вместо вычисления координат для линий можно вычислить угол, а затем применить преобразование поворота. В следующем коде показана функция, которая рисует одну руку. Параметр *фангле* задает угол руки в градусах.

```C++
void Scene::DrawClockHand(float fHandLength, float fAngle, float fStrokeWidth)
{
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(fAngle, m_ellipse.point)
            );

    // endPoint defines one end of the hand.
    D2D_POINT_2F endPoint = D2D1::Point2F(
        m_ellipse.point.x,
        m_ellipse.point.y - (m_ellipse.radiusY * fHandLength)
        );

    // Draw a line from the center of the ellipse to endPoint.
    m_pRenderTarget->DrawLine(
        m_ellipse.point, endPoint, m_pStroke, fStrokeWidth);
}
```

Этот код рисует вертикальную линию, начиная от центра циферблата и заканчивая *конечной точкой* точки. Линия поворачивается вокруг центра эллипса путем применения преобразования поворота. Центральная точка вращения — это центр эллипса, который формирует циферблат часов.

![Схема, показывающая поворот часового руки.](images/graphics19.png)

В следующем коде показано, как рисуется весь циферблат.

```C++
void Scene::RenderScene()
{
    m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::SkyBlue));

    m_pRenderTarget->FillEllipse(m_ellipse, m_pFill);
    m_pRenderTarget->DrawEllipse(m_ellipse, m_pStroke);

    // Draw hands
    SYSTEMTIME time;
    GetLocalTime(&time);

    // 60 minutes = 30 degrees, 1 minute = 0.5 degree
    const float fHourAngle = (360.0f / 12) * (time.wHour) + (time.wMinute * 0.5f);
    const float fMinuteAngle =(360.0f / 60) * (time.wMinute);

    DrawClockHand(0.6f,  fHourAngle,   6);
    DrawClockHand(0.85f, fMinuteAngle, 4);

    // Restore the identity transformation.
    m_pRenderTarget->SetTransform( D2D1::Matrix3x2F::Identity() );
}
```

вы можете скачать полный проект Visual Studio из [примера Direct2D Clock](direct2d-clock-sample.md). (Только для развлечений, в качестве версии для загрузки добавляется радиальная градианта на циферблат часов.)

## <a name="combining-transforms"></a>Объединение преобразований

Четыре базовых преобразования можно объединить, умножив две или более матрицы. Например, следующий код сочетает поворот с переводом.

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

Класс [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) предоставляет [**оператор \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) для умножения матрицы. Порядок, в котором умножаются матрицы, важен. Задание преобразования (M × N) означает "сначала применить M, а затем N". Например, вот поворот, за которым следует перевод:

![Схема, на которой показан поворот и перевод.](images/graphics20.png)

Ниже приведен код для этого преобразования:

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

Теперь Сравните это преобразование с преобразованием в обратный порядок, переводом, а затем поворотом.

![Диаграмма, на которой показан перевод, за которым следует поворот.](images/graphics21.png)

Поворот выполняется вокруг центра исходного прямоугольника. Ниже приведен код для этого преобразования.

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

Как видите, матрицы одинаковы, но порядок операций изменился. Это происходит потому, что перемножение матриц не коммутативной: M × N ≠ N × M.

## <a name="next"></a>Следующая

[Приложение. преобразования матрицы](appendix--matrix-transforms.md)