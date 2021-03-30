---
title: Использование меню
description: В этом разделе приведены примеры кода для задач, связанных с меню.
ms.assetid: b1391e37-a146-46ec-a329-aa57cfcfd351
keywords:
- ресурсы, меню
- меню, создание
- меню — ресурсы шаблона
- ресурсы, меню-шаблон
- Расширенное меню — Формат шаблона
- формат шаблона старого меню
- меню загрузки — ресурсы шаблона
- меню, класс
- меню, ярлык
- Создание меню
- меню классов
- контекстные меню
- точечные рисунки пункта меню
- меню, рисуемых владельцем
- меню, рисуемое владельцем
- пользовательские растровые флажки
- меню, флажки
- меню, шрифты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d216b5fe5e6c25a98b5bdf3abe9d55b4bb0b34f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791214"
---
# <a name="using-menus"></a><span data-ttu-id="fde4f-121">Использование меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-121">Using Menus</span></span>

<span data-ttu-id="fde4f-122">В этом разделе описаны следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="fde4f-122">This section describes the following tasks:</span></span>

-   [<span data-ttu-id="fde4f-123">Использование ресурса Menu-Template</span><span class="sxs-lookup"><span data-stu-id="fde4f-123">Using a Menu-Template Resource</span></span>](#using-a-menu-template-resource)
    -   [<span data-ttu-id="fde4f-124">Расширенный формат Menu-Template</span><span class="sxs-lookup"><span data-stu-id="fde4f-124">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
    -   [<span data-ttu-id="fde4f-125">Старый формат Menu-Template</span><span class="sxs-lookup"><span data-stu-id="fde4f-125">Old Menu-Template Format</span></span>](#old-menu-template-format)
    -   [<span data-ttu-id="fde4f-126">Загрузка ресурса Menu-Template</span><span class="sxs-lookup"><span data-stu-id="fde4f-126">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
    -   [<span data-ttu-id="fde4f-127">Создание меню класса</span><span class="sxs-lookup"><span data-stu-id="fde4f-127">Creating a Class Menu</span></span>](#creating-a-class-menu)
-   [<span data-ttu-id="fde4f-128">Создание контекстного меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-128">Creating a Shortcut Menu</span></span>](#creating-a-shortcut-menu)
    -   [<span data-ttu-id="fde4f-129">Обработка сообщения WM \_ CONTEXTMENU</span><span class="sxs-lookup"><span data-stu-id="fde4f-129">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
    -   [<span data-ttu-id="fde4f-130">Создание контекстного меню Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="fde4f-130">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
    -   [<span data-ttu-id="fde4f-131">Отображение контекстного меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-131">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)
-   [<span data-ttu-id="fde4f-132">Использование точечных рисунков Menu-Item</span><span class="sxs-lookup"><span data-stu-id="fde4f-132">Using Menu-Item Bitmaps</span></span>](#using-menu-item-bitmaps)
    -   [<span data-ttu-id="fde4f-133">Установка флага типа точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="fde4f-133">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
    -   [<span data-ttu-id="fde4f-134">Создание точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="fde4f-134">Creating the Bitmap</span></span>](#creating-the-bitmap)
    -   [<span data-ttu-id="fde4f-135">Добавление линий и графиков в меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-135">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
    -   [<span data-ttu-id="fde4f-136">Пример Menu-Item точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="fde4f-136">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)
-   [<span data-ttu-id="fde4f-137">Создание пунктов меню Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="fde4f-137">Creating Owner-Drawn Menu Items</span></span>](#creating-owner-drawn-menu-items)
    -   [<span data-ttu-id="fde4f-138">Установка флага Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="fde4f-138">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
    -   [<span data-ttu-id="fde4f-139">Меню, рисуемые владельцем, и \_ сообщение WM меасуреитем</span><span class="sxs-lookup"><span data-stu-id="fde4f-139">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="fde4f-140">Меню, рисуемые владельцем, и \_ сообщение WM DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="fde4f-140">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="fde4f-141">Меню, рисуемые владельцем, и \_ сообщение WM менучар</span><span class="sxs-lookup"><span data-stu-id="fde4f-141">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
    -   [<span data-ttu-id="fde4f-142">Установка шрифтов для Menu-Item текстовых строк</span><span class="sxs-lookup"><span data-stu-id="fde4f-142">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
    -   [<span data-ttu-id="fde4f-143">Пример пунктов меню Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="fde4f-143">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)
-   [<span data-ttu-id="fde4f-144">Использование пользовательских точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="fde4f-144">Using Custom Check Mark Bitmaps</span></span>](#using-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="fde4f-145">Создание пользовательских точечных рисунков с галочками</span><span class="sxs-lookup"><span data-stu-id="fde4f-145">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="fde4f-146">Связывание точечных рисунков с пунктом меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-146">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
    -   [<span data-ttu-id="fde4f-147">Установка атрибута галочки</span><span class="sxs-lookup"><span data-stu-id="fde4f-147">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
    -   [<span data-ttu-id="fde4f-148">Имитация флажков в меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-148">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
    -   [<span data-ttu-id="fde4f-149">Пример использования пользовательских точечных рисунков с галочкой</span><span class="sxs-lookup"><span data-stu-id="fde4f-149">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a><span data-ttu-id="fde4f-150">Использование ресурса Menu-Template</span><span class="sxs-lookup"><span data-stu-id="fde4f-150">Using a Menu-Template Resource</span></span>

<span data-ttu-id="fde4f-151">Обычно меню включается в приложение путем создания ресурса шаблона меню и последующей загрузки меню во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-151">You typically include a menu in an application by creating a menu-template resource and then loading the menu at run time.</span></span> <span data-ttu-id="fde4f-152">В этом разделе описывается формат шаблона меню и объясняется, как загрузить ресурс шаблона меню и использовать его в приложении.</span><span class="sxs-lookup"><span data-stu-id="fde4f-152">This section describes the format of a menu template, and explains how to load a menu-template resource and use it in your application.</span></span> <span data-ttu-id="fde4f-153">Сведения о создании ресурса шаблона меню см. в документации, входящей в состав средств разработки.</span><span class="sxs-lookup"><span data-stu-id="fde4f-153">For information about creating a menu-template resource, see the documentation included with your development tools.</span></span>

-   [<span data-ttu-id="fde4f-154">Расширенный формат Menu-Template</span><span class="sxs-lookup"><span data-stu-id="fde4f-154">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
-   [<span data-ttu-id="fde4f-155">Старый формат Menu-Template</span><span class="sxs-lookup"><span data-stu-id="fde4f-155">Old Menu-Template Format</span></span>](#old-menu-template-format)
-   [<span data-ttu-id="fde4f-156">Загрузка ресурса Menu-Template</span><span class="sxs-lookup"><span data-stu-id="fde4f-156">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
-   [<span data-ttu-id="fde4f-157">Создание меню класса</span><span class="sxs-lookup"><span data-stu-id="fde4f-157">Creating a Class Menu</span></span>](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a><span data-ttu-id="fde4f-158">Расширенный формат Menu-Template</span><span class="sxs-lookup"><span data-stu-id="fde4f-158">Extended Menu-Template Format</span></span>

<span data-ttu-id="fde4f-159">Расширенный формат шаблона меню поддерживает дополнительные функции меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-159">The extended menu-template format supports additional menu functionality.</span></span> <span data-ttu-id="fde4f-160">Как и в стандартном меню — ресурсы шаблона, расширенные ресурсы шаблона меню — это тип ресурса **\_ меню RT** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-160">Like standard menu-template resources, extended menu-template resources have the **RT\_MENU** resource type.</span></span> <span data-ttu-id="fde4f-161">Система различает два формата ресурсов по номеру версии, который является первым элементом в заголовке ресурса.</span><span class="sxs-lookup"><span data-stu-id="fde4f-161">The system distinguishes the two resource formats by the version number, which is the first member of the resource header.</span></span>

<span data-ttu-id="fde4f-162">Расширенный шаблон меню состоит из структуры [**\_ \_ заголовка шаблона менуекс**](menuex-template-header.md) , за которой следуют еще одна структура определения элемента [**\_ шаблона \_ менуекс**](menuex-template-item.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-162">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one more [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) item definition structures.</span></span>

### <a name="old-menu-template-format"></a><span data-ttu-id="fde4f-163">Старый формат Menu-Template</span><span class="sxs-lookup"><span data-stu-id="fde4f-163">Old Menu-Template Format</span></span>

<span data-ttu-id="fde4f-164">Шаблон старого меню (Microsoft Windows NT 3,51 и более ранних версий) определяет меню, но не поддерживает новые функции меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-164">An old menu template (Microsoft Windows NT 3.51 and earlier) defines a menu, but does not support the new menu functionality.</span></span> <span data-ttu-id="fde4f-165">Старый ресурс шаблона меню имеет тип ресурса **\_ меню RT** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-165">An old menu-template resource has the **RT\_MENU** resource type.</span></span>

<span data-ttu-id="fde4f-166">Старый шаблон меню состоит из структуры [**менуитемтемплатехеадер**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) , за которой следует одна или несколько структур [**менуитемтемплате**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-166">An old menu template consists of a [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) structure followed by one or more [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) structures.</span></span>

### <a name="loading-a-menu-template-resource"></a><span data-ttu-id="fde4f-167">Загрузка ресурса Menu-Template</span><span class="sxs-lookup"><span data-stu-id="fde4f-167">Loading a Menu-Template Resource</span></span>

<span data-ttu-id="fde4f-168">Чтобы загрузить ресурс шаблона меню, используйте функцию [**лоадмену**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) , указав маркер для модуля, содержащего ресурс, и идентификатор шаблона меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-168">To load a menu-template resource, use the [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) function, specifying a handle to the module that contains the resource and the menu template's identifier.</span></span> <span data-ttu-id="fde4f-169">Функция **лоадмену** возвращает маркер меню, который можно использовать для назначения меню окну.</span><span class="sxs-lookup"><span data-stu-id="fde4f-169">The **LoadMenu** function returns a menu handle that you can use to assign the menu to a window.</span></span> <span data-ttu-id="fde4f-170">Это окно станет окном «владелец» меню, получающим все сообщения, созданные в меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-170">This window becomes the menu's owner window, receiving all the messages generated by the menu.</span></span>

<span data-ttu-id="fde4f-171">Чтобы создать меню из шаблона меню, который уже находится в памяти, используйте функцию [**лоадменуиндирект**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-171">To create a menu from a menu template that is already in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span> <span data-ttu-id="fde4f-172">Это полезно, если приложение создает шаблоны меню динамически.</span><span class="sxs-lookup"><span data-stu-id="fde4f-172">This is useful if your application generates menu templates dynamically.</span></span>

<span data-ttu-id="fde4f-173">Чтобы назначить меню окну, используйте функцию [**сетмену**](/windows/desktop/api/Winuser/nf-winuser-setmenu) или укажите маркер меню в параметре *HMENU* функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) при создании окна.</span><span class="sxs-lookup"><span data-stu-id="fde4f-173">To assign a menu to a window, use the [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) function or specify the menu's handle in the *hMenu* parameter of the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function when creating a window.</span></span> <span data-ttu-id="fde4f-174">Другой способ назначения меню окну — Указание шаблона меню при регистрации класса окна; шаблон определяет указанное меню в качестве меню класса для этого класса окна.</span><span class="sxs-lookup"><span data-stu-id="fde4f-174">Another way you can assign a menu to a window is to specify a menu template when you register a window class; the template identifies the specified menu as the class menu for that window class.</span></span>

<span data-ttu-id="fde4f-175">Чтобы система автоматически назначила определенное меню окну, укажите шаблон меню при регистрации класса окна.</span><span class="sxs-lookup"><span data-stu-id="fde4f-175">To have the system automatically assign a specific menu to a window, specify the menu's template when you register the window's class.</span></span> <span data-ttu-id="fde4f-176">Шаблон определяет указанное меню в качестве меню класса для этого класса окна.</span><span class="sxs-lookup"><span data-stu-id="fde4f-176">The template identifies the specified menu as the class menu for that window class.</span></span> <span data-ttu-id="fde4f-177">Затем, когда вы создаете окно указанного класса, система автоматически назначает указанное меню окну.</span><span class="sxs-lookup"><span data-stu-id="fde4f-177">Then, when you create a window of the specified class, the system automatically assigns the specified menu to the window.</span></span>

<span data-ttu-id="fde4f-178">Нельзя назначить меню окну, которое является дочерним окном.</span><span class="sxs-lookup"><span data-stu-id="fde4f-178">You cannot assign a menu to a window that is a child window.</span></span>

<span data-ttu-id="fde4f-179">Чтобы создать меню класса, включите идентификатор ресурса меню-шаблона в качестве элемента **лпсзменунаме** структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) , а затем передайте указатель на структуру функции [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-179">To create a class menu, include the identifier of the menu-template resource as the **lpszMenuName** member of a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure and then pass a pointer to the structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span>

### <a name="creating-a-class-menu"></a><span data-ttu-id="fde4f-180">Создание меню класса</span><span class="sxs-lookup"><span data-stu-id="fde4f-180">Creating a Class Menu</span></span>

<span data-ttu-id="fde4f-181">В следующем примере показано, как создать меню класса для приложения, создать окно, которое использует меню «класс» и команды «обработать» в процедуре окна.</span><span class="sxs-lookup"><span data-stu-id="fde4f-181">The following example shows how to create a class menu for an application, create a window that uses the class menu, and process menu commands in the window procedure.</span></span>

<span data-ttu-id="fde4f-182">Ниже приведена соответствующая часть файла заголовка приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-182">Following is the relevant portion of the application's header file:</span></span>


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



<span data-ttu-id="fde4f-183">Ниже перечислены соответствующие части самого приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-183">Following are the relevant portions of the application itself:</span></span>


```
HINSTANCE hinst; 
 
int APIENTRY WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg = { };  // message 
    WNDCLASS wc;    // windowclass data 
    HWND hwnd;      // handle to the main window 
 
    // Create the window class for the main window. Specify 
    // the identifier of the menu-template resource as the 
    // lpszMenuName member of the WNDCLASS structure to create 
    // the class menu. 
 
    wc.style = 0; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  MAKEINTRESOURCE(IDM_MYMENURESOURCE); 
    wc.lpszClassName = "MainWClass"; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    hinst = hinstance; 
 
    // Create the main window. Set the hmenu parameter to NULL so 
    // that the system uses the class menu for the window. 
 
    hwnd = CreateWindow("MainWClass", "Sample Application", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, hinstance, 
        NULL); 
 
    if (hwnd == NULL) 
        return FALSE; 
 
    // Make the window visible and send a WM_PAINT message to the 
    // window procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
 
    // Start the main message loop. 
 
    while (GetMessage(&msg, NULL, 0, 0)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(hPrevInstance); 
} 
 
 
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    switch (uMsg) 
    { 
        // Process other window messages. 
 
        case WM_COMMAND: 
 
            // Test for the identifier of a command item. 
 
            switch(LOWORD(wParam)) 
            { 
                case IDM_FI_OPEN: 
                    DoFileOpen();   // application-defined 
                    break; 
 
                case IDM_FI_CLOSE: 
                    DoFileClose();  // application-defined 
                    break; 
                // Process other menu commands. 
 
                default: 
                    break; 
 
            } 
            return 0; 
 
        // Process other window messages. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="creating-a-shortcut-menu"></a><span data-ttu-id="fde4f-184">Создание контекстного меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-184">Creating a Shortcut Menu</span></span>

<span data-ttu-id="fde4f-185">Чтобы использовать контекстное меню в приложении, передайте его обработчик функции [**траккпопупменуекс**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-185">To use a shortcut menu in an application, pass its handle to the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="fde4f-186">Приложение обычно вызывает **траккпопупменуекс** в оконной процедуре в ответ на генерируемое пользователем сообщение, например [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown) или [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown).</span><span class="sxs-lookup"><span data-stu-id="fde4f-186">An application typically calls **TrackPopupMenuEx** in a window procedure in response to a user-generated message, such as [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown).</span></span>

<span data-ttu-id="fde4f-187">Помимо маркера всплывающего меню, [**траккпопупменуекс**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) требует указать маркер для окна владельца, позицию контекстного меню (в экранных координатах) и кнопку мыши, которую пользователь может использовать для выбора элемента.</span><span class="sxs-lookup"><span data-stu-id="fde4f-187">In addition to the pop-up menu handle, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) requires that you specify a handle to the owner window, the position of the shortcut menu (in screen coordinates), and the mouse button that the user can use to choose an item.</span></span>

<span data-ttu-id="fde4f-188">Старая функция [**метод TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) по-прежнему поддерживается, но новые приложения должны использовать функцию [**траккпопупменуекс**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-188">The older [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function is still supported, but new applications should use the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="fde4f-189">Функция **траккпопупменуекс** требует те же параметры, что и **метод TrackPopupMenu**, но также позволяет указать часть экрана, которую меню не должно скрывать.</span><span class="sxs-lookup"><span data-stu-id="fde4f-189">The **TrackPopupMenuEx** function requires the same parameters as **TrackPopupMenu**, but also lets you specify a portion of the screen that the menu should not obscure.</span></span> <span data-ttu-id="fde4f-190">Приложение обычно вызывает эти функции в оконной процедуре при обработке сообщения [**WM \_ CONTEXTMENU**](wm-contextmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-190">An application typically calls these functions in a window procedure when processing the [**WM\_CONTEXTMENU**](wm-contextmenu.md) message.</span></span>

<span data-ttu-id="fde4f-191">Можно указать расположение контекстного меню, указав координаты x и y вместе с флагом **TPM \_ центералигн**, **TPM \_ Лефталигн** или **\_ RIGHTALIGN доверенного платформенного модуля** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-191">You can specify the position of a shortcut menu by providing x- and y-coordinates along with the **TPM\_CENTERALIGN**, **TPM\_LEFTALIGN**, or **TPM\_RIGHTALIGN** flag.</span></span> <span data-ttu-id="fde4f-192">Флаг задает расположение контекстного меню относительно координат x и y.</span><span class="sxs-lookup"><span data-stu-id="fde4f-192">The flag specifies the position of the shortcut menu relative to the x- and y-coordinates.</span></span>

<span data-ttu-id="fde4f-193">Необходимо предоставить пользователю возможность выбирать элемент из контекстного меню, используя ту же кнопку мыши, которая используется для вывода меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-193">You should permit the user to choose an item from a shortcut menu by using the same mouse button used to display the menu.</span></span> <span data-ttu-id="fde4f-194">Для этого укажите флаг **TPM \_ Лефтбуттон** или **TPM \_ ригхтбуттон** , чтобы указать, какая кнопка мыши может использоваться для выбора пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-194">To do this, specify either **TPM\_LEFTBUTTON** or **TPM\_RIGHTBUTTON** flag to indicate which mouse button the user can use to choose a menu item.</span></span>

-   [<span data-ttu-id="fde4f-195">Обработка сообщения WM \_ CONTEXTMENU</span><span class="sxs-lookup"><span data-stu-id="fde4f-195">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
-   [<span data-ttu-id="fde4f-196">Создание контекстного меню Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="fde4f-196">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
-   [<span data-ttu-id="fde4f-197">Отображение контекстного меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-197">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a><span data-ttu-id="fde4f-198">Обработка сообщения WM \_ CONTEXTMENU</span><span class="sxs-lookup"><span data-stu-id="fde4f-198">Processing the WM\_CONTEXTMENU Message</span></span>

<span data-ttu-id="fde4f-199">Сообщение [**WM \_ CONTEXTMENU**](wm-contextmenu.md) создается, когда процедура окна приложения передает сообщение [**WM \_ рбуттонуп**](/windows/desktop/inputdev/wm-rbuttonup) или [**WM \_ нкрбуттонуп**](/windows/desktop/inputdev/wm-ncrbuttonup) в функцию [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-199">The [**WM\_CONTEXTMENU**](wm-contextmenu.md) message is generated when an application's window procedure passes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="fde4f-200">Приложение может обработать это сообщение, чтобы отобразить контекстное меню, соответствующее определенной части экрана.</span><span class="sxs-lookup"><span data-stu-id="fde4f-200">The application can process this message to display a shortcut menu appropriate to a specific portion of its screen.</span></span> <span data-ttu-id="fde4f-201">Если в приложении не отображается контекстное меню, оно должно передавать сообщение **дефвиндовпрок** для обработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fde4f-201">If the application does not display a shortcut menu, it should pass the message to **DefWindowProc** for default handling.</span></span>

<span data-ttu-id="fde4f-202">Ниже приведен пример обработки сообщений [**WM \_ CONTEXTMENU**](wm-contextmenu.md) , как это может появиться в процедуре окна приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-202">Following is an example of [**WM\_CONTEXTMENU**](wm-contextmenu.md) message processing as it might appear in an application's window procedure.</span></span> <span data-ttu-id="fde4f-203">Слова с низким и высоким порядком параметров *lParam* определяют экранные координаты мыши при отпускании правой кнопки мыши (Обратите внимание, что эти координаты могут принимать отрицательные значения в системах с несколькими мониторами).</span><span class="sxs-lookup"><span data-stu-id="fde4f-203">The low-order and high-order words of the *lParam* parameter specify the screen coordinates of the mouse when the right mouse button is released (note that these coordinates can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="fde4f-204">Определяемая приложением функция **oncontextmenu** возвращает **значение true** , если она отображает контекстное меню, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="fde4f-204">The application-defined **OnContextMenu** function returns **TRUE** if it displays a context menu, or **FALSE** if it does not.</span></span>


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



<span data-ttu-id="fde4f-205">Следующая определяемая приложением функция oncontextmenu отображает контекстное меню, если указанная позицией мыши находится в клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="fde4f-205">The following application-defined OnContextMenu function displays a shortcut menu if the specified mouse position is within the window's client area.</span></span> <span data-ttu-id="fde4f-206">Более сложная функция может отображать одно из нескольких различных меню в зависимости от того, какая часть клиентской области задана.</span><span class="sxs-lookup"><span data-stu-id="fde4f-206">A more sophisticated function might display one of several different menus, depending on which portion of the client area is specified.</span></span> <span data-ttu-id="fde4f-207">Для фактического вывода контекстного меню в этом примере вызывается определяемая приложением функция с именем Дисплайконтекстмену.</span><span class="sxs-lookup"><span data-stu-id="fde4f-207">To actually display the shortcut menu, this example calls an application-defined function called DisplayContextMenu.</span></span> <span data-ttu-id="fde4f-208">Описание этой функции см. [в разделе Отображение контекстного меню](#displaying-a-shortcut-menu).</span><span class="sxs-lookup"><span data-stu-id="fde4f-208">For a description of this function, see [Displaying a Shortcut Menu](#displaying-a-shortcut-menu).</span></span>


```
BOOL WINAPI OnContextMenu(HWND hwnd, int x, int y) 
{ 
    RECT rc;                    // client area of window 
    POINT pt = { x, y };        // location of mouse click 
 
    // Get the bounding rectangle of the client area. 
 
    GetClientRect(hwnd, &rc); 
 
    // Convert the mouse position to client coordinates. 
 
    ScreenToClient(hwnd, &pt); 
 
    // If the position is in the client area, display a  
    // shortcut menu. 
 
    if (PtInRect(&rc, pt)) 
    { 
        ClientToScreen(hwnd, &pt); 
        DisplayContextMenu(hwnd, pt); 
        return TRUE; 
    } 
 
    // Return FALSE if no menu is displayed. 
 
    return FALSE; 
} 
```



### <a name="creating-a-shortcut-font-attributes-menu"></a><span data-ttu-id="fde4f-209">Создание контекстного меню Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="fde4f-209">Creating a Shortcut Font-Attributes Menu</span></span>

<span data-ttu-id="fde4f-210">Пример в этом разделе содержит фрагменты кода из приложения, которое создает и отображает контекстное меню, позволяющее пользователю устанавливать шрифты и атрибуты шрифта.</span><span class="sxs-lookup"><span data-stu-id="fde4f-210">The example in this section contains portions of code from an application that creates and displays a shortcut menu that enables the user to set fonts and font attributes.</span></span> <span data-ttu-id="fde4f-211">Приложение отображает меню в клиентской области его главного окна каждый раз, когда пользователь нажимает левую кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="fde4f-211">The application displays the menu in the client area of its main window whenever the user clicks the left mouse button.</span></span>

<span data-ttu-id="fde4f-212">Ниже приведен шаблон меню для контекстного меню, предоставленного в файле определения ресурсов приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-212">Here is the menu template for the shortcut menu that is provided in the application's resource-definition file.</span></span>


```
PopupMenu MENU 
BEGIN 
  POPUP "Dummy Popup" 
    BEGIN 
      POPUP "Fonts" 
        BEGIN 
          MENUITEM "Courier",     IDM_FONT_COURIER 
          MENUITEM "Times Roman", IDM_FONT_TMSRMN 
          MENUITEM "Swiss",       IDM_FONT_SWISS 
          MENUITEM "Helvetica",   IDM_FONT_HELV 
          MENUITEM "Old English", IDM_FONT_OLDENG 
        END 
      POPUP "Sizes" 
        BEGIN 
          MENUITEM "7",  IDM_SIZE_7 
          MENUITEM "8",  IDM_SIZE_8 
          MENUITEM "9",  IDM_SIZE_9 
          MENUITEM "10", IDM_SIZE_10 
          MENUITEM "11", IDM_SIZE_11 
          MENUITEM "12", IDM_SIZE_12 
          MENUITEM "14", IDM_SIZE_14 
        END 
      POPUP "Styles" 
        BEGIN 
          MENUITEM "Bold",        IDM_STYLE_BOLD 
          MENUITEM "Italic",      IDM_STYLE_ITALIC 
          MENUITEM "Strike Out",  IDM_STYLE_SO 
          MENUITEM "Superscript", IDM_STYLE_SUPER 
          MENUITEM "Subscript",   IDM_STYLE_SUB 
        END 
    END 
 
END 
```



<span data-ttu-id="fde4f-213">В следующем примере приводится процедура окна и вспомогательные функции, используемые для создания и вывода контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-213">The following example gives the window procedure and supporting functions used to create and display the shortcut menu.</span></span>


```
LRESULT APIENTRY MenuWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rc;    // client area             
    POINT pt;   // location of mouse click  
 
    switch (uMsg) 
    { 
        case WM_LBUTTONDOWN: 
 
            // Get the bounding rectangle of the client area. 
 
            GetClientRect(hwnd, (LPRECT) &rc); 
 
            // Get the client coordinates for the mouse click.  
 
            pt.x = GET_X_LPARAM(lParam); 
            pt.y = GET_Y_LPARAM(lParam); 
 
            // If the mouse click took place inside the client 
            // area, execute the application-defined function 
            // that displays the shortcut menu. 
 
            if (PtInRect((LPRECT) &rc, pt)) 
                HandlePopupMenu(hwnd, pt); 
            break; 
        // Process other window messages.  
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
 
VOID APIENTRY HandlePopupMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // menu template          
    HMENU hmenuTrackPopup;  // shortcut menu   
 
    //  Load the menu template containing the shortcut menu from the 
    //  application's resources. 
 
    hmenu = LoadMenu(hinst, "PopupMenu"); 
    if (hmenu == NULL) 
        return; 
 
    // Get the first shortcut menu in the menu template. This is the 
    // menu that TrackPopupMenu displays. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // TrackPopup uses screen coordinates, so convert the 
    // coordinates of the mouse click to screen coordinates. 
 
    ClientToScreen(hwnd, (LPPOINT) &pt); 
 
    // Draw and track the shortcut menu.  
 
    TrackPopupMenu(hmenuTrackPopup, TPM_LEFTALIGN | TPM_LEFTBUTTON, 
        pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



### <a name="displaying-a-shortcut-menu"></a><span data-ttu-id="fde4f-214">Отображение контекстного меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-214">Displaying a Shortcut Menu</span></span>

<span data-ttu-id="fde4f-215">Функция, показанная в следующем примере, выводит контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-215">The function shown in the following example displays a shortcut menu.</span></span>

<span data-ttu-id="fde4f-216">Приложение включает ресурс меню, определяемый строкой «Шорткутексампле».</span><span class="sxs-lookup"><span data-stu-id="fde4f-216">The application includes a menu resource identified by the string "ShortcutExample."</span></span> <span data-ttu-id="fde4f-217">Строка меню просто содержит имя меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-217">The menu bar simply contains a menu name.</span></span> <span data-ttu-id="fde4f-218">Приложение использует функцию [**метод TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) для вывода меню, связанного с этим пунктом меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-218">The application uses the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function to display the menu associated with this menu item.</span></span> <span data-ttu-id="fde4f-219">(Сама строка меню не отображается, так как для **метод TrackPopupMenu** требуется маркер меню, подменю или контекстное меню.)</span><span class="sxs-lookup"><span data-stu-id="fde4f-219">(The menu bar itself is not displayed because **TrackPopupMenu** requires a handle to a menu, submenu, or shortcut menu.)</span></span>


```
VOID APIENTRY DisplayContextMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // top-level menu 
    HMENU hmenuTrackPopup;  // shortcut menu 
 
    // Load the menu resource. 
 
    if ((hmenu = LoadMenu(hinst, "ShortcutExample")) == NULL) 
        return; 
 
    // TrackPopupMenu cannot display the menu bar so get 
    // a handle to the first shortcut menu. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // Display the shortcut menu. Track the right mouse 
    // button. 
 
    TrackPopupMenu(hmenuTrackPopup, 
            TPM_LEFTALIGN | TPM_RIGHTBUTTON, 
            pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



## <a name="using-menu-item-bitmaps"></a><span data-ttu-id="fde4f-220">Использование точечных рисунков Menu-Item</span><span class="sxs-lookup"><span data-stu-id="fde4f-220">Using Menu-Item Bitmaps</span></span>

<span data-ttu-id="fde4f-221">Для вывода пункта меню система может использовать точечный рисунок вместо текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="fde4f-221">The system can use a bitmap instead of a text string to display a menu item.</span></span> <span data-ttu-id="fde4f-222">Чтобы использовать точечный рисунок, необходимо задать флаг **\_ точечного рисунка миим** для пункта меню и указать маркер для точечного рисунка, который должен отображаться системой для элемента меню в элементе **хбмпитем** структуры [**объектами menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-222">To use a bitmap, you must set the **MIIM\_BITMAP** flag for the menu item and specify a handle to the bitmap that the system should display for the menu item in the **hbmpItem** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="fde4f-223">В этом разделе описывается использование точечных рисунков для пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-223">This section describes how to use bitmaps for menu items.</span></span>

-   [<span data-ttu-id="fde4f-224">Установка флага типа точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="fde4f-224">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
-   [<span data-ttu-id="fde4f-225">Создание точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="fde4f-225">Creating the Bitmap</span></span>](#creating-the-bitmap)
-   [<span data-ttu-id="fde4f-226">Добавление линий и графиков в меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-226">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
-   [<span data-ttu-id="fde4f-227">Пример Menu-Item точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="fde4f-227">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a><span data-ttu-id="fde4f-228">Установка флага типа точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="fde4f-228">Setting the Bitmap Type Flag</span></span>

<span data-ttu-id="fde4f-229">Флаг **\_ растрового** **\_ изображения миим** или MF указывает, что система использует точечный рисунок, а не текстовую строку для вывода пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-229">The **MIIM\_BITMAP** or **MF\_BITMAP** flag tells the system to use a bitmap rather than a text string to display a menu item.</span></span> <span data-ttu-id="fde4f-230">Во время выполнения необходимо **задать \_ растровое изображение миим** или флаг **MF \_ Bitmap** . его нельзя задать в файле определения ресурса.</span><span class="sxs-lookup"><span data-stu-id="fde4f-230">A menu item's **MIIM\_BITMAP** or **MF\_BITMAP** flag must be set at run time; you cannot set it in the resource-definition file.</span></span>

<span data-ttu-id="fde4f-231">Для новых приложений можно использовать функцию [**сетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) или [**инсертменуитем**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) , чтобы установить флаг типа **\_ точечного рисунка миим** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-231">For new applications, you can use the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) or [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) function to set the **MIIM\_BITMAP** type flag.</span></span> <span data-ttu-id="fde4f-232">Чтобы изменить пункт меню из текстового элемента на элемент точечного рисунка, используйте **сетменуитеминфо**.</span><span class="sxs-lookup"><span data-stu-id="fde4f-232">To change a menu item from a text item to a bitmap item, use **SetMenuItemInfo**.</span></span> <span data-ttu-id="fde4f-233">Чтобы добавить новый элемент Bitmap в меню, используйте функцию **инсертменуитем** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-233">To add a new bitmap item to a menu, use the **InsertMenuItem** function.</span></span>

<span data-ttu-id="fde4f-234">Приложения, написанные для более ранних версий системы, могут продолжать использовать функции [**модифимену**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**инсертмену**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)или [**аппендмену**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) для установки флага **\_ битовой карты MF** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-234">Applications written for earlier versions of the system can continue to use the [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to set the **MF\_BITMAP** flag.</span></span> <span data-ttu-id="fde4f-235">Чтобы изменить пункт меню из элемента текстовой строки на растровый элемент, используйте **модифимену**.</span><span class="sxs-lookup"><span data-stu-id="fde4f-235">To change a menu item from a text string item to a bitmap item, use **ModifyMenu**.</span></span> <span data-ttu-id="fde4f-236">Чтобы добавить новый элемент Bitmap в меню, используйте флаг **MF \_ Bitmap** с функцией **инсертмену** или **аппендмену** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-236">To add a new bitmap item to a menu, use the **MF\_BITMAP** flag with the **InsertMenu** or **AppendMenu** function.</span></span>

### <a name="creating-the-bitmap"></a><span data-ttu-id="fde4f-237">Создание точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="fde4f-237">Creating the Bitmap</span></span>

<span data-ttu-id="fde4f-238">При задании флага **\_ растрового изображения Миим** или **MF \_** для пункта меню необходимо также указать маркер для точечного рисунка, который система должна отображать для пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-238">When you set the **MIIM\_BITMAP** or **MF\_BITMAP** type flag for a menu item, you must also specify a handle to the bitmap that the system should display for the menu item.</span></span> <span data-ttu-id="fde4f-239">Можно указать точечный рисунок как ресурс точечного рисунка или создать точечный рисунок во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-239">You can provide the bitmap as a bitmap resource or create the bitmap at run time.</span></span> <span data-ttu-id="fde4f-240">При использовании ресурса точечного рисунка можно использовать функцию [**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) для загрузки точечного рисунка и получения его маркера.</span><span class="sxs-lookup"><span data-stu-id="fde4f-240">If you use a bitmap resource, you can use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap and obtain its handle.</span></span>

<span data-ttu-id="fde4f-241">Чтобы создать точечный рисунок во время выполнения, используйте функции Windows интерфейс графических устройств (GDI).</span><span class="sxs-lookup"><span data-stu-id="fde4f-241">To create the bitmap at run time, use Windows Graphics Device Interface (GDI) functions.</span></span> <span data-ttu-id="fde4f-242">GDI предоставляет несколько способов создания точечного рисунка во время выполнения, но разработчики обычно используют следующий метод:</span><span class="sxs-lookup"><span data-stu-id="fde4f-242">GDI provides several ways to create a bitmap at run time, but developers typically use the following method:</span></span>

1.  <span data-ttu-id="fde4f-243">Используйте функцию [**креатекомпатибледк**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) , чтобы создать контекст устройства, совместимый с контекстом устройства, используемым главным окном приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-243">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the device context used by the application's main window.</span></span>
2.  <span data-ttu-id="fde4f-244">Используйте функцию [**креатекомпатиблебитмап**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) для создания точечного рисунка, совместимого с главным окном приложения, или используйте функцию [**креатебитмап**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) для создания монохромного точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="fde4f-244">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window or use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>
3.  <span data-ttu-id="fde4f-245">Используйте функцию [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) , чтобы выбрать точечный рисунок в совместимом контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="fde4f-245">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="fde4f-246">Для рисования изображения в растровом изображении используются функции рисования GDI, такие как [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) и [**lineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto).</span><span class="sxs-lookup"><span data-stu-id="fde4f-246">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap.</span></span>

<span data-ttu-id="fde4f-247">Дополнительные сведения см. в разделе [точечные рисунки](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="fde4f-247">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="adding-lines-and-graphs-to-a-menu"></a><span data-ttu-id="fde4f-248">Добавление линий и графиков в меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-248">Adding Lines and Graphs to a Menu</span></span>

<span data-ttu-id="fde4f-249">В следующем примере кода показано, как создать меню, содержащее растровые изображения элементов меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-249">The following code sample shows how to create a menu that contains menu-item bitmaps.</span></span> <span data-ttu-id="fde4f-250">Он создает два меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-250">It creates two menus.</span></span> <span data-ttu-id="fde4f-251">Первое — меню диаграммы, содержащее три точечных рисунка элемента меню: круговую диаграмму, график и линейчатую диаграмму.</span><span class="sxs-lookup"><span data-stu-id="fde4f-251">The first is a Chart menu that contains three menu-item bitmaps: a pie chart, a line chart, and a bar chart.</span></span> <span data-ttu-id="fde4f-252">В примере показано, как загрузить эти растровые изображения из файла ресурсов приложения, а затем использовать функции [**креатепопупмену**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) и [**аппендмену**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) для создания меню и пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-252">The example demonstrates how to load these bitmaps from the application's resource file, and then use the [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) and [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to create the menu and menu items.</span></span>

<span data-ttu-id="fde4f-253">Второе меню — это меню «строки».</span><span class="sxs-lookup"><span data-stu-id="fde4f-253">The second menu is a Lines menu.</span></span> <span data-ttu-id="fde4f-254">Он содержит точечные рисунки, отображающие стили линий, предоставляемые стандартным пером в системе.</span><span class="sxs-lookup"><span data-stu-id="fde4f-254">It contains bitmaps showing the line styles provided by the predefined pen in the system.</span></span> <span data-ttu-id="fde4f-255">Растровые изображения в стиле строки создаются во время выполнения с помощью функций GDI.</span><span class="sxs-lookup"><span data-stu-id="fde4f-255">The line-style bitmaps are created at run time by using GDI functions.</span></span>

<span data-ttu-id="fde4f-256">Ниже приведены определения ресурсов точечных рисунков в файле определения ресурсов приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-256">Here are the definitions of the bitmap resources in the application's resource-definition file.</span></span>


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



<span data-ttu-id="fde4f-257">Ниже приведены соответствующие части файла заголовка приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-257">Here are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_SOLID       PS_SOLID 
#define IDM_DASH        PS_DASH 
#define IDM_DASHDOT     PS_DASHDOT 
#define IDM_DASHDOTDOT  PS_DASHDOTDOT 
 
#define IDM_PIE  1 
#define IDM_LINE 2 
#define IDM_BAR  3 
 
// Line-type flags  
 
#define SOLID       0 
#define DOT         1 
#define DASH        2 
#define DASHDOT     3 
#define DASHDOTDOT  4 
 
// Count of pens  
 
#define CPENS 5 
 
// Chart-type flags  
 
#define PIE  1 
#define LINE 2 
#define BAR  3 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
VOID MakeChartMenu(HWND); 
VOID MakeLineMenu(HWND, HPEN, HBITMAP); 
```



<span data-ttu-id="fde4f-258">В следующем примере показано, как в приложении создаются растровые изображения меню и элементов меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-258">The following example shows how menus and menu-item bitmaps are created in an application.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HPEN hpen[CPENS]; 
    static HBITMAP hbmp[CPENS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create the Chart and Line menus.  
 
            MakeChartMenu(hwnd); 
            MakeLineMenu(hwnd, hpen, hbmp); 
            return 0; 
 
        // Process other window messages. 
 
        case WM_DESTROY: 
 
            for (i = 0; i < CPENS; i++) 
            { 
                DeleteObject(hbmp[i]); 
                DeleteObject(hpen[i]); 
            } 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
VOID MakeChartMenu(HWND hwnd) 
{ 
    HBITMAP hbmpPie;    // handle to pie chart bitmap   
    HBITMAP hbmpLine;   // handle to line chart bitmap  
    HBITMAP hbmpBar;    // handle to bar chart bitmap   
    HMENU hmenuMain;    // handle to main menu          
    HMENU hmenuChart;   // handle to Chart menu  
 
    // Load the pie, line, and bar chart bitmaps from the 
    // resource-definition file. 
 
    hbmpPie = LoadBitmap(hinst, MAKEINTRESOURCE(PIE)); 
    hbmpLine = LoadBitmap(hinst, MAKEINTRESOURCE(LINE)); 
    hbmpBar = LoadBitmap(hinst, MAKEINTRESOURCE(BAR)); 
 
    // Create the Chart menu and add it to the menu bar. 
    // Append the Pie, Line, and Bar menu items to the Chart 
    // menu. 
 
    hmenuMain = GetMenu(hwnd); 
    hmenuChart = CreatePopupMenu(); 
    AppendMenu(hmenuMain, MF_STRING | MF_POPUP, (UINT) hmenuChart, 
        "Chart"); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_PIE, (LPCTSTR) hbmpPie); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_LINE, 
        (LPCTSTR) hbmpLine); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_BAR, (LPCTSTR) hbmpBar); 
 
    return; 
} 
 
VOID MakeLineMenu(HWND hwnd, HPEN phpen, HBITMAP phbmp) 
{ 
    HMENU hmenuLines;       // handle to Lines menu      
    HMENU hmenu;            // handle to main menu              
    COLORREF crMenuClr;     // menu-item background color       
    HBRUSH hbrBackground;   // handle to background brush       
    HBRUSH hbrOld;          // handle to previous brush         
    WORD wLineX;            // width of line bitmaps            
    WORD wLineY;            // height of line bitmaps           
    HDC hdcMain;            // handle to main window's DC       
    HDC hdcLines;           // handle to compatible DC          
    HBITMAP hbmpOld;        // handle to previous bitmap        
    int i;                  // loop counter                     
 
    // Create the Lines menu. Add it to the menu bar.  
 
    hmenu = GetMenu(hwnd); 
    hmenuLines = CreatePopupMenu(); 
    AppendMenu(hmenu, MF_STRING | MF_POPUP, 
        (UINT) hmenuLines, "&Lines"); 
 
    // Create a brush for the menu-item background color.  
 
    crMenuClr = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crMenuClr); 
 
    // Create a compatible device context for the line bitmaps, 
    // and then select the background brush into it. 
 
    hdcMain = GetDC(hwnd); 
    hdcLines = CreateCompatibleDC(hdcMain); 
    hbrOld = SelectObject(hdcLines, hbrBackground); 
 
    // Get the dimensions of the check-mark bitmap. The width of 
    // the line bitmaps will be five times the width of the 
    // check-mark bitmap. 
 
    wLineX = GetSystemMetrics(SM_CXMENUCHECK) * (WORD) 5; 
    wLineY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    // Create the bitmaps and select them, one at a time, into the 
    // compatible device context. Initialize each bitmap by 
    // filling it with the menu-item background color. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        phbmp[i] = CreateCompatibleBitmap(hdcMain, wLineX, wLineY); 
        if (i == 0) 
            hbmpOld = SelectObject(hdcLines, phbmp[i]); 
        else 
            SelectObject(hdcLines, phbmp[i]); 
        ExtFloodFill(hdcLines, 0, 0, crMenuClr, FLOODFILLBORDER); 
    } 
 
    // Create the pens.  
 
    phpen[0] = CreatePen(PS_SOLID, 1, RGB(0, 0, 0)); 
    phpen[1] = CreatePen(PS_DOT, 1, RGB(0, 0, 0)); 
    phpen[2] = CreatePen(PS_DASH, 1, RGB(0, 0, 0)); 
    phpen[3] = CreatePen(PS_DASHDOT, 1, RGB(0, 0, 0)); 
    phpen[4] = CreatePen(PS_DASHDOTDOT, 1, RGB(0, 0, 0)); 
 
    // Select a pen and a bitmap into the compatible device 
    // context, draw a line into the bitmap, and then append 
    // the bitmap as an item in the Lines menu. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        SelectObject(hdcLines, phbmp[i]); 
        SelectObject(hdcLines, phpen[i]); 
        MoveToEx(hdcLines, 0, wLineY / 2, NULL); 
        LineTo(hdcLines, wLineX, wLineY / 2); 
        AppendMenu(hmenuLines, MF_BITMAP, i + 1, 
            (LPCTSTR) phbmp[i]); 
    } 
 
    // Release the main window's device context and destroy the 
    // compatible device context. Also, destroy the background 
    // brush. 
 
    ReleaseDC(hwnd, hdcMain); 
    SelectObject(hdcLines, hbrOld); 
    DeleteObject(hbrBackground); 
    SelectObject(hdcLines, hbmpOld); 
    DeleteDC(hdcLines); 
 
    return; 
} 
```



### <a name="example-of-menu-item-bitmaps"></a><span data-ttu-id="fde4f-259">Пример Menu-Item точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="fde4f-259">Example of Menu-Item Bitmaps</span></span>

<span data-ttu-id="fde4f-260">Пример в этом разделе создает два меню, каждое из которых содержит несколько пунктов точечного меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-260">The example in this topic creates two menus, each containing several bitmap menu items.</span></span> <span data-ttu-id="fde4f-261">Для каждого меню приложение добавляет соответствующее имя меню в строку меню главного окна.</span><span class="sxs-lookup"><span data-stu-id="fde4f-261">For each menu, the application adds a corresponding menu name to the main window's menu bar.</span></span>

<span data-ttu-id="fde4f-262">Первое меню содержит пункты меню, отображающие три типа диаграмм: круговые, линии и линейчатые.</span><span class="sxs-lookup"><span data-stu-id="fde4f-262">The first menu contains menu items showing each of three chart types: pie, line, and bar.</span></span> <span data-ttu-id="fde4f-263">Точечные рисунки для этих пунктов меню определяются как ресурсы и загружаются с помощью функции [**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-263">The bitmaps for these menu items are defined as resources and are loaded by using the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function.</span></span> <span data-ttu-id="fde4f-264">Связанное с этим меню представляет собой имя меню "Диаграмма" в строке меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-264">Associated with this menu is a "Chart" menu name on the menu bar.</span></span>

<span data-ttu-id="fde4f-265">Второе меню содержит пункты меню, показывающие каждый из пяти стилей линий, используемых с функцией [**креатепен**](/windows/desktop/api/wingdi/nf-wingdi-createpen) : **PS \_ сплошной**, **PS \_ тире**, **PS \_ Dot**, **PS \_ дашдот** и **PS \_ дашдотдот**.</span><span class="sxs-lookup"><span data-stu-id="fde4f-265">The second menu contains menu items showing each of the five line styles used with the [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) function: **PS\_SOLID**, **PS\_DASH**, **PS\_DOT**, **PS\_DASHDOT**, and **PS\_DASHDOTDOT**.</span></span> <span data-ttu-id="fde4f-266">Приложение создает точечные рисунки для этих пунктов меню во время выполнения с помощью функций рисования GDI.</span><span class="sxs-lookup"><span data-stu-id="fde4f-266">The application creates the bitmaps for these menu items at run time using GDI drawing functions.</span></span> <span data-ttu-id="fde4f-267">Это меню связано с названием меню **строки** в строке меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-267">Associated with this menu is a **Lines** menu name on the menu bar.</span></span>

<span data-ttu-id="fde4f-268">Определение в процедуре окна приложения — это два статических массива дескрипторов битовой карты.</span><span class="sxs-lookup"><span data-stu-id="fde4f-268">Defined in the application's window procedure are two static arrays of bitmap handles.</span></span> <span data-ttu-id="fde4f-269">Один массив содержит дескрипторы трех растровых изображений, используемых для меню **диаграммы** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-269">One array contains the handles of the three bitmaps used for the **Chart** menu.</span></span> <span data-ttu-id="fde4f-270">Другой содержит маркеры из пяти растровых изображений, используемых в меню « **строки** ».</span><span class="sxs-lookup"><span data-stu-id="fde4f-270">The other contains the handles of the five bitmaps used for the **Lines** menu.</span></span> <span data-ttu-id="fde4f-271">При обработке сообщения [**, \_ созданного**](/windows/desktop/winmsg/wm-create) обработчиком WM, процедура Window загружает точечные рисунки диаграммы, создает точечные рисунки линий, а затем добавляет соответствующие пункты меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-271">When processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, the window procedure loads the chart bitmaps, creates the line bitmaps, and then adds the corresponding menu items.</span></span> <span data-ttu-id="fde4f-272">При обработке сообщения [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) процедура Window удаляет все точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="fde4f-272">When processing the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the window procedure deletes all of the bitmaps.</span></span>

<span data-ttu-id="fde4f-273">Ниже приведены соответствующие части файла заголовка приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-273">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_PIE         1 
#define IDM_LINE        2 
#define IDM_BAR         3 
 
#define IDM_SOLID       4 
#define IDM_DASH        5 
#define IDM_DASHDOT     6 
#define IDM_DASHDOTDOT  7 
 
// Number of items on the Chart and Lines menus 
 
#define C_LINES         5 
#define C_CHARTS        3 
 
// Bitmap resource identifiers 
 
#define IDB_PIE         1 
#define IDB_LINE        2 
#define IDB_BAR         3 
 
// Dimensions of the line bitmaps 
 
#define CX_LINEBMP      40 
#define CY_LINEBMP      10 
```



<span data-ttu-id="fde4f-274">Ниже приведены соответствующие части процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="fde4f-274">Following are the relevant portions of the window procedure.</span></span> <span data-ttu-id="fde4f-275">Процедура Window выполняет большую часть своей инициализации, вызывая определяемые приложением функции Лоадчартбитмапс, Креателинебитмапс и Аддбитмапмену, описанные далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="fde4f-275">The window procedure performs most of its initialization by calling the application-defined LoadChartBitmaps, CreateLineBitmaps, and AddBitmapMenu functions, described later in this topic.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    static HBITMAP aHbmLines[C_LINES]; 
    static HBITMAP aHbmChart[C_CHARTS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
             // Call application-defined functions to load the 
             // bitmaps for the Chart menu and create those for 
             // the Lines menu. 
 
            LoadChartBitmaps(aHbmChart); 
            CreateLineBitmaps(aHbmLines); 
 
             // Call an application-defined function to create 
             // menus containing the bitmap menu items. The function 
             // also adds a menu name to the window's menu bar. 
 
            AddBitmapMenu( 
                    hwnd,      // menu bar's owner window 
                    "&Chart",  // text of menu name on menu bar 
                    IDM_PIE,   // ID of first item on menu 
                    aHbmChart, // array of bitmap handles 
                    C_CHARTS   // number of items on menu 
                    ); 
            AddBitmapMenu(hwnd, "&Lines", IDM_SOLID, 
                    aHbmLines, C_LINES); 
            break; 
 
        case WM_DESTROY: 
            for (i = 0; i < C_LINES; i++) 
                DeleteObject(aHbmLines[i]); 
            for (i = 0; i < C_CHARTS; i++) 
                DeleteObject(aHbmChart[i]); 
            PostQuitMessage(0); 
            break; 
 
        // Process additional messages here. 
 
        default: 
            return (DefWindowProc(hwnd, uMsg, wParam, lParam)); 
    } 
    return 0; 
} 
```



<span data-ttu-id="fde4f-276">Определяемая приложением функция Лоадчартбитмапс загружает ресурсы точечного рисунка для меню диаграммы путем вызова функции [**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="fde4f-276">The application-defined LoadChartBitmaps function loads the bitmap resources for the chart menu by calling the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, as follows.</span></span>


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



<span data-ttu-id="fde4f-277">Определяемая приложением функция Креателинебитмапс создает точечные рисунки для меню "линии" с помощью функций рисования GDI.</span><span class="sxs-lookup"><span data-stu-id="fde4f-277">The application-defined CreateLineBitmaps function creates the bitmaps for the Lines menu by using GDI drawing functions.</span></span> <span data-ttu-id="fde4f-278">Функция создает контекст устройства памяти (DC) с теми же свойствами, что и контроллер домена рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="fde4f-278">The function creates a memory device context (DC) with the same properties as the desktop window's DC.</span></span> <span data-ttu-id="fde4f-279">Для каждого стиля линии функция создает точечный рисунок, выделяет его в памяти контроллера домена и рисует в нем.</span><span class="sxs-lookup"><span data-stu-id="fde4f-279">For each line style, the function creates a bitmap, selects it into the memory DC, and draws in it.</span></span>


```
VOID WINAPI CreateLineBitmaps(HBITMAP *paHbm) 
{ 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
    COLORREF clrMenu = GetSysColor(COLOR_MENU); 
    HBRUSH hbrOld; 
    HPEN hpenOld; 
    HBITMAP hbmOld; 
    int fnDrawMode; 
    int i; 
 
     // Create a brush using the menu background color, 
     // and select it into the memory DC. 
 
    hbrOld = SelectObject(hdcMem, CreateSolidBrush(clrMenu)); 
 
     // Create the bitmaps. Select each one into the memory 
     // DC that was created and draw in it. 
 
    for (i = 0; i < C_LINES; i++) 
    { 
        // Create the bitmap and select it into the DC. 
 
        paHbm[i] = CreateCompatibleBitmap(hdcDesktop, 
                CX_LINEBMP, CY_LINEBMP); 
        hbmOld = SelectObject(hdcMem, paHbm[i]); 
 
        // Fill the background using the brush. 
 
        PatBlt(hdcMem, 0, 0, CX_LINEBMP, CY_LINEBMP, PATCOPY); 
 
        // Create the pen and select it into the DC. 
 
        hpenOld = SelectObject(hdcMem, 
                CreatePen(PS_SOLID + i, 1, RGB(0, 0, 0))); 
 
         // Draw the line. To preserve the background color where 
         // the pen is white, use the R2_MASKPEN drawing mode. 
 
        fnDrawMode = SetROP2(hdcMem, R2_MASKPEN); 
        MoveToEx(hdcMem, 0, CY_LINEBMP / 2, NULL); 
        LineTo(hdcMem, CX_LINEBMP, CY_LINEBMP / 2); 
        SetROP2(hdcMem, fnDrawMode); 
 
        // Delete the pen, and select the old pen and bitmap. 
 
        DeleteObject(SelectObject(hdcMem, hpenOld)); 
        SelectObject(hdcMem, hbmOld); 
    } 
 
    // Delete the brush and select the original brush. 
 
    DeleteObject(SelectObject(hdcMem, hbrOld)); 
 
    // Delete the memory DC and release the desktop DC. 
 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
} 
```



<span data-ttu-id="fde4f-280">Определяемая приложением функция Аддбитмапмену создает меню и добавляет в нее указанное число пунктов точечного меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-280">The application-defined AddBitmapMenu function creates a menu and adds the specified number of bitmap menu items to it.</span></span> <span data-ttu-id="fde4f-281">Затем он добавляет соответствующее имя меню в строку меню указанного окна.</span><span class="sxs-lookup"><span data-stu-id="fde4f-281">Then it adds a corresponding menu name to the specified window's menu bar.</span></span>


```
VOID WINAPI AddBitmapMenu( 
        HWND hwnd,          // window that owned the menu bar 
        LPSTR lpszText,     // text of menu name on menu bar 
        UINT uID,           // ID of first bitmap menu item 
        HBITMAP *paHbm,     // bitmaps for the menu items 
        int cItems)         // number bitmap menu items 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup = CreatePopupMenu(); 
    MENUITEMINFO mii; 
    int i; 
 
    // Add the bitmap menu items to the menu. 
 
    for (i = 0; i < cItems; i++) 
    { 
        mii.fMask = MIIM_ID | MIIM_BITMAP | MIIM_DATA; 
        mii.wID = uID + i; 
        mii.hbmpItem = &paHbm[i]; 
        InsertMenuItem(hmenuPopup, i, TRUE, &mii); 
    } 
 
    // Add a menu name to the menu bar. 
 
    mii.fMask = MIIM_STRING | MIIM_DATA | MIIM_SUBMENU; 
    mii.fType = MFT_STRING; 
    mii.hSubMenu = hmenuPopup; 
    mii.dwTypeData = lpszText; 
    InsertMenuItem(hmenuBar, 
        GetMenuItemCount(hmenuBar), TRUE, &mii); 
} 
```



## <a name="creating-owner-drawn-menu-items"></a><span data-ttu-id="fde4f-282">Создание пунктов меню Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="fde4f-282">Creating Owner-Drawn Menu Items</span></span>

<span data-ttu-id="fde4f-283">Если вам нужен полный контроль над видом элемента меню, можно использовать элемент меню, рисуемый владельцем приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-283">If you need complete control over the appearance of a menu item, you can use an owner-drawn menu item in your application.</span></span> <span data-ttu-id="fde4f-284">В этом разделе описываются шаги, связанные с созданием и использованием элемента меню, рисуемого владельцем.</span><span class="sxs-lookup"><span data-stu-id="fde4f-284">This section describes the steps involved in creating and using an owner-drawn menu item.</span></span>

-   [<span data-ttu-id="fde4f-285">Установка флага Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="fde4f-285">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
-   [<span data-ttu-id="fde4f-286">Меню, рисуемые владельцем, и \_ сообщение WM меасуреитем</span><span class="sxs-lookup"><span data-stu-id="fde4f-286">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
-   [<span data-ttu-id="fde4f-287">Меню, рисуемые владельцем, и \_ сообщение WM DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="fde4f-287">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
-   [<span data-ttu-id="fde4f-288">Меню, рисуемые владельцем, и \_ сообщение WM менучар</span><span class="sxs-lookup"><span data-stu-id="fde4f-288">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
-   [<span data-ttu-id="fde4f-289">Установка шрифтов для Menu-Item текстовых строк</span><span class="sxs-lookup"><span data-stu-id="fde4f-289">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
-   [<span data-ttu-id="fde4f-290">Пример пунктов меню Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="fde4f-290">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a><span data-ttu-id="fde4f-291">Установка флага Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="fde4f-291">Setting the Owner-Drawn Flag</span></span>

<span data-ttu-id="fde4f-292">Нельзя определить элемент меню, рисуемый владельцем, в файле определения ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-292">You cannot define an owner-drawn menu item in your application's resource-definition file.</span></span> <span data-ttu-id="fde4f-293">Вместо этого необходимо создать новый пункт меню или изменить существующий с помощью флага меню **MFT \_ овнердрав** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-293">Instead, you must create a new menu item or modify an existing one by using the **MFT\_OWNERDRAW** menu flag.</span></span>

<span data-ttu-id="fde4f-294">Для указания элемента меню, рисуемого владельцем, можно использовать функцию [**инсертменуитем**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) или [**сетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-294">You can use the [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) or [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function to specify an owner-drawn menu item.</span></span> <span data-ttu-id="fde4f-295">Используйте **инсертменуитем** для вставки нового пункта меню в указанную позицию в строке меню или меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-295">Use **InsertMenuItem** to insert a new menu item at the specified position in a menu bar or menu.</span></span> <span data-ttu-id="fde4f-296">Используйте **сетменуитеминфо** для изменения содержимого меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-296">Use **SetMenuItemInfo** to change the contents of a menu.</span></span>

<span data-ttu-id="fde4f-297">При вызове этих двух функций необходимо указать указатель на структуру [**объектами menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , указывающую свойства нового пункта меню или свойства, которые необходимо изменить для существующего элемента меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-297">When calling these two functions, you must specify a pointer to a [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, which specifies the properties of the new menu item or the properties you want to change for an existing menu item.</span></span> <span data-ttu-id="fde4f-298">Чтобы сделать элемент элементом, рисуемым владельцем, укажите значение **миим \_ ftype** для элемента **Фмаск** и значение **\_ овнердрав MFT** для члена **ftype** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-298">To make an item an owner-drawn item, specify the **MIIM\_FTYPE** value for the **fMask** member and the **MFT\_OWNERDRAW** value for the **fType** member.</span></span>

<span data-ttu-id="fde4f-299">Устанавливая соответствующие элементы структуры [**объектами menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , можно связать определяемое приложением значение, которое называется **данными элемента**, с каждым пунктом меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-299">By setting the appropriate members of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, you can associate an application-defined value, which is called **item data**, with each menu item.</span></span> <span data-ttu-id="fde4f-300">Для этого укажите значение **\_ данных миим** для элемента **фмаск** и значение, определяемое приложением для элемента **двитемдата** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-300">To do so, specify the **MIIM\_DATA** value for the **fMask** member and the application-defined value for the **dwItemData** member.</span></span>

<span data-ttu-id="fde4f-301">Данные элемента можно использовать с любым типом пункта меню, но это особенно удобно для элементов, рисуемых владельцем.</span><span class="sxs-lookup"><span data-stu-id="fde4f-301">You can use item data with any type of menu item, but it is particularly useful for owner-drawn items.</span></span> <span data-ttu-id="fde4f-302">Например, предположим, что структура содержит сведения, используемые для рисования пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-302">For example, suppose a structure contains information used to draw a menu item.</span></span> <span data-ttu-id="fde4f-303">Приложение может использовать данные элемента для элемента меню для сохранения указателя на структуру.</span><span class="sxs-lookup"><span data-stu-id="fde4f-303">An application might use the item data for a menu item to store a pointer to the structure.</span></span> <span data-ttu-id="fde4f-304">Данные элемента отправляются в окно владельца меню с сообщениями [**WM \_ Меасуреитем**](../controls/wm-measureitem.md) и [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-304">The item data is sent to the menu's owner window with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages.</span></span> <span data-ttu-id="fde4f-305">Чтобы получить данные элемента для меню в любое время, используйте функцию [**жетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-305">To retrieve the item data for a menu at any time, use the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function.</span></span>

<span data-ttu-id="fde4f-306">Приложения, написанные для более ранних версий системы, могут по-прежнему вызывать [**аппендмену**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**инсертмену**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)или [**Модифимену**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) для назначения флага **MF \_ овнердрав** элементу меню, рисуемому владельцем.</span><span class="sxs-lookup"><span data-stu-id="fde4f-306">Applications written for earlier versions of the system can continue to call [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) to assign the **MF\_OWNERDRAW** flag to an owner-drawn menu item.</span></span>

<span data-ttu-id="fde4f-307">При вызове любой из этих трех функций можно передать значение в качестве параметра *лпневитем* .</span><span class="sxs-lookup"><span data-stu-id="fde4f-307">When you call any of these three functions, you can pass a value as the *lpNewItem* parameter.</span></span> <span data-ttu-id="fde4f-308">Это значение может представлять любую информацию, значимую для приложения, и будет доступна приложению при отображении элемента.</span><span class="sxs-lookup"><span data-stu-id="fde4f-308">This value can represent any information that is meaningful to your application, and that will be available to your application when the item is to be displayed.</span></span> <span data-ttu-id="fde4f-309">Например, значение может содержать указатель на структуру; структура, в свою очередь, может содержать текстовую строку и маркер для логического шрифта, который приложение будет использовать для рисования строки.</span><span class="sxs-lookup"><span data-stu-id="fde4f-309">For example, the value could contain a pointer to a structure; the structure, in turn, might contain a text string and a handle to the logical font your application will use to draw the string.</span></span>

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a><span data-ttu-id="fde4f-310">Owner-Drawn меню и \_ сообщение МЕАСУРЕИТЕМ WM</span><span class="sxs-lookup"><span data-stu-id="fde4f-310">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>

<span data-ttu-id="fde4f-311">Прежде чем система выведет на экран элемент меню, рисуемый владельцем впервые, он отправляет сообщение [**WM \_ меасуреитем**](../controls/wm-measureitem.md) в оконную процедуру окна, которому принадлежит меню элемента.</span><span class="sxs-lookup"><span data-stu-id="fde4f-311">Before the system displays an owner-drawn menu item for the first time, it sends the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message to the window procedure of the window that owns the item's menu.</span></span> <span data-ttu-id="fde4f-312">Это сообщение содержит указатель на структуру [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) , которая идентифицирует элемент и содержит данные элемента, которые могли быть назначены приложению.</span><span class="sxs-lookup"><span data-stu-id="fde4f-312">This message contains a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the item and contains the item data that an application may have assigned to it.</span></span> <span data-ttu-id="fde4f-313">Процедура окна должна заполнить члены структуры **итемвидс** и **итемхеигхт** перед возвратом из обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-313">The window procedure must fill the **itemWidth** and **itemHeight** members of the structure before returning from processing the message.</span></span> <span data-ttu-id="fde4f-314">Система использует информацию этих членов при создании ограничивающего прямоугольника, в котором приложение рисует пункт меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-314">The system uses the information in these members when creating the bounding rectangle in which an application draws the menu item.</span></span> <span data-ttu-id="fde4f-315">Он также использует информацию для определения того, когда пользователь выбирает элемент.</span><span class="sxs-lookup"><span data-stu-id="fde4f-315">It also uses the information to detect when the user chooses the item.</span></span>

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a><span data-ttu-id="fde4f-316">Owner-Drawn меню и \_ сообщение DRAWITEM WM</span><span class="sxs-lookup"><span data-stu-id="fde4f-316">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>

<span data-ttu-id="fde4f-317">Каждый раз, когда элемент должен быть нарисован (например, когда он впервые отображается или когда пользователь выбирает его), система отправляет сообщение [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) в оконную процедуру окна "владелец" меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-317">Whenever the item must be drawn (for example, when it is first displayed or when the user selects it), the system sends the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message to the window procedure of the menu's owner window.</span></span> <span data-ttu-id="fde4f-318">Это сообщение содержит указатель на структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , которая содержит сведения об элементе, включая данные элемента, которые могли быть назначены приложению.</span><span class="sxs-lookup"><span data-stu-id="fde4f-318">This message contains a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure, which contains information about the item, including the item data that an application may have assigned to it.</span></span> <span data-ttu-id="fde4f-319">Кроме того, **дравитемструкт** содержит флаги, указывающие состояние элемента (например, является ли он серым или выделенным), а также ограничивающий прямоугольник и контекст устройства, используемый приложением для рисования элемента.</span><span class="sxs-lookup"><span data-stu-id="fde4f-319">In addition, **DRAWITEMSTRUCT** contains flags that indicate the state of the item (such as whether it is grayed or selected) as well as a bounding rectangle and a device context that the application uses to draw the item.</span></span>

<span data-ttu-id="fde4f-320">При обработке сообщения [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) приложение должно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="fde4f-320">An application must do the following while processing the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message:</span></span>

-   <span data-ttu-id="fde4f-321">Определите необходимый тип рисунка.</span><span class="sxs-lookup"><span data-stu-id="fde4f-321">Determine the type of drawing that is necessary.</span></span> <span data-ttu-id="fde4f-322">Для этого проверьте элемент **итемактион** структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-322">To do so, check the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span>
-   <span data-ttu-id="fde4f-323">Нарисуйте элемент меню соответствующим образом, используя ограничивающий прямоугольник и контекст устройства, полученные из структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-323">Draw the menu item appropriately, using the bounding rectangle and device context obtained from the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="fde4f-324">Приложение должно рисовать только в ограничивающем прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="fde4f-324">The application must draw only within the bounding rectangle.</span></span> <span data-ttu-id="fde4f-325">Из соображений производительности система не обрезает фрагменты изображения, рисуемые за пределами прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="fde4f-325">For performance reasons, the system does not clip portions of the image that are drawn outside the rectangle.</span></span>
-   <span data-ttu-id="fde4f-326">Восстановите все объекты GDI, выбранные для контекста устройства этого пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-326">Restore all GDI objects selected for the menu item's device context.</span></span>

<span data-ttu-id="fde4f-327">Если пользователь выбирает пункт меню, система устанавливает для элемента **итемактион** структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) значение **Ода \_ SELECT** Value и устанавливает **\_ выбранное значение ODS** в элементе **ItemState** .</span><span class="sxs-lookup"><span data-stu-id="fde4f-327">If the user selects the menu item, the system sets the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure to the **ODA\_SELECT** value and sets the **ODS\_SELECTED** value in the **itemState** member.</span></span> <span data-ttu-id="fde4f-328">Это подсказка приложения для перерисовки пункта меню, чтобы показать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="fde4f-328">This is an application's cue to redraw the menu item to indicate that it is selected.</span></span>

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a><span data-ttu-id="fde4f-329">Owner-Drawn меню и \_ сообщение МЕНУЧАР WM</span><span class="sxs-lookup"><span data-stu-id="fde4f-329">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>

<span data-ttu-id="fde4f-330">В меню, отличном от рисуемых владельцем меню, можно указать клавишу меню, вставив знак подчеркивания рядом с символом в строке меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-330">Menus other than owner-drawn menus can specify a menu mnemonic by inserting an underscore next to a character in the menu string.</span></span> <span data-ttu-id="fde4f-331">Это позволяет пользователю выбрать меню, нажав клавишу ALT и нажимая клавишу «Menu».</span><span class="sxs-lookup"><span data-stu-id="fde4f-331">This allows the user to select the menu by pressing ALT and pressing the menu mnemonic character.</span></span> <span data-ttu-id="fde4f-332">Однако в меню, рисуемых владельцем, при этом нельзя указать назначенную ему команду меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-332">In owner-drawn menus, however, you cannot specify a menu mnemonic in this manner.</span></span> <span data-ttu-id="fde4f-333">Вместо этого приложение должно обработать сообщение [**WM \_ менучар**](wm-menuchar.md) , чтобы предоставить меню, рисуемое владельцем, с помощью мнемоник меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-333">Instead, your application must process the [**WM\_MENUCHAR**](wm-menuchar.md) message to provide owner-drawn menus with menu mnemonics.</span></span>

<span data-ttu-id="fde4f-334">Сообщение [**WM \_ менучар**](wm-menuchar.md) отправляется, когда пользователь вводит назначенную клавишу меню, не совпадающую ни с одной из стандартных мнемоник текущего меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-334">The [**WM\_MENUCHAR**](wm-menuchar.md) message is sent when the user types a menu mnemonic that does not match any of the predefined mnemonics of the current menu.</span></span> <span data-ttu-id="fde4f-335">Значение, содержащееся в параметре *wParam* , указывает символ ASCII, соответствующий ключу, который пользователь нажал с помощью клавиши ALT.</span><span class="sxs-lookup"><span data-stu-id="fde4f-335">The value contained in *wParam* specifies the ASCII character that corresponds to the key the user pressed with the ALT key.</span></span> <span data-ttu-id="fde4f-336">Слово *wParam* с низким приоритетом определяет тип выбранного меню и может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fde4f-336">The low-order word of *wParam* specifies the type of the selected menu and can be one of the following values:</span></span>

-   <span data-ttu-id="fde4f-337">**MF \_ Всплывающее окно** , если текущее меню является подменю.</span><span class="sxs-lookup"><span data-stu-id="fde4f-337">**MF\_POPUP** if the current menu is a submenu.</span></span>
-   <span data-ttu-id="fde4f-338">**MF \_ СИСМЕНУ** , если меню является системным меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-338">**MF\_SYSMENU** if the menu is the system menu.</span></span>

<span data-ttu-id="fde4f-339">Слово « *wParam* » высокого порядка содержит маркер меню для текущего меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-339">The high-order word of *wParam* contains the menu handle to the current menu.</span></span> <span data-ttu-id="fde4f-340">Окно с меню, рисуемым владельцем, может обрабатывать [**WM \_ менучар**](wm-menuchar.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fde4f-340">The window with the owner-drawn menus can process [**WM\_MENUCHAR**](wm-menuchar.md) as follows:</span></span>


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



<span data-ttu-id="fde4f-341">Два в слове с высоким порядком возвращаемого значения уведомляют систему о том, что младшее слово возвращаемого значения содержит Отсчитываемый от нуля индекс выбираемого элемента меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-341">The two in the high-order word of the return value informs the system that the low-order word of the return value contains the zero-based index of the menu item to be selected.</span></span>

<span data-ttu-id="fde4f-342">Следующие константы соответствуют возможным возвращаемым значениям из сообщения [**\_ менучар WM**](wm-menuchar.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-342">The following constants correspond to the possible return values from the [**WM\_MENUCHAR**](wm-menuchar.md) message.</span></span>



| <span data-ttu-id="fde4f-343">Константа</span><span class="sxs-lookup"><span data-stu-id="fde4f-343">Constant</span></span>         | <span data-ttu-id="fde4f-344">Значение</span><span class="sxs-lookup"><span data-stu-id="fde4f-344">Value</span></span> | <span data-ttu-id="fde4f-345">Значение</span><span class="sxs-lookup"><span data-stu-id="fde4f-345">Meaning</span></span>                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fde4f-346">**МНК \_ игнорировать**</span><span class="sxs-lookup"><span data-stu-id="fde4f-346">**MNC\_IGNORE**</span></span>  | <span data-ttu-id="fde4f-347">0</span><span class="sxs-lookup"><span data-stu-id="fde4f-347">0</span></span>     | <span data-ttu-id="fde4f-348">Система должна отказаться от нажатого пользователем символа и создать короткий звуковой сигнал на системном докладчике.</span><span class="sxs-lookup"><span data-stu-id="fde4f-348">The system should discard the character the user pressed and create a short beep on the system speaker.</span></span>                                                       |
| <span data-ttu-id="fde4f-349">**МНК \_ Закрыть**</span><span class="sxs-lookup"><span data-stu-id="fde4f-349">**MNC\_CLOSE**</span></span>   | <span data-ttu-id="fde4f-350">1</span><span class="sxs-lookup"><span data-stu-id="fde4f-350">1</span></span>     | <span data-ttu-id="fde4f-351">Система должна закрыть активное меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-351">The system should close the active menu.</span></span>                                                                                                                      |
| <span data-ttu-id="fde4f-352">**\_выполнение МНК**</span><span class="sxs-lookup"><span data-stu-id="fde4f-352">**MNC\_EXECUTE**</span></span> | <span data-ttu-id="fde4f-353">2</span><span class="sxs-lookup"><span data-stu-id="fde4f-353">2</span></span>     | <span data-ttu-id="fde4f-354">Система должна выбрать элемент, указанный в младшем слове возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-354">The system should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="fde4f-355">Окно-владелец получает сообщение [**\_ командной строки WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-355">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span> |
| <span data-ttu-id="fde4f-356">**МНК \_ SELECT**</span><span class="sxs-lookup"><span data-stu-id="fde4f-356">**MNC\_SELECT**</span></span>  | <span data-ttu-id="fde4f-357">3</span><span class="sxs-lookup"><span data-stu-id="fde4f-357">3</span></span>     | <span data-ttu-id="fde4f-358">Система должна выбрать элемент, указанный в младшем слове возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-358">The system should select the item specified in the low-order word of the return value.</span></span>                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a><span data-ttu-id="fde4f-359">Установка шрифтов для Menu-Item текстовых строк</span><span class="sxs-lookup"><span data-stu-id="fde4f-359">Setting Fonts for Menu-Item Text Strings</span></span>

<span data-ttu-id="fde4f-360">В этом разделе содержится пример из приложения, в котором используются элементы меню, рисуемые владельцем.</span><span class="sxs-lookup"><span data-stu-id="fde4f-360">This topic contains an example from an application that uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="fde4f-361">Меню содержит элементы, устанавливающие атрибуты текущего шрифта, и элементы отображаются с помощью соответствующего атрибута Font.</span><span class="sxs-lookup"><span data-stu-id="fde4f-361">The menu contains items that set the attributes of the current font, and the items are displayed using the appropriate font attribute.</span></span>

<span data-ttu-id="fde4f-362">Вот как это меню определено в файле определения ресурса.</span><span class="sxs-lookup"><span data-stu-id="fde4f-362">Here is how the menu is defined in the resource-definition file.</span></span> <span data-ttu-id="fde4f-363">Обратите внимание, что строки для элементов меню обычный, полужирный, курсив и подчеркивание присваиваются во время выполнения, поэтому их строки в файле определения ресурсов пусты.</span><span class="sxs-lookup"><span data-stu-id="fde4f-363">Note that the strings for the Regular, Bold, Italic, and Underline menu items are assigned at run time, so their strings are empty in the resource-definition file.</span></span>


```
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "",    IDM_REGULAR 
        MENUITEM SEPARATOR 
        MENUITEM    "",    IDM_BOLD 
        MENUITEM    "",    IDM_ITALIC 
        MENUITEM    "",    IDM_ULINE 
    END 
END 
```



<span data-ttu-id="fde4f-364">Окно приложения обрабатывает сообщения, участвующие в использовании элементов меню, рисуемых владельцем.</span><span class="sxs-lookup"><span data-stu-id="fde4f-364">The application's window procedure processes the messages involved in using owner-drawn menu items.</span></span> <span data-ttu-id="fde4f-365">Приложение использует сообщение о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="fde4f-365">The application uses the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to do the following:</span></span>

-   <span data-ttu-id="fde4f-366">Установите флаг **MF \_ овнердрав** для пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-366">Set the **MF\_OWNERDRAW** flag for the menu items.</span></span>
-   <span data-ttu-id="fde4f-367">Задайте текстовые строки для пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-367">Set the text strings for the menu items.</span></span>
-   <span data-ttu-id="fde4f-368">Получение дескрипторов шрифтов, используемых для рисования элементов.</span><span class="sxs-lookup"><span data-stu-id="fde4f-368">Obtain handles of the fonts used to draw the items.</span></span>
-   <span data-ttu-id="fde4f-369">Получение значений цвета текста и фона для выбранных пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-369">Obtain the text and background color values for selected menu items.</span></span>

<span data-ttu-id="fde4f-370">Текстовые строки и дескрипторы шрифтов хранятся в массиве определяемых приложением структур МИТЕМ.</span><span class="sxs-lookup"><span data-stu-id="fde4f-370">The text strings and font handles are stored in an array of application-defined MYITEM structures.</span></span> <span data-ttu-id="fde4f-371">Определяемая приложением функция Жетафонт создает шрифт, соответствующий указанному атрибуту Font, и возвращает маркер для шрифта.</span><span class="sxs-lookup"><span data-stu-id="fde4f-371">The application-defined GetAFont function creates a font that corresponds to the specified font attribute and returns a handle to the font.</span></span> <span data-ttu-id="fde4f-372">Дескрипторы уничтожаются во время обработки сообщения [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-372">The handles are destroyed during the processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>

<span data-ttu-id="fde4f-373">Во время обработки сообщения [**WM \_ меасуреитем**](../controls/wm-measureitem.md) в примере получается ширина и высота строки элемента меню, и эти значения копируются в структуру [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-373">During the processing of the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message, the example gets the width and height of a menu-item string and copies these values into the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure.</span></span> <span data-ttu-id="fde4f-374">Система использует значения Width и Height для вычисления размера меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-374">The system uses the width and height values to calculate the size of the menu.</span></span>

<span data-ttu-id="fde4f-375">Во время обработки сообщения [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) строка элемента меню рисуется с помощью комнаты слева рядом со строкой для точечного рисунка галочки.</span><span class="sxs-lookup"><span data-stu-id="fde4f-375">During the processing of the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message, the menu item's string is drawn with room left next to the string for the check-mark bitmap.</span></span> <span data-ttu-id="fde4f-376">Если пользователь выбирает элемент, для рисования элемента используются выделенные цвета текста и фона.</span><span class="sxs-lookup"><span data-stu-id="fde4f-376">If the user selects the item, the selected text and background colors are used to draw the item.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    typedef struct _MYITEM 
    { 
        HFONT hfont; 
        LPSTR psz; 
    } MYITEM;             // structure for item font and string  
 
    MYITEM *pmyitem;      // pointer to item's font and string        
    static MYITEM myitem[CITEMS];   // array of MYITEMS               
    static HMENU hmenu;             // handle to main menu            
    static COLORREF crSelText;  // text color of selected item        
    static COLORREF crSelBkgnd; // background color of selected item  
    COLORREF crText;            // text color of unselected item      
    COLORREF crBkgnd;           // background color unselected item   
    LPMEASUREITEMSTRUCT lpmis;  // pointer to item of data             
    LPDRAWITEMSTRUCT lpdis;     // pointer to item drawing data        
    HDC hdc;                    // handle to screen DC                
    SIZE size;                  // menu-item text extents             
    WORD wCheckX;               // check-mark width                   
    int nTextX;                 // width of menu item                 
    int nTextY;                 // height of menu item                
    int i;                      // loop counter                       
    HFONT hfontOld;             // handle to old font                 
    BOOL fSelected = FALSE;     // menu-item selection flag
    size_t * pcch;
    HRESULT hResult;           
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Modify the Regular, Bold, Italic, and Underline 
            // menu items to make them owner-drawn items. Associate 
            // a MYITEM structure with each item to contain the 
            // string for and font handle to each item. 
 
            hmenu = GetMenu(hwnd); 
            ModifyMenu(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED | MF_OWNERDRAW, IDM_REGULAR, 
                (LPTSTR) &myitem[REGULAR]); 
            ModifyMenu(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_BOLD, (LPTSTR) &myitem[BOLD]); 
            ModifyMenu(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ITALIC, 
                (LPTSTR) &myitem[ITALIC]); 
            ModifyMenu(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ULINE, (LPTSTR) &myitem[ULINE]); 
 
            // Retrieve each item's font handle and copy it into 
            // the hfont member of each item's MYITEM structure. 
            // Also, copy each item's string into the structures. 
 
            myitem[REGULAR].hfont = GetAFont(REGULAR); 
            myitem[REGULAR].psz = "Regular"; 
            myitem[BOLD].hfont = GetAFont(BOLD); 
            myitem[BOLD].psz = "Bold"; 
            myitem[ITALIC].hfont = GetAFont(ITALIC); 
            myitem[ITALIC].psz = "Italic"; 
            myitem[ULINE].hfont = GetAFont(ULINE); 
            myitem[ULINE].psz = "Underline"; 
 
            // Retrieve the text and background colors of the 
            // selected menu text. 
 
            crSelText = GetSysColor(COLOR_HIGHLIGHTTEXT); 
            crSelBkgnd = GetSysColor(COLOR_HIGHLIGHT); 
 
            return 0; 
 
        case WM_MEASUREITEM: 
 
            // Retrieve a device context for the main window.  
 
            hdc = GetDC(hwnd); 
 
            // Retrieve pointers to the menu item's 
            // MEASUREITEMSTRUCT structure and MYITEM structure. 
 
            lpmis = (LPMEASUREITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpmis->itemData; 
 
            // Select the font associated with the item into 
            // the main window's device context. 
 
            hfontOld = SelectObject(hdc, pmyitem->hfont); 
 
            // Retrieve the width and height of the item's string, 
            // and then copy the width and height into the 
            // MEASUREITEMSTRUCT structure's itemWidth and 
            // itemHeight members.
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            GetTextExtentPoint32(hdc, pmyitem->psz, 
                *pcch, &size); 
            lpmis->itemWidth = size.cx; 
            lpmis->itemHeight = size.cy; 
 
            // Select the old font back into the device context, 
            // and then release the device context. 
 
            SelectObject(hdc, hfontOld); 
            ReleaseDC(hwnd, hdc); 
 
            return TRUE; 
 
            break; 
 
        case WM_DRAWITEM: 
 
            // Get pointers to the menu item's DRAWITEMSTRUCT 
            // structure and MYITEM structure. 
 
            lpdis = (LPDRAWITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpdis->itemData; 
 
            // If the user has selected the item, use the selected 
            // text and background colors to display the item. 
 
            if (lpdis->itemState & ODS_SELECTED) 
            { 
                crText = SetTextColor(lpdis->hDC, crSelText); 
                crBkgnd = SetBkColor(lpdis->hDC, crSelBkgnd); 
                fSelected = TRUE; 
            } 
 
            // Remember to leave space in the menu item for the 
            // check-mark bitmap. Retrieve the width of the bitmap 
            // and add it to the width of the menu item. 
 
            wCheckX = GetSystemMetrics(SM_CXMENUCHECK); 
            nTextX = wCheckX + lpdis->rcItem.left; 
            nTextY = lpdis->rcItem.top; 
 
            // Select the font associated with the item into the 
            // item's device context, and then draw the string. 
 
            hfontOld = SelectObject(lpdis->hDC, pmyitem->hfont);
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            ExtTextOut(lpdis->hDC, nTextX, nTextY, ETO_OPAQUE, 
                &lpdis->rcItem, pmyitem->psz, 
                *pcch, NULL); 
 
            // Select the previous font back into the device 
            // context. 
 
            SelectObject(lpdis->hDC, hfontOld); 
 
            // Return the text and background colors to their 
            // normal state (not selected). 
 
            if (fSelected) 
            { 
                SetTextColor(lpdis->hDC, crText); 
                SetBkColor(lpdis->hDC, crBkgnd); 
            } 
 
            return TRUE; 
 
        // Process other messages.  
 
        case WM_DESTROY: 
 
            // Destroy the menu items' font handles.  
 
            for (i = 0; i < CITEMS; i++) 
                DeleteObject(myitem[i].hfont); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HFONT GetAFont(int fnFont) 
{ 
    static LOGFONT lf;  // structure for font information  
 
    // Get a handle to the ANSI fixed-pitch font, and copy 
    // information about the font to a LOGFONT structure. 
 
    GetObject(GetStockObject(ANSI_FIXED_FONT), sizeof(LOGFONT), 
        &lf); 
 
    // Set the font attributes, as appropriate.  
 
    if (fnFont == BOLD) 
        lf.lfWeight = FW_BOLD; 
    else 
        lf.lfWeight = FW_NORMAL; 
 
    lf.lfItalic = (fnFont == ITALIC); 
    lf.lfItalic = (fnFont == ULINE); 
 
    // Create the font, and then return its handle.  
 
    return CreateFont(lf.lfHeight, lf.lfWidth, 
        lf.lfEscapement, lf.lfOrientation, lf.lfWeight, 
        lf.lfItalic, lf.lfUnderline, lf.lfStrikeOut, lf.lfCharSet, 
        lf.lfOutPrecision, lf.lfClipPrecision, lf.lfQuality, 
        lf.lfPitchAndFamily, lf.lfFaceName); 
} 
```



### <a name="example-of-owner-drawn-menu-items"></a><span data-ttu-id="fde4f-377">Пример пунктов меню Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="fde4f-377">Example of Owner-Drawn Menu Items</span></span>

<span data-ttu-id="fde4f-378">В примере в этом разделе в меню используются элементы меню, рисуемые владельцем.</span><span class="sxs-lookup"><span data-stu-id="fde4f-378">The example in this topic uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="fde4f-379">Пункты меню выбирают конкретные атрибуты шрифта, и приложение отображает каждый элемент меню, используя шрифт с соответствующим атрибутом.</span><span class="sxs-lookup"><span data-stu-id="fde4f-379">The menu items select specific font attributes, and the application displays each menu item using a font that has the corresponding attribute.</span></span> <span data-ttu-id="fde4f-380">Например, элемент меню **курсив** отображается курсивом.</span><span class="sxs-lookup"><span data-stu-id="fde4f-380">For example, the **Italic** menu item is displayed in an italic font.</span></span> <span data-ttu-id="fde4f-381">Откроется меню с **символами** в строке меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-381">The **Character** menu name on the menu bar opens the menu.</span></span>

<span data-ttu-id="fde4f-382">Строка меню и раскрывающееся меню определяются с помощью расширенного ресурса шаблона меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-382">The menu bar and drop-down menu are defined initially by an extended menu-template resource.</span></span> <span data-ttu-id="fde4f-383">Поскольку шаблон меню не может указывать элементы, рисуемые владельцем, меню изначально содержит четыре пункта текстового меню со следующими строками: "обычный", "полужирный", "Курсив" и "подчеркнутый".</span><span class="sxs-lookup"><span data-stu-id="fde4f-383">Because a menu template cannot specify owner-drawn items, the menu initially contains four text menu items with the following strings: "Regular," "Bold," "Italic," and "Underline."</span></span> <span data-ttu-id="fde4f-384">Процедура окна приложения изменяет их на рисуемые владельцем элементы при обработке сообщения о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-384">The application's window procedure changes these to owner-drawn items when it processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="fde4f-385">При получении сообщения о **\_ создании WM** процедура Window вызывает функцию, определяемую приложением, которая выполняет следующие действия для каждого пункта меню:</span><span class="sxs-lookup"><span data-stu-id="fde4f-385">When it receives the **WM\_CREATE** message, the window procedure calls the application-defined OnCreate function, which performs the following steps for each menu item:</span></span>

-   <span data-ttu-id="fde4f-386">Выделяет определенную приложением структуру МИТЕМ.</span><span class="sxs-lookup"><span data-stu-id="fde4f-386">Allocates an application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="fde4f-387">Возвращает текст пункта меню и сохраняет его в определяемой приложением структуре МИТЕМ.</span><span class="sxs-lookup"><span data-stu-id="fde4f-387">Gets the text of the menu item and saves it in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="fde4f-388">Создает шрифт, используемый для вывода пункта меню, и сохраняет его маркер в определяемой приложением структуре МИТЕМ.</span><span class="sxs-lookup"><span data-stu-id="fde4f-388">Creates the font used to display the menu item and saves its handle in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="fde4f-389">Изменяет тип элемента меню на **MFT \_ овнердрав** и сохраняет указатель на определенную приложением структуру митем в виде данных элемента.</span><span class="sxs-lookup"><span data-stu-id="fde4f-389">Changes the menu item type to **MFT\_OWNERDRAW** and saves a pointer to the application-defined MYITEM structure as item data.</span></span>

<span data-ttu-id="fde4f-390">Поскольку указатель на каждую определенную приложением структуру МИТЕМ сохраняется как данные элемента, он передается в процедуру окна вместе с сообщениями [**WM \_ Меасуреитем**](../controls/wm-measureitem.md) и [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) для соответствующего пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-390">Because a pointer to each application-defined MYITEM structure is saved as item data, it is passed to the window procedure in conjunction with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages for the corresponding menu item.</span></span> <span data-ttu-id="fde4f-391">Указатель содержится в элементе **итемдата** в структурах [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) и [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-391">The pointer is contained in the **itemData** member of both the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) and [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structures.</span></span>

<span data-ttu-id="fde4f-392">Сообщение [**WM \_ меасуреитем**](../controls/wm-measureitem.md) отправляется для каждого элемента меню, рисуемого владельцем, при первом его отображении.</span><span class="sxs-lookup"><span data-stu-id="fde4f-392">A [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message is sent for each owner-drawn menu item the first time it is displayed.</span></span> <span data-ttu-id="fde4f-393">Приложение обрабатывает это сообщение, выбирая шрифт для пункта меню в контексте устройства, а затем определяя пространство, необходимое для вывода текста пункта меню в этом шрифте.</span><span class="sxs-lookup"><span data-stu-id="fde4f-393">The application processes this message by selecting the font for the menu item into a device context and then determining the space required to display the menu item text in that font.</span></span> <span data-ttu-id="fde4f-394">Текст шрифта и пункта меню определяется `MYITEM` структурой пункта меню (структурой, определенной приложением).</span><span class="sxs-lookup"><span data-stu-id="fde4f-394">The font and menu item text are both specified by the menu item's `MYITEM` structure (the structure defined by the application).</span></span> <span data-ttu-id="fde4f-395">Приложение определяет размер текста с помощью функции [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-395">The application determines the size of the text by using the [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) function.</span></span>

<span data-ttu-id="fde4f-396">Процедура окна обрабатывает сообщение [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) , отображая текст пункта меню соответствующим шрифтом.</span><span class="sxs-lookup"><span data-stu-id="fde4f-396">The window procedure processes the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message by displaying the menu item text in the appropriate font.</span></span> <span data-ttu-id="fde4f-397">Текст шрифта и пункта меню задаются `MYITEM` структурой пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-397">The font and menu item text are both specified by the menu item's `MYITEM` structure.</span></span> <span data-ttu-id="fde4f-398">Приложение выбирает цвета текста и фона, соответствующие состоянию пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-398">The application selects text and background colors appropriate to the menu item's state.</span></span>

<span data-ttu-id="fde4f-399">Процедура Window обрабатывает сообщение [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) для уничтожения шрифтов и освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="fde4f-399">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message to destroy fonts and free memory.</span></span> <span data-ttu-id="fde4f-400">Приложение удаляет шрифт и освобождает структуру МИТЕМ, определяемую приложением, для каждого пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-400">The application deletes the font and frees the application-defined MYITEM structure for each menu item.</span></span>

<span data-ttu-id="fde4f-401">Ниже приведены соответствующие части файла заголовка приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-401">The following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_REGULAR   11 
#define IDM_BOLD      12 
#define IDM_ITALIC    13 
#define IDM_UNDERLINE 14 
 
// Structure associated with menu items 
 
typedef struct tagMYITEM 
{ 
    HFONT hfont; 
    int   cchItemText; 
    char  szItemText[1]; 
} MYITEM; 
 
#define CCH_MAXITEMTEXT 256 
 
```



<span data-ttu-id="fde4f-402">Ниже приведены соответствующие части процедуры окна приложения и связанные с ней функции.</span><span class="sxs-lookup"><span data-stu-id="fde4f-402">The following are the relevant portions of the application's window procedure and its associated functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_MEASUREITEM: 
            OnMeasureItem(hwnd, (LPMEASUREITEMSTRUCT) lParam); 
            return TRUE; 
 
        case WM_DRAWITEM: 
            OnDrawItem(hwnd, (LPDRAWITEMSTRUCT) lParam); 
            return TRUE; 
 
        // Additional message processing goes here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Modify each menu item. Assume that the IDs IDM_REGULAR 
    // through IDM_UNDERLINE are consecutive numbers. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
         // Allocate an item structure, leaving space for a 
         // string of up to CCH_MAXITEMTEXT characters. 
 
        pMyItem = (MYITEM *) LocalAlloc(LMEM_FIXED, 
                sizeof(MYITEM) + CCH_MAXITEMTEXT); 
 
        // Save the item text in the item structure. 
 
        mii.fMask = MIIM_STRING; 
        mii.dwTypeData = pMyItem->szItemText; 
        mii.cch = CCH_MAXITEMTEXT; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem->cchItemText = mii.cch; 
 
        // Reallocate the structure to the minimum required size. 
 
        pMyItem = (MYITEM *) LocalReAlloc(pMyItem, 
                sizeof(MYITEM) + mii.cch, LMEM_MOVEABLE); 
 
        // Create the font used to draw the item. 
 
        pMyItem->hfont = CreateMenuItemFont(uID); 
 
        // Change the item to an owner-drawn item, and save 
        // the address of the item structure as item data. 
 
        mii.fMask = MIIM_FTYPE | MIIM_DATA; 
        mii.fType = MFT_OWNERDRAW; 
        mii.dwItemData = (ULONG_PTR) pMyItem; 
        SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
    } 
    return TRUE; 
} 
 
HFONT CreateMenuItemFont(UINT uID) 
{ 
    LOGFONT lf;
    HRESULT hr; 
 
    ZeroMemory(&lf, sizeof(lf)); 
    lf.lfHeight = 20; 
    hr = StringCchCopy(lf.lfFaceName, 32, "Times New Roman");
    if (FAILED(hr))
    {
    // TODO: writer error handler
    } 
 
    switch (uID) 
    { 
        case IDM_BOLD: 
            lf.lfWeight = FW_HEAVY; 
            break; 
 
        case IDM_ITALIC: 
            lf.lfItalic = TRUE; 
            break; 
 
        case IDM_UNDERLINE: 
            lf.lfUnderline = TRUE; 
            break; 
    } 
    return CreateFontIndirect(&lf); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get  
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Free resources associated with each menu item. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
        // Get the item data. 
 
        mii.fMask = MIIM_DATA; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem = (MYITEM *) mii.dwItemData; 
 
        // Destroy the font and free the item structure. 
 
        DeleteObject(pMyItem->hfont); 
        LocalFree(pMyItem); 
    } 
} 
 
VOID WINAPI OnMeasureItem(HWND hwnd, LPMEASUREITEMSTRUCT lpmis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpmis->itemData; 
    HDC hdc = GetDC(hwnd); 
    HFONT hfntOld = (HFONT)SelectObject(hdc, pMyItem->hfont); 
    SIZE size; 
 
    GetTextExtentPoint32(hdc, pMyItem->szItemText, 
            pMyItem->cchItemText, &size); 
 
    lpmis->itemWidth = size.cx; 
    lpmis->itemHeight = size.cy; 
 
    SelectObject(hdc, hfntOld); 
    ReleaseDC(hwnd, hdc); 
} 
 
VOID WINAPI OnDrawItem(HWND hwnd, LPDRAWITEMSTRUCT lpdis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpdis->itemData; 
    COLORREF clrPrevText, clrPrevBkgnd; 
    HFONT hfntPrev; 
    int x, y; 
 
    // Set the appropriate foreground and background colors. 
 
    if (lpdis->itemState & ODS_SELECTED) 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHTTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHT)); 
    } 
    else 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_MENUTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_MENU)); 
    } 
 
    // Determine where to draw and leave space for a check mark. 
 
    x = lpdis->rcItem.left; 
    y = lpdis->rcItem.top; 
    x += GetSystemMetrics(SM_CXMENUCHECK); 
 
    // Select the font and draw the text. 
 
    hfntPrev = (HFONT)SelectObject(lpdis->hDC, pMyItem->hfont); 
    ExtTextOut(lpdis->hDC, x, y, ETO_OPAQUE, 
            &lpdis->rcItem, pMyItem->szItemText, 
            pMyItem->cchItemText, NULL); 
 
    // Restore the original font and colors. 
 
    SelectObject(lpdis->hDC, hfntPrev); 
    SetTextColor(lpdis->hDC, clrPrevText); 
    SetBkColor(lpdis->hDC, clrPrevBkgnd); 
} 
```



## <a name="using-custom-check-mark-bitmaps"></a><span data-ttu-id="fde4f-403">Использование пользовательских точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="fde4f-403">Using Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="fde4f-404">Система предоставляет растровое изображение галочки по умолчанию для отображения рядом с выбранным пунктом меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-404">The system provides a default check-mark bitmap for displaying next to a menu item that is selected.</span></span> <span data-ttu-id="fde4f-405">Можно настроить отдельный элемент меню, предоставив пару точечных рисунков, чтобы заменить точечный рисунок галочки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fde4f-405">You can customize an individual menu item by providing a pair of bitmaps to replace the default check-mark bitmap.</span></span> <span data-ttu-id="fde4f-406">Система отображает одно растровое изображение, когда элемент выбран и другой при его очистке.</span><span class="sxs-lookup"><span data-stu-id="fde4f-406">The system displays one bitmap when the item is selected and the other when it is clear.</span></span> <span data-ttu-id="fde4f-407">В этом разделе описываются шаги, связанные с созданием и использованием пользовательских точечных рисунков с галочкой.</span><span class="sxs-lookup"><span data-stu-id="fde4f-407">This section describes the steps involved in creating and using custom check-mark bitmaps.</span></span>

-   [<span data-ttu-id="fde4f-408">Создание пользовательских точечных рисунков с галочками</span><span class="sxs-lookup"><span data-stu-id="fde4f-408">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
-   [<span data-ttu-id="fde4f-409">Связывание точечных рисунков с пунктом меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-409">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
-   [<span data-ttu-id="fde4f-410">Установка атрибута галочки</span><span class="sxs-lookup"><span data-stu-id="fde4f-410">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
-   [<span data-ttu-id="fde4f-411">Имитация флажков в меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-411">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
-   [<span data-ttu-id="fde4f-412">Пример использования пользовательских точечных рисунков с галочкой</span><span class="sxs-lookup"><span data-stu-id="fde4f-412">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a><span data-ttu-id="fde4f-413">Создание пользовательских точечных рисунков с галочками</span><span class="sxs-lookup"><span data-stu-id="fde4f-413">Creating Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="fde4f-414">Пользовательское растровое изображение галочки должно иметь тот же размер, что и точечный рисунок галочки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fde4f-414">A custom check-mark bitmap must be the same size as the default check-mark bitmap.</span></span> <span data-ttu-id="fde4f-415">Вы можете получить размер отметки по умолчанию для точечного рисунка, вызвав функцию [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-415">You can retrieve the default check-mark size of the bitmap by calling the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="fde4f-416">Слово с низким приоритетом возвращаемого значения этой функции указывает ширину; слово в высоком порядке указывает высоту.</span><span class="sxs-lookup"><span data-stu-id="fde4f-416">The low-order word of this function's return value specifies the width; the high-order word specifies the height.</span></span>

<span data-ttu-id="fde4f-417">Вы можете использовать ресурсы точечного рисунка для предоставления точечных рисунков галочки.</span><span class="sxs-lookup"><span data-stu-id="fde4f-417">You can use bitmap resources to provide check-mark bitmaps.</span></span> <span data-ttu-id="fde4f-418">Однако, поскольку требуемый размер растрового изображения зависит от типа дисплея, может потребоваться изменить размер растрового изображения во время выполнения с помощью функции [**стретчблт**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-418">However, because the required bitmap size varies depending on the display type, you may need to resize the bitmap at run time by using the [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) function.</span></span> <span data-ttu-id="fde4f-419">В зависимости от точечного рисунка искажение, вызванное изменением размера, может привести к неприемлемым результатам.</span><span class="sxs-lookup"><span data-stu-id="fde4f-419">Depending on the bitmap, the distortion caused by sizing could produce unacceptable results.</span></span>

<span data-ttu-id="fde4f-420">Вместо использования ресурса точечного рисунка можно создать точечный рисунок во время выполнения с помощью функций GDI.</span><span class="sxs-lookup"><span data-stu-id="fde4f-420">Instead of using a bitmap resource, you can create a bitmap at run time by using GDI functions.</span></span>

<span data-ttu-id="fde4f-421">**Создание точечного рисунка во время выполнения**</span><span class="sxs-lookup"><span data-stu-id="fde4f-421">**To create a bitmap at run time**</span></span>

1.  <span data-ttu-id="fde4f-422">Используйте функцию [**креатекомпатибледк**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) , чтобы создать контекст устройства, совместимый с тем, который используется главным окном приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-422">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the one used by the application's main window.</span></span>

    <span data-ttu-id="fde4f-423">В параметре *HDC* функции можно указать значение **null** или возврат из функции.</span><span class="sxs-lookup"><span data-stu-id="fde4f-423">The function's *hdc* parameter can specify either **NULL** or the return value from the function.</span></span> <span data-ttu-id="fde4f-424">[**Креатекомпатибледк**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) возвращает маркер для совместимого контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="fde4f-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) returns a handle to the compatible device context.</span></span>

2.  <span data-ttu-id="fde4f-425">Используйте функцию [**креатекомпатиблебитмап**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) , чтобы создать точечный рисунок, совместимый с главным окном приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-425">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window.</span></span>

    <span data-ttu-id="fde4f-426">Параметры *нвидс* и *нхеигхт* этой функции устанавливают размер растрового изображения. они должны указывать сведения о ширине и высоте, возвращаемые функцией [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-426">This function's *nWidth* and *nHeight* parameters set the size of the bitmap; they should specify the width and height information returned by the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span>

    > [!Note]  
    > <span data-ttu-id="fde4f-427">Для создания монохромного точечного рисунка можно также использовать функцию [**креатебитмап**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-427">You can also use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>

     

3.  <span data-ttu-id="fde4f-428">Используйте функцию [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) , чтобы выбрать точечный рисунок в совместимом контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="fde4f-428">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="fde4f-429">Используйте функции рисования GDI, такие как [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) и [**lineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), для рисования изображения в растровом изображении или для копирования изображения в растровое изображение с помощью таких функций, как [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) и [**стретчблт**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-429">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap, or use functions such as [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) and [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) to copy an image into the bitmap.</span></span>

<span data-ttu-id="fde4f-430">Дополнительные сведения см. в разделе [точечные рисунки](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="fde4f-430">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="associating-bitmaps-with-a-menu-item"></a><span data-ttu-id="fde4f-431">Связывание точечных рисунков с пунктом меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-431">Associating Bitmaps with a Menu Item</span></span>

<span data-ttu-id="fde4f-432">Пара битов точечных рисунков связывается с пунктом меню путем передачи дескрипторов растровых изображений в функцию [**сетменуитембитмапс**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-432">You associate a pair of check-mark bitmaps with a menu item by passing the handles of the bitmaps to the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span> <span data-ttu-id="fde4f-433">Параметр *хбитмапунчеккед* Определяет битовую карту, а параметр *хбитмапчеккед* определяет выбранный точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="fde4f-433">The *hBitmapUnchecked* parameter identifies the clear bitmap, and the *hBitmapChecked* parameter identifies the selected bitmap.</span></span> <span data-ttu-id="fde4f-434">Если вы хотите удалить один или оба флажка из пункта меню, можно задать для параметра *хбитмапунчеккед* или *хбитмапчеккед* значение **null**.</span><span class="sxs-lookup"><span data-stu-id="fde4f-434">If you want to remove one or both check marks from a menu item, you can set the *hBitmapUnchecked* or *hBitmapChecked* parameter, or both, to **NULL**.</span></span>

### <a name="setting-the-check-mark-attribute"></a><span data-ttu-id="fde4f-435">Установка атрибута галочки</span><span class="sxs-lookup"><span data-stu-id="fde4f-435">Setting the Check-mark Attribute</span></span>

<span data-ttu-id="fde4f-436">Функция [**чеккменуитем**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) задает для выбранного или сброшенного атрибута элемента меню флажок.</span><span class="sxs-lookup"><span data-stu-id="fde4f-436">The [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) function sets a menu item's check-mark attribute to either selected or cleared.</span></span> <span data-ttu-id="fde4f-437">Можно указать значение, установленное в параметре **MF \_** , чтобы присвоить атрибуту галочки значение выбрано, а **\_ непроверенное — MF** — очистить.</span><span class="sxs-lookup"><span data-stu-id="fde4f-437">You can specify the **MF\_CHECKED** value to set the check-mark attribute to selected and the **MF\_UNCHECKED** value to set it to clear.</span></span>

<span data-ttu-id="fde4f-438">Вы также можете задать состояние проверки пункта меню с помощью функции [**сетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-438">You can also set the check state of a menu item by using the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="fde4f-439">Иногда группа элементов меню представляет набор взаимоисключающих параметров.</span><span class="sxs-lookup"><span data-stu-id="fde4f-439">Sometimes a group of menu items represents a set of mutually exclusive options.</span></span> <span data-ttu-id="fde4f-440">С помощью функции [**чеккменурадиоитем**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) можно проверить один пункт меню и одновременно снять флажок рядом с другими элементами меню в группе.</span><span class="sxs-lookup"><span data-stu-id="fde4f-440">By using the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function, you can check one menu item while simultaneously removing the check mark from all other menu items in the group.</span></span>

### <a name="simulating-check-boxes-in-a-menu"></a><span data-ttu-id="fde4f-441">Имитация флажков в меню</span><span class="sxs-lookup"><span data-stu-id="fde4f-441">Simulating Check Boxes in a Menu</span></span>

<span data-ttu-id="fde4f-442">В этом разделе содержится пример, демонстрирующий имитацию флажков в меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-442">This topic contains an example that shows how to simulate check boxes in a menu.</span></span> <span data-ttu-id="fde4f-443">Этот пример содержит меню символов, элементы которого позволяют пользователю задать атрибуты полужирного начертания, курсива и подчеркивания текущего шрифта.</span><span class="sxs-lookup"><span data-stu-id="fde4f-443">The example contains a Character menu whose items allow the user to set the bold, italic, and underline attributes of the current font.</span></span> <span data-ttu-id="fde4f-444">Если атрибут Font действует, флажок рядом с соответствующим пунктом меню отображается галочкой. в противном случае рядом с элементом отображается пустой флажок.</span><span class="sxs-lookup"><span data-stu-id="fde4f-444">When a font attribute is in effect, a check mark is displayed in the check box next to the corresponding menu item; otherwise, an empty check box is displayed next to the item.</span></span>

<span data-ttu-id="fde4f-445">В примере точечный рисунок галочки по умолчанию заменен двумя точечными рисунками: точечный рисунок с выбранным флажком и точечный рисунок с пустым полем.</span><span class="sxs-lookup"><span data-stu-id="fde4f-445">The example replaces the default check-mark bitmap with two bitmaps: a bitmap with a selected check box and the bitmap with an empty box.</span></span> <span data-ttu-id="fde4f-446">Выделенное битовое изображение флажка отображается рядом с пунктом меню полужирный, курсив или подчеркнутый, если для атрибута элемента установлен флажок установить значение **MF \_**.</span><span class="sxs-lookup"><span data-stu-id="fde4f-446">The selected check box bitmap is displayed next to the Bold, Italic, or Underline menu item when the item's check-mark attribute is set to **MF\_CHECKED**.</span></span> <span data-ttu-id="fde4f-447">Если атрибут галочки установлен в значение **MF \_** снят, отображается битовое изображение флажка очистить или пусто.</span><span class="sxs-lookup"><span data-stu-id="fde4f-447">The clear or empty check box bitmap is displayed when the check-mark attribute is set to **MF\_UNCHECKED**.</span></span>

<span data-ttu-id="fde4f-448">Система предоставляет предопределенный точечный рисунок, который содержит изображения, используемые для флажков и переключателей.</span><span class="sxs-lookup"><span data-stu-id="fde4f-448">The system provides a predefined bitmap that contains the images used for check boxes and radio buttons.</span></span> <span data-ttu-id="fde4f-449">В этом примере изолируются флажки "выбранные" и "пустые", они копируются в два отдельных точечных рисунка, а затем используются в качестве выделенных и очищенных растровых изображений для элементов в меню " **символ** ".</span><span class="sxs-lookup"><span data-stu-id="fde4f-449">The example isolates the selected and empty check boxes, copies them to two separate bitmaps, and then uses them as the selected and cleared bitmaps for items in the **Character** menu.</span></span>

<span data-ttu-id="fde4f-450">Чтобы получить маркер для точечного рисунка с флажком, в примере вызывается функция [**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) с указанием **значения NULL** в качестве параметра *HINSTANCE* и **ОБМ \_ CheckBox** в качестве параметра *лпбитмапнаме* .</span><span class="sxs-lookup"><span data-stu-id="fde4f-450">To retrieve a handle to the system-defined check box bitmap, the example calls the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, specifying **NULL** as the *hInstance* parameter and **OBM\_CHECKBOXES** as the *lpBitmapName* parameter.</span></span> <span data-ttu-id="fde4f-451">Поскольку изображения в точечном рисунке имеют одинаковый размер, в примере их можно изолировать, разделив ширину и высоту растрового изображения на количество изображений в их строках и столбцах.</span><span class="sxs-lookup"><span data-stu-id="fde4f-451">Because the images in the bitmap are all the same size, the example can isolate them by dividing the bitmap width and height by the number of images in its rows and columns.</span></span>

<span data-ttu-id="fde4f-452">В следующей части файла определения ресурсов показано, как определяются элементы меню в меню « **символ** ».</span><span class="sxs-lookup"><span data-stu-id="fde4f-452">The following portion of a resource-definition file shows how the menu items in the **Character** menu are defined.</span></span> <span data-ttu-id="fde4f-453">Обратите внимание, что атрибуты шрифта изначально не действуют, поэтому атрибуту галочки для **обычного** элемента присваивается значение выбрано и по умолчанию атрибуту галочки оставшихся элементов присваивается значение Clear.</span><span class="sxs-lookup"><span data-stu-id="fde4f-453">Note that no font attributes are in effect initially, so the check-mark attribute for the **Regular** item is set to selected and, by default, the check-mark attribute of the remaining items is set to clear.</span></span>


```
#include "men3.h" 
 
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "&Regular",     IDM_REGULAR, CHECKED 
        MENUITEM SEPARATOR 
        MENUITEM    "&Bold",        IDM_BOLD 
        MENUITEM    "&Italic",      IDM_ITALIC 
        MENUITEM    "&Underline",   IDM_ULINE 
    END 
END
```



<span data-ttu-id="fde4f-454">Ниже приведено соответствующее содержимое файла заголовка приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-454">Here are the relevant contents of the application's header file.</span></span>


```
// Menu-item identifiers  
 
#define IDM_REGULAR 0x1 
#define IDM_BOLD    0x2 
#define IDM_ITALIC  0x4 
#define IDM_ULINE   0x8 
 
// Check-mark flags  
 
#define CHECK   1 
#define UNCHECK 2 
 
// Font-attribute mask  
 
#define ATTRIBMASK 0xe 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
HBITMAP GetMyCheckBitmaps(UINT); 
BYTE CheckOrUncheckMenuItem(BYTE, HMENU); 
```



<span data-ttu-id="fde4f-455">В следующем примере показаны части процедуры окна, которые создают точечные рисунки с галочкой. Задайте атрибут галочки для пунктов меню **полужирный**, **курсив** и **Подчеркивание** . и уничтожать растровые изображения галочки.</span><span class="sxs-lookup"><span data-stu-id="fde4f-455">The following example shows the portions of the window procedure that create the check-mark bitmaps; set the check-mark attribute of the **Bold**, **Italic**, and **Underline** menu items; and destroy check-mark bitmaps.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HBITMAP hbmpCheck;   // handle to checked bitmap    
    static HBITMAP hbmpUncheck; // handle to unchecked bitmap  
    static HMENU hmenu;         // handle to main menu         
    BYTE fbFontAttrib;          // font-attribute flags        
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Call the application-defined GetMyCheckBitmaps 
            // function to get the predefined checked and 
            // unchecked check box bitmaps. 
 
            hbmpCheck = GetMyCheckBitmaps(CHECK); 
            hbmpUncheck = GetMyCheckBitmaps(UNCHECK); 
 
            // Set the checked and unchecked bitmaps for the menu 
            // items. 
 
            hmenu = GetMenu(hwndMain); 
            SetMenuItemBitmaps(hmenu, IDM_BOLD, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ITALIC, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ULINE, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the menu commands.  
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // CheckOrUncheckMenuItem is an application- 
                    // defined function that sets the menu item 
                    // checkmarks and returns the user-selected 
                    // font attributes. 
 
                    fbFontAttrib = CheckOrUncheckMenuItem( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // Set the font attributes.  
 
                    return 0; 
 
                // Process other command messages.  
 
                default: 
                    break; 
            } 
 
            break; 
 
        // Process other window messages.  
 
        case WM_DESTROY: 
 
            // Destroy the checked and unchecked bitmaps.  
 
            DeleteObject(hbmpCheck); 
            DeleteObject(hbmpUncheck); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HBITMAP GetMyCheckBitmaps(UINT fuCheck) 
{ 
    COLORREF crBackground;  // background color                  
    HBRUSH hbrBackground;   // background brush                  
    HBRUSH hbrTargetOld;    // original background brush         
    HDC hdcSource;          // source device context             
    HDC hdcTarget;          // target device context             
    HBITMAP hbmpCheckboxes; // handle to check-box bitmap        
    BITMAP bmCheckbox;      // structure for bitmap data         
    HBITMAP hbmpSourceOld;  // handle to original source bitmap  
    HBITMAP hbmpTargetOld;  // handle to original target bitmap  
    HBITMAP hbmpCheck;      // handle to check-mark bitmap       
    RECT rc;                // rectangle for check-box bitmap    
    WORD wBitmapX;          // width of check-mark bitmap        
    WORD wBitmapY;          // height of check-mark bitmap       
 
    // Get the menu background color and create a solid brush 
    // with that color. 
 
    crBackground = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crBackground); 
 
    // Create memory device contexts for the source and 
    // destination bitmaps. 
 
    hdcSource = CreateCompatibleDC((HDC) NULL); 
    hdcTarget = CreateCompatibleDC(hdcSource); 
 
    // Get the size of the system default check-mark bitmap and 
    // create a compatible bitmap of the same size. 
 
    wBitmapX = GetSystemMetrics(SM_CXMENUCHECK); 
    wBitmapY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    hbmpCheck = CreateCompatibleBitmap(hdcSource, wBitmapX, 
        wBitmapY); 
 
    // Select the background brush and bitmap into the target DC. 
 
    hbrTargetOld = SelectObject(hdcTarget, hbrBackground); 
    hbmpTargetOld = SelectObject(hdcTarget, hbmpCheck); 
 
    // Use the selected brush to initialize the background color 
    // of the bitmap in the target device context. 
 
    PatBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, PATCOPY); 
 
    // Load the predefined check box bitmaps and select it 
    // into the source DC. 
 
    hbmpCheckboxes = LoadBitmap((HINSTANCE) NULL, 
        (LPTSTR) OBM_CHECKBOXES); 
 
    hbmpSourceOld = SelectObject(hdcSource, hbmpCheckboxes); 
 
    // Fill a BITMAP structure with information about the 
    // check box bitmaps, and then find the upper-left corner of 
    // the unchecked check box or the checked check box. 
 
    GetObject(hbmpCheckboxes, sizeof(BITMAP), &bmCheckbox); 
 
    if (fuCheck == UNCHECK) 
    { 
        rc.left = 0; 
        rc.right = (bmCheckbox.bmWidth / 4); 
    } 
    else 
    { 
        rc.left = (bmCheckbox.bmWidth / 4); 
        rc.right = (bmCheckbox.bmWidth / 4) * 2; 
    } 
 
    rc.top = 0; 
    rc.bottom = (bmCheckbox.bmHeight / 3); 
 
    // Copy the appropriate bitmap into the target DC. If the 
    // check-box bitmap is larger than the default check-mark 
    // bitmap, use StretchBlt to make it fit; otherwise, just 
    // copy it. 
 
    if (((rc.right - rc.left) > (int) wBitmapX) || 
            ((rc.bottom - rc.top) > (int) wBitmapY)) 
    {
        StretchBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, 
            hdcSource, rc.left, rc.top, rc.right - rc.left, 
            rc.bottom - rc.top, SRCCOPY); 
    }
 
    else 
    {
        BitBlt(hdcTarget, 0, 0, rc.right - rc.left, 
            rc.bottom - rc.top, 
            hdcSource, rc.left, rc.top, SRCCOPY); 
    }
 
    // Select the old source and destination bitmaps into the 
    // source and destination DCs, and then delete the DCs and 
    // the background brush. 
 
    SelectObject(hdcSource, hbmpSourceOld); 
    SelectObject(hdcTarget, hbrTargetOld); 
    hbmpCheck = SelectObject(hdcTarget, hbmpTargetOld); 
 
    DeleteObject(hbrBackground); 
    DeleteObject(hdcSource); 
    DeleteObject(hdcTarget); 
 
    // Return a handle to the new check-mark bitmap.  
 
    return hbmpCheck; 
} 
 
 
BYTE CheckOrUncheckMenuItem(BYTE bMenuItemID, HMENU hmenu) 
{ 
    DWORD fdwMenu; 
    static BYTE fbAttributes; 
 
    switch (bMenuItemID) 
    { 
        case IDM_REGULAR: 
 
            // Whenever the Regular menu item is selected, add a 
            // check mark to it and then remove checkmarks from 
            // any font-attribute menu items. 
 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
            } 
            fbAttributes = IDM_REGULAR; 
            return fbAttributes; 
 
        case IDM_BOLD: 
        case IDM_ITALIC: 
        case IDM_ULINE: 
 
            // Toggle the check mark for the selected menu item and 
            // set the font attribute flags appropriately. 
 
            fdwMenu = GetMenuState(hmenu, (UINT) bMenuItemID, 
                MF_BYCOMMAND); 
            if (!(fdwMenu & MF_CHECKED)) 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes |= bMenuItemID; 
            }
            else 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes ^= bMenuItemID; 
            } 
 
            // If any font attributes are currently selected, 
            // remove the check mark from the Regular menu item; 
            // if no attributes are selected, add a check mark 
            // to the Regular menu item. 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes &= (BYTE) ~IDM_REGULAR; 
            }
            else 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes = IDM_REGULAR; 
            } 
 
            return fbAttributes; 
    } 
} 
```



### <a name="example-of-using-custom-check-mark-bitmaps"></a><span data-ttu-id="fde4f-456">Пример использования пользовательских точечных рисунков с галочкой</span><span class="sxs-lookup"><span data-stu-id="fde4f-456">Example of Using Custom Check-mark Bitmaps</span></span>

<span data-ttu-id="fde4f-457">В примере, приведенном в этом разделе, к пунктам меню в двух меню присваиваются точечные рисунки с пользовательскими галочками.</span><span class="sxs-lookup"><span data-stu-id="fde4f-457">The example in this topic assigns custom check-mark bitmaps to menu items in two menus.</span></span> <span data-ttu-id="fde4f-458">Пункты меню в первом меню указывают атрибуты символов: полужирный, курсив и подчеркнутый.</span><span class="sxs-lookup"><span data-stu-id="fde4f-458">The menu items in the first menu specify character attributes: bold, italic, and underline.</span></span> <span data-ttu-id="fde4f-459">Каждый пункт меню может быть выбран или снят.</span><span class="sxs-lookup"><span data-stu-id="fde4f-459">Each menu item can be either selected or cleared.</span></span> <span data-ttu-id="fde4f-460">Для этих пунктов меню в примере используются точечные рисунки с галочками, которые похожи на выбранные и сброшенные состояния элемента управления "флажок".</span><span class="sxs-lookup"><span data-stu-id="fde4f-460">For these menu items, the example uses check-mark bitmaps that resemble the selected and cleared states of a check box control.</span></span>

<span data-ttu-id="fde4f-461">Пункты меню во втором меню задают параметры выравнивания абзаца: слева, по центру и справа.</span><span class="sxs-lookup"><span data-stu-id="fde4f-461">The menu items in the second menu specify paragraph alignment settings: left, centered, and right.</span></span> <span data-ttu-id="fde4f-462">В любое время выбирается только один из этих пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-462">Only one of these menu items is selected at any time.</span></span> <span data-ttu-id="fde4f-463">Для этих пунктов меню в примере используются точечные рисунки с галочками, которые похожи на выбранные и четкие состояния элемента управления "переключатель".</span><span class="sxs-lookup"><span data-stu-id="fde4f-463">For these menu items, the example uses check-mark bitmaps that resemble the selected and clear states of a radio button control.</span></span>

<span data-ttu-id="fde4f-464">Процедура окна обрабатывает сообщение о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) , вызывая функцию, определяемую приложением.</span><span class="sxs-lookup"><span data-stu-id="fde4f-464">The window procedure processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message by calling the application-defined OnCreate function.</span></span> <span data-ttu-id="fde4f-465">`OnCreate` создает четыре точечных рисунка галочки и затем назначает их соответствующим пунктам меню с помощью функции [**сетменуитембитмапс**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-465">`OnCreate` creates the four check-mark bitmaps and then assigns them to their appropriate menu items by using the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span>

<span data-ttu-id="fde4f-466">Для создания каждого точечного рисунка OnCreate вызывает определяемую приложением функцию Креатеменубитмапс, указывая указатель на функцию рисования, относящуюся к точечному рисунку.</span><span class="sxs-lookup"><span data-stu-id="fde4f-466">To create each bitmap, OnCreate calls the application-defined CreateMenuBitmaps function, specifying a pointer to a bitmap-specific drawing function.</span></span> <span data-ttu-id="fde4f-467">Креатеменубитмапс создает монохромное растровое изображение требуемого размера, выбирает его в контексте устройства памяти и стирает фон.</span><span class="sxs-lookup"><span data-stu-id="fde4f-467">CreateMenuBitmaps creates a monochrome bitmap of the required size, selects it into a memory device context, and erases the background.</span></span> <span data-ttu-id="fde4f-468">Затем вызывается указанная функция рисования для заполнения переднего плана.</span><span class="sxs-lookup"><span data-stu-id="fde4f-468">Then it calls the specified drawing function to fill in the foreground.</span></span>

<span data-ttu-id="fde4f-469">Четыре определяемые приложением функции рисования: Дравчекк, Дравунчекк, **драврадиочекк** и драврадиаунчекк.</span><span class="sxs-lookup"><span data-stu-id="fde4f-469">The four application-defined drawing functions are DrawCheck, DrawUncheck, **DrawRadioCheck**, and DrawRadioUncheck.</span></span> <span data-ttu-id="fde4f-470">Они нарисуют прямоугольник с символом X, пустым прямоугольником, эллипсом, содержащим меньший эллипс, и пустой эллипс соответственно.</span><span class="sxs-lookup"><span data-stu-id="fde4f-470">They draw a rectangle with an X, an empty rectangle, an ellipse containing a smaller filled ellipse, and an empty ellipse, respectively.</span></span>

<span data-ttu-id="fde4f-471">Процедура Window обрабатывает сообщение [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) , удаляя точечные рисунки галочки.</span><span class="sxs-lookup"><span data-stu-id="fde4f-471">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message by deleting the check-mark bitmaps.</span></span> <span data-ttu-id="fde4f-472">Он извлекает каждый растровый маркер с помощью функции [**жетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) , а затем передает в функцию маркер.</span><span class="sxs-lookup"><span data-stu-id="fde4f-472">It retrieves each bitmap handle by using the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function and then passes a handle to the function.</span></span>

<span data-ttu-id="fde4f-473">Когда пользователь выбирает пункт меню, в окно владельца отправляется [**\_ командное сообщение WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-473">When the user chooses a menu item, a [**WM\_COMMAND**](wm-command.md) message is sent to the owner window.</span></span> <span data-ttu-id="fde4f-474">Для пунктов меню в меню " **символ** " процедура Window вызывает определяемую приложением функцию чеккчарактеритем.</span><span class="sxs-lookup"><span data-stu-id="fde4f-474">For menu items on the **Character** menu, the window procedure calls the application-defined CheckCharacterItem function.</span></span> <span data-ttu-id="fde4f-475">Для элементов в меню « **абзац** » процедура Window вызывает определяемую приложением функцию чеккпараграфитем.</span><span class="sxs-lookup"><span data-stu-id="fde4f-475">For items on the **Paragraph** menu, the window procedure calls the application-defined CheckParagraphItem function.</span></span>

<span data-ttu-id="fde4f-476">Каждый элемент в меню « **символ** » можно выбирать и очищать независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="fde4f-476">Each item on the **Character** menu can be selected and cleared independently.</span></span> <span data-ttu-id="fde4f-477">Таким образом, Чеккчарактеритем просто переключается на состояние проверки указанного элемента меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-477">Therefore, CheckCharacterItem simply switches the specified menu item's check state.</span></span> <span data-ttu-id="fde4f-478">Сначала функция вызывает функцию [**жетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) для получения текущего состояния элемента меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-478">First, the function calls the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function to get the current menu item state.</span></span> <span data-ttu-id="fde4f-479">Затем он переключает флаг **состояния \_ checked MFA** и устанавливает новое состояние, вызывая функцию [**сетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-479">Then it switches the **MFS\_CHECKED** state flag and sets the new state by calling the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="fde4f-480">В отличие от атрибутов символов, одновременно можно выбрать только одно выравнивание абзаца.</span><span class="sxs-lookup"><span data-stu-id="fde4f-480">Unlike character attributes, only one paragraph alignment can be selected at a time.</span></span> <span data-ttu-id="fde4f-481">Таким образом, Чеккпараграфитем проверяет указанный пункт меню и снимает флажки для всех остальных элементов меню.</span><span class="sxs-lookup"><span data-stu-id="fde4f-481">Therefore, CheckParagraphItem checks the specified menu item and removes the check mark from all other items on the menu.</span></span> <span data-ttu-id="fde4f-482">Для этого вызывается функция [**чеккменурадиоитем**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) .</span><span class="sxs-lookup"><span data-stu-id="fde4f-482">To do so, it calls the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function.</span></span>

<span data-ttu-id="fde4f-483">Ниже приведены соответствующие части файла заголовка приложения.</span><span class="sxs-lookup"><span data-stu-id="fde4f-483">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_BOLD      11 
#define IDM_ITALIC    12 
#define IDM_UNDERLINE 13 
 
// Menu-item identifiers for the Paragraph menu 
 
#define IDM_PARAGRAPH 20 
#define IDM_LEFT      21 
#define IDM_CENTER    22 
#define IDM_RIGHT     23 
 
// Function-pointer type for drawing functions 
 
typedef VOID (WINAPI * DRAWFUNC)(HDC hdc, SIZE size); 
 
```



<span data-ttu-id="fde4f-484">Ниже приведены соответствующие части процедуры окна приложения и связанные функции.</span><span class="sxs-lookup"><span data-stu-id="fde4f-484">The following are the relevant portions of the application's window procedure and related functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_UNDERLINE: 
                    CheckCharacterItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                case IDM_LEFT: 
                case IDM_CENTER: 
                case IDM_RIGHT: 
                    CheckParagraphItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                // Process other commands here. 
 
            } 
            break; 
 
        // Process other messages here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
VOID WINAPI CheckCharacterItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the state of the specified menu item. 
 
    mii.fMask = MIIM_STATE;    // information to get 
    GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
 
    // Toggle the checked state. 
 
    mii.fState ^= MFS_CHECKED; 
    SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
} 
 
VOID WINAPI CheckParagraphItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Check the specified item and uncheck all the others. 
 
    CheckMenuRadioItem( 
            hmenuPopup,         // handle to menu 
            IDM_LEFT,           // first item in range 
            IDM_RIGHT,          // last item in range 
            uID,                // item to check 
            MF_BYCOMMAND        // IDs, not positions 
            ); 
} 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    HBITMAP hbmChecked; 
    HBITMAP hbmUnchecked; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_BOLD; uID <= IDM_UNDERLINE; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Get a handle to the Paragraph pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawRadioCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawRadioUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_LEFT; uID <= IDM_RIGHT; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Initially check the IDM_LEFT paragraph item. 
 
    CheckMenuRadioItem(hmenuPopup, IDM_LEFT, IDM_RIGHT, 
            IDM_LEFT, MF_BYCOMMAND); 
    return TRUE; 
} 
 
HBITMAP WINAPI CreateMenuBitmap(DRAWFUNC lpfnDraw) 
{ 
    // Create a DC compatible with the desktop window's DC. 
 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
 
    // Determine the required bitmap size. 
 
    SIZE size = { GetSystemMetrics(SM_CXMENUCHECK), 
                  GetSystemMetrics(SM_CYMENUCHECK) }; 
 
    // Create a monochrome bitmap and select it. 
 
    HBITMAP hbm = CreateBitmap(size.cx, size.cy, 1, 1, NULL); 
    HBITMAP hbmOld = SelectObject(hdcMem, hbm); 
 
    // Erase the background and call the drawing function. 
 
    PatBlt(hdcMem, 0, 0, size.cx, size.cy, WHITENESS); 
    (*lpfnDraw)(hdcMem, size); 
 
    // Clean up. 
 
    SelectObject(hdcMem, hbmOld); 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
    return hbm; 
} 
 
VOID WINAPI DrawCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    MoveToEx(hdc, 0, 0, NULL); 
    LineTo(hdc, size.cx, size.cy); 
    MoveToEx(hdc, 0, size.cy - 1, NULL); 
    LineTo(hdc, size.cx - 1, 0); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, GetStockObject(BLACK_BRUSH)); 
    Ellipse(hdc, 2, 2, size.cx - 2, size.cy - 2); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_BOLD, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_LEFT, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
} 
```



 

 