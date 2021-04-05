---
title: Краткое руководство по Direct2D
description: Содержит сводку действий, необходимых для рисования с помощью Direct2D, а также пример кода.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, пример кода рисования прямоугольника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133927"
---
# <a name="direct2d-quickstart"></a>Краткое руководство по Direct2D

Direct2D — это API неуправляемого кода с непосредственным режимом, предназначенный для создания двухмерной графики. В этом разделе показано, как использовать Direct2D в обычном приложении Win32 для рисования в **HWND**.

> [!Note]  
> Если вы хотите создать приложение для Магазина Windows, использующее Direct2D, см. раздел [Краткое руководство по Direct2D для Windows 8](direct2d-quickstart-with-device-context.md) .

 

В этом разделе содержатся следующие подразделы.

-   [Рисование простого прямоугольника](#drawing-a-simple-rectangle)
-   [Шаг 1. включение заголовка Direct2D](#step-1-include-direct2d-header)
-   [Шаг 2. Создание ID2D1Factory](#step-2-create-an-id2d1factory)
-   [Шаг 3. Создание ID2D1HwndRenderTarget](#step-3-create-an-id2d1hwndrendertarget)
-   [Шаг 4. Создание кисти](#step-4-create-a-brush)
-   [Шаг 5. Рисование прямоугольника](#step-5-draw-the-rectangle)
-   [Шаг 6. освобождение ресурсов](#step-6-release-resources)
-   [Создание простого приложения Direct2D](#create-a-simple-direct2d-application)
-   [См. также](#related-topics)

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

Помимо заголовков, необходимых для приложения Win32, включите заголовок D2D1. h.

## <a name="step-2-create-an-id2d1factory"></a>Шаг 2. Создание ID2D1Factory

Одно из первых действий в любом Direct2D примере — создание [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



Интерфейс [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) является отправной точкой для использования Direct2D; Используйте **ID2D1Factory** для создания ресурсов Direct2D.

При создании фабрики можно указать, является ли он многопотоковым или многопоточным. (Дополнительные сведения о многопоточных фабриках см. в примечаниях на [**странице справки ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) В этом примере создается однопотоковая фабрика.

Как правило, приложение должно создавать фабрику один раз и хранить ее в течение жизненного цикла приложения.

## <a name="step-3-create-an-id2d1hwndrendertarget"></a>Шаг 3. Создание ID2D1HwndRenderTarget

После создания фабрики используйте ее для создания целевого объекта рендеринга.


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



Целевой объект отрисовки — это устройство, которое может выполнять операции рисования и создавать аппаратно-зависимые ресурсы рисования, такие как кисти. Различные типы целевых объектов отрисовки отображаются на разных устройствах. В предыдущем примере используется [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), который подготавливается к просмотру в части экрана.

По возможности целевой модуль прорисовки использует GPU для ускорения операций отрисовки и создания ресурсов рисования. В противном случае целевой объект прорисовки использует ЦП для обработки инструкций по отрисовке и создания ресурсов. (Это поведение можно изменить с помощью флагов [**\_ \_ \_ типа целевого объекта прорисовки D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) при создании целевого объекта рендеринга.)

Метод [**креатехвндрендертаржет**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) принимает три параметра. Первый параметр, структура [**\_ \_ \_ свойств целевого объекта отрисовки D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , задает параметры удаленного отображения, следует ли принудительно подготавливать целевой объект отрисовки к программному или аппаратному обеспечению и dpi. Код в этом примере использует вспомогательную функцию [**D2D1:: рендертаржетпропертиес**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) для принятия свойств целевого объекта рендеринга по умолчанию.

Второй параметр, [**D2D1 HWND для \_ \_ визуализации \_ целевых \_ свойств**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) структура, указывает **HWND** , для которого отображается содержимое, начальный размер целевого объекта отрисовки (в пикселях) и [**Параметры представления**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options). В этом примере используется вспомогательная функция [**D2D1:: хвндрендертаржетпропертиес**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) для указания HWND и начального размера. Он использует параметры представления по умолчанию.

Третий параметр является адресом указателя, получающего ссылку на целевой объект прорисовки.

При создании целевого объекта рендеринга и возможности аппаратного ускорения выделяются ресурсы на GPU компьютера. Создавая целевой объект рендеринга один раз и постоянно сохраняющий его, вы получаете выигрыш в производительности. Приложение должно создавать целевые объекты прорисовки один раз и удерживать их в течение жизненного цикла приложения или до тех пор, пока не будет получено сообщение об ошибке [**\_ повторного создания \_ D2DERR**](direct2d-error-codes.md) . При возникновении этой ошибки необходимо повторно создать целевой объект рендеринга (и все созданные им ресурсы).

## <a name="step-4-create-a-brush"></a>Шаг 4. Создание кисти

Как и в случае с фабрикой, целевой объект отрисовки может создавать ресурсы рисования. В этом примере целевой объект прорисовки создает кисть.


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



Кисть — это объект, который закрашивает область, например штрих фигуры или заливку геометрии. Кисть в этом примере закрашивает область стандартным сплошным цветом, черным.

Direct2D также предоставляет другие типы кистей: градиентные кисти для рисования линейных и радиальных градиентов, а также растровую кисть для рисования с помощью точечных рисунков и шаблонов.

Некоторые API-интерфейсы рисования предоставляют перья для рисования контуров и кистей для заливки фигур. Direct2D отличается: он не предоставляет объект Pen, но использует кисть для рисования контуров и заливки фигур. При рисовании контуров используйте интерфейс [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) с кистью для управления операциями обводки пути.

Кисть можно использовать только с целевым объектом рендеринга, который ее создал, и с другими целевыми объектами отрисовки в том же домене ресурсов. Как правило, необходимо создавать кисти один раз и хранить их в течение жизненного цикла целевого объекта рендеринга, который их создал. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) — это одиночное исключение; так как создание **ID2D1SolidColorBrush** является сравнительно недорогым, можно создать его каждый раз при рисовании кадра без заметного попадания в производительность. Можно также использовать один **ID2D1SolidColorBrush** и изменять его цвет при каждом его использовании.

## <a name="step-5-draw-the-rectangle"></a>Шаг 5. Рисование прямоугольника

Затем используйте целевой объект рендеринга для рисования прямоугольника.


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



Метод [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) принимает два параметра: прямоугольник для рисования и кисть, используемую для рисования контура прямоугольника. При необходимости можно также указать ширину штриха, шаблон штриха, соединение строки и параметры конца.

Перед выдачей команд рисования необходимо вызвать метод [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) , а после завершения выдачи команд рисования необходимо вызвать метод [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Метод **EndDraw** возвращает **значение HRESULT** , указывающее, были ли команды рисования успешными.

## <a name="step-6-release-resources"></a>Шаг 6. освобождение ресурсов

Если для рисования больше нет кадров или получено [**D2DERR \_ повторного создания \_ целевой**](direct2d-error-codes.md) ошибки, освободите целевой объект рендеринга и все созданные им устройства.


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



Когда приложение завершит использование ресурсов Direct2D (например, когда он собирается завершить работу), освободите фабрику Direct2D.


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a>Создание простого приложения Direct2D

В коде этого раздела показаны основные элементы приложения Direct2D. Для краткости в разделе опущена платформа приложений и код обработки ошибок, который является характеристикой хорошо написанного приложения. Более подробное пошаговое руководство содержит полный код для создания простого приложения Direct2D и демонстрирует лучшие методики проектирования, см. раздел [Создание простого приложения Direct2D](direct2d-quickstart.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание простого приложения Direct2D](direct2d-quickstart.md)
</dt> </dl>

 

 