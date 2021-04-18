---
title: Учебник начало работы с DirectWrite
description: В этом документе показано, как использовать DirectWrite и Direct2D для создания простого текста, содержащего один формат, а затем текст, содержащий несколько форматов.
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite, учебник
- DirectWrite, руководство по началу работы
- DirectWrite, Direct2D
- Direct2D
- DirectWrite, интерфейс Идвритетекстлайаут
- Интерфейс Идвритетекстлайаут
- DirectWrite, интерфейс Идвритетипографи
- Интерфейс Идвритетипографи
- DirectWrite, интерфейс Идвритетекстформат
- Интерфейс Идвритетекстформат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338444"
---
# <a name="tutorial-getting-started-with-directwrite"></a>Учебник. начало работы с DirectWrite

В этом документе показано, как использовать [DirectWrite](direct-write-portal.md) и [Direct2D](rendering-by-using-direct2d.md) для создания простого текста, содержащего один формат, а затем текст, содержащий несколько форматов.

Этот учебник содержит следующие компоненты.

-   [Исходный код](#source-code)
-   [Рисование простого текста](#drawing-simple-text)
    -   [Часть 1. объявление ресурсов DirectWrite и Direct2D.](#part-1-declare-directwrite-and-direct2d-resources)
    -   [Часть 2. создание независимых ресурсов устройства.](#part-2-create-device-independent-resources)
    -   [Часть 3. Создание ресурсов Device-Dependent.](#part-3-create-device-dependent-resources)
    -   [Часть 4. Рисование текста с помощью метода Direct2D DrawText.](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [Часть 5. Отрисовка содержимого окна с помощью Direct2D](#part-5-render-the-window-contents-using-direct2d)
-   [Рисование текста с несколькими форматами.](#drawing-text-with-multiple-formats)
    -   [Часть 1. Создание интерфейса Идвритетекстлайаут.](#part-1-create-an-idwritetextlayout-interface)
    -   [Часть 2. Применение форматирования с помощью Идвритетекстлайаут.](#part-2-applying-formatting-with-idwritetextlayout)
    -   [Часть 3. Добавление типографских функций с помощью Идвритетипографи.](#part-3-adding-typographic-features-with-idwritetypography)
    -   [Часть 4. Рисование текста с помощью метода Direct2D Дравтекстлайаут.](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a>Исходный код

Исходный код, приведенный в этом обзоре, взят из [примера DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples). Каждая часть реализуется в отдельном классе (Симплетекст и Мултиформаттедтекст) и отображается в отдельном дочернем окне. Каждый класс представляет окно Microsoft Win32. Помимо метода *WndProc* , каждый класс содержит следующие методы.



| Функция                              | Описание                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| **CreateDeviceIndependentResources**  | Создает ресурсы, независимые от устройства, поэтому их можно использовать в любом месте.                      |
| **дискарддевицеиндепендентресаурцес** | Освобождает ресурсы, независимые от устройства, после того, как они больше не нужны.                          |
| **CreateDeviceResources**             | Создает ресурсы, такие как кисти и целевые объекты рендеринга, привязанные к конкретному устройству.        |
| **дискарддевицересаурцес**            | Освобождает ресурсы, зависящие от устройства, после того, как они больше не нужны.                            |
| **DrawD2DContent**                    | Использует [Direct2D](../direct2d/direct2d-portal.md) для отображения на экране.                              |
| **DrawText**                          | Рисует текстовую строку с помощью [Direct2D](../direct2d/direct2d-portal.md).                            |
| **онресизе**                          | Изменяет размер целевого объекта отрисовки [Direct2D](../direct2d/direct2d-portal.md) при изменении размера окна. |



 

Вы можете использовать предоставленный образец или выполнить приведенные ниже инструкции, чтобы добавить [DirectWrite](direct-write-portal.md) и [Direct2D](rendering-by-using-direct2d.md) в собственное приложение Win32. Дополнительные сведения о примере и связанных файлах проекта см. в [примере директвритехелловорлд](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="drawing-simple-text"></a>Рисование простого текста

В этом разделе показано, как использовать [DirectWrite](direct-write-portal.md) и [Direct2D](../direct2d/direct2d-portal.md) для отрисовки простого текста, имеющего один формат, как показано на следующем снимке экрана.

![снимок экрана "Hello World, использующий DirectWrite!" в одном формате](images/simplecropped.png)

Для рисования простого текста на экране необходимо четыре компонента:

-   Строка символов для отображения.
-   Экземпляр [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).
-   Размеры области, в которой будет содержаться текст.
-   Объект, который может визуализировать текст. В этом руководстве. используется целевой объект рендеринга [Direct2D](../direct2d/direct2d-portal.md) .

Интерфейс [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) описывает имя, размер, вес, стиль и растяжение гарнитуры, используемые для форматирования текста, а также сведения о языковых стандартах. **Идвритетекстформат** также определяет методы для установки и получения следующих свойств:

-   Межстрочный шаг.
-   Выравнивание текста относительно левого и правого краев поля макета.
-   Выравнивание абзаца относительно верхнего и нижнего края поля макета.
-   Направление чтения.
-   Степень гранулярности обрезки текста для текста, который переполняет поле макета.
-   Позиция приращения вкладки.
-   Направление потока абзацев.

Для рисования текста, использующего оба процесса, описанных в этом документе, требуется интерфейс [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .

Прежде чем можно будет создать объект [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) или любой другой объект [DirectWrite](direct-write-portal.md) , необходим экземпляр [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) . **Идвритефактори** используется для создания экземпляров **идвритетекстформат** и других объектов DirectWrite. Чтобы получить экземпляр фабрики, используйте функцию [**двритекреатефактори**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a>Часть 1. объявление ресурсов DirectWrite и Direct2D.

В этой части вы объявили объекты, которые будут использоваться позже для создания и отображения текста в качестве частных членов данных класса. Все интерфейсы, функции и типы данных для [DirectWrite](direct-write-portal.md) объявляются в файле заголовка *дврите. h* , а их [Direct2D](../direct2d/direct2d-portal.md) объявляются в *D2D1. h*; Если вы еще не сделали этого, включите эти заголовки в свой проект.

1.  В файле заголовка класса (Симплетекст. h) объявите указатели на [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) и [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) интерфейсы как закрытые члены.
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  Объявите элементы для хранения текстовой строки для отображения и длины строки.
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  Объявите указатели на интерфейсы [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)и [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) для отрисовки текста с помощью [Direct2D](../direct2d/direct2d-portal.md).
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a>Часть 2. создание независимых ресурсов устройства.

[Direct2D](rendering-by-using-direct2d.md) предоставляет два типа ресурсов: ресурсы, зависящие от устройства, и ресурсы, независимые от устройств. Ресурсы, зависящие от устройства, связаны с устройством отрисовки и больше не работают, если это устройство удалено. С другой стороны, независимые от устройства ресурсы могут быть последними в области приложения.

Ресурсы [DirectWrite](direct-write-portal.md) не зависят от устройства.

В этом разделе вы создадите независимые от устройства ресурсы, используемые приложением. Эти ресурсы должны быть освобождены с помощью вызова метода **Release** интерфейса.

Некоторые используемые ресурсы должны быть созданы только один раз и не привязаны к устройству. Инициализация этих ресурсов помещается в метод *симплетекст:: креатедевицеиндепендентресаурцес* , который вызывается при инициализации класса.

1.  В методе *симплетекст:: креатедевицеиндепендентресаурцес* в файле реализации класса (симплетекст. cpp) вызовите функцию [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) , чтобы создать интерфейс [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , который является корневым интерфейсом фабрики для всех объектов [Direct2D](../direct2d/direct2d-portal.md) . Вы используете ту же фабрику для создания экземпляров других ресурсов Direct2D.
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  Вызовите функцию [**двритекреатефактори**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) , чтобы создать интерфейс [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) , который является корневым интерфейсом фабрики для всех объектов [DirectWrite](direct-write-portal.md) . Вы используете ту же фабрику для создания экземпляров других ресурсов DirectWrite.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  Инициализируйте текстовую строку и сохраняет ее длину.

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  Создайте объект интерфейса [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) с помощью метода [**Идвритефактори:: креатетекстформат**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) . **Идвритетекстформат** задает шрифт, вес, растяжение, стиль и языковой стандарт, которые будут использоваться для отрисовки текстовой строки.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  Центрирование текста по горизонтали и вертикали путем вызова методов [**идвритетекстформат:: сеттексталигнмент**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) и [**Идвритетекстформат:: сетпараграфалигнмент**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) .
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

В этой части были инициализированы независимые от устройства ресурсы, используемые приложением. В следующей части вы инициализируем ресурсы, зависящие от устройства.

### <a name="part-3-create-device-dependent-resources"></a>Часть 3. Создание ресурсов Device-Dependent.

В этой части вы создадите [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) и [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) для отрисовки текста.

Цель отрисовки — это объект Direct2D, который создает ресурсы рисования и визуализирует команды рисования на устройстве отрисовки. [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) — это целевой объект отрисовки, который готовится к просмотру в **HWND**.

Одним из ресурсов рисования, которые может создать целевой объект рендеринга, является кисть для рисования контуров, заливок и текста. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) закрашивается сплошным цветом.

Интерфейсы [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) и [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) привязываются к устройству отрисовки, когда они создаются и должны быть освобождены и созданы повторно, если устройство станет недействительным.

1.  В методе Симплетекст:: Креатедевицересаурцес проверьте, имеет ли указатель целевого объекта прорисовки **значение NULL**. Если это так, извлеките размер области рендеринга и создайте [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) этого размера. Используйте **ID2D1HwndRenderTarget** для создания [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  В методе Симплетекст::D Искарддевицересаурцес Освободите и кисть, и целевой объект прорисовки.
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

Теперь, когда вы создали целевой объект отрисовки и кисть, их можно использовать для визуализации текста.

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a>Часть 4. Рисование текста с помощью метода Direct2D DrawText.

1.  В методе Симплетекст::D Равтекст класса определите область для макета текста, извлекая размеры области отрисовки и создав прямоугольник [Direct2D](../direct2d/direct2d-portal.md) с теми же размерами.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Используйте метод [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) и объект [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) для отрисовки текста на экране. Метод **ID2D1RenderTarget::D равтекст** принимает следующие параметры:
    -   Строка для отображения.
    -   Указатель на интерфейс [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .
    -   Прямоугольник макета [Direct2D](../direct2d/direct2d-portal.md) .
    -   Указатель на интерфейс, предоставляющий [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a>Часть 5. Отрисовка содержимого окна с помощью Direct2D

Чтобы отобразить содержимое окна с помощью [Direct2D](../direct2d/direct2d-portal.md) при получении сообщения Paint, выполните следующие действия.

1.  Создайте ресурсы, зависимые от устройства, вызвав метод Симплетекст:: Креатедевицересаурцес, реализованный в части 3.
2.  Вызовите метод [**ID2D1HwndRenderTarget:: бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) целевого объекта прорисовки.
3.  Очистите целевой объект отрисовки, вызвав метод [**ID2D1HwndRenderTarget:: Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) .
4.  Вызовите метод Симплетекст::D Равтекст, реализованный в части 4.
5.  Вызовите метод [**ID2D1HwndRenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) целевого объекта прорисовки.
6.  При необходимости удалите ресурсы, зависящие от устройства, чтобы их можно было повторно создать при перерисовке окна.


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



Класс Симплетекст реализован в Симплетекст. h и Симплетекст. cpp.

## <a name="drawing-text-with-multiple-formats"></a>Рисование текста с несколькими форматами.

В этом разделе показано, как использовать [DirectWrite](direct-write-portal.md) и [Direct2D](../direct2d/direct2d-portal.md) для отрисовки текста с несколькими форматами, как показано на следующем снимке экрана.

![снимок экрана: "Hello World, используя DirectWrite!", с некоторыми частями в различных стилях, размерах и форматах](images/multiformattedcropped.png)

Код для этого раздела реализуется как класс Мултиформаттедтекст в [примере двритехелловорлд](/samples/browse/?redirectedfrom=MSDN-samples). Он основан на шагах из предыдущего раздела.

Чтобы создать многострочный текст, в дополнение к интерфейсу [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , представленному в предыдущем разделе, используется интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Интерфейс **идвритетекстлайаут** Описывает форматирование и компоновку блока текста. В дополнение к форматированию по умолчанию, заданному объектом **идвритетекстформат** , форматирование для отдельных диапазонов текста можно изменить с помощью **идвритетекстлайаут**. К ним относятся имя семейства шрифтов, размер, вес, стиль, растяжение, зачеркнутый и подчеркивание.

[**Идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) также предоставляет методы проверки попадания. Метрики проверки попадания, возвращаемые этими методами, задаются относительно поля макета, заданного при создании объекта интерфейса **идвритетекстлайаут** с помощью метода [**креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) интерфейса [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .

Интерфейс [**идвритетипографи**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) используется для добавления дополнительных типографских функций [OpenType](../intl/opentype-font-format.md) в макет текста, таких как каллиграфические символы и альтернативные наборы стилистических текстовых наборов. Типографские функции можно добавлять к конкретному фрагменту текста в макете, вызывая метод [**аддфонтфеатуре**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) интерфейса **идвритетипографи** . Этот метод получает структуру [**\_ \_ возможностей шрифта дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) в качестве параметра, который содержит константу перечисления **\_ \_ \_ тега функции шрифта дврите** и параметр выполнения **UINT32** . Список зарегистрированных функций OpenType можно найти в [реестре тегов макета OpenType](https://www.microsoft.com/typography/otspec/features_ae.htm) на Microsoft.com. Эквивалентные константы перечисления DirectWrite см. в разделе **\_ \_ \_ тег функции шрифта дврите**.

### <a name="part-1-create-an-idwritetextlayout-interface"></a>Часть 1. Создание интерфейса Идвритетекстлайаут.

1.  Объявите указатель на интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) в качестве члена класса мултиформаттедтекст.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  В конце метода Мултиформаттедтекст:: Креатедевицеиндепендентресаурцес создайте объект интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , вызвав метод [**креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) . Интерфейс **идвритетекстлайаут** предоставляет дополнительные возможности форматирования, такие как возможность применения различных форматов к выбранным фрагментам текста.
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a>Часть 2. Применение форматирования с помощью Идвритетекстлайаут.

Форматирование, например размер шрифта, вес и подчеркивание, можно применить к подстрокам текста, отображаемым с помощью интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

1.  Установите размер шрифта для подстроки "Di" из "DirectWrite" в значение 100, объявив [**\_ \_ диапазон текста дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) и вызвав метод [**идвритетекстлайаут:: сетфонтсизе**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) .
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  Подчеркивание подстроки "DirectWrite" путем вызова метода [**идвритетекстлайаут:: сетундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) .
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  Установите жирный шрифт для подстроки "DirectWrite", вызвав метод [**идвритетекстлайаут:: сетфонтвеигхт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) .
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a>Часть 3. Добавление типографских функций с помощью Идвритетипографи.

1.  Объявите и создайте объект интерфейса [**идвритетипографи**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) , вызвав метод [**Идвритефактори:: креатетипографи**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) .
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  Добавьте функцию шрифта, объявив объект [**\_ \_ функции шрифта дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) с указанным набором стилистических 7 и вызвав метод [**идвритетипографи:: аддфонтфеатуре**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) .
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  Задайте макет текста для использования оформления всей строки путем объявления переменной [**\_ \_ диапазона текста дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) и вызова метода [**идвритетекстлайаут:: сеттипографи**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) и передачи текстового диапазона.
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  Задайте новую ширину и высоту для объекта макета текста в методе Мултиформаттедтекст:: Онресизе.
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a>Часть 4. Рисование текста с помощью метода Direct2D Дравтекстлайаут.

Чтобы нарисовать текст с параметрами макета текста, заданными в объекте [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , измените код в методе мултиформаттедтекст::D равтекст, чтобы использовать [**Идвритетекстлайаут::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).

1.  Делкаре переменную [**D2D1 \_ \_ 2F**](../direct2d/d2d1-point-2f.md) и установите ее в верхнюю левую точку окна.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Выведите текст на экран, вызвав метод [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) целевого объекта прорисовки [Direct2D](../direct2d/direct2d-portal.md) и передав указатель [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

Класс Мултиформаттедтекст реализован в Мултиформаттедтекст. h и Мултиформаттедтекст. cpp.

 

 