---
title: Как наклон объекта
description: Показывает, как наклон объекта.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890949"
---
# <a name="how-to-skew-an-object"></a><span data-ttu-id="d9805-103">Как наклон объекта</span><span class="sxs-lookup"><span data-stu-id="d9805-103">How to Skew an Object</span></span>

<span data-ttu-id="d9805-104">Для наклона (или наклона) объекта означает искажение объекта на указанный угол от оси x, оси y или и того, и другого.</span><span class="sxs-lookup"><span data-stu-id="d9805-104">To skew (or shear) an object means to distort an object by a specified angle from the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="d9805-105">Например, при наклоне квадрата получается параллелограмм.</span><span class="sxs-lookup"><span data-stu-id="d9805-105">For example, when you skew a square, it becomes a parallelogram.</span></span>

<span data-ttu-id="d9805-106">Метод [**Matrix3x2F:: скос**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) принимает 3 параметра:</span><span class="sxs-lookup"><span data-stu-id="d9805-106">The [**Matrix3x2F::Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) method takes 3 parameters:</span></span>

-   <span data-ttu-id="d9805-107">*angleX*: угол отклонения оси x, измеряемый в градусах против часовой стрелки от оси y.</span><span class="sxs-lookup"><span data-stu-id="d9805-107">*angleX*: The x-axis skew angle, which is measured in degrees counterclockwise from the y-axis.</span></span>
-   <span data-ttu-id="d9805-108">*угол*: угол отклонения оси y, измеряемый в градусах по часовой стрелке от оси x.</span><span class="sxs-lookup"><span data-stu-id="d9805-108">*angleY*: The y-axis skew angle, which is measured in degrees clockwise from the x-axis.</span></span>
-   <span data-ttu-id="d9805-109">*центерпоинт*: точка, относительно которой выполняется отклонение.</span><span class="sxs-lookup"><span data-stu-id="d9805-109">*centerPoint*: The point about which the skew is performed.</span></span>

<span data-ttu-id="d9805-110">Чтобы спрогнозировать воздействие преобразования «наклон», рассмотрите, что *angleX* — угол наклона, измеряемый в градусах против часовой стрелки от оси y.</span><span class="sxs-lookup"><span data-stu-id="d9805-110">To predict the effect of a skew transformation, consider that *angleX* is the skew angle measured in degrees counterclockwise from the y-axis.</span></span> <span data-ttu-id="d9805-111">Например, если для *angleX* задано значение 30, объект наклоняет 30 градусов против часовой стрелки вдоль оси y о *центерпоинт*.</span><span class="sxs-lookup"><span data-stu-id="d9805-111">For example, if *angleX* is set to 30, the object skews 30 degrees counterclockwise along the y-axis about the *centerPoint*.</span></span> <span data-ttu-id="d9805-112">На следующем рисунке показан квадрат с наклоном по горизонтали на 30 градусов относительно левого верхнего угла квадрата.</span><span class="sxs-lookup"><span data-stu-id="d9805-112">The following illustration shows a square skewed horizontally 30 degrees about the upper-left corner of the square.</span></span>

![Иллюстрация квадратно наклоненного 30 градусов против часовой стрелки от оси y](images/skewx.png)

<span data-ttu-id="d9805-114">Аналогичным образом, *угол* — это угол наклона, измеряемый в градусах по часовой стрелке от оси x.</span><span class="sxs-lookup"><span data-stu-id="d9805-114">Similarly, *angleY* is a skew angle measured in degrees clockwise from the x-axis.</span></span> <span data-ttu-id="d9805-115">Например, если для параметра « *угол* » задано значение 30, то объект наклоняет 30 градусов по часовой стрелке вдоль оси x *центерпоинт*.</span><span class="sxs-lookup"><span data-stu-id="d9805-115">For example, if *angleY* is set to 30, the object skews 30 degrees clockwise along the x-axis about the *centerPoint*.</span></span> <span data-ttu-id="d9805-116">На следующем рисунке показан квадрат с наклоном по вертикали на 30 градусов относительно левого верхнего угла квадрата.</span><span class="sxs-lookup"><span data-stu-id="d9805-116">The following illustration shows a square skewed vertically 30 degrees about the upper-left corner of the square.</span></span>

![Иллюстрация квадратно наклоненного 30 градусов по часовой стрелке от оси x](images/skewy.png)

<span data-ttu-id="d9805-118">Если для параметра *angleX* и *Angle* задано значение 30 градусов, а *центерпоинт* — верхний левый угол квадрата, вы увидите следующий отклоненный квадрат (сплошной контур).</span><span class="sxs-lookup"><span data-stu-id="d9805-118">If you set both *angleX* and *angleY* to 30 degrees, and the *centerPoint* to the upper-left corner of the square, you will see the following skewed square (solid outlined).</span></span> <span data-ttu-id="d9805-119">Обратите внимание, что отклоненный квадрат наклонен на 30 градусов против часовой стрелки от оси y до 30 градусов по часовой стрелке от оси x.</span><span class="sxs-lookup"><span data-stu-id="d9805-119">Notice that the skewed square is skewed 30 degrees counterclockwise from the y-axis and 30 degrees clockwise from the x-axis.</span></span>

![Иллюстрация квадратно наклоненного 30 градусов против часовой стрелки от оси y до 30 градусов по часовой стрелке от оси x](images/skewxy.png)

<span data-ttu-id="d9805-121">В следующем примере кода квадратный угол 45 градусов наклоняется по горизонтали относительно левого верхнего угла квадрата.</span><span class="sxs-lookup"><span data-stu-id="d9805-121">The following code example skews the square 45 degrees horizontally about the upper-left corner of the square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 301.5f, 186.0f, 361.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the skew transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Skew(
            45.0f,
            0.0f,
            D2D1::Point2F(126.0f, 301.5f))
        );

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



<span data-ttu-id="d9805-122">На следующем рисунке показан результат применения преобразования «наклон» к квадрату, где исходный квадрат является пунктирным контуром, а наклоненный объект (параллелограмм) — сплошной контур.</span><span class="sxs-lookup"><span data-stu-id="d9805-122">The following illustration shows the effect of applying the skew transformation to the square, where the original square is a dotted outline and the skewed object (parallelogram) is a solid outline.</span></span> <span data-ttu-id="d9805-123">Обратите внимание, что угол наклона составляет 45 градусов против часовой стрелки от оси y.</span><span class="sxs-lookup"><span data-stu-id="d9805-123">Notice that the skew angle is 45 degrees counterclockwise from the y-axis.</span></span>

![Иллюстрация квадратно наклоненного 45 градусов против часовой стрелки от оси y](images/skew-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="d9805-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d9805-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9805-126">Общие сведения о преобразованиях Direct2D</span><span class="sxs-lookup"><span data-stu-id="d9805-126">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="d9805-127">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="d9805-127">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 