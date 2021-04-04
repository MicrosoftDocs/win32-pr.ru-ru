---
title: Общие сведения о целевых объектах рендеринга
description: Описывает различные типы целевых объектов рендеринга Direct2D и их использование.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, целевые объекты отрисовки
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987637"
---
# <a name="render-targets-overview"></a>Общие сведения о целевых объектах рендеринга

Целевой объект отрисовки — это ресурс, который наследует от интерфейса [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Целевой объект прорисовки создает ресурсы для рисования и выполняет фактические операции рисования. В этом разделе описываются различные типы целевых объектов рендеринга Direct2D и способы их использования.

-   [Целевые объекты рендеринга](#render-targets-overview)
    -   [Функции целевого объекта прорисовки](#render-target-features)
    -   [Целевые ресурсы рендеринга](#render-target-resources)
    -   [Команды рисования](#drawing-commands)
    -   [Обработка ошибок](#error-handling)
-   [Пример: отрисовка содержимого в окне](#example-render-content-to-a-window)

## <a name="render-targets"></a>Целевые объекты рендеринга

Целевой объект отрисовки — это ресурс, который наследует от интерфейса [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Целевой объект прорисовки создает ресурсы для рисования и выполняет фактические операции рисования. Существует несколько видов целевых объектов отрисовки, которые можно использовать для визуализации графики следующими способами.

-   Объекты [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) отображают содержимое в окне.
-   Объекты [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) отрисовывается в контексте устройства GDI.
-   Целевые объекты прорисовки растрового изображения отображают содержимое на экран, расположенный на экране.
-   Объекты для визуализации объекта DXGI визуализируются на поверхности DXGI для использования с Direct3D.

Так как целевой объект прорисовки связан с конкретным устройством отрисовки, это ресурс, зависящий от устройства, и прекращает работу при удалении устройства.

### <a name="render-target-features"></a>Функции целевого объекта прорисовки

Можно указать, использует ли целевой объект прорисовки аппаратное ускорение и отображается ли удаленное отображение на локальном или удаленном компьютере. Целевые объекты отрисовки могут быть настроены для отрисовки с псевдонимами или сглаженными. Для визуализации сцен с большим количеством примитивов разработчик может также визуализировать плоскую графику в режиме с псевдонимами и использовать многовыборочную раскрывающий сглаживание для достижения большей масштабируемости.

Целевые объекты рендеринга также могут группировать операции рисования в слои, представленные интерфейсом [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) . Слои удобно использовать для сбора операций рисования, объединяемых вместе при отрисовке кадра. В некоторых сценариях это может быть полезной альтернативой для подготовки к просмотру целевого объекта прорисовки изображения, а затем повторного использования содержимого растрового изображения, так как затраты на распределение для уровней ниже, чем для [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Целевые объекты рендеринга могут создавать новые объекты рендеринга, совместимые с самими, что полезно для промежуточного отображения на экране, сохраняя различные свойства целевого объекта рендеринга, установленные в исходном объекте.

Также можно выполнить отрисовку с помощью GDI для целевого объекта отрисовки Direct2D, вызвав [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в целевом объекте прорисовки для [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), который содержит методы [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) и [**релеаседк**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) , которые можно использовать для получения контекста устройства GDI. Отрисовка через GDI возможна только в том случае, если целевой объект прорисовки был создан с установленным флагом [**D2D1 \_ рендеринга, \_ \_ \_ \_ совместимым с GDI**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) . Это полезно для приложений, которые в основном подготавливаются к работе с Direct2D, но имеют модель расширяемости или другое устаревшее содержимое, которое требует возможности отрисовки с помощью GDI. Дополнительные сведения см. в статье [Общие сведения о взаимооперациях Direct2D и GDI](direct2d-and-gdi-interoperation-overview.md).

### <a name="render-target-resources"></a>Целевые ресурсы рендеринга

Как и в случае с фабрикой, целевой объект отрисовки может создавать ресурсы рисования. Все ресурсы, созданные целевым объектом рендеринга, — это ресурсы, зависящие от устройства (как и в целевом объекте прорисовки). Целевой объект прорисовки может создавать ресурсы следующих типов:

-   Растровые изображения
-   Кисти
-   Слои
-   Сетки

### <a name="drawing-commands"></a>Команды рисования

Для отображения содержимого используются методы рисования целевого объекта рендеринга. Перед началом рисования вызовите метод [**ID2D1RenderTarget:: бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . После завершения рисования вызовите метод [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Между этими вызовами используются методы рисования и заливки для отрисовки ресурсов рисования. Большинство методов рисования и заливки принимают фигуру (либо примитив, либо геометрию) и кисть для заполнения или структурирования фигуры.

Целевые объекты отрисовки предоставляют методы для обрезки, применения масок непрозрачности и преобразования пространства координат.

Direct2D использует левую систему координат: положительные значения оси x откладываются вправо, а положительные значения оси y — сверху вниз.

### <a name="error-handling"></a>Обработка ошибок

Команды прорисовки целевого объекта не указывают, была ли запрошенная операция успешной. Чтобы определить, есть ли ошибки прорисовки, вызовите метод [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) целевого объекта Render или метод [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) для получения **значения HRESULT**.

## <a name="example-render-content-to-a-window"></a>Пример: отрисовка содержимого в окне

В следующем примере используется метод [**креатехвндрендертаржет**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) для создания [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



В следующем примере для рисования текста в окне используется [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) .


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



В этом примере код пропущен.

 

 