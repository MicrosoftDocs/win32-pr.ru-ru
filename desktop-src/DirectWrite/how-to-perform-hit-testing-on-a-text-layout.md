---
title: Выполнение проверки нажатия на макете текста
description: содержит краткое руководство по добавлению проверки попадания в DirectWrite приложение, которое отображает текст с помощью интерфейса идвритетекстлайаут.
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d42967b069a7a5008de75c1cecb453a6158857eb2b05d2dd0298584a67cef69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816577"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a>Выполнение проверки нажатия на макете текста

содержит краткое руководство по добавлению проверки попадания в [DirectWrite](direct-write-portal.md) приложение, которое отображает текст с помощью интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Результатом работы с этим руководством является приложение, которое подчеркивает символ, который щелкнули левой кнопкой мыши, как показано на следующем снимке экрана.

![снимок экрана "щелкните этот текст"](images/hittest.png)

В этом примере содержатся следующие компоненты:

- [Шаг 1. Создание макета текста.](#step-1-create-a-text-layout)
- [Шаг 2. Добавление метода OnClick.](#step-2-add-an-onclick-method)
- [Шаг 3. Проверка нажатия.](#step-3-perform-hit-testing)
- [Шаг 4. подчеркивание текста, на который выполнен щелчок.](#step-4-underline-the-clicked-text)
- [Шаг 5. Обработайте \_ сообщение WM лбуттондовн.](/windows)

## <a name="step-1-create-a-text-layout"></a>Шаг 1. Создание макета текста.

Для начала вам потребуется приложение, использующее объект [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Если у вас уже есть приложение, отображающее текст с макетом, перейдите к шагу 2.

Чтобы добавить текстовый макет, необходимо выполнить следующие действия.

1. Объявите указатель на интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) в качестве члена класса.

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. В конце метода **креатедевицеиндепендентресаурцес** создайте объект интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , вызвав метод [**креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .

    ```cpp
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

3. Затем необходимо изменить вызов метода [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) на [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , как показано в следующем коде.

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a>Шаг 2. Добавление метода OnClick.

Теперь добавьте в класс метод, который будет использовать функцию проверки нажатия в макете текста.

1. Объявите метод **OnClick** в файле заголовка класса.

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. Определите метод **OnClick** в файле реализации класса.

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a>Шаг 3. Проверка нажатия.

Чтобы определить, где пользователь щелкнул макет текста, мы будем использовать метод [**идвритетекстлайаут:: хиттестпоинт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .

Добавьте следующий фрагмент в метод **OnClick** , определенный на шаге 2.

1. Объявите переменные, которые будут переданы в метод в качестве параметров.

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    Метод [**хиттестпоинт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) выводит следующие параметры.

    | Переменная         | Описание                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | *хиттестметрикс* | Геометрия, полностью охватывающая место проверки попадания.                                                                                     |
    | *Внутрь*       | Указывает, находится ли место проверки попадания внутри текстовой строки или нет. Если значение равно FALSE, возвращается ближайшее к границе текста расположение. |
    | *истраилингхит*  | Указывает, находится ли место проверки попадания в начале или конце символа.                                        |

2. Вызовите метод [**хиттестпоинт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) объекта [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    Код в этом примере передает переменные *x* и *y* для данной должности без каких бы то ни было изменений. Это можно сделать в этом примере, так как макет текста имеет тот же размер, что и окно, и находится в левом верхнем углу окна. Если это не так, необходимо было бы определить координаты относительно начала макета текста.

## <a name="step-4-underline-the-clicked-text"></a>Шаг 4. подчеркивание текста, на который выполнен щелчок.

Добавьте следующий элемент в **OnClick** , определенный на шаге 2, после вызова метода [**хиттестпоинт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

Этот код выполняет следующие программы.

1. Проверяет, находится ли точка проверки попадания в тексте с помощью *переменной in* .
2. Элемент **текстпоситион** структуры *хиттестметрикс* содержит Отсчитываемый от нуля индекс символа, который щелкнули.

    Получает подчеркивание для этого символа путем передачи этого значения в метод [**идвритетекстлайаут:: черкивания**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) .

3. Объявляет переменную [**\_ \_ диапазона текста дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) с начальной позицией, равной **хиттестметрикс. текстпоситион** , и длиной 1.
4. Переключает подчеркивание с помощью метода [**идвритетекстлайаут:: сетундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) .

После установки подчеркивания перерисуйте текст, вызвав метод **DrawD2DContent** класса.

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a>Шаг 5. Обработайте \_ сообщение WM лбуттондовн.

Наконец, добавьте сообщение **WM \_ лбуттондовн** в обработчик сообщений для вашего приложения и вызовите метод **OnClick** класса.

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

**Получить \_ Макросы x \_ lParam** и **Get \_ x \_ lParam** объявляются в файле заголовка виндовскс. h. Они легко извлекают координаты x и y щелчка мыши.
