---
title: Общие сведения о взаимодействии Direct2D и GDI
description: Описывает, как использовать Direct2D и GDI совместно.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D, взаимодействие GDI
- Direct2D, взаимодействие
- взаимодействие, Direct2D
- Интерфейс графических устройств (GDI)
- GDI (интерфейс графических устройств)
- взаимодействие, интерфейс графических устройств (GDI)
- Direct3D, взаимодействие
- Direct3D, Direct2D взаимодействие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951bebc9ea7ca63496a9cdc93fa33ddb74817661e7f5bc072b55d207bfcbdeb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918253"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a>Общие сведения о взаимодействии Direct2D и GDI

В этом разделе описывается, как использовать Direct2D и [GDI](/windows/desktop/gdi/windows-gdi) совместно. Существует два способа объединения Direct2D с GDI: вы можете записывать содержимое GDI в Direct2D-совместимый целевой объект прорисовки, а также записывать содержимое Direct2D в [контекст устройства GDI (DC)](/windows/desktop/gdi/device-contexts).

В этом разделе содержатся следующие подразделы.

-   [Предварительные требования](#prerequisites)
-   [Нарисуйте содержимое Direct2D в контексте устройства GDI](#draw-direct2d-content-to-a-gdi-device-context)
-   [ID2D1DCRenderTargets, преобразования GDI и языковые сборки Windows с письмом справа налево](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [Прорисовка содержимого GDI в Direct2D GDI-Compatible рендеринга](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [Связанные темы](#related-topics)

## <a name="prerequisites"></a>Предварительные требования

В этом обзоре предполагается, что вы знакомы с базовыми операциями рисования Direct2D. Инструкции см. в [кратком](direct2d-quickstart.md)руководстве по Direct2D. Также предполагается, что вы знакомы с операциями рисования GDI.

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a>Нарисуйте содержимое Direct2D в контексте устройства GDI

Для рисования содержимого Direct2D в GDI DC используется [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget). Чтобы создать целевой объект прорисовки контроллера домена, используйте метод [**ID2D1Factory:: креатедкрендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) . Этот метод принимает два параметра.

Первый параметр, структура [**\_ \_ \_ свойств целевого объекта отрисовки D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , определяет отрисовку, удаленное взаимодействие, dpi, формат пикселей и сведения об использовании. Чтобы целевой объект прорисовки контроллера домена работал с GDI, установите формат DXGI в режиме [DXGI \_ \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , а режим Alpha — в режим D2D1 альфа, предварительно [**\_ \_ \_ умноженный**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) или **D2D1 альфа- \_ \_ режим \_ игнорируется**.

Вторым параметром является адрес указателя, получающего ссылку на целевой объект прорисовки контроллера домена.

Следующий код создает целевой объект прорисовки контроллера домена.


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



В приведенном выше коде *m \_ pD2DFactory* является указателем на [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), а *m \_ пдкрт* — указателем на [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).

Прежде чем можно будет подготовиться к просмотру с помощью целевого объекта прорисовки контроллера домена, необходимо использовать метод [**бинддк**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) , чтобы связать его с контроллером GDI. Это делается каждый раз, когда используется другой контроллер домена, или размер области, которую требуется нарисовать для изменения.

Метод [**бинддк**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) принимает два параметра: *HDC* и *псубрект*. Параметр *HDC* предоставляет маркер для контекста устройства, который получает выходные данные целевого объекта отрисовки. Параметр *псубрект* — это прямоугольник, описывающий часть контекста устройства, в которой отображается содержимое. Целевой объект прорисовки контроллера домена обновляет свой размер в соответствии с областью контекста устройства, описанной в *псубрект*, при изменении размера.

Следующий код привязывает контроллер домена к целевому объекту прорисовки контроллера домена.


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



После того как вы свяжете целевой объект прорисовки контроллера домена с контроллером домена, его можно будет использовать для рисования. Следующий код демонстрирует создание содержимого Direct2D и GDI с помощью контроллера домена.


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



Этот код создает выходные данные, как показано на следующем рисунке (добавлены выноски для выделения разницы между Direct2D и визуализацией GDI).

![Иллюстрация двух круговых диаграмм, отображаемых с помощью Direct2D и GDI](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a>ID2D1DCRenderTargets, преобразования GDI и языковые сборки Windows с письмом справа налево

При использовании [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)он визуализирует содержимое Direct2D во внутреннее растровое изображение, а затем визуализирует его на контроллере домена с помощью GDI.

GDI может применить преобразование GDI (через метод [**сетворлдтрансформ**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) ) или другой результат к тому же контроллеру домена, который используется целевым объектом рендеринга. в этом случае GDI преобразует точечный рисунок, созданный Direct2D. Использование преобразования GDI для преобразования содержимого Direct2D может привести к ухудшению визуального качества выходных данных, так как вы преобразуете точечный рисунок, для которого уже рассчитано сглаживание и позиционирование подпикселей.

Например, предположим, что используется целевой объект отрисовки для рисования сцены, содержащей сглаженные геометрические фигуры и текст. Если вы используете преобразование GDI, чтобы применить преобразование масштабирования к контроллеру домена и масштабировать сцену таким образом, чтобы его размер в 10 раз больше, вы увидите пиксельные и зубчатые края. (Если же вы применили аналогичное преобразование с помощью Direct2D, визуальное качество сцены не будет снижено.)

В некоторых случаях может не быть очевидно, что GDI выполняет дополнительную обработку, что может ухудшить качество содержимого Direct2D. например, при сборке Windows с направлением справа налево содержимое, отображаемое [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) , может быть горизонтально инвертировано, когда GDI копирует его в место назначения. Фактическое переинвертирование содержимого зависит от текущих параметров контроллера домена.

В зависимости от типа отображаемого содержимого может потребоваться запретить инверсию. Если содержимое Direct2D содержит текст ClearType, эта инверсия приведет к ухудшению качества текста.

Поведением отрисовки справа налево можно управлять с помощью функции GDI [**сетлайаут**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) . Чтобы предотвратить зеркальное отображение, вызовите функцию GDI **сетлайаут** и укажите **Макет \_ битмапориентатионпресервед** в качестве единственного значения для второго параметра (не объединяйте его с **макетом \_ RTL**), как показано в следующем примере:


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a>Прорисовка содержимого GDI в Direct2D GDI-Compatible рендеринга

В предыдущем разделе описано, как записать содержимое Direct2D в GDI DC. Вы также можете записать содержимое GDI в Direct2D-совместимый целевой объект отрисовки. Этот подход полезен для приложений, которые в основном отображаются с помощью Direct2D, но имеют модель расширяемости или другое устаревшее содержимое, которое требует возможности отрисовки с помощью GDI.

Для отрисовки содержимого GDI в Direct2D, совместимом с GDI, используйте [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), который предоставляет доступ к контексту устройства, который может принимать вызовы GDI. В отличие от других интерфейсов, объект **ID2D1GdiInteropRenderTarget** не создается напрямую. Вместо этого используйте метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) существующего целевого экземпляра прорисовки. В следующем коде показано, как это сделать.


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



В приведенном выше коде *m \_ pD2DFactory* является указателем на [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), а *m \_ пгдирт* — указателем на [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).

Обратите внимание, что при создании целевого объекта прорисовки, совместимого с GDI, задается флаг [**\_ \_ \_ \_ \_ совместимости с использованием целевого объекта визуализации D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) . Если требуется формат пикселей, используйте [ \_ Формат DXGI \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Если требуется альфа-режим, используйте режим [**альфа D2D1 Alpha с предварительным \_ \_ \_ умножением**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) или **\_ \_ режим \_ альфа D2D1**.

Обратите внимание, что метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) всегда проходит успешный результат. Чтобы проверить, работают ли методы интерфейса [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) для данного целевого объекта рендеринга, создайте [**D2D1 \_ \_ целевые \_ Свойства прорисовки**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , определяющие совместимость GDI и соответствующий формат пикселей, а затем вызовите метод « [**неподдерживаемый**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) » целевого объекта отрисовки, чтобы определить, совместима ли цель отрисовки с GDI.

В следующем примере показано, как нарисовать круговую диаграмму (содержимое GDI) для целевого объекта прорисовки, совместимого с GDI.


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



Код выводит диаграммы, как показано на следующем рисунке с выносками для выделения качества отрисовки. Правая круговая диаграмма (содержимое GDI) имеет более низкое качество отрисовки, чем у левой круговой диаграммы (Direct2D содержимое). Это обусловлено тем, что Direct2D может выполнять отрисовку с помощью сглаживания

![Иллюстрация двух кольцевых диаграмм, отображаемых в Direct2D-совместимом целевом объекте отрисовки](images/gdicontentind2d.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ID2D1Factory:: Креатедкрендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[**\_ \_ Свойства целевого объекта ПРОРИСОВКи D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[Контексты устройств GDI](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[ПАКЕТ SDK ДЛЯ GDI](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 