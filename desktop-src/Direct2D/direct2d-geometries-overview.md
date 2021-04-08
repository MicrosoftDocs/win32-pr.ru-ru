---
title: 'Обзор геометрий '
description: Описывает основы геометрических объектов Direct2D, которые можно использовать для представления фигур, управления ими и их анализа.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Direct2D, общие сведения о геометрических фигурах
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cb97b0737bfad391fb9ba2501793a970fcbd9886
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797077"
---
# <a name="geometries-overview"></a><span data-ttu-id="5410f-104">Обзор геометрий </span><span class="sxs-lookup"><span data-stu-id="5410f-104">Geometries overview</span></span>

<span data-ttu-id="5410f-105">В этом обзоре описывается создание и использование объектов [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) для определения двумерных иллюстраций и управления ими.</span><span class="sxs-lookup"><span data-stu-id="5410f-105">This overview describes how to create and use [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) objects to define and manipulate 2D figures.</span></span> <span data-ttu-id="5410f-106">В него входят следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="5410f-106">It contains the following sections.</span></span>

## <a name="what-is-a-direct2d-geometry"></a><span data-ttu-id="5410f-107">Что такое Direct2D Geometry?</span><span class="sxs-lookup"><span data-stu-id="5410f-107">What is a Direct2D geometry?</span></span>

<span data-ttu-id="5410f-108">Direct2D геометрия — это объект [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) .</span><span class="sxs-lookup"><span data-stu-id="5410f-108">A Direct2D geometry is an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object.</span></span> <span data-ttu-id="5410f-109">Это может быть простой геометрический объект ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)или [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), геометрическая траектория ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) или составная геометрия ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) и [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span><span class="sxs-lookup"><span data-stu-id="5410f-109">This object can be a simple geometry ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), or [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), a path geometry ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)), or a composite geometry ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) and [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span></span>

<span data-ttu-id="5410f-110">Геометрические объекты Direct2D позволяют описывать двухмерные цифры и предлагают множество применений, например определение областей проверки попадания, областей клипов и даже путей анимации.</span><span class="sxs-lookup"><span data-stu-id="5410f-110">Direct2D geometries enable you to describe two-dimensional figures and offer many uses, such as defining hit-test regions, clip regions, and even animation paths.</span></span>

<span data-ttu-id="5410f-111">Геометрические объекты Direct2D являются неизменяемыми и аппаратно-независимыми ресурсами, созданными [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="5410f-111">Direct2D geometries are immutable and device-independent resources created by [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span> <span data-ttu-id="5410f-112">Как правило, необходимо создавать геометрические объекты один раз и хранить их на протяжении всего жизненного цикла приложения или до их изменения.</span><span class="sxs-lookup"><span data-stu-id="5410f-112">Generally, you should create geometries one time and keep them for the life of the application, or until they have to be changed.</span></span> <span data-ttu-id="5410f-113">Дополнительные сведения о аппаратно-независимых и аппаратно зависимых ресурсах см. в разделе [Общие сведения о ресурсах](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="5410f-113">For more information about device-independent and device-dependent resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="5410f-114">В следующих разделах описываются различные виды геометрических объектов.</span><span class="sxs-lookup"><span data-stu-id="5410f-114">The following sections describe the different kinds of geometries.</span></span>

## <a name="simple-geometries"></a><span data-ttu-id="5410f-115">Простые геометрические объекты</span><span class="sxs-lookup"><span data-stu-id="5410f-115">Simple geometries</span></span>

<span data-ttu-id="5410f-116">Простые геометрические объекты включают [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)и [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , и их можно использовать для создания базовых геометрических фигур, таких как прямоугольники, скругленные прямоугольники, круги и эллипсы.</span><span class="sxs-lookup"><span data-stu-id="5410f-116">Simple geometries include [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), and [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects, and can be used to create basic geometric figures, such as rectangles, rounded rectangles, circles, and ellipses.</span></span>

<span data-ttu-id="5410f-117">Чтобы создать простую геометрию, используйте один из методов [**ID2D1Factory:: create<*Жеометритипе*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="5410f-117">To create a simple geometry, use one of the [**ID2D1Factory::Create<*geometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) methods.</span></span> <span data-ttu-id="5410f-118">Эти методы создают объект указанного типа.</span><span class="sxs-lookup"><span data-stu-id="5410f-118">These methods create an object of the specified type.</span></span> <span data-ttu-id="5410f-119">Например, чтобы создать прямоугольник, вызовите метод [**ID2D1Factory:: креатеректанглежеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), который возвращает объект [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) . чтобы создать скругленный прямоугольник, вызовите метод [**ID2D1Factory:: креатераундедректанглежеометри**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), который возвращает объект [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) и т. д.</span><span class="sxs-lookup"><span data-stu-id="5410f-119">For example, to create a rectangle, call [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), which returns an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object; to create a rounded rectangle, call [**ID2D1Factory::CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), which returns an [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) object, and so on.</span></span>

<span data-ttu-id="5410f-120">В следующем примере кода вызывается метод [**креатиллипсежеометри**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) , который передается в виде эллипса с *центром* , имеющим значение (100, 100), *x-RADIUS —* 100, а *y — RADIUS —* 50.</span><span class="sxs-lookup"><span data-stu-id="5410f-120">The following code example calls the [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) method, passing in an ellipse structure with the *center* set to (100, 100), *x-radius* to 100, and *y-radius* to 50.</span></span> <span data-ttu-id="5410f-121">Затем он вызывает [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), передавая полученную геометрию эллипса, указатель на черный [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)и толщину штриха, равную 5.</span><span class="sxs-lookup"><span data-stu-id="5410f-121">Then, it calls [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), passing in the returned ellipse geometry, a pointer to a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), and a stroke width of 5.</span></span> <span data-ttu-id="5410f-122">На следующем рисунке показаны выходные данные из примера кода.</span><span class="sxs-lookup"><span data-stu-id="5410f-122">The following illustration shows the output from the code example.</span></span>

![Иллюстрация эллипса](images/geometry-ovw-drawstep6.png)


```C++
ID2D1EllipseGeometry *m_pEllipseGeometry;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateEllipseGeometry(
        D2D1::Ellipse(D2D1::Point2F(100.f, 60.f), 100.f, 50.f),
        &m_pEllipseGeometry
        );
}
```




```C++
m_pRenderTarget->DrawGeometry(m_pEllipseGeometry, m_pBlackBrush, 5);
```



<span data-ttu-id="5410f-124">Чтобы нарисовать контур любой геометрии, используйте метод [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) .</span><span class="sxs-lookup"><span data-stu-id="5410f-124">To draw the outline of any geometry, use the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method.</span></span> <span data-ttu-id="5410f-125">Чтобы закрасить внутреннюю область, используйте метод [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="5410f-125">To paint its interior, use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

## <a name="path-geometries"></a><span data-ttu-id="5410f-126">Геометрические контуры</span><span class="sxs-lookup"><span data-stu-id="5410f-126">Path geometries</span></span>

<span data-ttu-id="5410f-127">Геометрические контуры представлены интерфейсом [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="5410f-127">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="5410f-128">Эти объекты можно использовать для описания сложных геометрических фигур, состоящих из сегментов, таких как дуги, кривые и линии.</span><span class="sxs-lookup"><span data-stu-id="5410f-128">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="5410f-129">На следующем рисунке показан рисунок, созданный с помощью геометрии Path.</span><span class="sxs-lookup"><span data-stu-id="5410f-129">The following illustration shows a drawing created by using path geometry.</span></span>

![Иллюстрация River, горы и Sun](images/path-geo-mnts.png)

<span data-ttu-id="5410f-131">Дополнительные сведения и примеры см. в разделе [Общие сведения о геометрических контурах](path-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5410f-131">For more information and examples, see the [Path Geometries Overview](path-geometries-overview.md).</span></span>

## <a name="composite-geometries"></a><span data-ttu-id="5410f-132">Составные геометрические объекты</span><span class="sxs-lookup"><span data-stu-id="5410f-132">Composite geometries</span></span>

<span data-ttu-id="5410f-133">Составная геометрия представляет собой геометрию, сгруппированную или объединенную с другим объектом Geometry или с преобразованием.</span><span class="sxs-lookup"><span data-stu-id="5410f-133">A composite geometry is a geometry grouped or combined with another geometry object, or with a transform.</span></span> <span data-ttu-id="5410f-134">К составным геометриям относятся объекты [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) и [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) .</span><span class="sxs-lookup"><span data-stu-id="5410f-134">Composite geometries include [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) and [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) objects.</span></span>

### <a name="geometry-groups"></a><span data-ttu-id="5410f-135">Группы Geometry</span><span class="sxs-lookup"><span data-stu-id="5410f-135">Geometry groups</span></span>

<span data-ttu-id="5410f-136">Группы geometry — это удобный способ одновременного группирования нескольких геометрических объектов, чтобы объединить все фигуры из нескольких различных геометрических объектов в одну.</span><span class="sxs-lookup"><span data-stu-id="5410f-136">Geometry groups are a convenient way to group several geometries at the same time so all figures of several distinct geometries are concatenated into one.</span></span> <span data-ttu-id="5410f-137">Чтобы создать объект [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) , вызовите метод [**Креатежеометриграуп**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) для объекта [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , передав *филлмоде* с возможными значениями в [**\_ \_ \_ альтернативном режиме D2D1 Fill**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (альтернативный вариант) и в **\_ \_ режиме D2D1 \_ Fill**, массив объектов Geometry, которые нужно добавить в группу Geometry, и число элементов в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="5410f-137">To create a [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) object, call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) method on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in the *fillMode* with possible values of [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternate) and **D2D1\_FILL\_MODE\_WINDING**, an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>

<span data-ttu-id="5410f-138">В следующем примере кода сначала объявляется массив объектов Geometry.</span><span class="sxs-lookup"><span data-stu-id="5410f-138">The following code example first declares an array of geometry objects.</span></span> <span data-ttu-id="5410f-139">Эти объекты представляют собой четыре концентрические круги, имеющие следующие радиусы: 25, 50, 75 и 100.</span><span class="sxs-lookup"><span data-stu-id="5410f-139">These objects are four concentric circles that have the following radii: 25, 50, 75, and 100.</span></span> <span data-ttu-id="5410f-140">Затем вызовите [**креатежеометриграуп**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) для объекта [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , передавая [**\_ \_ \_ альтернативный режим заполнения D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), массив объектов Geometry для добавления в группу geometry и число элементов в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="5410f-140">Then call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>


```C++
ID2D1Geometry *ppGeometries[] =
{
    m_pEllipseGeometry1,
    m_pEllipseGeometry2,
    m_pEllipseGeometry3,
    m_pEllipseGeometry4
};

hr = m_pD2DFactory->CreateGeometryGroup(
    D2D1_FILL_MODE_ALTERNATE,
    ppGeometries,
    ARRAYSIZE(ppGeometries),
    &m_pGeoGroup_AlternateFill
    );

if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateGeometryGroup(
        D2D1_FILL_MODE_WINDING,
        ppGeometries,
        ARRAYSIZE(ppGeometries),
        &m_pGeoGroup_WindingFill
        );
}
```

<span data-ttu-id="5410f-141">На следующем рисунке показаны результаты отрисовки двух геометрических объектов группы из примера.</span><span class="sxs-lookup"><span data-stu-id="5410f-141">The following illustration shows the results of rendering the two group geometries from the example.</span></span>

![Иллюстрация двух наборов из четырех концентрических кругов, один с заполненными переменными кольца и один с заполнением всех колец](images/create-geometry-group.png)

### <a name="transformed-geometries"></a><span data-ttu-id="5410f-143">Преобразованные геометрические объекты</span><span class="sxs-lookup"><span data-stu-id="5410f-143">Transformed geometries</span></span>

<span data-ttu-id="5410f-144">Существует несколько способов преобразования геометрии.</span><span class="sxs-lookup"><span data-stu-id="5410f-144">There are multiple ways to transform a geometry.</span></span> <span data-ttu-id="5410f-145">Метод [**сеттрансформ**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) целевого объекта отрисовки можно использовать для преобразования всех элементов, которые Рисует объект прорисовки, или можно связать преобразование непосредственно с геометрическим объектом с помощью метода [**Креатетрансформеджеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) для создания [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5410f-145">You can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of a render target to transform everything that the render target draws, or you can associate a transform directly with a geometry by using the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) method to create an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span></span>

<span data-ttu-id="5410f-146">Метод, который следует использовать, зависит от желаемого результата.</span><span class="sxs-lookup"><span data-stu-id="5410f-146">The method that you should use depends on the effect that you want.</span></span> <span data-ttu-id="5410f-147">При использовании целевого объекта отрисовки для преобразования и последующего отображения геометрии преобразование влияет на все сведения об объекте Geometry, включая ширину всех примененных штрихов.</span><span class="sxs-lookup"><span data-stu-id="5410f-147">When you use the render target to transform and then render a geometry, the transform affects everything about the geometry, including the width of any stroke that you have applied.</span></span> <span data-ttu-id="5410f-148">С другой стороны, при использовании [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)преобразование влияет только на координаты, описывающие фигуру.</span><span class="sxs-lookup"><span data-stu-id="5410f-148">On the other hand, when you use an [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), the transform affects only the coordinates that describe the shape.</span></span> <span data-ttu-id="5410f-149">Преобразование не повлияет на толщину штриха при прорисовке геометрии.</span><span class="sxs-lookup"><span data-stu-id="5410f-149">The transformation will not affect the stroke thickness when the geometry is drawn.</span></span>

> [!Note]  
> <span data-ttu-id="5410f-150">Начиная с Windows 8, универсальное преобразование не повлияет на толщину штриха в штрихах с [**\_ \_ \_ \_ фиксированным**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)преобразованием типа D2D1 или [**D2D1 \_ Stroke \_ \_ \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span><span class="sxs-lookup"><span data-stu-id="5410f-150">Starting with Windows 8 the world transform will not affect the stroke thickness of strokes with [**D2D1\_STROKE\_TRANSFORM\_TYPE\_FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)or [**D2D1\_STROKE\_TRANSFORM\_TYPE\_HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span></span> <span data-ttu-id="5410f-151">Эти типы преобразования следует использовать для преобразования независимых штрихов</span><span class="sxs-lookup"><span data-stu-id="5410f-151">You should use these transform types to achieve transform independent strokes</span></span>

 

<span data-ttu-id="5410f-152">В следующем примере создается [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), а затем рисуется без его преобразования.</span><span class="sxs-lookup"><span data-stu-id="5410f-152">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), then draws it without transforming it.</span></span> <span data-ttu-id="5410f-153">Он создает выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="5410f-153">It produces the output shown in the following illustration.</span></span>

![Иллюстрация прямоугольника](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```




```C++
// Draw the untransformed rectangle geometry.
m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="5410f-155">В следующем примере используется целевой объект отрисовки для масштабирования геометрии по коэффициенту 3, после чего рисуется.</span><span class="sxs-lookup"><span data-stu-id="5410f-155">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="5410f-156">На следующем рисунке показан результат рисования прямоугольника без преобразования и преобразования.</span><span class="sxs-lookup"><span data-stu-id="5410f-156">The following illustration shows the result of drawing the rectangle without the transform and with the transform.</span></span> <span data-ttu-id="5410f-157">Обратите внимание, что после преобразования штрих становится толще, несмотря на то, что толщина штриха равна 1.</span><span class="sxs-lookup"><span data-stu-id="5410f-157">Notice that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![Рисунок меньшего прямоугольника внутри более крупного прямоугольника с толстой обводкой](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="5410f-159">В следующем примере используется метод [**креатетрансформеджеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) для масштабирования геометрии по коэффициенту 3, после чего рисуется.</span><span class="sxs-lookup"><span data-stu-id="5410f-159">The next example uses the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="5410f-160">Он создает выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="5410f-160">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="5410f-161">Обратите внимание, что, хотя размер прямоугольника больше, его штрих не увеличился.</span><span class="sxs-lookup"><span data-stu-id="5410f-161">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![Рисунок меньшего прямоугольника внутри более крупного прямоугольника с одинаковой толщиной обводки](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );
```




```C++
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```



## <a name="geometries-as-masks"></a><span data-ttu-id="5410f-163">Геометрические объекты как маски</span><span class="sxs-lookup"><span data-stu-id="5410f-163">Geometries as masks</span></span>

<span data-ttu-id="5410f-164">Вы можете использовать объект [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) в качестве геометрической маски при вызове метода [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="5410f-164">You can use an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object as a geometric mask when you call the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="5410f-165">Геометрическая маска задает область слоя, которая является составной для целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="5410f-165">The geometric mask specifies the area of the layer that is composited into the render target.</span></span> <span data-ttu-id="5410f-166">Дополнительные сведения см. в разделе геометрические маски в [обзоре слоев](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5410f-166">For more information, see the Geometric Masks section of the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="geometric-operations"></a><span data-ttu-id="5410f-167">Геометрические операции</span><span class="sxs-lookup"><span data-stu-id="5410f-167">Geometric operations</span></span>

<span data-ttu-id="5410f-168">Интерфейс [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) предоставляет несколько геометрических операций, которые можно использовать для обработки и измерения геометрических значений.</span><span class="sxs-lookup"><span data-stu-id="5410f-168">The [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) interface provides several geometric operations that you can use to manipulate and measure geometric figures.</span></span> <span data-ttu-id="5410f-169">Например, их можно использовать для вычисления и возврата их границ, сравнения, чтобы увидеть, как одна геометрия является пространственно связанной с другой (полезна для проверки попадания), вычислите области и длины и многое другое.</span><span class="sxs-lookup"><span data-stu-id="5410f-169">For example, you can use them to calculate and return their bounds, compare to see how one geometry is spatially related to another (useful for hit testing), calculate the areas and lengths, and more.</span></span> <span data-ttu-id="5410f-170">В следующей таблице описаны общие геометрические операции.</span><span class="sxs-lookup"><span data-stu-id="5410f-170">The following table describes the common geometric operations.</span></span>



| <span data-ttu-id="5410f-171">Операция</span><span class="sxs-lookup"><span data-stu-id="5410f-171">Operation</span></span>                                                   | <span data-ttu-id="5410f-172">Метод</span><span class="sxs-lookup"><span data-stu-id="5410f-172">Method</span></span>                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5410f-173">Объединить</span><span class="sxs-lookup"><span data-stu-id="5410f-173">Combine</span></span>                                                     | [<span data-ttu-id="5410f-174">**комбиневисжеометри**</span><span class="sxs-lookup"><span data-stu-id="5410f-174">**CombineWithGeometry**</span></span>](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| <span data-ttu-id="5410f-175">Границы/расширенные границы/границы извлечения, обновление "грязной" области</span><span class="sxs-lookup"><span data-stu-id="5410f-175">Bounds/ Widened Bounds/Retrieve Bounds, Dirty Region update</span></span> | <span data-ttu-id="5410f-176">[**Расширяющие**](id2d1geometry-widen.md), [**привязку**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**жетвиденедбаундс**](id2d1geometry-getwidenedbounds.md)</span><span class="sxs-lookup"><span data-stu-id="5410f-176">[**Widen**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span></span>                             |
| <span data-ttu-id="5410f-177">Проверка нажатия</span><span class="sxs-lookup"><span data-stu-id="5410f-177">Hit Testing</span></span>                                                 | <span data-ttu-id="5410f-178">[**Филлконтаинспоинт**](id2d1geometry-fillcontainspoint.md), [ **строкеконтаинспоинт**](id2d1geometry-strokecontainspoint.md)</span><span class="sxs-lookup"><span data-stu-id="5410f-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span></span>                                             |
| <span data-ttu-id="5410f-179">Stroke</span><span class="sxs-lookup"><span data-stu-id="5410f-179">Stroke</span></span>                                                      | [<span data-ttu-id="5410f-180">**строкеконтаинспоинт**</span><span class="sxs-lookup"><span data-stu-id="5410f-180">**StrokeContainsPoint**</span></span>](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| <span data-ttu-id="5410f-181">Сравнение</span><span class="sxs-lookup"><span data-stu-id="5410f-181">Comparison</span></span>                                                  | [<span data-ttu-id="5410f-182">**компаревисжеометри**</span><span class="sxs-lookup"><span data-stu-id="5410f-182">**CompareWithGeometry**</span></span>](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| <span data-ttu-id="5410f-183">Упрощение (удаление дуг и квадратичных кривых Безье)</span><span class="sxs-lookup"><span data-stu-id="5410f-183">Simplification (removes arcs and quadratic Bezier curves)</span></span>   | [<span data-ttu-id="5410f-184">**Целях**</span><span class="sxs-lookup"><span data-stu-id="5410f-184">**Simplify**</span></span>](id2d1geometry-simplify.md)                                                                                                                                 |
| <span data-ttu-id="5410f-185">Тесселяция</span><span class="sxs-lookup"><span data-stu-id="5410f-185">Tessellation</span></span>                                                | [<span data-ttu-id="5410f-186">**Проводить тесселяцию**</span><span class="sxs-lookup"><span data-stu-id="5410f-186">**Tessellate**</span></span>](id2d1geometry-tessellate.md)                                                                                                                             |
| <span data-ttu-id="5410f-187">Структура (удалить пересечение)</span><span class="sxs-lookup"><span data-stu-id="5410f-187">Outline (remove intersection)</span></span>                               | [<span data-ttu-id="5410f-188">**Контур**</span><span class="sxs-lookup"><span data-stu-id="5410f-188">**Outline**</span></span>](id2d1geometry-outline.md)                                                                                                                                   |
| <span data-ttu-id="5410f-189">Вычисление области или длины геометрии</span><span class="sxs-lookup"><span data-stu-id="5410f-189">Calculate the area or length of a geometry</span></span>                  | <span data-ttu-id="5410f-190">[**Компутеареа**](id2d1geometry-computearea.md), [**компутеленгс**](id2d1geometry-computelength.md), [**компутепоинтатленгс**](id2d1geometry-computepointatlength.md)</span><span class="sxs-lookup"><span data-stu-id="5410f-190">[**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span></span> |



 

> [!Note]  
> <span data-ttu-id="5410f-191">Начиная с Windows 8, можно использовать метод [**компутепоинтандсегментатленгс**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) в [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) для вычисления области или длины геометрии.</span><span class="sxs-lookup"><span data-stu-id="5410f-191">Starting in Windows 8, you can use the [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) method on the [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) to calculate the area or length of a geometry.</span></span>

 

### <a name="combining-geometries"></a><span data-ttu-id="5410f-192">Объединение геометрических объектов</span><span class="sxs-lookup"><span data-stu-id="5410f-192">Combining geometries</span></span>

<span data-ttu-id="5410f-193">Чтобы объединить одну геометрию с другой, вызовите метод [**ID2D1Geometry:: комбиневисжеометри**](id2d1geometry-combinewithgeometry.md) .</span><span class="sxs-lookup"><span data-stu-id="5410f-193">To combine one geometry with another, call the [**ID2D1Geometry::CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) method.</span></span> <span data-ttu-id="5410f-194">При объединении геометрических объектов необходимо указать один из четырех способов выполнения операции объединения: D2D1 объединение [**\_ \_ режима \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) объединения (Union), [**D2D1 \_ \_ \_ Intersect**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Intersect), [**D2D1 \_ \_ режим объединения \_ XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (XOR) и [**\_ режим объединения D2D1 \_ \_ Exclude**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (исключить).</span><span class="sxs-lookup"><span data-stu-id="5410f-194">When you combine the geometries, you specify one of the four ways to perform the combine operation: [**D2D1\_COMBINE\_MODE\_UNION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (union), [**D2D1\_COMBINE\_MODE\_INTERSECT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (intersect), [**D2D1\_COMBINE\_MODE\_XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (xor), and [**D2D1\_COMBINE\_MODE\_EXCLUDE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (exclude).</span></span> <span data-ttu-id="5410f-195">В следующем примере кода показаны два круга, Объединенные с использованием режима объединения UNION, где первый круг имеет центральную точку (75, 75) и радиус 50, а второй круг — Центральная точка (125, 75) и радиус для 50.</span><span class="sxs-lookup"><span data-stu-id="5410f-195">The following code example shows two circles that are combined by using the union combine mode, where the first circle has the center point of (75, 75) and the radius of 50, and the second circle has the center point of (125, 75) and the radius of 50.</span></span>


```C++
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
```



<span data-ttu-id="5410f-196">На следующем рисунке показаны два круга в сочетании с режимом объединения UNION.</span><span class="sxs-lookup"><span data-stu-id="5410f-196">The following illustration shows two circles combined with a combine mode of union.</span></span>

![Иллюстрация двух перекрывающихся кругов, Объединенных в объединение](images/combine-mode-union.png)

<span data-ttu-id="5410f-198">Иллюстрации всех режимов объединения см. в разделе [**\_ \_ перечисление режима объединения D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span><span class="sxs-lookup"><span data-stu-id="5410f-198">For illustrations of all the combine modes, see the [**D2D1\_COMBINE\_MODE enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span></span>

### <a name="widen"></a><span data-ttu-id="5410f-199">Расширяет</span><span class="sxs-lookup"><span data-stu-id="5410f-199">Widen</span></span>

<span data-ttu-id="5410f-200">Метод [**Widening**](id2d1geometry-widen.md) создает новую геометрию, заливка которой эквивалентна обводки существующей геометрии, а затем записывает результат в указанный объект [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) .</span><span class="sxs-lookup"><span data-stu-id="5410f-200">The [**Widen**](id2d1geometry-widen.md) method generates a new geometry whose fill is equivalent to stroking the existing geometry, and then writes the result to the specified [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) object.</span></span> <span data-ttu-id="5410f-201">В следующем примере кода вызывается метод [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) для объекта [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="5410f-201">The following code example calls [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) on the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object.</span></span> <span data-ttu-id="5410f-202">Если операция **Open** выполнена, она вызывает **расширение** для объекта Geometry.</span><span class="sxs-lookup"><span data-stu-id="5410f-202">If **Open** succeeds, it calls **Widen** on the geometry object.</span></span>


```C++
ID2D1GeometrySink *pGeometrySink = NULL;
hr = pPathGeometry->Open(&pGeometrySink);
if (SUCCEEDED(hr))
{
    hr = pGeometry->Widen(
            strokeWidth,
            pIStrokeStyle,
            pWorldTransform,
            pGeometrySink
            );
```



### <a name="tessellate"></a><span data-ttu-id="5410f-203">Проводить тесселяцию</span><span class="sxs-lookup"><span data-stu-id="5410f-203">Tessellate</span></span>

<span data-ttu-id="5410f-204">Метод [**тесселяции**](id2d1geometry-tessellate.md) создает набор треугольников с отсчетом по часовой стрелке, охватывающий геометрию после преобразования, используя указанную матрицу и плоскую с использованием заданного значения допуска.</span><span class="sxs-lookup"><span data-stu-id="5410f-204">The [**Tessellate**](id2d1geometry-tessellate.md) method creates a set of clockwise-wound triangles that cover the geometry after it is transformed by using the specified matrix and flattened by using the specified tolerance.</span></span> <span data-ttu-id="5410f-205">В следующем примере кода используется **тесселяция** для создания списка треугольников, представляющих *ппасжеометри*.</span><span class="sxs-lookup"><span data-stu-id="5410f-205">The following code example uses **Tessellate** to create a list of triangles that represent *pPathGeometry*.</span></span> <span data-ttu-id="5410f-206">Треугольники хранятся в [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *пмеш*, а затем передаются в член класса *m \_ пстрокемеш* для последующего использования при отрисовке.</span><span class="sxs-lookup"><span data-stu-id="5410f-206">The triangles are stored in an [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, then transferred to a class member, *m\_pStrokeMesh*, for later use when rendering.</span></span>


```C++
ID2D1Mesh *pMesh = NULL;
hr = m_pRT->CreateMesh(&pMesh);
if (SUCCEEDED(hr))
{
    ID2D1TessellationSink *pSink = NULL;
    hr = pMesh->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Tessellate(
                NULL, // world transform (already handled in Widen)
                pSink
                );
        if (SUCCEEDED(hr))
        {
            hr = pSink->Close();
            if (SUCCEEDED(hr))
            {
                SafeReplace(&m_pStrokeMesh, pMesh);
            }
        }
        pSink->Release();
    }
    pMesh->Release();
}
```



### <a name="fillcontainspoint-and-strokecontainspoint"></a><span data-ttu-id="5410f-207">Филлконтаинспоинт и Строкеконтаинспоинт</span><span class="sxs-lookup"><span data-stu-id="5410f-207">FillContainsPoint and StrokeContainsPoint</span></span>

<span data-ttu-id="5410f-208">Метод [**филлконтаинспоинт**](id2d1geometry-fillcontainspoint.md) указывает, содержит ли область, заполненную геометрией, указанную точку.</span><span class="sxs-lookup"><span data-stu-id="5410f-208">The [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) method indicates whether the area filled by the geometry contains the specified point.</span></span> <span data-ttu-id="5410f-209">Этот метод можно использовать для проверки нажатия.</span><span class="sxs-lookup"><span data-stu-id="5410f-209">You can use this method to do hit testing.</span></span> <span data-ttu-id="5410f-210">Следующий пример кода вызывает **филлконтаинспоинт** для объекта [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , передавая точку в (0, 0) и матрицу [**идентификаторов**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) .</span><span class="sxs-lookup"><span data-stu-id="5410f-210">The following code example calls **FillContainsPoint** on an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) object, passing in a point at (0,0) and an [**Identity**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) matrix.</span></span>


```C++
BOOL containsPoint1;
hr = m_pCircleGeometry1->FillContainsPoint(
    D2D1::Point2F(0,0),
    D2D1::Matrix3x2F::Identity(),
    &containsPoint1
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



<span data-ttu-id="5410f-211">Метод [**строкеконтаинспоинт**](id2d1geometry-strokecontainspoint.md) определяет, содержит ли штрих геометрии указанную точку.</span><span class="sxs-lookup"><span data-stu-id="5410f-211">The [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) method determines whether the geometry's stroke contains the specified point.</span></span> <span data-ttu-id="5410f-212">Этот метод можно использовать для проверки нажатия.</span><span class="sxs-lookup"><span data-stu-id="5410f-212">You can use this method to do hit testing.</span></span> <span data-ttu-id="5410f-213">В следующем примере кода используется **строкеконтаинспоинт**.</span><span class="sxs-lookup"><span data-stu-id="5410f-213">The following code example uses **StrokeContainsPoint**.</span></span>


```C++
BOOL containsPoint;

hr = m_pCircleGeometry1->StrokeContainsPoint(
    D2D1::Point2F(0,0),
    10,     // stroke width
    NULL,   // stroke style
    NULL,   // world transform
    &containsPoint
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



### <a name="simplify"></a><span data-ttu-id="5410f-214">Упрощение </span><span class="sxs-lookup"><span data-stu-id="5410f-214">Simplify</span></span>

<span data-ttu-id="5410f-215">Метод [**упростит**](id2d1geometry-simplify.md) удаляет дуги и квадратичные кривые Безье из заданной геометрии.</span><span class="sxs-lookup"><span data-stu-id="5410f-215">The [**Simplify**](id2d1geometry-simplify.md) method removes arcs and quadratic Bezier curves from a specified geometry.</span></span> <span data-ttu-id="5410f-216">Таким образом, полученная геометрия содержит только строки и, при необходимости, кубические кривые Безье.</span><span class="sxs-lookup"><span data-stu-id="5410f-216">So, the resulting geometry contains only lines and, optionally, cubic Bezier curves.</span></span> <span data-ttu-id="5410f-217">В следующем примере кода **упрощено** используется для преобразования геометрии с кривыми Безье в геометрию, содержащую только сегменты линий.</span><span class="sxs-lookup"><span data-stu-id="5410f-217">The following code example uses **Simplify** to transform a geometry with Bezier curves into a geometry that contains only line segments.</span></span>


```C++
HRESULT D2DFlatten(
    ID2D1Geometry *pGeometry,
    float flatteningTolerance,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES,
                    NULL, // world transform
                    flatteningTolerance,
                    pSink
                    );

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="computelength-and-computearea"></a><span data-ttu-id="5410f-218">Компутеленгс и Компутеареа</span><span class="sxs-lookup"><span data-stu-id="5410f-218">ComputeLength and ComputeArea</span></span>

<span data-ttu-id="5410f-219">Метод [**компутеленгс**](id2d1geometry-computelength.md) вычисляет длину указанной геометрии, если каждый сегмент был отменен в строке.</span><span class="sxs-lookup"><span data-stu-id="5410f-219">The [**ComputeLength**](id2d1geometry-computelength.md) method calculates the length of the specified geometry if each segment were unrolled into a line.</span></span> <span data-ttu-id="5410f-220">Это включает неявный заключительный сегмент, если геометрическая геометрия закрыта.</span><span class="sxs-lookup"><span data-stu-id="5410f-220">This includes the implicit closing segment if the geometry is closed.</span></span> <span data-ttu-id="5410f-221">В следующем примере кода используется **компутеленгс** для расчета длины указанного круга (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="5410f-221">The following code example uses **ComputeLength** to compute the length of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float length;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeLength(
    D2D1::IdentityMatrix(),
    &length
    );

if (SUCCEEDED(hr))
{
    // Process the length of the geometry.
}
```



<span data-ttu-id="5410f-222">Метод [**компутеареа**](id2d1geometry-computearea.md) вычисляет область заданного геометрического объекта.</span><span class="sxs-lookup"><span data-stu-id="5410f-222">The [**ComputeArea**](id2d1geometry-computearea.md) method calculates the area of the specified geometry.</span></span> <span data-ttu-id="5410f-223">В следующем примере кода используется **компутеареа** для вычислить площадь указанного круга (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="5410f-223">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a><span data-ttu-id="5410f-224">компаревисжеометри</span><span class="sxs-lookup"><span data-stu-id="5410f-224">CompareWithGeometry</span></span>

<span data-ttu-id="5410f-225">Метод [**компаревисжеометри**](id2d1geometry-comparewithgeometry.md) описывает пересечение между геометрическим объектом, который вызывает этот метод, и заданной геометрией.</span><span class="sxs-lookup"><span data-stu-id="5410f-225">The [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) method describes the intersection between the geometry that calls this method and the specified geometry.</span></span> <span data-ttu-id="5410f-226">Возможные значения пересечения включают несвязанное [**D2D1 \_ Геометрическое отношение (содержит \_ несвязное \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) ), Геометрическое отношение D2D1 содержится (содержится), **D2D1 \_ геометрическая \_ связь \_ содержит** (Contains) и **\_ \_ \_ Перекрытие геометрической связи** . **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5410f-226">The possible values for intersection include [**D2D1\_GEOMETRY\_RELATION\_DISJOINT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (disjoint), **D2D1\_GEOMETRY\_RELATION\_IS\_CONTAINED** (is contained), **D2D1\_GEOMETRY\_RELATION\_CONTAINS** (contains), and **D2D1\_GEOMETRY\_RELATION\_OVERLAP** (overlap).</span></span> <span data-ttu-id="5410f-227">"несвязанный" означает, что две геометрические заливки не пересекаются.</span><span class="sxs-lookup"><span data-stu-id="5410f-227">"disjoint" means that two geometry fills do not intersect at all.</span></span> <span data-ttu-id="5410f-228">"содержится" означает, что геометрия полностью содержится в указанной геометрии.</span><span class="sxs-lookup"><span data-stu-id="5410f-228">"is contained" means that the geometry is completely contained by the specified geometry.</span></span> <span data-ttu-id="5410f-229">"Contains" означает, что геометрия полностью содержит указанную геометрию, а "перекрытие" означает перекрытие двух геометрических объектов, но ни одно из них не полностью содержит другое.</span><span class="sxs-lookup"><span data-stu-id="5410f-229">"contains" means that the geometry completely contains the specified geometry, and "overlap" means the two geometries overlap but neither completely contains the other.</span></span>

<span data-ttu-id="5410f-230">В следующем примере кода показано, как сравнить два круга с одинаковым радиусом 50, но они смещены на 50.</span><span class="sxs-lookup"><span data-stu-id="5410f-230">The following code example shows how to compare two circles that have the same radius of 50 but are offset by 50.</span></span>


```C++
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

```




```C++
D2D1_GEOMETRY_RELATION result = D2D1_GEOMETRY_RELATION_UNKNOWN;

// Compare circle1 with circle2
hr = m_pCircleGeometry1->CompareWithGeometry(
    m_pCircleGeometry2,
    D2D1::IdentityMatrix(),
    0.1f,
    &result
    );

if (SUCCEEDED(hr))
{
    static const WCHAR szGeometryRelation[] = L"Two circles overlap.";
    m_pRenderTarget->SetTransform(D2D1::IdentityMatrix());
    if (result == D2D1_GEOMETRY_RELATION_OVERLAP)
    {
        m_pRenderTarget->DrawText(
            szGeometryRelation,
            ARRAYSIZE(szGeometryRelation) - 1,
            m_pTextFormat,
            D2D1::RectF(25.0f, 160.0f, 200.0f, 300.0f),
            m_pTextBrush
            );
    }
}
```



### <a name="outline"></a><span data-ttu-id="5410f-231">Контур</span><span class="sxs-lookup"><span data-stu-id="5410f-231">Outline</span></span>

<span data-ttu-id="5410f-232">Метод [**структуры**](id2d1geometry-outline.md) определяет контур геометрии (версию геометрии, в которой никакая фигура не пересекает саму себя или другие фигуры) и записывает результат в [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span><span class="sxs-lookup"><span data-stu-id="5410f-232">The [**Outline**](id2d1geometry-outline.md) method computes the outline of the geometry (a version of the geometry in which no figure crosses itself or any other figure) and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span> <span data-ttu-id="5410f-233">В следующем примере кода используется **Структура** для создания эквивалентной геометрии без каких-либо самостоятельных подразделов.</span><span class="sxs-lookup"><span data-stu-id="5410f-233">The following code example uses **Outline** to construct an equivalent geometry without any self-intersections.</span></span> <span data-ttu-id="5410f-234">В нем используется допуск плоской обработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5410f-234">It uses the default flattening tolerance.</span></span>


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="getbounds-and-getwidenedbounds"></a><span data-ttu-id="5410f-235">Привязкой и Жетвиденедбаундс</span><span class="sxs-lookup"><span data-stu-id="5410f-235">GetBounds and GetWidenedBounds</span></span>

<span data-ttu-id="5410f-236">Метод [**Bounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) Извлекает границы геометрии.</span><span class="sxs-lookup"><span data-stu-id="5410f-236">The [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) method retrieves the bounds of the geometry.</span></span> <span data-ttu-id="5410f-237">В следующем примере **кода используются методические границы для** получения границ заданного круга (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="5410f-237">The following code example uses **GetBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
D2D1_RECT_F bounds;

hr = m_pCircleGeometry1->GetBounds(
      D2D1::IdentityMatrix(),
      &bounds
     );

if (SUCCEEDED(hr))
{
    // Retrieve the bounds.
}
```



<span data-ttu-id="5410f-238">Метод [**жетвиденедбаундс**](id2d1geometry-getwidenedbounds.md) Извлекает границы геометрии после его расширения с помощью заданной ширины и стиля штриха и преобразуется указанной матрицей.</span><span class="sxs-lookup"><span data-stu-id="5410f-238">The [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) method retrieves the bounds of the geometry after it is widened by the specified stroke width and style and transformed by the specified matrix.</span></span> <span data-ttu-id="5410f-239">В следующем примере кода используется **жетвиденедбаундс** для получения границ заданного круга (**m \_ pCircleGeometry1**) после его расширения по заданной толщине штрихов.</span><span class="sxs-lookup"><span data-stu-id="5410f-239">The following code example uses **GetWidenedBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**) after it is widened by the specified stroke width.</span></span>


```C++
float dashes[] = {1.f, 1.f, 2.f, 3.f, 5.f};

m_pD2DFactory->CreateStrokeStyle(
    D2D1::StrokeStyleProperties(
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_ROUND,
        D2D1_LINE_JOIN_ROUND,   // lineJoin
        10.f,   //miterLimit
        D2D1_DASH_STYLE_CUSTOM,
        0.f     //dashOffset
        ),
     dashes,
     ARRAYSIZE(dashes)-1,
     &m_pStrokeStyle
     );
```




```C++
D2D1_RECT_F bounds1;
hr = m_pCircleGeometry1->GetWidenedBounds(
      5.0,
      m_pStrokeStyle,
      D2D1::IdentityMatrix(),
      &bounds1
     );
if (SUCCEEDED(hr))
{
    // Retrieve the widened bounds.
}
```



### <a name="computepointatlength"></a><span data-ttu-id="5410f-240">компутепоинтатленгс</span><span class="sxs-lookup"><span data-stu-id="5410f-240">ComputePointAtLength</span></span>

<span data-ttu-id="5410f-241">Метод [**компутепоинтатленгс**](id2d1geometry-computepointatlength.md) вычисляет точку и вектор касательных на заданном расстоянии вдоль геометрии.</span><span class="sxs-lookup"><span data-stu-id="5410f-241">The [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) method calculates the point and tangent vector at the specified distance along the geometry.</span></span> <span data-ttu-id="5410f-242">В следующем примере кода используется **компутепоинтатленгс**.</span><span class="sxs-lookup"><span data-stu-id="5410f-242">The following code example uses **ComputePointAtLength**.</span></span>


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a><span data-ttu-id="5410f-243">См. также</span><span class="sxs-lookup"><span data-stu-id="5410f-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5410f-244">Общие сведения о геометрических контурах</span><span class="sxs-lookup"><span data-stu-id="5410f-244">Path Geometries Overview</span></span>](path-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="5410f-245">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="5410f-245">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 