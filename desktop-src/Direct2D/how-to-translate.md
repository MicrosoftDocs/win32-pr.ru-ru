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
# <a name="how-to-translate-an-object"></a><span data-ttu-id="f71c7-103">Преобразование объекта</span><span class="sxs-lookup"><span data-stu-id="f71c7-103">How to Translate an Object</span></span>

<span data-ttu-id="f71c7-104">Для преобразования двухмерного объекта необходимо переместить объект вдоль оси x, оси y или обоих объектов.</span><span class="sxs-lookup"><span data-stu-id="f71c7-104">To translate a 2-D object is to move the object along the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="f71c7-105">Для создания преобразования преобразования можно вызвать один из двух следующих методов.</span><span class="sxs-lookup"><span data-stu-id="f71c7-105">You can call either one of the following two methods to create a translation transformation.</span></span>

-   <span data-ttu-id="f71c7-106">[**Translation (размер \_ D2D1 \_ F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): принимает упорядоченную пару, определяющую расстояние, которое будет переводиться вдоль оси x и оси y.</span><span class="sxs-lookup"><span data-stu-id="f71c7-106">[**Translation(D2D1\_SIZE\_F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): takes an ordered pair that defines the distance to translate along the x-axis and the y-axis.</span></span>
-   <span data-ttu-id="f71c7-107">[**Преобразование (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): принимает расстояние для перемещения вдоль оси x и расстояния, которое необходимо преобразовать вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="f71c7-107">[**Translation(float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): takes the distance to translate along the x-axis and the distance to translate along the y-axis.</span></span>

<span data-ttu-id="f71c7-108">В следующем коде создается матрица преобразования перевода, которая перемещает квадратные 20 единиц вправо вдоль оси x и 10 единиц вниз вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="f71c7-108">The following code creates a translation transformation matrix that moves the square 20 units to the right along the x-axis and 10 units downward along the y-axis.</span></span>


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



<span data-ttu-id="f71c7-109">На следующем рисунке показан результат применения преобразования «Преобразование» к квадрату, где исходный квадрат является пунктирным контуром, а преобразованный квадрат — сплошной.</span><span class="sxs-lookup"><span data-stu-id="f71c7-109">The following illustration shows the effect of applying the translation transformation to the square, where the original square is a dotted outline and the translated square is a solid outline.</span></span>

![Иллюстрация квадрата, на которую перемещается 20 единиц вправо по оси x и 10 единиц вниз по оси y](images/translation-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="f71c7-111">См. также</span><span class="sxs-lookup"><span data-stu-id="f71c7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f71c7-112">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="f71c7-112">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="f71c7-113">Общие сведения о преобразованиях Direct2D</span><span class="sxs-lookup"><span data-stu-id="f71c7-113">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 