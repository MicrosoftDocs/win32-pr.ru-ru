---
title: Выполнение проверки нажатия на макете текста
description: Содержит краткое руководство по добавлению проверки попадания в приложение DirectWrite, которое отображает текст с помощью интерфейса Идвритетекстлайаут.
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca80ac641920c4e63c08f4cbb0fd9e24eb7b2d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "103999994"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a><span data-ttu-id="6effb-103">Выполнение проверки нажатия на макете текста</span><span class="sxs-lookup"><span data-stu-id="6effb-103">How to Perform Hit Testing on a Text Layout</span></span>

<span data-ttu-id="6effb-104">Содержит краткое руководство по добавлению проверки попадания в приложение [DirectWrite](direct-write-portal.md) , которое отображает текст с помощью интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6effb-104">Provides a short tutorial about how to add hit testing to a [DirectWrite](direct-write-portal.md) application that displays text by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="6effb-105">Результатом работы с этим руководством является приложение, которое подчеркивает символ, который щелкнули левой кнопкой мыши, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="6effb-105">The result of this tutorial is an application that underlines the character that is clicked on by the left mouse button, as shown in the following screen shot.</span></span>

![снимок экрана "щелкните этот текст"](images/hittest.png)

<span data-ttu-id="6effb-107">В этом примере содержатся следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="6effb-107">This how to contains the following parts:</span></span>

- [<span data-ttu-id="6effb-108">Шаг 1. Создание макета текста.</span><span class="sxs-lookup"><span data-stu-id="6effb-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
- [<span data-ttu-id="6effb-109">Шаг 2. Добавление метода OnClick.</span><span class="sxs-lookup"><span data-stu-id="6effb-109">Step 2: Add an OnClick method.</span></span>](#step-2-add-an-onclick-method)
- [<span data-ttu-id="6effb-110">Шаг 3. Проверка нажатия.</span><span class="sxs-lookup"><span data-stu-id="6effb-110">Step 3: Perform Hit Testing.</span></span>](#step-3-perform-hit-testing)
- [<span data-ttu-id="6effb-111">Шаг 4. подчеркивание текста, на который выполнен щелчок.</span><span class="sxs-lookup"><span data-stu-id="6effb-111">Step 4: Underline the Clicked Text.</span></span>](#step-4-underline-the-clicked-text)
- [<span data-ttu-id="6effb-112">Шаг 5. Обработайте \_ сообщение WM лбуттондовн.</span><span class="sxs-lookup"><span data-stu-id="6effb-112">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>](/windows)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="6effb-113">Шаг 1. Создание макета текста.</span><span class="sxs-lookup"><span data-stu-id="6effb-113">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="6effb-114">Для начала вам потребуется приложение, использующее объект [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6effb-114">To begin, you will need an application that uses an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="6effb-115">Если у вас уже есть приложение, отображающее текст с макетом, перейдите к шагу 2.</span><span class="sxs-lookup"><span data-stu-id="6effb-115">If you already have an application that displays text with a text layout, go to Step 2.</span></span>

<span data-ttu-id="6effb-116">Чтобы добавить текстовый макет, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6effb-116">To add a text layout you must do the following:</span></span>

1. <span data-ttu-id="6effb-117">Объявите указатель на интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) в качестве члена класса.</span><span class="sxs-lookup"><span data-stu-id="6effb-117">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. <span data-ttu-id="6effb-118">В конце метода **креатедевицеиндепендентресаурцес** создайте объект интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , вызвав метод [**креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6effb-118">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>

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

3. <span data-ttu-id="6effb-119">Затем необходимо изменить вызов метода [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) на [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="6effb-119">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) as shown in the following code.</span></span>

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a><span data-ttu-id="6effb-120">Шаг 2. Добавление метода OnClick.</span><span class="sxs-lookup"><span data-stu-id="6effb-120">Step 2: Add an OnClick method.</span></span>

<span data-ttu-id="6effb-121">Теперь добавьте в класс метод, который будет использовать функцию проверки нажатия в макете текста.</span><span class="sxs-lookup"><span data-stu-id="6effb-121">Now add a method to the class that will use the hit testing functionality of the text layout.</span></span>

1. <span data-ttu-id="6effb-122">Объявите метод **OnClick** в файле заголовка класса.</span><span class="sxs-lookup"><span data-stu-id="6effb-122">Declare an **OnClick** method in the class header file.</span></span>

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. <span data-ttu-id="6effb-123">Определите метод **OnClick** в файле реализации класса.</span><span class="sxs-lookup"><span data-stu-id="6effb-123">Define an **OnClick** method in the class implementation file.</span></span>

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a><span data-ttu-id="6effb-124">Шаг 3. Проверка нажатия.</span><span class="sxs-lookup"><span data-stu-id="6effb-124">Step 3: Perform Hit Testing.</span></span>

<span data-ttu-id="6effb-125">Чтобы определить, где пользователь щелкнул макет текста, мы будем использовать метод [**идвритетекстлайаут:: хиттестпоинт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .</span><span class="sxs-lookup"><span data-stu-id="6effb-125">To determine where the user has clicked the text layout we will use the [**IDWriteTextLayout::HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

<span data-ttu-id="6effb-126">Добавьте следующий фрагмент в метод **OnClick** , определенный на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="6effb-126">Add the following to the **OnClick** method that you defined in Step 2.</span></span>

1. <span data-ttu-id="6effb-127">Объявите переменные, которые будут переданы в метод в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="6effb-127">Declare the variables we will pass as parameters to the method.</span></span>

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    <span data-ttu-id="6effb-128">Метод [**хиттестпоинт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) выводит следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="6effb-128">The [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method outputs the following parameters.</span></span>

    | <span data-ttu-id="6effb-129">Переменная</span><span class="sxs-lookup"><span data-stu-id="6effb-129">Variable</span></span>         | <span data-ttu-id="6effb-130">Описание</span><span class="sxs-lookup"><span data-stu-id="6effb-130">Description</span></span>                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="6effb-131">*хиттестметрикс*</span><span class="sxs-lookup"><span data-stu-id="6effb-131">*hitTestMetrics*</span></span> | <span data-ttu-id="6effb-132">Геометрия, полностью охватывающая место проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="6effb-132">The geometry fully enclosing the hit-test location.</span></span>                                                                                     |
    | <span data-ttu-id="6effb-133">*Внутрь*</span><span class="sxs-lookup"><span data-stu-id="6effb-133">*isInside*</span></span>       | <span data-ttu-id="6effb-134">Указывает, находится ли место проверки попадания внутри текстовой строки или нет.</span><span class="sxs-lookup"><span data-stu-id="6effb-134">Indicates whether the hit-test location is inside the text string or not.</span></span> <span data-ttu-id="6effb-135">Если значение равно FALSE, возвращается ближайшее к границе текста расположение.</span><span class="sxs-lookup"><span data-stu-id="6effb-135">When FALSE, the position nearest the text's edge is returned.</span></span> |
    | <span data-ttu-id="6effb-136">*истраилингхит*</span><span class="sxs-lookup"><span data-stu-id="6effb-136">*isTrailingHit*</span></span>  | <span data-ttu-id="6effb-137">Указывает, находится ли место проверки попадания в начале или конце символа.</span><span class="sxs-lookup"><span data-stu-id="6effb-137">Indicates whether the hit-test location is at the leading or the trailing side of the character.</span></span>                                        |

2. <span data-ttu-id="6effb-138">Вызовите метод [**хиттестпоинт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) объекта [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6effb-138">Call the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method of the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    <span data-ttu-id="6effb-139">Код в этом примере передает переменные *x* и *y* для данной должности без каких бы то ни было изменений.</span><span class="sxs-lookup"><span data-stu-id="6effb-139">The code in this example passes the *x* and *y* variables for the position without any modification.</span></span> <span data-ttu-id="6effb-140">Это можно сделать в этом примере, так как макет текста имеет тот же размер, что и окно, и находится в левом верхнем углу окна.</span><span class="sxs-lookup"><span data-stu-id="6effb-140">This can be done in this example because the text layout is the same size as the window and originates in the upper-left corner of the window.</span></span> <span data-ttu-id="6effb-141">Если это не так, необходимо было бы определить координаты относительно начала макета текста.</span><span class="sxs-lookup"><span data-stu-id="6effb-141">If this was not the case, you would have to determine the coordinates in relation to the origin of the text layout.</span></span>

## <a name="step-4-underline-the-clicked-text"></a><span data-ttu-id="6effb-142">Шаг 4. подчеркивание текста, на который выполнен щелчок.</span><span class="sxs-lookup"><span data-stu-id="6effb-142">Step 4: Underline the Clicked Text.</span></span>

<span data-ttu-id="6effb-143">Добавьте следующий элемент в **OnClick** , определенный на шаге 2, после вызова метода [**хиттестпоинт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .</span><span class="sxs-lookup"><span data-stu-id="6effb-143">Add the following to the **OnClick** you defined in Step 2, after the call to the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

<span data-ttu-id="6effb-144">Этот код выполняет следующие программы.</span><span class="sxs-lookup"><span data-stu-id="6effb-144">This code does the following.</span></span>

1. <span data-ttu-id="6effb-145">Проверяет, находится ли точка проверки попадания в тексте с помощью *переменной in* .</span><span class="sxs-lookup"><span data-stu-id="6effb-145">Checks if the hit-test point was inside the text using the *isInside* variable.</span></span>
2. <span data-ttu-id="6effb-146">Элемент **текстпоситион** структуры *хиттестметрикс* содержит Отсчитываемый от нуля индекс символа, который щелкнули.</span><span class="sxs-lookup"><span data-stu-id="6effb-146">The **textPosition** member of the *hitTestMetrics* structure contains the zero-based index of the character clicked.</span></span>

    <span data-ttu-id="6effb-147">Получает подчеркивание для этого символа путем передачи этого значения в метод [**идвритетекстлайаут:: черкивания**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) .</span><span class="sxs-lookup"><span data-stu-id="6effb-147">Gets the underline for this character by passing this value to the [**IDWriteTextLayout::GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) method.</span></span>

3. <span data-ttu-id="6effb-148">Объявляет переменную [**\_ \_ диапазона текста дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) с начальной позицией, равной **хиттестметрикс. текстпоситион** , и длиной 1.</span><span class="sxs-lookup"><span data-stu-id="6effb-148">Declares a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable with the start position set to **hitTestMetrics.textPosition** and a length of 1.</span></span>
4. <span data-ttu-id="6effb-149">Переключает подчеркивание с помощью метода [**идвритетекстлайаут:: сетундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) .</span><span class="sxs-lookup"><span data-stu-id="6effb-149">Toggles the underline by using the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>

<span data-ttu-id="6effb-150">После установки подчеркивания перерисуйте текст, вызвав метод **DrawD2DContent** класса.</span><span class="sxs-lookup"><span data-stu-id="6effb-150">After setting the underline, redraw the text by calling the **DrawD2DContent** method of the class.</span></span>

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a><span data-ttu-id="6effb-151">Шаг 5. Обработайте \_ сообщение WM лбуттондовн.</span><span class="sxs-lookup"><span data-stu-id="6effb-151">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>

<span data-ttu-id="6effb-152">Наконец, добавьте сообщение **WM \_ лбуттондовн** в обработчик сообщений для вашего приложения и вызовите метод **OnClick** класса.</span><span class="sxs-lookup"><span data-stu-id="6effb-152">Finally, add the **WM\_LBUTTONDOWN** message to the message handler for your application and call the **OnClick** method of the class.</span></span>

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

<span data-ttu-id="6effb-153">**Получить \_ Макросы x \_ lParam** и **Get \_ x \_ lParam** объявляются в файле заголовка виндовскс. h.</span><span class="sxs-lookup"><span data-stu-id="6effb-153">**GET\_X\_LPARAM** and **GET\_X\_LPARAM** macros are declared in the windowsx.h header file.</span></span> <span data-ttu-id="6effb-154">Они легко извлекают координаты x и y щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="6effb-154">They easily retrieve the x and y position of the mouse click.</span></span>
