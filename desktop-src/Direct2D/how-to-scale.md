---
title: Масштабирование объекта
description: Показывает, как масштабировать объект.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f46ae37197cb7cbfeb3f86588e1b5298cfc467
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488077"
---
# <a name="how-to-scale-an-object"></a><span data-ttu-id="b4c72-103">Масштабирование объекта</span><span class="sxs-lookup"><span data-stu-id="b4c72-103">How to Scale an Object</span></span>

<span data-ttu-id="b4c72-104">В этом разделе описывается масштабирование объекта с помощью класса [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="b4c72-104">This topic describes how to scale an object by using the [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="b4c72-105">Чтобы масштабировать объект, можно увеличить или уменьшить объект.</span><span class="sxs-lookup"><span data-stu-id="b4c72-105">To scale an object means to make the object larger or smaller.</span></span> <span data-ttu-id="b4c72-106">Для масштабирования объекта можно вызвать один из следующих двух методов.</span><span class="sxs-lookup"><span data-stu-id="b4c72-106">You can call one of the following two methods to scale an object.</span></span>

-   <span data-ttu-id="b4c72-107">**Matrix3x2F:: Scale (D2D1 \_ \_ , размер F скалефактор, \_ точка D2D1, \_ 2F центерпоинт)**</span><span class="sxs-lookup"><span data-stu-id="b4c72-107">**Matrix3x2F::Scale(D2D1\_SIZE\_F scalefactor, D2D1\_POINT\_2F centerpoint)**</span></span>
-   <span data-ttu-id="b4c72-108">**Matrix3x2F:: Scale (плавающая точка ScaleX, масштабирование с плавающей точкой, D2D1, \_ \_ 2F центерпоинт)**</span><span class="sxs-lookup"><span data-stu-id="b4c72-108">**Matrix3x2F::Scale(float scalex, float scaley, D2D1\_POINT\_2F centerpoint)**</span></span>

<span data-ttu-id="b4c72-109">Первый метод сохраняет *ScaleX* и *Scale* в виде упорядоченной пары значений с плавающей запятой в структуре [**D2D1 \_ size \_ F**](/windows/desktop/Direct2D/d2d1-size-f) .</span><span class="sxs-lookup"><span data-stu-id="b4c72-109">The first method stores *scalex* and *scaley* as an ordered pair of floating-point values in the [**D2D1\_SIZE\_F**](/windows/desktop/Direct2D/d2d1-size-f) structure.</span></span> <span data-ttu-id="b4c72-110">Второй метод определяет *ScaleX* и *масштабирует* как отдельные параметры.</span><span class="sxs-lookup"><span data-stu-id="b4c72-110">The second method defines *scalex* and *scaley* as individual parameters.</span></span>

<span data-ttu-id="b4c72-111">Независимо от используемого метода необходимо указать как значения *ScaleX* , так и коэффициенты *масштабирования* .</span><span class="sxs-lookup"><span data-stu-id="b4c72-111">Regardless of which method that you use, you must specify both *scalex* and *scaley* factors.</span></span> <span data-ttu-id="b4c72-112">Значение *ScaleX* является коэффициентом масштабирования в направлении x.</span><span class="sxs-lookup"><span data-stu-id="b4c72-112">The *scalex* value is the scale factor in the x direction.</span></span> <span data-ttu-id="b4c72-113">Например, значение *ScaleX* , равное 1,5, растягивает объект на 150 процентов вдоль оси x.</span><span class="sxs-lookup"><span data-stu-id="b4c72-113">For example, a *scalex* value of 1.5 stretches the object to 150 percent along the x-axis.</span></span> <span data-ttu-id="b4c72-114">Точно так же *масштабное* значение является коэффициентом масштабирования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="b4c72-114">Similarly, the *scaley* value is the scale factor in the y direction.</span></span> <span data-ttu-id="b4c72-115">Например, значение *шкалы* 0,5 сжимает высоту объекта на 50 процентов вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="b4c72-115">For example, a *scaley* value of 0.5 shrinks the height of the object by 50 percent along the y-axis.</span></span>

<span data-ttu-id="b4c72-116">Чтобы указать точку в качестве центра операции масштабирования, используйте параметр *центерпоинт* .</span><span class="sxs-lookup"><span data-stu-id="b4c72-116">To specify a point as the center of the scaling operation, use the *centerpoint* parameter.</span></span> <span data-ttu-id="b4c72-117">По умолчанию объект выравнивается по центру относительно его происхождения (0, 0).</span><span class="sxs-lookup"><span data-stu-id="b4c72-117">By default, an object is centered about its origin (0,0).</span></span>

<span data-ttu-id="b4c72-118">В следующем примере кода создается преобразование «масштаб» для увеличения размера квадрата до 130% от исходного размера.</span><span class="sxs-lookup"><span data-stu-id="b4c72-118">The following example code creates a scale transformation to increase the size of a square to 130% of its original size.</span></span> <span data-ttu-id="b4c72-119">*Центерпоинт* задается в левом верхнем углу исходного квадрата.</span><span class="sxs-lookup"><span data-stu-id="b4c72-119">The *centerpoint* is set to be the upper-left corner of the original square.</span></span>


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



<span data-ttu-id="b4c72-120">На следующем рисунке показан результат применения преобразования «масштаб» к квадрату.</span><span class="sxs-lookup"><span data-stu-id="b4c72-120">The following illustration shows the effect of applying the scale transformation to the square.</span></span> <span data-ttu-id="b4c72-121">Исходный квадрат является пунктирным контуром, а масштабируемый квадрат — сплошным контуром.</span><span class="sxs-lookup"><span data-stu-id="b4c72-121">The original square is a dotted outline and the scaled square is a solid outline.</span></span>

![Иллюстрация квадратного изменения размера до 130% от исходного размера](images/scale-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="b4c72-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b4c72-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4c72-124">Общие сведения о преобразованиях Direct2D</span><span class="sxs-lookup"><span data-stu-id="b4c72-124">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="b4c72-125">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="b4c72-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 