---
title: Общие сведения о слоях
description: Основные сведения о Direct2D слоях.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, слои
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ac68ba25d1e8f35c5a41daec4d7a5295235a5d98
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549189"
---
# <a name="layers-overview"></a>Общие сведения о слоях

В этом обзоре описываются основы использования Direct2D слоев. В него входят следующие разделы.

-   [Что такое слои?](#what-are-layers)
-   [Слои в Windows 8 и более поздних версиях](#layers-in-windows-8-and-later)
    -   [ID2D1DeviceContext и Пушлайер](#id2d1devicecontext-and-pushlayer)
    -   [D2D1 \_ Layer \_ PARAMETERS1 и D2D1 \_ Layer \_ OPTIONS1](/windows)
    -   [Режимы смешения](#blend-modes)
    -   [Взаимодействия](#interoperation)
-   [Создание слоев](#creating-layers)
-   [Границы содержимого](#content-bounds)
-   [Геометрические маски](#geometric-masks)
-   [Маски непрозрачности](#opacity-masks)
-   [Альтернативы слоям](#alternatives-to-layers)
-   [Обрезка произвольной фигуры](#clipping-an-arbitrary-shape)
    -   [Выровняйте картинки по оси](#axis-aligned-clips)
-   [Связанные темы](#related-topics)

## <a name="what-are-layers"></a>Что такое слои?

Уровни, представленные объектами [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , позволяют приложению управлять группой операций рисования. Слой можно использовать, отправляя его в целевой объект прорисовки. Последующие операции рисования, выполняемые целевым объектом отрисовки, направляются на слой. Завершив работу с слоем, можно «присвоить» слой из целевого объекта прорисовки, который комбинирует содержимое слоя обратно в целевой объект отрисовки.

Как и кисти, слои — это ресурсы, зависящие от устройства, созданные объектами прорисовки. Слои можно использовать для любого целевого объекта отрисовки в том же домене ресурсов, который содержит целевой объект рендеринга, который ее создал. Однако ресурс уровня может использоваться только одним целевым объектом отрисовки за раз. Дополнительные сведения о ресурсах см. в разделе [Общие сведения о ресурсах](resources-and-resource-domains.md).

Хотя уровни предлагают мощный метод отрисовки для создания интересных эффектов, чрезмерное число слоев в приложении может негативно сказаться на его производительности, так как при управлении слоями и ресурсами слоя могут воздействовать различные затраты. Например, есть затраты на заполнение или очистку слоя и его обратное смешение, особенно на более высоком оборудовании. Затем есть затраты на управление ресурсами уровня. Если вы перераспределяете их часто, то конечные остановки GPU будут самыми значительными проблемами. При проектировании приложения попытайтесь максимально увеличить повторное использование ресурсов слоя.

## <a name="layers-in-windows-8-and-later"></a>Слои в Windows 8 и более поздних версиях

В Windows 8 появились новые API-интерфейсы, которые упрощают работу, улучшают производительность и добавляют компоненты к слоям.

### <a name="id2d1devicecontext-and-pushlayer"></a>ID2D1DeviceContext и Пушлайер

Интерфейс [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) является производным от интерфейса [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) и является ключом к отображению содержимого Direct2D в Windows 8. Дополнительные сведения об этом интерфейсе см. в разделе [устройства и контексты устройств](devices-and-device-contexts.md). С помощью интерфейса контекста устройства можно пропустить вызов метода [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , а затем передать NULL методу [**ID2D1DeviceContext::P ушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) . Direct2D автоматически управляет ресурсом слоя и может совместно использовать ресурсы между слоями и графами эффектов.

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a>D2D1 \_ Layer \_ PARAMETERS1 и D2D1 \_ Layer \_ OPTIONS1

Структура [**D2D1 \_ Layer \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) аналогична [**\_ \_ параметрам слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), за исключением того, что последний член структуры теперь является перечислением [**D2D1 \_ \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) .

[**D2D1 \_ СЛОЙ \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) не имеет параметра ClearType и имеет два различных параметра, которые можно использовать для повышения производительности:

-   [**D2D1 \_ СЛОЙ \_ OPTIONS1 \_ инициализируется \_ из \_ фона**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D отображает примитивы на слой, не снимая его с прозрачным черным цветом. Это не значение по умолчанию, но в большинстве случаев это приводит к повышению производительности.

-   [**D2D1 \_ СЛОЙ \_ OPTIONS1 \_ игнорировать \_ альфа**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)-канал: Если для базовой поверхности задан [**\_ режим D2D1 \_ Alpha \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), этот параметр позволяет Direct2D избежать изменения альфа-канала слоя. Не используйте его в других случаях.

### <a name="blend-modes"></a>Режимы смешения

Начиная с Windows 8, контекст устройства имеет [**простой режим смешения**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) , который определяет, как каждый примитив смешивается с целевой поверхностью. Этот режим также применяется к слоям при вызове метода [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .

Например, если вы используете слой для обрезки примитивов с прозрачностью, для правильного результата задайте режим [**копирования D2D1- \_ примитивного \_ смешения \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) в контексте устройства. Режим копирования обеспечивает линейную интерполяцию контекста устройства: все 4 цветовые каналы, включая альфа-канал, каждого пикселя с содержимым целевой поверхности в соответствии с геометрической маской слоя.

### <a name="interoperation"></a>Взаимодействие

Начиная с Windows 8, Direct2D поддерживает взаимодействие с Direct3D и GDI во время отправки слоя или клипа. Метод [**ID2D1GdiInteropRenderTarget:: GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) вызывается, пока слой передается для взаимодействия с GDI. Вы вызываете [**ID2D1DeviceContext:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) , а затем готовитесь к просмотру на основной поверхности для взаимодействия с Direct3D. Вы отвечаете за отображение внутри слоя или клипа с помощью Direct3D или GDI. При попытке отображения за пределами слоя или клипа результаты не определены.

## <a name="creating-layers"></a>Создание слоев

Работа с слоями требует знакомства с методами [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))и [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , а также структурой [**\_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) , которая содержит набор данных параметрической, определяющих, как можно использовать слой. В следующем списке описываются методы и структура.

-   Вызовите метод [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , чтобы создать ресурс слоя.
    > [!Note]  
    > Начиная с Windows 8, можно пропустить вызов метода [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , а затем передать NULL методу [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) в интерфейсе [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) . Это проще и позволяет Direct2D автоматически управлять ресурсом слоя и совместно использовать ресурсы между слоями и графами эффектов.

     

-   После того как целевой объект прорисовки начал Рисование (после вызова метода [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) ), можно использовать метод [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) . Метод **пушлайер** добавляет указанный слой в целевой объект отрисовки, чтобы целевой объект получал все последующие операции рисования до вызова [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . Этот метод принимает объект [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , возвращаемый путем вызова [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) и *Лайерпараметерс* в структуре [**\_ \_ параметров уровня D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) . В следующей таблице описаны поля структуры. 

    | Поле                 | Описание|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **контентбаундс**     | Границы содержимого слоя. Содержимое за пределами этих границ гарантированно не будет отображаться. По умолчанию этот параметр имеет значение [**инфинитерект**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect). Если используется значение по умолчанию, границы содержимого фактически передаются в качестве границ целевого объекта отрисовки. |
    | **жеометрикмаск**     | Используемых Область, определяемая [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), в которую должен быть обрезан слой. Задайте **значение NULL** , если слой не должен быть обрезан до геометрии. |
    | **маскантиалиасмоде** | Значение, указывающее режим сглаживания для геометрической маски, указанной в поле **жеометрикмаск** . |
    | **масктрансформ**     | Значение, указывающее преобразование, применяемое к геометрической маске при создании слоя. Это относится к универсальному преобразованию.  |
    | **данной**           | Значение прозрачности слоя. Непрозрачность каждого ресурса слоя умножается на это значение при совмещении с целевым объектом.  |
    | **опаЦитибруш**      | Используемых Кисть, используемая для изменения прозрачности слоя. Кисть сопоставляется с слоем, а альфа-канал каждого сопоставленного пикселя кисти умножается на соответствующий пиксель слоя. Задайте **значение NULL** , если слой не должен иметь маску непрозрачности.   |
    | **лайероптионс**      | Значение, указывающее, будет ли слой вырисовывать текст с помощью сглаживания ClearType. По умолчанию этот параметр имеет значение OFF. Если включить его, технология ClearType будет работать правильно, но это приводит к немного меньшей скорости рендеринга.    |

    

     

    > [!Note]  
    > Начиная с Windows 8, нельзя визуализировать с помощью технологии ClearType в слое, поэтому параметр **лайероптионс** всегда должен иметь значение [**D2D1 \_ Layer \_ \_ None**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options) .

     

    Для удобства Direct2D предоставляет метод [**D2D1:: лайерпараметерс**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) , помогающий создавать структуры [**\_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .

-   Чтобы составить содержимое слоя в целевой объект рендеринга, вызовите метод [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . Перед вызовом метода [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) необходимо вызвать метод **поплайер** .

В следующем примере показано, как использовать [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))и [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer). Для всех полей в [**структуре \_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) заданы значения по умолчанию, за исключением **опаЦитибруш**, для которого задано значение [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).


```C++
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);
```



В этом примере код пропущен.

Обратите внимание, что при вызове [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) и [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)убедитесь, что каждый **пушлайер** имеет соответствующий вызов **поплайер** . Если количество вызовов **поплайер** превышает число вызовов **пушлайер** , то целевой объект прорисовки помещается в состояние ошибки. Если функция [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) вызывается до того, как все необработанные слои будут извлечены, то целевой объект прорисовки помещается в состояние ошибки и возвращает ошибку. Чтобы очистить состояние ошибки, используйте [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="content-bounds"></a>Границы содержимого

**Контентбаундс** устанавливает предельный размер отображаемых данных слоя. Только те элементы, которые находятся в границах содержимого, являются составными для целевого объекта рендеринга.

В следующем примере показано, как задать **контентбаундс** , чтобы исходное изображение было обрезано с учетом содержимого в левом верхнем углу в точке (10, 108) и правом нижнем углу в (121, 177). На следующем рисунке показано исходное изображение и результат обрезки изображения до границ содержимого.

![Иллюстрация границ содержимого на исходном изображении и полученное обрезанное изображение](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



В этом примере код пропущен.

> [!Note]
>
> Полученное обрезанное изображение будет дополнительно затронуто при указании **жеометрикмаск**. Дополнительные сведения см. в разделе [геометрические маски](#geometric-masks) .

 

## <a name="geometric-masks"></a>Геометрические маски

Геометрическая маска — это клип или фрагмент, определяемый объектом [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , который маскирует слой при прорисовке объектом прорисовки. Для маскирования результатов до геометрии можно использовать поле **жеометрикмаск** структуры [**\_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) . Например, если нужно отобразить изображение, маскированное по блоку «A», можно сначала создать геометрию, представляющую блок-символ «A», и использовать эту геометрию в качестве геометрической маски для слоя. Затем, после того, как слой помещается, можно нарисовать изображение. При извлечении слоя изображение обрезается по фигуре блока "A".

В следующем примере показано, как создать [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) , содержащий форму Mountain, а затем передать геометрию пути в [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)). Затем он рисует растровое изображение и квадраты. Если в слое для отрисовки имеется только точечный рисунок, для повышения эффективности используйте [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) с размытой растровой кистью. На следующем рисунке показан результат выполнения этого примера.

![Иллюстрация изображения листа и полученного изображения после применения геометрической маски Mountain](images/layers-bitmapmask.png)

В первом примере определяется геометрия, которая будет использоваться в качестве маски.


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



В следующем примере геометрия используется в качестве маски для слоя.


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f), 
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



В этом примере код пропущен.

> [!Note]
>
> В общем случае при указании **жеометрикмаск** можно использовать значение по умолчанию [**инфинитерект**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)для **контентбаундс**.
>
> Если **контентбаундс** имеет значение NULL и **жеометрикмаск** имеет значение, отличное от NULL, то границы содержимого фактически являются границами геометрической маски после применения преобразования маски.
>
> Если **контентбаундс** имеет значение, отличное от NULL, а **жеометрикмаск** имеет значение, отличное от NULL, то преобразованная геометрическая маска фактически обрезается по границам содержимого, а границы содержимого считаются бесконечными.

 

## <a name="opacity-masks"></a>Маски непрозрачности

Маска непрозрачности — это маска, описываемая кистью или точечным рисунком, которая применяется к другому объекту, чтобы сделать этот объект частично или полностью прозрачным. Он позволяет использовать альфа-канал кисти для использования в качестве маски содержимого. Например, можно определить кисть радиального градиента, которая отличается от непрозрачной и прозрачной для создания вигнеттеного действия.

В следующем примере используется [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ прадиалградиентбруш*) в качестве маски непрозрачности. Затем он рисует растровое изображение и квадраты. Если в слое для отрисовки имеется только точечный рисунок, для повышения эффективности используйте [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) с размытой растровой кистью. На следующем рисунке показаны выходные данные из этого примера.

![Иллюстрация изображения деревьев и полученного изображения после применения маски непрозрачности](images/layers-opacitymask.png)


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



В этом примере код пропущен.

> [!Note]  
> В этом примере используется слой для применения маски непрозрачности к одному объекту, чтобы максимально упростить пример. При применении маски непрозрачности к одному объекту более эффективно использовать методы [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) или [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , а не слой.

 

Инструкции по применению маски непрозрачности без использования слоя см. в разделе [Общие сведения о масках непрозрачности](opacity-masks-overview.md).

## <a name="alternatives-to-layers"></a>Альтернативы слоям

Как упоминалось ранее, чрезмерное количество слоев может негативно сказаться на производительности приложения. Чтобы повысить производительность, старайтесь не использовать слои везде, где это возможно. Вместо этого используйте их альтернативы. В следующем примере кода показано, как использовать [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) и [**попаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) для обрезки области в качестве альтернативы использованию слоя с границами содержимого.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



Аналогично, используйте [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) с растровой кистью с маскированием в качестве альтернативы использованию слоя с маской непрозрачности, если в слое для отрисовки имеется только одно содержимое, как показано в следующем примере.


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



В качестве альтернативы использованию слоя с геометрической маской можно использовать битовую маску для обрезки области, как показано в следующем примере.


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



Наконец, если вы хотите применить непрозрачность к одному примитиву, необходимо умножить степень прозрачности на цвет кисти, а затем визуализировать примитив. Не требуется слой или битовая карта маски непрозрачности.


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a>Обрезка произвольной фигуры

На рисунке ниже показан результат применения клипа к изображению.

![изображение, в котором показан пример изображения до и после клипа.](images/clip.png)

Этот результат можно получить с помощью слоев с геометрической маской или методом [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) с кистью непрозрачности.

Ниже приведен пример использования слоя.


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Ниже приведен пример использования метода [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



В этом примере кода при вызове метода Пушлайер вы не передаетесь на слой, созданный приложением. Direct2D создает слой для вас. Direct2D может управлять выделением и уничтожением этого ресурса без участия в приложении. Это позволяет Direct2D использовать слои внутренним образом и применять оптимизации управления ресурсами.

> [!Note]  
> В Windows 8 многие оптимизации были применены к использованию уровней, и мы рекомендуем использовать API слоя вместо [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , когда это возможно.

 

### <a name="axis-aligned-clips"></a>Выровняйте картинки по оси

Если регион, который будет обрезан, вырезается по оси поверхности рисования, а не произвольно. Этот вариант подходит для использования прямоугольника обрезки вместо слоя. Повышение производительности — это больше для геометрических объектов, чем у сглаженных геометрических объектов. Дополнительные сведения о выровняйте по оси клипов см. в разделе [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по Direct2D](reference.md)
</dt> </dl>

 

 