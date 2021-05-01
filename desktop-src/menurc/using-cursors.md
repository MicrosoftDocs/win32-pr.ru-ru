---
title: Использование курсоров
description: В этом разделе приводятся примеры кода, демонстрирующие выполнение задач, связанных с курсорами.
ms.assetid: eab7b781-783e-4fc5-868d-6ff773c40a21
keywords:
- ресурсы, курсоры
- курсоры, пользовательские
- пользовательские курсоры
- курсор песочных часов
- курсоры, создание
- курсоры, Песочные часы
- создание курсоров
- уничтожение курсоров
- Отображение курсоров
- ограничивать курсоры
- курсоры, уничтожение
- курсоры, отображение
- курсоры, ограничивать
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cf681fd17f3e79e4559e9936be232ae09f8453
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327129"
---
# <a name="using-cursors"></a><span data-ttu-id="6b0a4-116">Использование курсоров</span><span class="sxs-lookup"><span data-stu-id="6b0a4-116">Using Cursors</span></span>

<span data-ttu-id="6b0a4-117">В этом разделе рассматриваются следующие темы.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-117">This section discusses the following topics.</span></span>

-   [<span data-ttu-id="6b0a4-118">Создание курсора</span><span class="sxs-lookup"><span data-stu-id="6b0a4-118">Creating a Cursor</span></span>](#creating-a-cursor)
-   [<span data-ttu-id="6b0a4-119">Отображение курсора</span><span class="sxs-lookup"><span data-stu-id="6b0a4-119">Displaying a Cursor</span></span>](#displaying-a-cursor)
-   [<span data-ttu-id="6b0a4-120">Ограничивать курсор</span><span class="sxs-lookup"><span data-stu-id="6b0a4-120">Confining a Cursor</span></span>](#confining-a-cursor)
-   [<span data-ttu-id="6b0a4-121">Использование функций Cursor для создания Маусетрап</span><span class="sxs-lookup"><span data-stu-id="6b0a4-121">Using Cursor Functions to Create a Mousetrap</span></span>](#using-cursor-functions-to-create-a-mousetrap)
-   [<span data-ttu-id="6b0a4-122">Перемещение курсора с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="6b0a4-122">Using the Keyboard to Move the Cursor</span></span>](#using-the-keyboard-to-move-the-cursor)

## <a name="creating-a-cursor"></a><span data-ttu-id="6b0a4-123">Создание курсора</span><span class="sxs-lookup"><span data-stu-id="6b0a4-123">Creating a Cursor</span></span>

<span data-ttu-id="6b0a4-124">В следующем примере создаются два маркера курсора: один для стандартного курсора песочных часов и один для пользовательского курсора, включаемого в качестве ресурса в файл определения ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-124">The following example creates two cursor handles: one for the standard hourglass cursor and one for a custom cursor included as a resource in the application's resource-definition file.</span></span>


```
HINSTANCE hinst;            // handle to current instance 
HCURSOR hCurs1, hCurs2;     // cursor handles 
 
// Create a standard hourglass cursor. 
 
hCurs1 = LoadCursor(NULL, IDC_WAIT); 
 
// Create a custom cursor based on a resource. 
 
hCurs2 = LoadCursor(hinst, MAKEINTRESOURCE(240)); 
```



<span data-ttu-id="6b0a4-125">В качестве ресурсов следует реализовывать пользовательские курсоры.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-125">You should implement custom cursors as resources.</span></span> <span data-ttu-id="6b0a4-126">Вместо того чтобы создавать курсоры во время выполнения, используйте функцию [**лоадкурсор**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**лоадкурсорфромфиле**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)или [**лоадимаже**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) , чтобы избежать зависимости от устройства, упростить локализацию и позволить приложениям совместно использовать макеты курсоров.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-126">Rather than create the cursors at run time, use the [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea), or [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) function to avoid device dependence, to simplify localization, and to enable applications to share cursor designs.</span></span>

<span data-ttu-id="6b0a4-127">В следующем примере функция [**креатекурсор**](/windows/desktop/api/Winuser/nf-winuser-createcursor) используется для создания пользовательского курсора во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-127">The following example uses the [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) function to create a custom cursor at run time.</span></span> <span data-ttu-id="6b0a4-128">Пример приведен здесь, чтобы продемонстрировать, как система интерпретирует маски курсора.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-128">The example is included here to illustrate how the system interprets cursor masks.</span></span>


```
HINSTANCE hinst;            // handle to current instance  
HCURSOR hCurs1, hCurs2;     // cursor handles 
 
HCURSOR hCurs3;             // cursor handle 
 
// Yin-shaped cursor AND mask 
 
BYTE ANDmaskCursor[] = 
{ 
    0xFF, 0xFC, 0x3F, 0xFF,   // line 1 
    0xFF, 0xC0, 0x1F, 0xFF,   // line 2 
    0xFF, 0x00, 0x3F, 0xFF,   // line 3 
    0xFE, 0x00, 0xFF, 0xFF,   // line 4 
 
    0xF7, 0x01, 0xFF, 0xFF,   // line 5 
    0xF0, 0x03, 0xFF, 0xFF,   // line 6 
    0xF0, 0x03, 0xFF, 0xFF,   // line 7 
    0xE0, 0x07, 0xFF, 0xFF,   // line 8 
 
    0xC0, 0x07, 0xFF, 0xFF,   // line 9 
    0xC0, 0x0F, 0xFF, 0xFF,   // line 10 
    0x80, 0x0F, 0xFF, 0xFF,   // line 11 
    0x80, 0x0F, 0xFF, 0xFF,   // line 12 
 
    0x80, 0x07, 0xFF, 0xFF,   // line 13 
    0x00, 0x07, 0xFF, 0xFF,   // line 14 
    0x00, 0x03, 0xFF, 0xFF,   // line 15 
    0x00, 0x00, 0xFF, 0xFF,   // line 16 
 
    0x00, 0x00, 0x7F, 0xFF,   // line 17 
    0x00, 0x00, 0x1F, 0xFF,   // line 18 
    0x00, 0x00, 0x0F, 0xFF,   // line 19 
    0x80, 0x00, 0x0F, 0xFF,   // line 20 
 
    0x80, 0x00, 0x07, 0xFF,   // line 21 
    0x80, 0x00, 0x07, 0xFF,   // line 22 
    0xC0, 0x00, 0x07, 0xFF,   // line 23 
    0xC0, 0x00, 0x0F, 0xFF,   // line 24 
 
    0xE0, 0x00, 0x0F, 0xFF,   // line 25 
    0xF0, 0x00, 0x1F, 0xFF,   // line 26 
    0xF0, 0x00, 0x1F, 0xFF,   // line 27 
    0xF8, 0x00, 0x3F, 0xFF,   // line 28 
 
    0xFE, 0x00, 0x7F, 0xFF,   // line 29 
    0xFF, 0x00, 0xFF, 0xFF,   // line 30 
    0xFF, 0xC3, 0xFF, 0xFF,   // line 31 
    0xFF, 0xFF, 0xFF, 0xFF    // line 32 
};
 
// Yin-shaped cursor XOR mask 
 
BYTE XORmaskCursor[] = 
{ 
    0x00, 0x00, 0x00, 0x00,   // line 1 
    0x00, 0x03, 0xC0, 0x00,   // line 2 
    0x00, 0x3F, 0x00, 0x00,   // line 3 
    0x00, 0xFE, 0x00, 0x00,   // line 4 
 
    0x0E, 0xFC, 0x00, 0x00,   // line 5 
    0x07, 0xF8, 0x00, 0x00,   // line 6 
    0x07, 0xF8, 0x00, 0x00,   // line 7 
    0x0F, 0xF0, 0x00, 0x00,   // line 8 
 
    0x1F, 0xF0, 0x00, 0x00,   // line 9 
    0x1F, 0xE0, 0x00, 0x00,   // line 10 
    0x3F, 0xE0, 0x00, 0x00,   // line 11 
    0x3F, 0xE0, 0x00, 0x00,   // line 12 
 
    0x3F, 0xF0, 0x00, 0x00,   // line 13 
    0x7F, 0xF0, 0x00, 0x00,   // line 14 
    0x7F, 0xF8, 0x00, 0x00,   // line 15 
    0x7F, 0xFC, 0x00, 0x00,   // line 16 
 
    0x7F, 0xFF, 0x00, 0x00,   // line 17 
    0x7F, 0xFF, 0x80, 0x00,   // line 18 
    0x7F, 0xFF, 0xE0, 0x00,   // line 19 
    0x3F, 0xFF, 0xE0, 0x00,   // line 20 
 
    0x3F, 0xC7, 0xF0, 0x00,   // line 21 
    0x3F, 0x83, 0xF0, 0x00,   // line 22 
    0x1F, 0x83, 0xF0, 0x00,   // line 23 
    0x1F, 0x83, 0xE0, 0x00,   // line 24 
 
    0x0F, 0xC7, 0xE0, 0x00,   // line 25 
    0x07, 0xFF, 0xC0, 0x00,   // line 26 
    0x07, 0xFF, 0xC0, 0x00,   // line 27 
    0x01, 0xFF, 0x80, 0x00,   // line 28 
 
    0x00, 0xFF, 0x00, 0x00,   // line 29 
    0x00, 0x3C, 0x00, 0x00,   // line 30 
    0x00, 0x00, 0x00, 0x00,   // line 31 
    0x00, 0x00, 0x00, 0x00    // line 32 
};
 
// Create a custom cursor at run time. 
 
hCurs3 = CreateCursor( hinst,   // app. instance 
             19,                // horizontal position of hot spot 
             2,                 // vertical position of hot spot 
             32,                // cursor width 
             32,                // cursor height 
             ANDmaskCursor,     // AND mask 
             XORmaskCursor );   // XOR mask 
```



<span data-ttu-id="6b0a4-129">Чтобы создать курсор, [**креатекурсор**](/windows/desktop/api/Winuser/nf-winuser-createcursor) применяет следующую таблицу истинности к маскам **and** и **XOR** .</span><span class="sxs-lookup"><span data-stu-id="6b0a4-129">To create the cursor, [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) applies the following truth table to the **AND** and **XOR** masks.</span></span>



| <span data-ttu-id="6b0a4-130">И маска</span><span class="sxs-lookup"><span data-stu-id="6b0a4-130">AND mask</span></span> | <span data-ttu-id="6b0a4-131">Маска XOR</span><span class="sxs-lookup"><span data-stu-id="6b0a4-131">XOR mask</span></span> | <span data-ttu-id="6b0a4-132">Отображение</span><span class="sxs-lookup"><span data-stu-id="6b0a4-132">Display</span></span>        |
|----------|----------|----------------|
| <span data-ttu-id="6b0a4-133">0</span><span class="sxs-lookup"><span data-stu-id="6b0a4-133">0</span></span>        | <span data-ttu-id="6b0a4-134">0</span><span class="sxs-lookup"><span data-stu-id="6b0a4-134">0</span></span>        | <span data-ttu-id="6b0a4-135">Черный</span><span class="sxs-lookup"><span data-stu-id="6b0a4-135">Black</span></span>          |
| <span data-ttu-id="6b0a4-136">0</span><span class="sxs-lookup"><span data-stu-id="6b0a4-136">0</span></span>        | <span data-ttu-id="6b0a4-137">1</span><span class="sxs-lookup"><span data-stu-id="6b0a4-137">1</span></span>        | <span data-ttu-id="6b0a4-138">Белый</span><span class="sxs-lookup"><span data-stu-id="6b0a4-138">White</span></span>          |
| <span data-ttu-id="6b0a4-139">1</span><span class="sxs-lookup"><span data-stu-id="6b0a4-139">1</span></span>        | <span data-ttu-id="6b0a4-140">0</span><span class="sxs-lookup"><span data-stu-id="6b0a4-140">0</span></span>        | <span data-ttu-id="6b0a4-141">Screen</span><span class="sxs-lookup"><span data-stu-id="6b0a4-141">Screen</span></span>         |
| <span data-ttu-id="6b0a4-142">1</span><span class="sxs-lookup"><span data-stu-id="6b0a4-142">1</span></span>        | <span data-ttu-id="6b0a4-143">1</span><span class="sxs-lookup"><span data-stu-id="6b0a4-143">1</span></span>        | <span data-ttu-id="6b0a4-144">Обратный экран</span><span class="sxs-lookup"><span data-stu-id="6b0a4-144">Reverse screen</span></span> |



 

<span data-ttu-id="6b0a4-145">Дополнительные сведения см. в разделе [точечные рисунки](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="6b0a4-145">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

<span data-ttu-id="6b0a4-146">Перед закрытием необходимо использовать функцию [**дестройкурсор**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) , чтобы уничтожить все курсоры, созданные с помощью [**креатекурсор**](/windows/desktop/api/Winuser/nf-winuser-createcursor).</span><span class="sxs-lookup"><span data-stu-id="6b0a4-146">Before closing, you must use the [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) function to destroy any cursors you created with [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor).</span></span> <span data-ttu-id="6b0a4-147">Нет необходимости удалять курсоры, созданные другими функциями.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-147">It is not necessary to destroy cursors created by other functions.</span></span>

## <a name="displaying-a-cursor"></a><span data-ttu-id="6b0a4-148">Отображение курсора</span><span class="sxs-lookup"><span data-stu-id="6b0a4-148">Displaying a Cursor</span></span>

<span data-ttu-id="6b0a4-149">Система автоматически отображает курсор класса (курсор, связанный с окном, на которое указывает курсор).</span><span class="sxs-lookup"><span data-stu-id="6b0a4-149">The system automatically displays the class cursor (the cursor associated with the window to which the cursor is pointing).</span></span> <span data-ttu-id="6b0a4-150">При регистрации класса окна можно назначить курсор класса.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-150">You can assign a class cursor while registering a window class.</span></span> <span data-ttu-id="6b0a4-151">В следующем примере показано, как назначить маркер курсора элементу **хкурсор** структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) , определяемой параметром *WC* .</span><span class="sxs-lookup"><span data-stu-id="6b0a4-151">The following example illustrates this by assigning a cursor handle to the **hCursor** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure identified by the *wc* parameter.</span></span>


```
WNDCLASS  wc; 
 
// Fill the window class structure with parameters that 
// describe the main window. 
 
wc.style = NULL;                        // class style(s) 
wc.lpfnWndProc = (WNDPROC) MainWndProc; // window procedure 
wc.cbClsExtra = 0;           // no per-class extra data 
wc.cbWndExtra = 0;           // no per-window extra data 
wc.hInstance = hinst;        // application that owns the class 
wc.hIcon = LoadIcon(NULL, IDI_APPLICATION);     // class icon 
wc.hCursor = LoadCursor(hinst, MAKEINTRESOURCE(230)); // class cursor 
wc.hbrBackground = GetStockObject(WHITE_BRUSH); // class background 
wc.lpszMenuName =  "GenericMenu";               // class menu 
wc.lpszClassName = "GenericWClass"              // class name 
 
// Register the window class. 
 
return RegisterClass(&wc); 
```



<span data-ttu-id="6b0a4-152">Когда класс окна зарегистрирован, курсор по умолчанию для всех окон, 230 определяемый в файле определения ресурсов приложения, является курсором, установленным в данном приложении.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-152">When the window class is registered, the cursor identified by 230 in the application's resource-definition file is the default cursor for all windows based on the class.</span></span>

<span data-ttu-id="6b0a4-153">Приложение может изменить структуру курсора с помощью функции [**сеткурсор**](/windows/desktop/api/Winuser/nf-winuser-setcursor) и указания другого маркера курсора.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-153">Your application can change the design of the cursor by using the [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) function and specifying a different cursor handle.</span></span> <span data-ttu-id="6b0a4-154">Однако при перемещении курсора система перерисовывает курсор класса в новом месте.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-154">However, when the cursor moves, the system redraws the class cursor at the new location.</span></span> <span data-ttu-id="6b0a4-155">Чтобы предотвратить перерисовку курсора класса, необходимо обработать сообщение [**WM \_ сеткурсор**](wm-setcursor.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0a4-155">To prevent the class cursor from being redrawn, you must process the [**WM\_SETCURSOR**](wm-setcursor.md) message.</span></span> <span data-ttu-id="6b0a4-156">При каждом перемещении курсора и вводе с помощью мыши система отправляет это сообщение в окно, в котором курсор перемещается.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-156">Each time the cursor moves and mouse input is not captured, the system sends this message to the window in which the cursor is moving.</span></span>

<span data-ttu-id="6b0a4-157">При обработке [**WM \_ сеткурсор**](wm-setcursor.md)можно указать разные курсоры для различных условий.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-157">You can specify different cursors for different conditions while processing [**WM\_SETCURSOR**](wm-setcursor.md).</span></span> <span data-ttu-id="6b0a4-158">Например, в следующем примере показано, как отобразить курсор при перемещении курсора над значком сворачивания приложения.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-158">For example, the following example shows how to display the cursor whenever the cursor moves over the icon of a minimized application.</span></span>


```
case WM_SETCURSOR: 
 
    // If the window is minimized, draw the hCurs3 cursor. 
    // If the window is not minimized, draw the default 
    // cursor (class cursor). 
 
    if (IsIconic(hwnd)) 
    { 
        SetCursor(hCurs3); 
        break; 
    } 
```



<span data-ttu-id="6b0a4-159">Когда окно не свернется, система отображает курсор класса.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-159">When the window is not minimized, the system displays the class cursor.</span></span>

<span data-ttu-id="6b0a4-160">Можно заменить курсор класса с помощью функции [**сеткласслонг**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) .</span><span class="sxs-lookup"><span data-stu-id="6b0a4-160">You can replace a class cursor by using the [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) function.</span></span> <span data-ttu-id="6b0a4-161">Эта функция изменяет параметры окна по умолчанию для всех окон указанного класса.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-161">This function changes the default window settings for all windows of a specified class.</span></span> <span data-ttu-id="6b0a4-162">В следующем примере существующий курсор класса заменяется `hCurs2` курсором.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-162">The following example replaces the existing class cursor with the `hCurs2` cursor.</span></span>


```
// Change the cursor for window class represented by hwnd. 
 
SetClassLongPtr(hwnd,    // window handle 
    GCLP_HCURSOR,        // change cursor 
    (LONG_PTR) hCurs2);  // new cursor 
```



<span data-ttu-id="6b0a4-163">Дополнительные сведения см. в разделе [классы окон](/windows/desktop/winmsg/window-classes) и ввод с помощью [мыши](/windows/desktop/inputdev/mouse-input).</span><span class="sxs-lookup"><span data-stu-id="6b0a4-163">For more information, see [Window Classes](/windows/desktop/winmsg/window-classes) and [Mouse Input](/windows/desktop/inputdev/mouse-input).</span></span>

## <a name="confining-a-cursor"></a><span data-ttu-id="6b0a4-164">Ограничивать курсор</span><span class="sxs-lookup"><span data-stu-id="6b0a4-164">Confining a Cursor</span></span>

<span data-ttu-id="6b0a4-165">В следующем примере курсор ограничивается окном приложения, а затем курсор восстанавливается в предыдущее окно.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-165">The following example confines the cursor to the application's window and then restores the cursor to its previous window.</span></span> <span data-ttu-id="6b0a4-166">В примере используется функция [**жетклипкурсор**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) для записи области, в которой курсор может перемещаться, и функция [**клипкурсор**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) для ограничения и восстановления курсора.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-166">The example uses the [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) function to record the area in which the cursor can move and the [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) function to confine and restore the cursor.</span></span>


```
RECT rcClip;           // new area for ClipCursor
RECT rcOldClip;        // previous area for ClipCursor
 
// Record the area in which the cursor can move. 
 
GetClipCursor(&rcOldClip); 
 
// Get the dimensions of the application's window. 
 
GetWindowRect(hwnd, &rcClip); 
 
// Confine the cursor to the application's window. 
 
ClipCursor(&rcClip); 
 
   // 
   // Process input from the confined cursor. 
   // 
 
// Restore the cursor to its previous area. 
 
ClipCursor(&rcOldClip); 
```



<span data-ttu-id="6b0a4-167">Поскольку в системе доступно только один курсор, приложение, которое ограничивает курсор, должно восстановить курсор до того, как оно будет восстановлено в другом окне.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-167">Because there is only one cursor at a time available in the system, an application that confines the cursor must restore the cursor before relinquishing control to another window.</span></span>

## <a name="using-cursor-functions-to-create-a-mousetrap"></a><span data-ttu-id="6b0a4-168">Использование функций Cursor для создания Маусетрап</span><span class="sxs-lookup"><span data-stu-id="6b0a4-168">Using Cursor Functions to Create a Mousetrap</span></span>

<span data-ttu-id="6b0a4-169">В следующем примере для создания простого сеткурсор используются функции [**сеткурсорпос**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos), [**жеткурсорпос**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos), [**креатекурсор**](/windows/desktop/api/Winuser/nf-winuser-createcursor), [**лоадкурсор**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)и [**маусетрап**](/windows/desktop/api/Winuser/nf-winuser-setcursor) .</span><span class="sxs-lookup"><span data-stu-id="6b0a4-169">The following example uses the [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos), [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos), [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor), [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), and [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) functions to create a simple mousetrap.</span></span> <span data-ttu-id="6b0a4-170">Он также использует функции курсора и таймера для отслеживания положения курсора каждые 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-170">It also uses cursor and timer functions to monitor the cursor's position every 10 seconds.</span></span> <span data-ttu-id="6b0a4-171">Если позиции курсора не изменились в течение последних 10 секунд, а главное окно приложения является минимальным, приложение изменяет курсор и перемещает его на значок маусетрап.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-171">If the cursor position has not changed in the last 10 seconds and the application's main window is minimized, the application changes the cursor and moves it to the mousetrap icon.</span></span>

<span data-ttu-id="6b0a4-172">Пример аналогичного маусетрап включается в [значки](icons.md).</span><span class="sxs-lookup"><span data-stu-id="6b0a4-172">An example for a similar mousetrap is included in [Icons](icons.md).</span></span> <span data-ttu-id="6b0a4-173">Он использует функции [**лоадкурсор**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) и [**лоадикон**](/windows/desktop/api/Winuser/nf-winuser-loadicona) вместо более зависимых от устройства функций [**креатекурсор**](/windows/desktop/api/Winuser/nf-winuser-createcursor) и [**креатеикон**](/windows/desktop/api/Winuser/nf-winuser-createicon) .</span><span class="sxs-lookup"><span data-stu-id="6b0a4-173">It uses the [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) and [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) functions instead of the more device-dependent [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) and [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) functions.</span></span>


```
HICON hIcon1;               // icon handles 
POINT ptOld;                // previous cursor location 
HCURSOR hCurs1;             // cursor handle 
 
 
// The following cursor masks are defined in a code 
// example that appears earlier in this section. 
 
// Yin-shaped cursor AND and XOR masks 
 
BYTE ANDmaskCursor[] = ... 
BYTE XORmaskCursor[] = ... 
 
// Yang-shaped icon AND mask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,  // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,  // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,  // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,  // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,  // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,  // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,  // line 7 
                      0xFF, 0xF0, 0x00, 0x07,  // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,  // line 9 
                      0xFF, 0xE0, 0x00, 0x03,  // line 10 
                      0xFF, 0xE0, 0x00, 0x01,  // line 11 
                      0xFF, 0xE0, 0x00, 0x01,  // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,  // line 13 
                      0xFF, 0xF0, 0x00, 0x00,  // line 14 
                      0xFF, 0xF8, 0x00, 0x00,  // line 15 
                      0xFF, 0xFC, 0x00, 0x00,  // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,  // line 17 
                      0xFF, 0xFF, 0x80, 0x00,  // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,  // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,  // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,  // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,  // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,  // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,  // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,  // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,  // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,  // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,  // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,  // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,  // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,  // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF}; // line 32 
 
// Yang-shaped icon XOR mask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,  // line 1 
                      0x00, 0x00, 0x00, 0x00,  // line 2 
                      0x00, 0x00, 0x00, 0x00,  // line 3 
                      0x00, 0x00, 0x00, 0x00,  // line 4 
 
                      0x00, 0x00, 0x00, 0x00,  // line 5 
                      0x00, 0x00, 0x00, 0x00,  // line 6 
                      0x00, 0x00, 0x00, 0x00,  // line 7 
                      0x00, 0x00, 0x38, 0x00,  // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,  // line 9 
                      0x00, 0x00, 0x7C, 0x00,  // line 10 
                      0x00, 0x00, 0x7C, 0x00,  // line 11  
                      0x00, 0x00, 0x38, 0x00,  // line 12 
 
                      0x00, 0x00, 0x00, 0x00,  // line 13 
                      0x00, 0x00, 0x00, 0x00,  // line 14 
                      0x00, 0x00, 0x00, 0x00,  // line 15 
                      0x00, 0x00, 0x00, 0x00,  // line 16 
 
                      0x00, 0x00, 0x00, 0x00,  // line 17 
                      0x00, 0x00, 0x00, 0x00,  // line 18 
                      0x00, 0x00, 0x00, 0x00,  // line 19 
                      0x00, 0x00, 0x00, 0x00,  // line 20 
 
                      0x00, 0x00, 0x00, 0x00,  // line 21 
                      0x00, 0x00, 0x00, 0x00,  // line 22 
                      0x00, 0x00, 0x00, 0x00,  // line 23 
                      0x00, 0x00, 0x00, 0x00,  // line 24 
 
                      0x00, 0x00, 0x00, 0x00,  // line 25 
                      0x00, 0x00, 0x00, 0x00,  // line 26 
                      0x00, 0x00, 0x00, 0x00,  // line 27 
                      0x00, 0x00, 0x00, 0x00,  // line 28 
 
                      0x00, 0x00, 0x00, 0x00,  // line 29 
                      0x00, 0x00, 0x00, 0x00,  // line 30 
                      0x00, 0x00, 0x00, 0x00,  // line 31 
                      0x00, 0x00, 0x00, 0x00}; // line 32 
 
hIcon1 = CreateIcon(hinst, // handle to app. instance 
             32,           // icon width 
             32,           // icon height 
             1,            // number of XOR planes 
             1,            // number of bits per pixel 
             ANDmaskIcon,  // AND mask 
             XORmaskIcon); // XOR mask 
 
hCurs1 = CreateCursor(hinst, // handle to app. instance
             19,             // horizontal position of hot spot 
             2,              // vertical position of hot spot 
             32,             // cursor width 
             32,             // cursor height 
             ANDmaskCursor,  // AND mask 
             XORmaskCursor); // XOR mask 
 
// Fill in the window class structure. 
 
WNDCLASS  wc; 
 
wc.hIcon = hIcon1;                        // class icon 
wc.hCursor = LoadCursor(NULL, IDC_ARROW); // class cursor 
 
//
// Register the window class and perform 
// other application initialization. 
//
 
// Set a timer for the mousetrap. 
 
GetCursorPos(&ptOld); 
 
SetTimer(hwnd, IDT_CURSOR, 10000, (TIMERPROC) NULL); 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // window handle 
    UINT message,       // type of message 
    UINT wParam,        // additional information 
    LONG lParam)        // additional information 
{ 
 
    HDC hdc;            // handle to device context 
    POINT pt;           // current cursor location 
    RECT rc;            // minimized window location 
 
    switch (message) 
    { 
        //
        // Process other messages. 
        // 
        case WM_TIMER: 
        // If the window is minimized, compare the 
        // current cursor position with the one 10 
        // seconds before. If the cursor position has 
        // not changed, move the cursor to the icon. 
 
            if (IsIconic(hwnd)) 
            { 
                GetCursorPos(&pt); 
 
                if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
                { 
                    GetWindowRect(hwnd, &rc); 
                    SetCursorPos(rc.left + 20, rc.top + 4); 
 
                    // Note that the additional constants 
                    // (20 and 4) are application-specific 
                    // values to align the yin-shaped cursor 
                    // and the yang-shaped icon. 
 
                } 
                else 
                { 
                    ptOld.x = pt.x; 
                    ptOld.y = pt.y; 
                } 
            } 
 
            return 0; 
 
        case WM_SETCURSOR: 
        // If the window is minimized, draw hCurs1. 
        // If the window is not minimized, draw the 
        // default cursor (class cursor). 
 
            if (IsIconic(hwnd)) 
            { 
                SetCursor(hCurs1); 
                break; 
            } 
 
        case WM_DESTROY: 
        // Destroy timer. 
 
            KillTimer(hwnd, IDT_CURSOR); 
 
            PostQuitMessage(0); 
            break; 
    } 
} 
```



## <a name="using-the-keyboard-to-move-the-cursor"></a><span data-ttu-id="6b0a4-174">Перемещение курсора с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="6b0a4-174">Using the Keyboard to Move the Cursor</span></span>

<span data-ttu-id="6b0a4-175">Поскольку система не требует мыши, приложение должно имитировать действия мыши с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-175">Because the system does not require a mouse, an application should be able to simulate mouse actions with the keyboard.</span></span> <span data-ttu-id="6b0a4-176">В следующем примере показано, как добиться этого с помощью функций [**жеткурсорпос**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) и [**сеткурсорпос**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) , а также путем обработки входных данных из клавиш со стрелками.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-176">The following example shows how to achieve this by using the [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) and [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) functions and by processing input from the arrow keys.</span></span>


```
HCURSOR hCurs1, hCurs2;    // cursor handles 
 
POINT pt;                  // cursor location  
RECT rc;                   // client area coordinates 
static int repeat = 1;     // repeat key counter 
 
// 
// Other declarations and initialization. 
// 
 
switch (message) 
{ 
// 
// Process other messages. 
// 
 
    case WM_KEYDOWN: 
 
        if (wParam != VK_LEFT && wParam != VK_RIGHT && 
        wParam != VK_UP && wParam != VK_DOWN) 
        { 
            break; 
        } 
 
        GetCursorPos(&pt); 
 
        // Convert screen coordinates to client coordinates. 
 
        ScreenToClient(hwnd, &pt); 
 
        switch (wParam) 
        { 
        // Move the cursor to reflect which 
        // arrow keys are pressed. 
 
            case VK_LEFT:               // left arrow 
                pt.x -= repeat; 
                break; 
 
            case VK_RIGHT:              // right arrow 
                pt.x += repeat; 
                break; 
 
            case VK_UP:                 // up arrow 
                pt.y -= repeat; 
                break; 
 
            case VK_DOWN:               // down arrow 
                pt.y += repeat; 
                break; 
 
            default: 
                return 0; 
        } 
 
        repeat++;           // Increment repeat count. 
 
        // Keep the cursor in the client area. 
 
        GetClientRect(hwnd, &rc); 
 
        if (pt.x >= rc.right) 
        { 
            pt.x = rc.right - 1; 
        } 
        else 
        { 
            if (pt.x < rc.left) 
            { 
                pt.x = rc.left; 
            } 
        } 
 
        if (pt.y >= rc.bottom) 
            pt.y = rc.bottom - 1; 
        else 
            if (pt.y < rc.top) 
                pt.y = rc.top; 
 
        // Convert client coordinates to screen coordinates. 
 
        ClientToScreen(hwnd, &pt); 
        SetCursorPos(pt.x, pt.y); 
        return 0; 

 
    case WM_KEYUP: 
 
        repeat = 1;            // Clear repeat count. 
        return 0; 
 
} 
```



 

 
