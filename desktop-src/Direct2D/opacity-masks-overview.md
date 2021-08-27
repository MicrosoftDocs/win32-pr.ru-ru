---
title: Общие сведения о масках непрозрачности
description: В этом разделе описывается использование точечных рисунков и кистей для определения масок непрозрачности. В него входят следующие разделы.
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513365474ed6b1f6f42d34f9b876226e00ba6e85
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786380"
---
# <a name="opacity-masks-overview"></a>Общие сведения о масках непрозрачности

В этом разделе описывается использование точечных рисунков и кистей для определения масок непрозрачности. В него входят следующие разделы.

-   [Предварительные требования](#prerequisites)
-   [Что такое маска непрозрачности?](#what-is-an-opacity-mask)
-   [Использование точечного рисунка в качестве маски непрозрачности с помощью метода ФиллопаЦитимаск](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [Использование кисти в качестве маски непрозрачности с помощью метода Филлжеометри](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [Использование кисти линейного градиента в качестве маски непрозрачности](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [Использование кисти радиального градиента в качестве маски непрозрачности](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [Применение маски непрозрачности к слою](#apply-an-opacity-mask-to-a-layer)
-   [См. также](#related-topics)

## <a name="prerequisites"></a>Предварительные требования

В этом обзоре предполагается, что вы знакомы с базовыми операциями рисования Direct2D, как описано в пошаговом руководстве [Создание простого Direct2D приложения](direct2d-quickstart.md) . Также следует ознакомиться с различными типами кистей, как описано в [обзоре кистей](direct2d-brushes-overview.md).

## <a name="what-is-an-opacity-mask"></a>Что такое маска непрозрачности?

Маска непрозрачности — это маска, описываемая кистью или точечным рисунком, которая применяется к другому объекту, чтобы сделать этот объект частично или полностью прозрачным. Маска непрозрачности использует сведения о альфа-канале для указания того, как исходные пикселы объекта смешиваются в конечном целевом объекте назначения. Прозрачные части маски указывают области, в которых базовое изображение скрыто, а непрозрачные части маски указывают, где отображается маскированный объект.

Существует несколько способов применения маски непрозрачности.

-   Используйте метод [**ID2D1RenderTarget:: филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) . Метод **филлопаЦитимаск** закрашивает прямоугольную область целевого объекта прорисовки, а затем применяет маску непрозрачности, определенную точечным рисунком. Используйте этот метод, если маска непрозрачности является точечным рисунком и требуется заполнить прямоугольную область.
-   Используйте метод [**ID2D1RenderTarget:: филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) . Метод **филлжеометри** Закрашивает внутреннюю часть геометрии с указанным [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), а затем применяет маску непрозрачности, определенную кистью. Используйте этот метод, если необходимо применить маску непрозрачности к геометрии или вы хотите использовать кисть в качестве маски непрозрачности.
-   Используйте [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , чтобы применить маску непрозрачности. Используйте этот подход, если необходимо применить маску непрозрачности к группе содержимого рисунка, а не только к одной фигуре или изображению. Дополнительные сведения см. в разделе [Общие сведения о слоях](direct2d-layers-overview.md).

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a>Использование точечного рисунка в качестве маски непрозрачности с помощью метода ФиллопаЦитимаск

Метод [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) закрашивает прямоугольную область целевого объекта прорисовки, а затем применяет маску непрозрачности, определенную [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap). Используйте этот метод при наличии точечного рисунка, который необходимо использовать в качестве маски непрозрачности для прямоугольной области.

На следующей схеме показан результат применения маски непрозрачности ( [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) с изображением цветок) к [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) с изображением Ферн растения. Полученный рисунок является растровым изображением растения, обрезанным на фигурном цветок.

![Схема точечного рисунка цвета, используемого в качестве маски непрозрачности на изображении Ферн растения](images/brushes-ovw-bitmapopacity.png)

В следующем примере кода показано, как это сделать.

В первом примере загружается следующий точечный рисунок *m \_ пбитмапмаск* для использования в качестве маски точечного рисунка. На следующем рисунке показан полученный результат. Обратите внимание, что хотя непрозрачная часть точечного рисунка отображается черным цветом, сведения о цвете в растровом изображении не влияют на маску непрозрачности. используется только информация о непрозрачности каждого пикселя в точечном рисунке. Полностью непрозрачные Пиксели в этом точечном рисунке окрашены черным цветом только в целях наглядности.

![Иллюстрация маски точечного рисунка цветок](images/bitmapmask.png)

В этом примере [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) загружается вспомогательным методом лоадресаурцебитмап, который определен в любом расположении в образце.


```C++
            if (SUCCEEDED(hr))
            {
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"BitmapMask",
                    L"Image",
                    &m_pBitmapMask
                    );
            }
```



В следующем примере определяется кисть *m \_ пфернбитмапбруш*, к которой применяется маска непрозрачности. В этом примере используется [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , содержащий изображение Ферн, но вместо него можно использовать [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)или [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) . На следующем рисунке показан полученный результат.

![Иллюстрация точечного рисунка, используемого растровой кистью](images/fern.png)


```C++
            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
                hr = m_pRenderTarget->CreateBitmapBrush(
                    m_pFernBitmap,
                    propertiesXClampYClamp,
                    &m_pFernBitmapBrush
                    );


            }
```





Теперь, когда определена маска непрозрачности и кисть, можно использовать метод [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) в методе отрисовки приложения. При вызове метода **филлопаЦитимаск** необходимо указать тип маски непрозрачности, которую вы используете: D2D1, **\_ \_ \_ содержимое \_** маски непрозрачности, **\_ текст непрозрачности D2D1, \_ \_ \_ \_ естественное**, а также **\_ \_ \_ \_ \_ \_ совместимый с содержимым GDI содержимое маски непрозрачности Text**. Значения этих трех типов см. в разделе [**\_ \_ \_ содержимое маски непрозрачности D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).

> [!Note]  
> начиная с Windows 8, [**\_ \_ \_ содержимое маски непрозрачности D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) не требуется. См. метод [**ID2D1DeviceContext:: филлопаЦитимаск**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) , у которого нет **параметра \_ \_ \_ содержимого маски непрозрачности D2D1** .

 

В следующем примере задается режим сглаживания целевого объекта отрисовки в [**D2D1 \_ \_ режим сглаживания с \_ псевдонимами**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) , чтобы маска непрозрачности работала правильно. Затем он вызывает метод [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) и передает ему маску непрозрачности (*m \_ пбитмапмаск*), кисть, к которой применяется маска непрозрачности (*m \_ пфернбитмапбруш*), тип содержимого внутри маски непрозрачности [**( \_ \_ \_ \_ график содержимого маски непрозрачности D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) и область для рисования. На следующем рисунке показан полученный результат.

![Иллюстрация изображения Ферн на предприятии с примененной маской непрозрачности](images/opacitymaskoutput.png)


```C++
        D2D1_RECT_F rcBrushRect = D2D1::RectF(5, 5, 155, 155);


        // D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask to function properly
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);
        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```





В этом примере код пропущен.

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a>Использование кисти в качестве маски непрозрачности с помощью метода Филлжеометри

В предыдущем разделе описано, как использовать [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) в качестве маски непрозрачности. Direct2D также предоставляет метод [**ID2D1RenderTarget:: филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , который позволяет при необходимости указать кисть в качестве маски непрозрачности при заполнении [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry). Это позволяет создавать маски непрозрачности на основе градиентов (с помощью [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) или [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) и точечных рисунков (с помощью **ID2D1Bitmap**).

Метод [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) принимает три параметра:

-   Первый параметр, [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), определяет фигуру для рисования.
-   Второй параметр, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), указывает кисть, используемую для рисования геометрии. Этот параметр должен быть [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , для которого в качестве режимов расширения x и y задано значение [**D2D1 в качестве \_ \_ \_ зажима режима расширения**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).
-   Третий параметр, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), задает кисть для использования в качестве маски непрозрачности. Эта кисть может быть [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)или [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). (Технически вы можете использовать [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), но использование сплошной цветовой кисти в качестве маски непрозрачности не дает интересных результатов.)

В следующих разделах описывается использование объектов [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) и [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) в качестве масок непрозрачности.

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a>Использование кисти линейного градиента в качестве маски непрозрачности

На следующей диаграмме показан результат применения кисти линейного градиента к прямоугольнику, который заполняется растровым изображением цветов.

![Схема точечного рисунка цветок с примененной кистью линейного градиента](images/brushes-ovw-lineargradient-opacitymask.png)

В следующих шагах описывается, как повторно создать этот результат.

1.  Определяет содержимое для маскирования. В следующем примере создается [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ плинеарфадефловерсбитмап*. В режиме расширения x и y для *m \_ плинеарфадефловерсбитмап* устанавливается значение D2D1 в качестве маскирующего [**\_ \_ режима \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) , чтобы его можно было использовать с маской непрозрачности методом [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .

    ```cpp
    if (SUCCEEDED(hr))
    {
        // Create the bitmap to be used by the bitmap brush.
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"LinearFadeFlowers",
            L"Image",
            &m_pLinearFadeFlowersBitmap
            );
    }
 
    if (SUCCEEDED(hr))
        {
            D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                D2D1::BitmapBrushProperties(
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                );
    ```

    
    <table>
    <colgroup>
    <col  />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>                if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateBitmapBrush(
                            m_pLinearFadeFlowersBitmap,
                            propertiesXClampYClamp,
                            &m_pLinearFadeFlowersBitmapBrush
                            );
                    }</code></pre></td>
    </tr>
    </tbody>
    </table>

    
    <table>
    <colgroup>
    <col  />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  Определите маску непрозрачности. В следующем примере кода создается кисть диагонального линейного градиента (*m \_ плинеарградиентбруш*), которая плавно исчезает от полностью непрозрачного черного в позиции 0 до полностью прозрачного белого в позиции 1.
```C++
                if (SUCCEEDED(hr))
                {
                    ID2D1GradientStopCollection *pGradientStops = NULL;

                    static const D2D1_GRADIENT_STOP gradientStops[] =
                    {
                        {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                        {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                    };

                    hr = m_pRenderTarget->CreateGradientStopCollection(
                        gradientStops,
                        2,
                        &pGradientStops);


                    if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateLinearGradientBrush(
                            D2D1::LinearGradientBrushProperties(
                                D2D1::Point2F(0, 0),
                                D2D1::Point2F(150, 150)),
                            pGradientStops,
                            &m_pLinearGradientBrush);
                    }

    
                pGradientStops->Release();
                }
```



    

3.  Используйте метод [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) . В последнем примере метод **филлжеометри** используется в качестве кисти содержимого для заполнения [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ пректжео*) на [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ плинеарфадефловерсбитмап*) и применяет маску непрозрачности (*m \_ плинеарградиентбруш*).
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

В этом примере код пропущен.

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a>Использование кисти радиального градиента в качестве маски непрозрачности

На следующей диаграмме показан визуальный результат применения кисти радиального градиента к прямоугольнику, который заполняется растровым изображением фолиаже.

![Схема точечного рисунка фолиаже с примененной кистью радиального градиента](images/brushes-ovw-radialgradient-opacitymask.png)

В первом примере создается [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ прадиалфадефловерсбитмапбруш*. Чтобы его можно было использовать с маской непрозрачности с помощью метода [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , в качестве режима расширения x и y для *m \_ прадиалфадефловерсбитмапбруш* устанавливается значение [**D2D1 в \_ \_ режиме расширения \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).


```C++
            if (SUCCEEDED(hr))
            {
                // Create the bitmap to be used by the bitmap brush.
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"RadialFadeFlowers",
                    L"Image",
                    &m_pRadialFadeFlowersBitmap
                    );
            }


            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
```





<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateBitmapBrush(
                        m_pLinearFadeFlowersBitmap,
                        propertiesXClampYClamp,
                        &m_pLinearFadeFlowersBitmapBrush
                        );
                }</code></pre></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



В следующем примере определяется кисть радиального градиента, которая будет использоваться в качестве маски непрозрачности.


```C++
            if (SUCCEEDED(hr))
            {
                ID2D1GradientStopCollection *pGradientStops = NULL;

                static const D2D1_GRADIENT_STOP gradientStops[] =
                {
                    {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                    {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                };

                hr = m_pRenderTarget->CreateGradientStopCollection(
                    gradientStops,
                    2,
                    &pGradientStops);




                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateRadialGradientBrush(
                        D2D1::RadialGradientBrushProperties(
                            D2D1::Point2F(75, 75),
                            D2D1::Point2F(0, 0),
                            75,
                            75),
                        pGradientStops,
                        &m_pRadialGradientBrush);
                }
                pGradientStops->Release();
            }
```





В окончательном примере кода используется [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ прадиалфадефловерсбитмапбруш*) и маска непрозрачности (*m \_ прадиалградиентбруш*) для заполнения [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ пректжео*).


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



В этом примере код пропущен.

## <a name="apply-an-opacity-mask-to-a-layer"></a>Применение маски непрозрачности к слою

При вызове [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) для отправки [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) на целевой объект прорисовки можно использовать структуру [**\_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) , чтобы применить кисть в качестве маски непрозрачности. В следующем примере кода используется [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) в качестве маски непрозрачности.


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



Дополнительные сведения об использовании слоев см. в разделе [Общие сведения о слоях](direct2d-layers-overview.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Обзор кистей](direct2d-brushes-overview.md)
</dt> <dt>

[Общие сведения о слоях](direct2d-layers-overview.md)
</dt> </dl>

 

 
