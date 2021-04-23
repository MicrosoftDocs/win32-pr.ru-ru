---
title: Поворот объекта
description: Показывает, как повернуть объект.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cd900a78ba4d81919df91b85fd97723172eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987707"
---
# <a name="how-to-rotate-an-object"></a><span data-ttu-id="efe8e-103">Поворот объекта</span><span class="sxs-lookup"><span data-stu-id="efe8e-103">How to Rotate an Object</span></span>

<span data-ttu-id="efe8e-104">В этом разделе описывается, как повернуть объект относительно заданной точки.</span><span class="sxs-lookup"><span data-stu-id="efe8e-104">This topic describes how to rotate an object about a specified point.</span></span> <span data-ttu-id="efe8e-105">Чтобы повернуть объект, вызовите метод [**Matrix3x2F:: вращение**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) .</span><span class="sxs-lookup"><span data-stu-id="efe8e-105">To rotate an object, call [**Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method.</span></span> <span data-ttu-id="efe8e-106">Этот метод принимает два параметра: заданный угол и Центральная точка.</span><span class="sxs-lookup"><span data-stu-id="efe8e-106">This method takes two parameters, the specified angle and the center point.</span></span> <span data-ttu-id="efe8e-107">Угол — это угол поворота по часовой стрелке в градусах, а центральная точка — это точка, на которую поворачивается объект.</span><span class="sxs-lookup"><span data-stu-id="efe8e-107">The angle is a clockwise rotation angle in degrees, and the center point is the point about which the object rotates.</span></span> <span data-ttu-id="efe8e-108">Центральная точка выражается в системе координат объекта, который преобразуется.</span><span class="sxs-lookup"><span data-stu-id="efe8e-108">The center point is expressed in the coordinate system of the object that is transformed.</span></span>

<span data-ttu-id="efe8e-109">Например, следующий код поворачивает квадрат по часовой стрелке 45 градусов относительно центра квадрата.</span><span class="sxs-lookup"><span data-stu-id="efe8e-109">For example, the following code rotates a square clockwise 45 degrees about the center of the square.</span></span>


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



<span data-ttu-id="efe8e-110">На следующем рисунке показан результат применения предыдущего преобразования вращения к квадрату.</span><span class="sxs-lookup"><span data-stu-id="efe8e-110">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="efe8e-111">Исходный квадрат является пунктирным контуром, а повернутый квадрат — сплошной контур.</span><span class="sxs-lookup"><span data-stu-id="efe8e-111">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![Иллюстрация квадрата, повернутого по часовой стрелке 45 градусов относительно центра исходного квадрата](images/rotate-ovw.png)

<span data-ttu-id="efe8e-113">На следующем рисунке показан результат поворота на один и тот же угол относительно другой центральной точки.</span><span class="sxs-lookup"><span data-stu-id="efe8e-113">The following illustration shows the effect of rotating by the same angle about a different center point.</span></span> <span data-ttu-id="efe8e-114">Обратите внимание, что повернутые объекты находятся в разных позициях относительно исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="efe8e-114">Notice that the rotated objects are in different positions relative to the original.</span></span> <span data-ttu-id="efe8e-115">Левый контур квадрата является результатом поворота по центру исходного квадрата, а правый контурный квадрат — результат поворота левого верхнего угла исходного квадрата.</span><span class="sxs-lookup"><span data-stu-id="efe8e-115">The left outlined square is the result of rotating about the center of the original square, and the right outlined square is the result of rotating about the upper-left corner of the original square.</span></span>

![Иллюстрация квадрата, повернутого по часовой стрелке 45 градусов относительно другой центральной точки](images/translate-rotationcompare.png)

## <a name="related-topics"></a><span data-ttu-id="efe8e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="efe8e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efe8e-118">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="efe8e-118">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="efe8e-119">Общие сведения о преобразованиях Direct2D</span><span class="sxs-lookup"><span data-stu-id="efe8e-119">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 