---
title: Использование Direct2D для подготовки к просмотру Server-Side
description: Описывает использование Direct2D для отрисовки на стороне сервера.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, отрисовка на стороне сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413083"
---
# <a name="using-direct2d-for-server-side-rendering"></a>Использование Direct2D для подготовки к просмотру Server-Side

Direct2D хорошо подходит для графических приложений, требующих отрисовку на стороне сервера в Windows Server. В этом обзоре описываются основные принципы использования Direct2D для отрисовки на стороне сервера. Он содержит следующие подразделы:

-   [Требования к отрисовке Server-Side](#requirements-for-server-side-rendering)
-   [Параметры доступных интерфейсов API](#options-for-available-apis)
    -   [ИСПОЛЬЗОВАНИЕМ](#gdi)
    -   [GDI+](#gdi)
    -   [Direct2D](#using-direct2d-for-server-side-rendering)
-   [Использование Direct2D для подготовки к просмотру Server-Side](#how-to-use-direct2d-for-server-side-rendering)
    -   [Программная отрисовка](#software-rendering)
    -   [Многопоточность](#multithreading)
    -   [Создание файла точечного рисунка](#generating-a-bitmap-file)
-   [Заключение](#conclusion)
-   [См. также](#related-topics)

## <a name="requirements-for-server-side-rendering"></a>Требования к отрисовке Server-Side

Ниже приведен типичный сценарий для сервера диаграммы: диаграммы и графики подготавливаются к просмотру на сервере и доставляются в виде растровых изображений в ответ на веб-запросы. Сервер может быть оснащен высокопроизводительной графической картой или вообще без графической карты.

Этот сценарий раскрывает три требования к приложениям. Во первых, приложение должно эффективно обслуживать несколько параллельных запросов, особенно на многоядерных серверах. Во-вторых, приложение должно использовать программную отрисовку при работе на серверах с высокопроизводительной графической картой или без графической карты. Наконец, приложение должно быть запущено в качестве службы в сеансе 0, чтобы не требовать входа пользователя в систему. Дополнительные сведения о сеансе 0 см. в разделе [влияние изоляции сеанса 0 на службы и драйверы в Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).

## <a name="options-for-available-apis"></a>Параметры доступных интерфейсов API

Существует три варианта отрисовки на стороне сервера: GDI, GDI+ и Direct2D. Как и GDI и GDI+, Direct2D — это собственный API двухмерной отрисовки, который предоставляет приложениям больший контроль над использованием графических устройств. Кроме того, Direct2D уникально поддерживает многопоточные и многопоточные фабрики. В следующих разделах сравнивается каждый API с точки зрения качества рисования и многопоточной отрисовки на стороне сервера.

### <a name="gdi"></a>GDI

В отличие от Direct2D и GDI+, GDI не поддерживает функции рисования высокого качества. Например, GDI не поддерживает сглаживание для создания гладких линий и имеет ограниченную поддержку прозрачности. На основе результатов тестирования производительности графики в Windows 7 и Windows Server 2008 R2 Direct2D масштабируется более эффективно, чем GDI, несмотря на переработку блокировок в GDI. Дополнительные сведения об этих результатах тестирования см. в разделе [проектирование производительности графики в Windows 7](/archive/blogs/e7/engineering-windows-7-graphics-performance).

Кроме того, приложения, использующие GDI, ограничены до 10240 дескрипторов GDI на процесс и 65536 дескрипторов GDI на сеанс. Причина заключается в том, что внутренние окна используют 16-разрядное слово для хранения индекса дескрипторов для каждого сеанса.

### <a name="gdi"></a>GDI+

Хотя GDI+ поддерживает сглаживание и альфа-смешение для высококачественного рисования, основная проблема с GDI+ для серверных сценариев заключается в том, что она не поддерживает выполнение в сеансе 0. Так как сеанс 0 поддерживает только неинтерактивные функции, функции, непосредственно или косвенно взаимодействующие с устройствами вывода, получают ошибки. Конкретные примеры функций включают не только те, которые относятся к устройствам вывода, но и те, которые косвенно работают с драйверами устройств.

Подобно GDI, GDI+ ограничен механизмом блокировки. Механизмы блокировки в GDI+ одинаковы в Windows 7 и Windows Server 2008 R2, как в предыдущих версиях.

### <a name="direct2d"></a>Direct2D

Direct2D — это высокопроизводительный, высококачественный графический API, обеспечивающий высокую производительность и качественную визуализацию с аппаратным ускорением. Она предлагает однопотоковую и многопоточной фабрику, а также линейное масштабирование программной отрисовки с детализацией.

Для этого Direct2D определяет корневой интерфейс фабрики. Как правило, объект, созданный в фабрике, может использоваться только с другими объектами, созданными из той же фабрики. Вызывающий объект может запросить однопотоковое или многопоточное фабрику при ее создании. При запросе однопотоковой фабрики не выполняется блокировка потоков. Если вызывающий объект запрашивает многопоточную фабрику, то при каждом вызове в Direct2D будет получено блокирование потока на уровне фабрики.

Кроме того, блокировка потоков в Direct2D более детализирована, чем в GDI и GDI+, поэтому увеличение числа потоков оказывает минимальное влияние на производительность.

## <a name="how-to-use-direct2d-for-server-side-rendering"></a>Использование Direct2D для подготовки к просмотру Server-Side

В следующих разделах описывается использование программной отрисовки, оптимальное использование однопотоковых и многопоточных фабрик, а также рисование и сохранение сложного рисунка в файл.

### <a name="software-rendering"></a>Программная отрисовка

Серверные приложения используют отрисовку программного обеспечения путем создания целевого объекта рендеринга [ивикбитмап](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , при этом для типа целевого объекта прорисовки задано значение D2D1 для \_ \_ целевого типа прорисовки \_ \_ программного обеспечения или D2D1 \_ \_ тип целевого объекта визуализации \_ \_ по умолчанию. Дополнительные сведения о целевых объектах рендеринга [ивикбитмап](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) см. в разделе метод [**ID2D1Factory:: креатевикбитмапрендертаржет**](id2d1factory-createwicbitmaprendertarget.md) . Дополнительные сведения о типах целевых объектов отрисовки см. в разделе [**D2D1 \_ Render \_ Target \_ Type**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).

### <a name="multithreading"></a>Многопоточность

Знание создания и совместного использования фабрик и целевых объектов рендеринга в разных потоках может значительно повлиять на производительность приложения. На следующих трех рисунках показаны три различных подхода. Оптимальный подход показан на рис. 3.

![Direct2D схема многопоточности с одним целевым объектом рендеринга.](images/server-side-rendering-1.png)

На рис. 1 разные потоки совместно используют одну и ту же фабрику и один и тот же целевой объект рендеринга. Такой подход может привести к непредсказуемым результатам в случаях, когда несколько потоков одновременно изменяют состояние общей цели рендеринга, например, одновременно устанавливая матрицу преобразования. Так как внутренняя блокировка в Direct2D не синхронизирует общий ресурс, например целевые объекты рендеринга, этот подход может вызвать сбой вызова [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) в потоке 1, так как в потоке 2 вызов **бегиндрав** уже использует общий целевой объект отрисовки.

![Direct2D Многопотоковая диаграмма с несколькими целевыми объектами отрисовки.](images/server-side-rendering-2.png)

Чтобы избежать непредсказуемых результатов, возникших на рис. 1, на рис. 2 показана многопоточная фабрика с каждым потоком, имеющим собственный целевой объект рендеринга. Этот подход работает, но фактически функционирует как приложение с одним потоком. Причина заключается в том, что блокировка на уровне фабрики применяется только к уровню операции рисования, и все вызовы рисования в той же фабрике сериализуются. В результате поток 1 блокируется при попытке ввести вызов рисования, а поток 2 — в середине выполнения другого вызова рисования.

![Direct2D Многопотоковая диаграмма с несколькими фабриками и несколькими целевыми объектами рендеринга.](images/server-side-rendering-3.png)

На рис. 3 показан оптимальный подход, в котором используются однопотоковые фабрики и однопотоковый целевой объект отрисовки. Поскольку при использовании однопотоковой фабрики не выполняется блокировка, операции рисования в каждом потоке могут выполняться параллельно для достижения оптимальной производительности.

### <a name="generating-a-bitmap-file"></a>Создание файла точечного рисунка

Чтобы создать файл точечного рисунка с помощью отрисовки программного обеспечения, используйте целевой объект рендеринга [ивикбитмап](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) . Используйте [ивикстреам](/windows/win32/api/wincodec/nn-wincodec-iwicstream) для записи точечного рисунка в файл. Используйте [ивикбитмапфраминкоде](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) для кодирования точечного рисунка в указанный формат изображения. В следующем примере кода показано, как выполнить прорисовку и сохранение следующего изображения в файл.

![пример выходного изображения.](images/saveasimagefile-sample.png)

В этом примере кода сначала создается [ивикбитмап](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) и целевой объект отрисовки [ивикбитмап](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) . Затем он визуализирует изображение с текстом, геометрическим контуром, представляющим почасовое стекло, а также преобразованное почасовое стекло в растровое изображение WIC. Затем он использует [ивикстреам:: инитиализефромфиленаме](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) для сохранения растрового изображения в файл. Если приложению необходимо сохранить точечный рисунок в памяти, используйте вместо него [ивикстреам:: инитиализефроммемори](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) . Наконец, он использует [ивикбитмапфраминкоде](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) для кодирования точечного рисунка.


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a>Заключение

Как видно из приведенного выше, использование Direct2D для отрисовки на стороне сервера является простым и простым. Кроме того, он обеспечивает высококачественную и высокопараллелизуемыеную отрисовку, которая может выполняться в средах сервера с низким уровнем прав.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по Direct2D](reference.md)
</dt> </dl>

 

 