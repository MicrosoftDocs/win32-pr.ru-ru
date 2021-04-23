---
title: Применение преобразований в Direct2D
description: Применение преобразований в Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8edddbb3150f16428c56bd4c6da828c9b2ce594e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791653"
---
# <a name="applying-transforms-in-direct2d"></a><span data-ttu-id="0b6ef-103">Применение преобразований в Direct2D</span><span class="sxs-lookup"><span data-stu-id="0b6ef-103">Applying Transforms in Direct2D</span></span>

<span data-ttu-id="0b6ef-104">При [рисовании с помощью Direct2D](drawing-with-direct2d.md)мы видели, что метод [**ID2D1RenderTarget:: филлеллипсе**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) рисует эллипс, выравниваемая по осям x и y.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-104">In [Drawing with Direct2D](drawing-with-direct2d.md), we saw that the [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws an ellipse that is aligned to the x- and y-axes.</span></span> <span data-ttu-id="0b6ef-105">Но предположим, что вы хотите нарисовать эллипс с наклоном на угол?</span><span class="sxs-lookup"><span data-stu-id="0b6ef-105">But suppose that you want to draw an ellipse tilted at an angle?</span></span>

![изображение, которое показывает наклонный эллипс.](images/graphics16.png)

<span data-ttu-id="0b6ef-107">Используя преобразования, можно изменить форму следующим образом.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-107">By using transforms, you can alter a shape in the following ways.</span></span>

-   <span data-ttu-id="0b6ef-108">Поворот вокруг точки.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-108">Rotation around a point.</span></span>
-   <span data-ttu-id="0b6ef-109">Масштабирование.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-109">Scaling.</span></span>
-   <span data-ttu-id="0b6ef-110">Преобразование (смещение в направлении X или Y).</span><span class="sxs-lookup"><span data-stu-id="0b6ef-110">Translation (displacement in the X or Y direction).</span></span>
-   <span data-ttu-id="0b6ef-111">Асимметрия (также называется *сдвигом*).</span><span class="sxs-lookup"><span data-stu-id="0b6ef-111">Skew (also known as *shear*).</span></span>

<span data-ttu-id="0b6ef-112">Преобразование — это математическая операция, которая сопоставляет набор точек с новым набором точек.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-112">A transform is a mathematical operation that maps a set of points to a new set of points.</span></span> <span data-ttu-id="0b6ef-113">Например, на следующей диаграмме показан треугольник, повернутый вокруг точки P3.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-113">For example, the following diagram shows a triangle rotated around the point P3.</span></span> <span data-ttu-id="0b6ef-114">После применения вращения точка P1 сопоставляется с P1 ", точка P2 сопоставлена с P2", а точка P3 сопоставляется с самой собой.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-114">After the rotation is applied, the point P1 is mapped to P1', the point P2 is mapped to P2', and the point P3 maps to itself.</span></span>

![Диаграмма, показывающая поворот вокруг точки.](images/graphics17.png)

<span data-ttu-id="0b6ef-116">Преобразования реализуются с помощью матриц.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-116">Transforms are implemented by using matrices.</span></span> <span data-ttu-id="0b6ef-117">Однако вам не нужно понимать математику матриц, чтобы использовать их.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-117">However, you do not have to understand the mathematics of matrices in order to use them.</span></span> <span data-ttu-id="0b6ef-118">Дополнительные сведения о математических вычислениях см. в разделе [приложение. Преобразование матрицы](appendix--matrix-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="0b6ef-118">If you want to learn more about the math, see [Appendix: Matrix Transforms](appendix--matrix-transforms.md).</span></span>

<span data-ttu-id="0b6ef-119">Чтобы применить преобразование в Direct2D, вызовите метод [**ID2D1RenderTarget:: сеттрансформ**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) .</span><span class="sxs-lookup"><span data-stu-id="0b6ef-119">To apply a transform in Direct2D, call the [**ID2D1RenderTarget::SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) method.</span></span> <span data-ttu-id="0b6ef-120">Этот метод принимает структуру [**D2D1 \_ Matrix \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) , определяющую преобразование.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-120">This method takes a [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure that defines the transformation.</span></span> <span data-ttu-id="0b6ef-121">Эту структуру можно инициализировать, вызвав методы класса [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="0b6ef-121">You can initialize this structure by calling methods on the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="0b6ef-122">Этот класс содержит статические методы, возвращающие матрицу для каждого типа преобразования:</span><span class="sxs-lookup"><span data-stu-id="0b6ef-122">This class contains static methods that return a matrix for each kind of transform:</span></span>

-   [<span data-ttu-id="0b6ef-123">**Matrix3x2F:: вращение**</span><span class="sxs-lookup"><span data-stu-id="0b6ef-123">**Matrix3x2F::Rotation**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   <span data-ttu-id="0b6ef-124">[**Matrix3x2F:: Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span><span class="sxs-lookup"><span data-stu-id="0b6ef-124">[**Matrix3x2F::Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span></span>
-   <span data-ttu-id="0b6ef-125">[**Matrix3x2F:: Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span><span class="sxs-lookup"><span data-stu-id="0b6ef-125">[**Matrix3x2F::Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span></span>
-   [<span data-ttu-id="0b6ef-126">**Matrix3x2F:: асимметрия**</span><span class="sxs-lookup"><span data-stu-id="0b6ef-126">**Matrix3x2F::Skew**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

<span data-ttu-id="0b6ef-127">Например, следующий код применяет поворот на 20 градусов вокруг точки (100, 100).</span><span class="sxs-lookup"><span data-stu-id="0b6ef-127">For example, the following code applies a 20-degree rotation around the point (100, 100).</span></span>


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

<span data-ttu-id="0b6ef-128">Преобразование применяется ко всем последующим операциям рисования до повторного вызова [**сеттрансформ**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) .</span><span class="sxs-lookup"><span data-stu-id="0b6ef-128">The transform is applied to all later drawing operations until you call [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) again.</span></span> <span data-ttu-id="0b6ef-129">Чтобы удалить текущее преобразование, вызовите **сеттрансформ** с помощью матрицы идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-129">To remove the current transform, call **SetTransform** with the identity matrix.</span></span> <span data-ttu-id="0b6ef-130">Чтобы создать матрицу идентификаторов, вызовите функцию [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) .</span><span class="sxs-lookup"><span data-stu-id="0b6ef-130">To create the identity matrix, call the [**Matrix3x2F::Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) function.</span></span>


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a><span data-ttu-id="0b6ef-131">Рисование часов</span><span class="sxs-lookup"><span data-stu-id="0b6ef-131">Drawing Clock Hands</span></span>

<span data-ttu-id="0b6ef-132">Перейдем преобразования, чтобы преобразовать нашу программу Circle в аналоговые часы.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-132">Let's put transforms to use by converting our Circle program into an analog clock.</span></span> <span data-ttu-id="0b6ef-133">Это можно сделать, добавив линии для стрелок.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-133">We can do this by adding lines for the hands.</span></span>

![снимок экрана программы аналогового времени.](images/graphics18.png)

<span data-ttu-id="0b6ef-135">Вместо вычисления координат для линий можно вычислить угол, а затем применить преобразование поворота.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-135">Instead of calculating the coordinates for the lines, we can calculate the angle and then apply a rotation transform.</span></span> <span data-ttu-id="0b6ef-136">В следующем коде показана функция, которая рисует одну руку.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-136">The following code shows a function that draws one clock hand.</span></span> <span data-ttu-id="0b6ef-137">Параметр *фангле* задает угол руки в градусах.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-137">The *fAngle* parameter gives the angle of the hand, in degrees.</span></span>

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

<span data-ttu-id="0b6ef-138">Этот код рисует вертикальную линию, начиная от центра циферблата и заканчивая *конечной точкой* точки.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-138">This code draws a vertical line, starting from the center of the clock face and ending at the point *endPoint*.</span></span> <span data-ttu-id="0b6ef-139">Линия поворачивается вокруг центра эллипса путем применения преобразования поворота.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-139">The line is rotated around the center of the ellipse by applying a rotation transform.</span></span> <span data-ttu-id="0b6ef-140">Центральная точка вращения — это центр эллипса, который формирует циферблат часов.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-140">The center point for the rotation is the center of ellipse that forms the clock face.</span></span>

![Схема, показывающая поворот часового руки.](images/graphics19.png)

<span data-ttu-id="0b6ef-142">В следующем коде показано, как рисуется весь циферблат.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-142">The following code shows how the whole clock face is drawn.</span></span>

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

<span data-ttu-id="0b6ef-143">Вы можете скачать полный проект Visual Studio из [примера Direct2D Clock](direct2d-clock-sample.md).</span><span class="sxs-lookup"><span data-stu-id="0b6ef-143">You can download the complete Visual Studio project from [Direct2D Clock Sample](direct2d-clock-sample.md).</span></span> <span data-ttu-id="0b6ef-144">(Только для развлечений, в качестве версии для загрузки добавляется радиальная градианта на циферблат часов.)</span><span class="sxs-lookup"><span data-stu-id="0b6ef-144">(Just for fun, the download version adds a radial gradiant to the clock face.)</span></span>

## <a name="combining-transforms"></a><span data-ttu-id="0b6ef-145">Объединение преобразований</span><span class="sxs-lookup"><span data-stu-id="0b6ef-145">Combining Transforms</span></span>

<span data-ttu-id="0b6ef-146">Четыре базовых преобразования можно объединить, умножив две или более матрицы.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-146">The four basic transforms can be combined by multiplying two or more matrices.</span></span> <span data-ttu-id="0b6ef-147">Например, следующий код сочетает поворот с переводом.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-147">For example, the following code combines a rotation with a translation.</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="0b6ef-148">Класс [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) предоставляет [**оператор \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) для умножения матрицы.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-148">The [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class provides [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for matrix multiplication.</span></span> <span data-ttu-id="0b6ef-149">Порядок, в котором умножаются матрицы, важен.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-149">The order in which you multiply the matrices is important.</span></span> <span data-ttu-id="0b6ef-150">Задание преобразования (M × N) означает "сначала применить M, а затем N".</span><span class="sxs-lookup"><span data-stu-id="0b6ef-150">Setting a transform (M × N) means "Apply M first, followed by N."</span></span> <span data-ttu-id="0b6ef-151">Например, вот поворот, за которым следует перевод:</span><span class="sxs-lookup"><span data-stu-id="0b6ef-151">For example, here is rotation followed by translation:</span></span>

![Схема, на которой показан поворот и перевод.](images/graphics20.png)

<span data-ttu-id="0b6ef-153">Ниже приведен код для этого преобразования:</span><span class="sxs-lookup"><span data-stu-id="0b6ef-153">Here is the code for this transform:</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="0b6ef-154">Теперь Сравните это преобразование с преобразованием в обратный порядок, переводом, а затем поворотом.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-154">Now compare that transform with a transform in the reverse order, translation followed by rotation.</span></span>

![Диаграмма, на которой показан перевод, за которым следует поворот.](images/graphics21.png)

<span data-ttu-id="0b6ef-156">Поворот выполняется вокруг центра исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-156">The rotation is performed around the center of the original rectangle.</span></span> <span data-ttu-id="0b6ef-157">Ниже приведен код для этого преобразования.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-157">Here is the code for this transform.</span></span>

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

<span data-ttu-id="0b6ef-158">Как видите, матрицы одинаковы, но порядок операций изменился.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-158">As you can see, the matrices are the same, but the order of operations has changed.</span></span> <span data-ttu-id="0b6ef-159">Это происходит потому, что перемножение матриц не коммутативной: M × N ≠ N × M.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-159">This happens because matrix multiplication is not commutative: M × N ≠ N × M.</span></span>

## <a name="next"></a><span data-ttu-id="0b6ef-160">Следующая</span><span class="sxs-lookup"><span data-stu-id="0b6ef-160">Next</span></span>

[<span data-ttu-id="0b6ef-161">Приложение. преобразования матрицы</span><span class="sxs-lookup"><span data-stu-id="0b6ef-161">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)