---
title: Краткое руководство по Direct2D для Windows 8
description: Содержит сводку действий, необходимых для рисования с помощью Direct2D, а также пример кода.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, пример кода рисования прямоугольника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28e5cfbbf4e63e129a43bec783a64203e20e30a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654325"
---
# <a name="direct2d-quickstart-for-windows-8"></a>Краткое руководство по Direct2D для Windows 8

Direct2D — это API неуправляемого кода с непосредственным режимом, предназначенный для создания двухмерной графики. В этом разделе показано, как использовать Direct2D для рисования в [**Windows:: UI:: Core:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).

В этом разделе содержатся следующие подразделы.

-   [Рисование простого прямоугольника](#drawing-a-simple-rectangle)
-   [Шаг 1. включение заголовка Direct2D](#step-1-include-direct2d-header)
-   [Шаг 2. Создание ID2D1Factory1](#step-2-create-an-id2d1factory1)
-   [Шаг 3. Создание ID2D1Device и ID2D1DeviceContext](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [Шаг 4. Создание кисти](#step-4-create-a-brush)
-   [Шаг 5. Рисование прямоугольника](#step-5-draw-the-rectangle)
-   [Пример кода](#example-code)

## <a name="drawing-a-simple-rectangle"></a>Рисование простого прямоугольника

Чтобы нарисовать прямоугольник с помощью [GDI](/windows/desktop/gdi/windows-gdi), можно обрабатывать сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , как показано в следующем коде.


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



Код для рисования того же прямоугольника с Direct2D аналогичен: он создает ресурсы для рисования, описывает фигуру для рисования, рисует фигуру, а затем освобождает ресурсы рисования. В последующих разделах подробно описывается каждый из этих шагов.

## <a name="step-1-include-direct2d-header"></a>Шаг 1. включение заголовка Direct2D

Помимо заголовков, необходимых для приложения, включите заголовки D2D1. h и D2D1 \_ 1. h.

## <a name="step-2-create-an-id2d1factory1"></a>Шаг 2. Создание ID2D1Factory1

Одно из первых действий в любом Direct2D примере — создание [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



Интерфейс [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) является отправной точкой для использования Direct2D; Используйте **ID2D1Factory1** для создания ресурсов Direct2D.

При создании фабрики можно указать, является ли он многопотоковым или многопоточным. (Дополнительные сведения о многопоточных фабриках см. в примечаниях на [**странице справки ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) В этом примере создается однопотоковая фабрика.

Как правило, приложение должно создавать фабрику один раз и хранить ее в течение жизненного цикла приложения.

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a>Шаг 3. Создание ID2D1Device и ID2D1DeviceContext

После создания фабрики используйте ее для создания устройства Direct2D, а затем используйте устройство для создания контекста устройства Direct2D. Чтобы создать эти объекты Direct2D, необходимо иметь [**устройство Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , [**Устройство DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)и [**цепочку подкачки DXGI**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1). Сведения о создании необходимых компонентов см. в разделе [устройства и контексты устройств](devices-and-device-contexts.md) .


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



Контекст устройства — это устройство, которое может выполнять операции рисования и создавать аппаратно-зависимые ресурсы рисования, такие как кисти. Вы также используете контекст устройства, чтобы связать [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) с поверхностью DXGI для использования в качестве целевого объекта отрисовки. Контекст устройства может быть отображен в разные типы целевых объектов.

В этом примере кода объявляются свойства точечного рисунка, ссылающегося на цепочку подкачки DXGI, которая подготавливается к [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow). Метод [**ID2D1DeviceContext:: креатебитмапфромдксгисурфаце**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) получает поверхность Direct2D из поверхности DXGI. Это делает его таким образом, чтобы все содержимое, отображаемое в целевой [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , отображалось на поверхности цепочки буферов обмена.

Получив поверхность Direct2D, используйте метод [**ID2D1DeviceContext:: сеттаржет**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) , чтобы задать его в качестве активного целевого объекта рендеринга.


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a>Шаг 4. Создание кисти

Как и в случае с фабрикой, контекст устройства может создавать ресурсы рисования. В этом примере контекст устройства создает кисть.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



Кисть — это объект, который закрашивает область, например штрих фигуры или заливку геометрии. Кисть в этом примере закрашивает область стандартным сплошным цветом, черным.

Direct2D также предоставляет другие типы кистей: градиентные кисти для рисования линейных и радиальных градиентов, [**растровую кисть**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) для рисования с помощью точечных рисунков и узоров, а также начиная с Windows 8 — [**кисть изображения**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) для рисования с помощью подготовленного изображения.

Некоторые API-интерфейсы рисования предоставляют перья для рисования контуров и кистей для заливки фигур. Direct2D отличается: он не предоставляет объект Pen, но использует кисть для рисования контуров и заливки фигур. При рисовании контуров используйте интерфейс [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) или начиная с Windows 8 интерфейс [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) с кистью для управления обводками пути.

Кисть можно использовать только с целевым объектом рендеринга, который ее создал, и с другими целевыми объектами отрисовки в том же домене ресурсов. Как правило, необходимо создавать кисти один раз и хранить их в течение жизненного цикла целевого объекта рендеринга, который их создал. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) — это одиночное исключение; так как создание **ID2D1SolidColorBrush** является сравнительно недорогым, можно создать его каждый раз при рисовании кадра без заметного попадания в производительность. Можно также использовать один **ID2D1SolidColorBrush** и изменять его цвет или непрозрачность каждый раз, когда вы его используете.

## <a name="step-5-draw-the-rectangle"></a>Шаг 5. Рисование прямоугольника

Затем используйте контекст устройства для рисования прямоугольника.


```C++
 
m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



Метод [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) принимает два параметра: прямоугольник для рисования и кисть, используемую для рисования контура прямоугольника. При необходимости можно также указать ширину штриха, шаблон штриха, соединение строки и параметры конца.

Перед выдачей команд рисования необходимо вызвать метод [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) , а после завершения выдачи команд рисования необходимо вызвать метод [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Метод **EndDraw** возвращает **значение HRESULT** , указывающее, были ли команды рисования успешными. Если это не удалось, вспомогательная функция Сровиффаилед выдаст исключение.

Метод повторной отправки [**идксгисвапчаин::P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) перемещает поверхность буфера на экран на поверхности экрана для отображения результата.

## <a name="example-code"></a>пример кода

В коде этого раздела показаны основные элементы приложения Direct2D. Для краткости в разделе опущена платформа приложений и код обработки ошибок, который является характеристикой хорошо написанного приложения.

 

 