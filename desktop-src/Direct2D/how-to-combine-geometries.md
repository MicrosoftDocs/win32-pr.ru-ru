---
title: Объединение геометрических объектов
description: Показывает, как объединить две геометрические объекты с помощью Direct2D.
ms.assetid: c5413e59-ae73-4797-b4ad-3a78ad700634
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8332421c62f49b60bb2186118ac7f741922fdc7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070330"
---
# <a name="how-to-combine-geometries"></a><span data-ttu-id="ae67c-103">Объединение геометрических объектов</span><span class="sxs-lookup"><span data-stu-id="ae67c-103">How to Combine Geometries</span></span>

<span data-ttu-id="ae67c-104">В этом разделе описывается объединение двух геометрических объектов.</span><span class="sxs-lookup"><span data-stu-id="ae67c-104">This topic describes how to combine two geometries.</span></span> <span data-ttu-id="ae67c-105">Direct2D поддерживает четыре режима объединения геометрических объектов: Union, INTERSECT, XOR и Exclude.</span><span class="sxs-lookup"><span data-stu-id="ae67c-105">Direct2D supports four modes for combining geometries: Union, Intersect, XOR, and Exclude.</span></span> <span data-ttu-id="ae67c-106">Эти режимы задаются в перечисляемом типе [**D2D1 в \_ \_ режиме объединения**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) .</span><span class="sxs-lookup"><span data-stu-id="ae67c-106">These modes are specified in the [**D2D1\_COMBINE\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) enum type.</span></span>

<span data-ttu-id="ae67c-107">**Объединение двух геометрических объектов с помощью любого из четырех режимов**</span><span class="sxs-lookup"><span data-stu-id="ae67c-107">**To combine two geometries by using any of the four modes**</span></span>

1.  <span data-ttu-id="ae67c-108">Объявите геометрию пути: переменную типа [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) , которая будет хранить результат комбинации геометрии.</span><span class="sxs-lookup"><span data-stu-id="ae67c-108">Declare a path geometry: a variable of type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) that will store the result of geometry combination.</span></span>
2.  <span data-ttu-id="ae67c-109">Объявите геометрический приемник: переменную типа [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) , которая будет хранить геометрию пути.</span><span class="sxs-lookup"><span data-stu-id="ae67c-109">Declare a geometry sink: a variable of type [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) that will store the path geometry.</span></span>
3.  <span data-ttu-id="ae67c-110">Создайте объект Geometry для пути, вызвав метод [**ID2D1Factory:: креатепасжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="ae67c-110">Create the path geometry object by calling the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method.</span></span>
4.  <span data-ttu-id="ae67c-111">Откройте объект приемника геометрии, вызвав метод [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .</span><span class="sxs-lookup"><span data-stu-id="ae67c-111">Open the geometry sink object by calling the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>
5.  <span data-ttu-id="ae67c-112">Используйте один из четырех режимов объединения двух геометрических объектов, вызвав метод [**ID2D1EllipseGeometry:: комбиневисжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) .</span><span class="sxs-lookup"><span data-stu-id="ae67c-112">Use one of the four modes to combine the two geometries by calling the [**ID2D1EllipseGeometry::CombineWithGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) method.</span></span>
6.  <span data-ttu-id="ae67c-113">Закройте объект геометрического приемника.</span><span class="sxs-lookup"><span data-stu-id="ae67c-113">Close the geometry sink object.</span></span>

<span data-ttu-id="ae67c-114">В следующем коде объявляются переменные типа [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) и **ID2D1GeometrySink**.</span><span class="sxs-lookup"><span data-stu-id="ae67c-114">The following code declares the variables of type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and **ID2D1GeometrySink**.</span></span>


```C++
    ID2D1PathGeometry *m_pPathGeometryUnion;
    ID2D1PathGeometry *m_pPathGeometryIntersect;
    ID2D1PathGeometry *m_pPathGeometryXOR;
    ID2D1PathGeometry *m_pPathGeometryExclude;
```



<span data-ttu-id="ae67c-115">Следующий код использует каждый из четырех режимов объединения двух объектов [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) и выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ae67c-115">The following code uses each of the four modes to combine the two [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects and performs the following actions:</span></span>

-   <span data-ttu-id="ae67c-116">Создает два эллипса, m \_ спеллипсежеометрйоне и m \_ спеллипсежеометритво.</span><span class="sxs-lookup"><span data-stu-id="ae67c-116">Creates two ellipses, m\_spEllipseGeometryOne and m\_spEllipseGeometryTwo.</span></span>
-   <span data-ttu-id="ae67c-117">Создает объект Geometry для пути.</span><span class="sxs-lookup"><span data-stu-id="ae67c-117">Creates a path geometry object.</span></span>
-   <span data-ttu-id="ae67c-118">Открывает объект геометрического приемника.</span><span class="sxs-lookup"><span data-stu-id="ae67c-118">Opens a geometry sink object.</span></span>
-   <span data-ttu-id="ae67c-119">Объединяет два эллипса.</span><span class="sxs-lookup"><span data-stu-id="ae67c-119">Combines the two ellipses.</span></span>
-   <span data-ttu-id="ae67c-120">Закрывает объект геометрического приемника.</span><span class="sxs-lookup"><span data-stu-id="ae67c-120">Closes the geometry sink object.</span></span>


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr = S_OK;
    ID2D1GeometrySink *pGeometrySink = NULL;

    // Create the first ellipse geometry to merge.
    const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
        D2D1::Point2F(75.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        circle1,
        &m_pCircleGeometry1
        );

    if (SUCCEEDED(hr))
    {
        // Create the second ellipse geometry to merge.
        const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
            D2D1::Point2F(125.0f, 75.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
    }


    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryUnion->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_UNION,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_INTERSECT to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryIntersect);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryIntersect->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_INTERSECT,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_XOR to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryXOR);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryXOR->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_XOR,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_EXCLUDE to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryExclude);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryExclude->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_EXCLUDE,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    return hr;
}
```



<span data-ttu-id="ae67c-121">Этот код создает выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="ae67c-121">This code produces the output shown in the following illustration.</span></span>

![Иллюстрация двух геометрических объектов и четырех режимов объединения геометрических объектов (Union, пересечения, XOR и Exclude)](images/combine-modes.png)

## <a name="related-topics"></a><span data-ttu-id="ae67c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ae67c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae67c-124">**\_Режим объединения \_ D2D1**</span><span class="sxs-lookup"><span data-stu-id="ae67c-124">**D2D1\_COMBINE\_MODE**</span></span>](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode)
</dt> <dt>

[<span data-ttu-id="ae67c-125">**ID2D1EllipseGeometry**</span><span class="sxs-lookup"><span data-stu-id="ae67c-125">**ID2D1EllipseGeometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)
</dt> <dt>

[<span data-ttu-id="ae67c-126">**ID2D1PathGeometry**</span><span class="sxs-lookup"><span data-stu-id="ae67c-126">**ID2D1PathGeometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)
</dt> <dt>

<span data-ttu-id="ae67c-127">**ID2D1GeometrySink**</span><span class="sxs-lookup"><span data-stu-id="ae67c-127">**ID2D1GeometrySink**</span></span>
</dt> </dl>

 

 