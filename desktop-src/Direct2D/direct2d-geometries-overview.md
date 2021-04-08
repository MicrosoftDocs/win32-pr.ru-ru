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
# <a name="geometries-overview"></a>Обзор геометрий 

В этом обзоре описывается создание и использование объектов [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) для определения двумерных иллюстраций и управления ими. В него входят следующие разделы.

## <a name="what-is-a-direct2d-geometry"></a>Что такое Direct2D Geometry?

Direct2D геометрия — это объект [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) . Это может быть простой геометрический объект ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)или [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), геометрическая траектория ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) или составная геометрия ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) и [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).

Геометрические объекты Direct2D позволяют описывать двухмерные цифры и предлагают множество применений, например определение областей проверки попадания, областей клипов и даже путей анимации.

Геометрические объекты Direct2D являются неизменяемыми и аппаратно-независимыми ресурсами, созданными [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory). Как правило, необходимо создавать геометрические объекты один раз и хранить их на протяжении всего жизненного цикла приложения или до их изменения. Дополнительные сведения о аппаратно-независимых и аппаратно зависимых ресурсах см. в разделе [Общие сведения о ресурсах](resources-and-resource-domains.md).

В следующих разделах описываются различные виды геометрических объектов.

## <a name="simple-geometries"></a>Простые геометрические объекты

Простые геометрические объекты включают [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)и [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , и их можно использовать для создания базовых геометрических фигур, таких как прямоугольники, скругленные прямоугольники, круги и эллипсы.

Чтобы создать простую геометрию, используйте один из методов [**ID2D1Factory:: create<*Жеометритипе*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) . Эти методы создают объект указанного типа. Например, чтобы создать прямоугольник, вызовите метод [**ID2D1Factory:: креатеректанглежеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), который возвращает объект [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) . чтобы создать скругленный прямоугольник, вызовите метод [**ID2D1Factory:: креатераундедректанглежеометри**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), который возвращает объект [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) и т. д.

В следующем примере кода вызывается метод [**креатиллипсежеометри**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) , который передается в виде эллипса с *центром* , имеющим значение (100, 100), *x-RADIUS —* 100, а *y — RADIUS —* 50. Затем он вызывает [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), передавая полученную геометрию эллипса, указатель на черный [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)и толщину штриха, равную 5. На следующем рисунке показаны выходные данные из примера кода.

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



Чтобы нарисовать контур любой геометрии, используйте метод [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) . Чтобы закрасить внутреннюю область, используйте метод [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .

## <a name="path-geometries"></a>Геометрические контуры

Геометрические контуры представлены интерфейсом [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Эти объекты можно использовать для описания сложных геометрических фигур, состоящих из сегментов, таких как дуги, кривые и линии. На следующем рисунке показан рисунок, созданный с помощью геометрии Path.

![Иллюстрация River, горы и Sun](images/path-geo-mnts.png)

Дополнительные сведения и примеры см. в разделе [Общие сведения о геометрических контурах](path-geometries-overview.md).

## <a name="composite-geometries"></a>Составные геометрические объекты

Составная геометрия представляет собой геометрию, сгруппированную или объединенную с другим объектом Geometry или с преобразованием. К составным геометриям относятся объекты [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) и [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) .

### <a name="geometry-groups"></a>Группы Geometry

Группы geometry — это удобный способ одновременного группирования нескольких геометрических объектов, чтобы объединить все фигуры из нескольких различных геометрических объектов в одну. Чтобы создать объект [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) , вызовите метод [**Креатежеометриграуп**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) для объекта [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , передав *филлмоде* с возможными значениями в [**\_ \_ \_ альтернативном режиме D2D1 Fill**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (альтернативный вариант) и в **\_ \_ режиме D2D1 \_ Fill**, массив объектов Geometry, которые нужно добавить в группу Geometry, и число элементов в этом массиве.

В следующем примере кода сначала объявляется массив объектов Geometry. Эти объекты представляют собой четыре концентрические круги, имеющие следующие радиусы: 25, 50, 75 и 100. Затем вызовите [**креатежеометриграуп**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) для объекта [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , передавая [**\_ \_ \_ альтернативный режим заполнения D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), массив объектов Geometry для добавления в группу geometry и число элементов в этом массиве.


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

На следующем рисунке показаны результаты отрисовки двух геометрических объектов группы из примера.

![Иллюстрация двух наборов из четырех концентрических кругов, один с заполненными переменными кольца и один с заполнением всех колец](images/create-geometry-group.png)

### <a name="transformed-geometries"></a>Преобразованные геометрические объекты

Существует несколько способов преобразования геометрии. Метод [**сеттрансформ**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) целевого объекта отрисовки можно использовать для преобразования всех элементов, которые Рисует объект прорисовки, или можно связать преобразование непосредственно с геометрическим объектом с помощью метода [**Креатетрансформеджеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) для создания [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).

Метод, который следует использовать, зависит от желаемого результата. При использовании целевого объекта отрисовки для преобразования и последующего отображения геометрии преобразование влияет на все сведения об объекте Geometry, включая ширину всех примененных штрихов. С другой стороны, при использовании [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)преобразование влияет только на координаты, описывающие фигуру. Преобразование не повлияет на толщину штриха при прорисовке геометрии.

> [!Note]  
> Начиная с Windows 8, универсальное преобразование не повлияет на толщину штриха в штрихах с [**\_ \_ \_ \_ фиксированным**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)преобразованием типа D2D1 или [**D2D1 \_ Stroke \_ \_ \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type). Эти типы преобразования следует использовать для преобразования независимых штрихов

 

В следующем примере создается [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), а затем рисуется без его преобразования. Он создает выходные данные, показанные на следующем рисунке.

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



В следующем примере используется целевой объект отрисовки для масштабирования геометрии по коэффициенту 3, после чего рисуется. На следующем рисунке показан результат рисования прямоугольника без преобразования и преобразования. Обратите внимание, что после преобразования штрих становится толще, несмотря на то, что толщина штриха равна 1.

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



В следующем примере используется метод [**креатетрансформеджеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) для масштабирования геометрии по коэффициенту 3, после чего рисуется. Он создает выходные данные, показанные на следующем рисунке. Обратите внимание, что, хотя размер прямоугольника больше, его штрих не увеличился.

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



## <a name="geometries-as-masks"></a>Геометрические объекты как маски

Вы можете использовать объект [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) в качестве геометрической маски при вызове метода [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) . Геометрическая маска задает область слоя, которая является составной для целевого объекта рендеринга. Дополнительные сведения см. в разделе геометрические маски в [обзоре слоев](direct2d-layers-overview.md).

## <a name="geometric-operations"></a>Геометрические операции

Интерфейс [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) предоставляет несколько геометрических операций, которые можно использовать для обработки и измерения геометрических значений. Например, их можно использовать для вычисления и возврата их границ, сравнения, чтобы увидеть, как одна геометрия является пространственно связанной с другой (полезна для проверки попадания), вычислите области и длины и многое другое. В следующей таблице описаны общие геометрические операции.



| Операция                                                   | Метод                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Объединить                                                     | [**комбиневисжеометри**](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| Границы/расширенные границы/границы извлечения, обновление "грязной" области | [**Расширяющие**](id2d1geometry-widen.md), [**привязку**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**жетвиденедбаундс**](id2d1geometry-getwidenedbounds.md)                             |
| Проверка нажатия                                                 | [**Филлконтаинспоинт**](id2d1geometry-fillcontainspoint.md), [ **строкеконтаинспоинт**](id2d1geometry-strokecontainspoint.md)                                             |
| Stroke                                                      | [**строкеконтаинспоинт**](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| Сравнение                                                  | [**компаревисжеометри**](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| Упрощение (удаление дуг и квадратичных кривых Безье)   | [**Целях**](id2d1geometry-simplify.md)                                                                                                                                 |
| Тесселяция                                                | [**Проводить тесселяцию**](id2d1geometry-tessellate.md)                                                                                                                             |
| Структура (удалить пересечение)                               | [**Контур**](id2d1geometry-outline.md)                                                                                                                                   |
| Вычисление области или длины геометрии                  | [**Компутеареа**](id2d1geometry-computearea.md), [**компутеленгс**](id2d1geometry-computelength.md), [**компутепоинтатленгс**](id2d1geometry-computepointatlength.md) |



 

> [!Note]  
> Начиная с Windows 8, можно использовать метод [**компутепоинтандсегментатленгс**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) в [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) для вычисления области или длины геометрии.

 

### <a name="combining-geometries"></a>Объединение геометрических объектов

Чтобы объединить одну геометрию с другой, вызовите метод [**ID2D1Geometry:: комбиневисжеометри**](id2d1geometry-combinewithgeometry.md) . При объединении геометрических объектов необходимо указать один из четырех способов выполнения операции объединения: D2D1 объединение [**\_ \_ режима \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) объединения (Union), [**D2D1 \_ \_ \_ Intersect**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Intersect), [**D2D1 \_ \_ режим объединения \_ XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (XOR) и [**\_ режим объединения D2D1 \_ \_ Exclude**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (исключить). В следующем примере кода показаны два круга, Объединенные с использованием режима объединения UNION, где первый круг имеет центральную точку (75, 75) и радиус 50, а второй круг — Центральная точка (125, 75) и радиус для 50.


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



На следующем рисунке показаны два круга в сочетании с режимом объединения UNION.

![Иллюстрация двух перекрывающихся кругов, Объединенных в объединение](images/combine-mode-union.png)

Иллюстрации всех режимов объединения см. в разделе [**\_ \_ перечисление режима объединения D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).

### <a name="widen"></a>Расширяет

Метод [**Widening**](id2d1geometry-widen.md) создает новую геометрию, заливка которой эквивалентна обводки существующей геометрии, а затем записывает результат в указанный объект [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) . В следующем примере кода вызывается метод [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) для объекта [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Если операция **Open** выполнена, она вызывает **расширение** для объекта Geometry.


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



### <a name="tessellate"></a>Проводить тесселяцию

Метод [**тесселяции**](id2d1geometry-tessellate.md) создает набор треугольников с отсчетом по часовой стрелке, охватывающий геометрию после преобразования, используя указанную матрицу и плоскую с использованием заданного значения допуска. В следующем примере кода используется **тесселяция** для создания списка треугольников, представляющих *ппасжеометри*. Треугольники хранятся в [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *пмеш*, а затем передаются в член класса *m \_ пстрокемеш* для последующего использования при отрисовке.


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



### <a name="fillcontainspoint-and-strokecontainspoint"></a>Филлконтаинспоинт и Строкеконтаинспоинт

Метод [**филлконтаинспоинт**](id2d1geometry-fillcontainspoint.md) указывает, содержит ли область, заполненную геометрией, указанную точку. Этот метод можно использовать для проверки нажатия. Следующий пример кода вызывает **филлконтаинспоинт** для объекта [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , передавая точку в (0, 0) и матрицу [**идентификаторов**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) .


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



Метод [**строкеконтаинспоинт**](id2d1geometry-strokecontainspoint.md) определяет, содержит ли штрих геометрии указанную точку. Этот метод можно использовать для проверки нажатия. В следующем примере кода используется **строкеконтаинспоинт**.


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



### <a name="simplify"></a>Упрощение 

Метод [**упростит**](id2d1geometry-simplify.md) удаляет дуги и квадратичные кривые Безье из заданной геометрии. Таким образом, полученная геометрия содержит только строки и, при необходимости, кубические кривые Безье. В следующем примере кода **упрощено** используется для преобразования геометрии с кривыми Безье в геометрию, содержащую только сегменты линий.


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



### <a name="computelength-and-computearea"></a>Компутеленгс и Компутеареа

Метод [**компутеленгс**](id2d1geometry-computelength.md) вычисляет длину указанной геометрии, если каждый сегмент был отменен в строке. Это включает неявный заключительный сегмент, если геометрическая геометрия закрыта. В следующем примере кода используется **компутеленгс** для расчета длины указанного круга (**m \_ pCircleGeometry1**).


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



Метод [**компутеареа**](id2d1geometry-computearea.md) вычисляет область заданного геометрического объекта. В следующем примере кода используется **компутеареа** для вычислить площадь указанного круга (**m \_ pCircleGeometry1**).


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a>компаревисжеометри

Метод [**компаревисжеометри**](id2d1geometry-comparewithgeometry.md) описывает пересечение между геометрическим объектом, который вызывает этот метод, и заданной геометрией. Возможные значения пересечения включают несвязанное [**D2D1 \_ Геометрическое отношение (содержит \_ несвязное \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) ), Геометрическое отношение D2D1 содержится (содержится), **D2D1 \_ геометрическая \_ связь \_ содержит** (Contains) и **\_ \_ \_ Перекрытие геометрической связи** . **\_ \_ \_ \_** "несвязанный" означает, что две геометрические заливки не пересекаются. "содержится" означает, что геометрия полностью содержится в указанной геометрии. "Contains" означает, что геометрия полностью содержит указанную геометрию, а "перекрытие" означает перекрытие двух геометрических объектов, но ни одно из них не полностью содержит другое.

В следующем примере кода показано, как сравнить два круга с одинаковым радиусом 50, но они смещены на 50.


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



### <a name="outline"></a>Контур

Метод [**структуры**](id2d1geometry-outline.md) определяет контур геометрии (версию геометрии, в которой никакая фигура не пересекает саму себя или другие фигуры) и записывает результат в [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). В следующем примере кода используется **Структура** для создания эквивалентной геометрии без каких-либо самостоятельных подразделов. В нем используется допуск плоской обработки по умолчанию.


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



### <a name="getbounds-and-getwidenedbounds"></a>Привязкой и Жетвиденедбаундс

Метод [**Bounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) Извлекает границы геометрии. В следующем примере **кода используются методические границы для** получения границ заданного круга (**m \_ pCircleGeometry1**).


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



Метод [**жетвиденедбаундс**](id2d1geometry-getwidenedbounds.md) Извлекает границы геометрии после его расширения с помощью заданной ширины и стиля штриха и преобразуется указанной матрицей. В следующем примере кода используется **жетвиденедбаундс** для получения границ заданного круга (**m \_ pCircleGeometry1**) после его расширения по заданной толщине штрихов.


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



### <a name="computepointatlength"></a>компутепоинтатленгс

Метод [**компутепоинтатленгс**](id2d1geometry-computepointatlength.md) вычисляет точку и вектор касательных на заданном расстоянии вдоль геометрии. В следующем примере кода используется **компутепоинтатленгс**.


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие сведения о геометрических контурах](path-geometries-overview.md)
</dt> <dt>

[Справочник по Direct2D](reference.md)
</dt> </dl>

 

 