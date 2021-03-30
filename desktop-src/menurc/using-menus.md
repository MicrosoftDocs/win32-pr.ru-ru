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
# <a name="using-menus"></a>Использование меню

В этом разделе описаны следующие задачи.

-   [Использование ресурса Menu-Template](#using-a-menu-template-resource)
    -   [Расширенный формат Menu-Template](#extended-menu-template-format)
    -   [Старый формат Menu-Template](#old-menu-template-format)
    -   [Загрузка ресурса Menu-Template](#loading-a-menu-template-resource)
    -   [Создание меню класса](#creating-a-class-menu)
-   [Создание контекстного меню](#creating-a-shortcut-menu)
    -   [Обработка сообщения WM \_ CONTEXTMENU](/windows)
    -   [Создание контекстного меню Font-Attributes](#creating-a-shortcut-font-attributes-menu)
    -   [Отображение контекстного меню](#displaying-a-shortcut-menu)
-   [Использование точечных рисунков Menu-Item](#using-menu-item-bitmaps)
    -   [Установка флага типа точечного рисунка](#setting-the-bitmap-type-flag)
    -   [Создание точечного рисунка](#creating-the-bitmap)
    -   [Добавление линий и графиков в меню](#adding-lines-and-graphs-to-a-menu)
    -   [Пример Menu-Item точечных рисунков](#example-of-menu-item-bitmaps)
-   [Создание пунктов меню Owner-Drawn](#creating-owner-drawn-menu-items)
    -   [Установка флага Owner-Drawn](#setting-the-owner-drawn-flag)
    -   [Меню, рисуемые владельцем, и \_ сообщение WM меасуреитем](/windows)
    -   [Меню, рисуемые владельцем, и \_ сообщение WM DRAWITEM](/windows)
    -   [Меню, рисуемые владельцем, и \_ сообщение WM менучар](/windows)
    -   [Установка шрифтов для Menu-Item текстовых строк](#setting-fonts-for-menu-item-text-strings)
    -   [Пример пунктов меню Owner-Drawn](#example-of-owner-drawn-menu-items)
-   [Использование пользовательских точечных рисунков](#using-custom-check-mark-bitmaps)
    -   [Создание пользовательских точечных рисунков с галочками](#creating-custom-check-mark-bitmaps)
    -   [Связывание точечных рисунков с пунктом меню](#associating-bitmaps-with-a-menu-item)
    -   [Установка атрибута галочки](#setting-the-check-mark-attribute)
    -   [Имитация флажков в меню](#simulating-check-boxes-in-a-menu)
    -   [Пример использования пользовательских точечных рисунков с галочкой](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a>Использование ресурса Menu-Template

Обычно меню включается в приложение путем создания ресурса шаблона меню и последующей загрузки меню во время выполнения. В этом разделе описывается формат шаблона меню и объясняется, как загрузить ресурс шаблона меню и использовать его в приложении. Сведения о создании ресурса шаблона меню см. в документации, входящей в состав средств разработки.

-   [Расширенный формат Menu-Template](#extended-menu-template-format)
-   [Старый формат Menu-Template](#old-menu-template-format)
-   [Загрузка ресурса Menu-Template](#loading-a-menu-template-resource)
-   [Создание меню класса](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a>Расширенный формат Menu-Template

Расширенный формат шаблона меню поддерживает дополнительные функции меню. Как и в стандартном меню — ресурсы шаблона, расширенные ресурсы шаблона меню — это тип ресурса **\_ меню RT** . Система различает два формата ресурсов по номеру версии, который является первым элементом в заголовке ресурса.

Расширенный шаблон меню состоит из структуры [**\_ \_ заголовка шаблона менуекс**](menuex-template-header.md) , за которой следуют еще одна структура определения элемента [**\_ шаблона \_ менуекс**](menuex-template-item.md) .

### <a name="old-menu-template-format"></a>Старый формат Menu-Template

Шаблон старого меню (Microsoft Windows NT 3,51 и более ранних версий) определяет меню, но не поддерживает новые функции меню. Старый ресурс шаблона меню имеет тип ресурса **\_ меню RT** .

Старый шаблон меню состоит из структуры [**менуитемтемплатехеадер**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) , за которой следует одна или несколько структур [**менуитемтемплате**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .

### <a name="loading-a-menu-template-resource"></a>Загрузка ресурса Menu-Template

Чтобы загрузить ресурс шаблона меню, используйте функцию [**лоадмену**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) , указав маркер для модуля, содержащего ресурс, и идентификатор шаблона меню. Функция **лоадмену** возвращает маркер меню, который можно использовать для назначения меню окну. Это окно станет окном «владелец» меню, получающим все сообщения, созданные в меню.

Чтобы создать меню из шаблона меню, который уже находится в памяти, используйте функцию [**лоадменуиндирект**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) . Это полезно, если приложение создает шаблоны меню динамически.

Чтобы назначить меню окну, используйте функцию [**сетмену**](/windows/desktop/api/Winuser/nf-winuser-setmenu) или укажите маркер меню в параметре *HMENU* функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) при создании окна. Другой способ назначения меню окну — Указание шаблона меню при регистрации класса окна; шаблон определяет указанное меню в качестве меню класса для этого класса окна.

Чтобы система автоматически назначила определенное меню окну, укажите шаблон меню при регистрации класса окна. Шаблон определяет указанное меню в качестве меню класса для этого класса окна. Затем, когда вы создаете окно указанного класса, система автоматически назначает указанное меню окну.

Нельзя назначить меню окну, которое является дочерним окном.

Чтобы создать меню класса, включите идентификатор ресурса меню-шаблона в качестве элемента **лпсзменунаме** структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) , а затем передайте указатель на структуру функции [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) .

### <a name="creating-a-class-menu"></a>Создание меню класса

В следующем примере показано, как создать меню класса для приложения, создать окно, которое использует меню «класс» и команды «обработать» в процедуре окна.

Ниже приведена соответствующая часть файла заголовка приложения.


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



Ниже перечислены соответствующие части самого приложения.


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



## <a name="creating-a-shortcut-menu"></a>Создание контекстного меню

Чтобы использовать контекстное меню в приложении, передайте его обработчик функции [**траккпопупменуекс**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . Приложение обычно вызывает **траккпопупменуекс** в оконной процедуре в ответ на генерируемое пользователем сообщение, например [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown) или [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown).

Помимо маркера всплывающего меню, [**траккпопупменуекс**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) требует указать маркер для окна владельца, позицию контекстного меню (в экранных координатах) и кнопку мыши, которую пользователь может использовать для выбора элемента.

Старая функция [**метод TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) по-прежнему поддерживается, но новые приложения должны использовать функцию [**траккпопупменуекс**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . Функция **траккпопупменуекс** требует те же параметры, что и **метод TrackPopupMenu**, но также позволяет указать часть экрана, которую меню не должно скрывать. Приложение обычно вызывает эти функции в оконной процедуре при обработке сообщения [**WM \_ CONTEXTMENU**](wm-contextmenu.md) .

Можно указать расположение контекстного меню, указав координаты x и y вместе с флагом **TPM \_ центералигн**, **TPM \_ Лефталигн** или **\_ RIGHTALIGN доверенного платформенного модуля** . Флаг задает расположение контекстного меню относительно координат x и y.

Необходимо предоставить пользователю возможность выбирать элемент из контекстного меню, используя ту же кнопку мыши, которая используется для вывода меню. Для этого укажите флаг **TPM \_ Лефтбуттон** или **TPM \_ ригхтбуттон** , чтобы указать, какая кнопка мыши может использоваться для выбора пункта меню.

-   [Обработка сообщения WM \_ CONTEXTMENU](/windows)
-   [Создание контекстного меню Font-Attributes](#creating-a-shortcut-font-attributes-menu)
-   [Отображение контекстного меню](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a>Обработка сообщения WM \_ CONTEXTMENU

Сообщение [**WM \_ CONTEXTMENU**](wm-contextmenu.md) создается, когда процедура окна приложения передает сообщение [**WM \_ рбуттонуп**](/windows/desktop/inputdev/wm-rbuttonup) или [**WM \_ нкрбуттонуп**](/windows/desktop/inputdev/wm-ncrbuttonup) в функцию [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Приложение может обработать это сообщение, чтобы отобразить контекстное меню, соответствующее определенной части экрана. Если в приложении не отображается контекстное меню, оно должно передавать сообщение **дефвиндовпрок** для обработки по умолчанию.

Ниже приведен пример обработки сообщений [**WM \_ CONTEXTMENU**](wm-contextmenu.md) , как это может появиться в процедуре окна приложения. Слова с низким и высоким порядком параметров *lParam* определяют экранные координаты мыши при отпускании правой кнопки мыши (Обратите внимание, что эти координаты могут принимать отрицательные значения в системах с несколькими мониторами). Определяемая приложением функция **oncontextmenu** возвращает **значение true** , если она отображает контекстное меню, или **значение false** в противном случае.


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



Следующая определяемая приложением функция oncontextmenu отображает контекстное меню, если указанная позицией мыши находится в клиентской области окна. Более сложная функция может отображать одно из нескольких различных меню в зависимости от того, какая часть клиентской области задана. Для фактического вывода контекстного меню в этом примере вызывается определяемая приложением функция с именем Дисплайконтекстмену. Описание этой функции см. [в разделе Отображение контекстного меню](#displaying-a-shortcut-menu).


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



### <a name="creating-a-shortcut-font-attributes-menu"></a>Создание контекстного меню Font-Attributes

Пример в этом разделе содержит фрагменты кода из приложения, которое создает и отображает контекстное меню, позволяющее пользователю устанавливать шрифты и атрибуты шрифта. Приложение отображает меню в клиентской области его главного окна каждый раз, когда пользователь нажимает левую кнопку мыши.

Ниже приведен шаблон меню для контекстного меню, предоставленного в файле определения ресурсов приложения.


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



В следующем примере приводится процедура окна и вспомогательные функции, используемые для создания и вывода контекстного меню.


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



### <a name="displaying-a-shortcut-menu"></a>Отображение контекстного меню

Функция, показанная в следующем примере, выводит контекстное меню.

Приложение включает ресурс меню, определяемый строкой «Шорткутексампле». Строка меню просто содержит имя меню. Приложение использует функцию [**метод TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) для вывода меню, связанного с этим пунктом меню. (Сама строка меню не отображается, так как для **метод TrackPopupMenu** требуется маркер меню, подменю или контекстное меню.)


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



## <a name="using-menu-item-bitmaps"></a>Использование точечных рисунков Menu-Item

Для вывода пункта меню система может использовать точечный рисунок вместо текстовой строки. Чтобы использовать точечный рисунок, необходимо задать флаг **\_ точечного рисунка миим** для пункта меню и указать маркер для точечного рисунка, который должен отображаться системой для элемента меню в элементе **хбмпитем** структуры [**объектами menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . В этом разделе описывается использование точечных рисунков для пунктов меню.

-   [Установка флага типа точечного рисунка](#setting-the-bitmap-type-flag)
-   [Создание точечного рисунка](#creating-the-bitmap)
-   [Добавление линий и графиков в меню](#adding-lines-and-graphs-to-a-menu)
-   [Пример Menu-Item точечных рисунков](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a>Установка флага типа точечного рисунка

Флаг **\_ растрового** **\_ изображения миим** или MF указывает, что система использует точечный рисунок, а не текстовую строку для вывода пункта меню. Во время выполнения необходимо **задать \_ растровое изображение миим** или флаг **MF \_ Bitmap** . его нельзя задать в файле определения ресурса.

Для новых приложений можно использовать функцию [**сетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) или [**инсертменуитем**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) , чтобы установить флаг типа **\_ точечного рисунка миим** . Чтобы изменить пункт меню из текстового элемента на элемент точечного рисунка, используйте **сетменуитеминфо**. Чтобы добавить новый элемент Bitmap в меню, используйте функцию **инсертменуитем** .

Приложения, написанные для более ранних версий системы, могут продолжать использовать функции [**модифимену**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**инсертмену**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)или [**аппендмену**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) для установки флага **\_ битовой карты MF** . Чтобы изменить пункт меню из элемента текстовой строки на растровый элемент, используйте **модифимену**. Чтобы добавить новый элемент Bitmap в меню, используйте флаг **MF \_ Bitmap** с функцией **инсертмену** или **аппендмену** .

### <a name="creating-the-bitmap"></a>Создание точечного рисунка

При задании флага **\_ растрового изображения Миим** или **MF \_** для пункта меню необходимо также указать маркер для точечного рисунка, который система должна отображать для пункта меню. Можно указать точечный рисунок как ресурс точечного рисунка или создать точечный рисунок во время выполнения. При использовании ресурса точечного рисунка можно использовать функцию [**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) для загрузки точечного рисунка и получения его маркера.

Чтобы создать точечный рисунок во время выполнения, используйте функции Windows интерфейс графических устройств (GDI). GDI предоставляет несколько способов создания точечного рисунка во время выполнения, но разработчики обычно используют следующий метод:

1.  Используйте функцию [**креатекомпатибледк**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) , чтобы создать контекст устройства, совместимый с контекстом устройства, используемым главным окном приложения.
2.  Используйте функцию [**креатекомпатиблебитмап**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) для создания точечного рисунка, совместимого с главным окном приложения, или используйте функцию [**креатебитмап**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) для создания монохромного точечного рисунка.
3.  Используйте функцию [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) , чтобы выбрать точечный рисунок в совместимом контексте устройства.
4.  Для рисования изображения в растровом изображении используются функции рисования GDI, такие как [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) и [**lineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto).

Дополнительные сведения см. в разделе [точечные рисунки](/windows/desktop/gdi/bitmaps).

### <a name="adding-lines-and-graphs-to-a-menu"></a>Добавление линий и графиков в меню

В следующем примере кода показано, как создать меню, содержащее растровые изображения элементов меню. Он создает два меню. Первое — меню диаграммы, содержащее три точечных рисунка элемента меню: круговую диаграмму, график и линейчатую диаграмму. В примере показано, как загрузить эти растровые изображения из файла ресурсов приложения, а затем использовать функции [**креатепопупмену**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) и [**аппендмену**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) для создания меню и пунктов меню.

Второе меню — это меню «строки». Он содержит точечные рисунки, отображающие стили линий, предоставляемые стандартным пером в системе. Растровые изображения в стиле строки создаются во время выполнения с помощью функций GDI.

Ниже приведены определения ресурсов точечных рисунков в файле определения ресурсов приложения.


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



Ниже приведены соответствующие части файла заголовка приложения.


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



В следующем примере показано, как в приложении создаются растровые изображения меню и элементов меню.


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



### <a name="example-of-menu-item-bitmaps"></a>Пример Menu-Item точечных рисунков

Пример в этом разделе создает два меню, каждое из которых содержит несколько пунктов точечного меню. Для каждого меню приложение добавляет соответствующее имя меню в строку меню главного окна.

Первое меню содержит пункты меню, отображающие три типа диаграмм: круговые, линии и линейчатые. Точечные рисунки для этих пунктов меню определяются как ресурсы и загружаются с помощью функции [**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) . Связанное с этим меню представляет собой имя меню "Диаграмма" в строке меню.

Второе меню содержит пункты меню, показывающие каждый из пяти стилей линий, используемых с функцией [**креатепен**](/windows/desktop/api/wingdi/nf-wingdi-createpen) : **PS \_ сплошной**, **PS \_ тире**, **PS \_ Dot**, **PS \_ дашдот** и **PS \_ дашдотдот**. Приложение создает точечные рисунки для этих пунктов меню во время выполнения с помощью функций рисования GDI. Это меню связано с названием меню **строки** в строке меню.

Определение в процедуре окна приложения — это два статических массива дескрипторов битовой карты. Один массив содержит дескрипторы трех растровых изображений, используемых для меню **диаграммы** . Другой содержит маркеры из пяти растровых изображений, используемых в меню « **строки** ». При обработке сообщения [**, \_ созданного**](/windows/desktop/winmsg/wm-create) обработчиком WM, процедура Window загружает точечные рисунки диаграммы, создает точечные рисунки линий, а затем добавляет соответствующие пункты меню. При обработке сообщения [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) процедура Window удаляет все точечные рисунки.

Ниже приведены соответствующие части файла заголовка приложения.


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



Ниже приведены соответствующие части процедуры окна. Процедура Window выполняет большую часть своей инициализации, вызывая определяемые приложением функции Лоадчартбитмапс, Креателинебитмапс и Аддбитмапмену, описанные далее в этом разделе.


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



Определяемая приложением функция Лоадчартбитмапс загружает ресурсы точечного рисунка для меню диаграммы путем вызова функции [**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , как показано ниже.


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



Определяемая приложением функция Креателинебитмапс создает точечные рисунки для меню "линии" с помощью функций рисования GDI. Функция создает контекст устройства памяти (DC) с теми же свойствами, что и контроллер домена рабочего стола. Для каждого стиля линии функция создает точечный рисунок, выделяет его в памяти контроллера домена и рисует в нем.


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



Определяемая приложением функция Аддбитмапмену создает меню и добавляет в нее указанное число пунктов точечного меню. Затем он добавляет соответствующее имя меню в строку меню указанного окна.


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



## <a name="creating-owner-drawn-menu-items"></a>Создание пунктов меню Owner-Drawn

Если вам нужен полный контроль над видом элемента меню, можно использовать элемент меню, рисуемый владельцем приложения. В этом разделе описываются шаги, связанные с созданием и использованием элемента меню, рисуемого владельцем.

-   [Установка флага Owner-Drawn](#setting-the-owner-drawn-flag)
-   [Меню, рисуемые владельцем, и \_ сообщение WM меасуреитем](/windows)
-   [Меню, рисуемые владельцем, и \_ сообщение WM DRAWITEM](/windows)
-   [Меню, рисуемые владельцем, и \_ сообщение WM менучар](/windows)
-   [Установка шрифтов для Menu-Item текстовых строк](#setting-fonts-for-menu-item-text-strings)
-   [Пример пунктов меню Owner-Drawn](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a>Установка флага Owner-Drawn

Нельзя определить элемент меню, рисуемый владельцем, в файле определения ресурса приложения. Вместо этого необходимо создать новый пункт меню или изменить существующий с помощью флага меню **MFT \_ овнердрав** .

Для указания элемента меню, рисуемого владельцем, можно использовать функцию [**инсертменуитем**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) или [**сетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) . Используйте **инсертменуитем** для вставки нового пункта меню в указанную позицию в строке меню или меню. Используйте **сетменуитеминфо** для изменения содержимого меню.

При вызове этих двух функций необходимо указать указатель на структуру [**объектами menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , указывающую свойства нового пункта меню или свойства, которые необходимо изменить для существующего элемента меню. Чтобы сделать элемент элементом, рисуемым владельцем, укажите значение **миим \_ ftype** для элемента **Фмаск** и значение **\_ овнердрав MFT** для члена **ftype** .

Устанавливая соответствующие элементы структуры [**объектами menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , можно связать определяемое приложением значение, которое называется **данными элемента**, с каждым пунктом меню. Для этого укажите значение **\_ данных миим** для элемента **фмаск** и значение, определяемое приложением для элемента **двитемдата** .

Данные элемента можно использовать с любым типом пункта меню, но это особенно удобно для элементов, рисуемых владельцем. Например, предположим, что структура содержит сведения, используемые для рисования пункта меню. Приложение может использовать данные элемента для элемента меню для сохранения указателя на структуру. Данные элемента отправляются в окно владельца меню с сообщениями [**WM \_ Меасуреитем**](../controls/wm-measureitem.md) и [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) . Чтобы получить данные элемента для меню в любое время, используйте функцию [**жетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

Приложения, написанные для более ранних версий системы, могут по-прежнему вызывать [**аппендмену**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**инсертмену**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)или [**Модифимену**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) для назначения флага **MF \_ овнердрав** элементу меню, рисуемому владельцем.

При вызове любой из этих трех функций можно передать значение в качестве параметра *лпневитем* . Это значение может представлять любую информацию, значимую для приложения, и будет доступна приложению при отображении элемента. Например, значение может содержать указатель на структуру; структура, в свою очередь, может содержать текстовую строку и маркер для логического шрифта, который приложение будет использовать для рисования строки.

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a>Owner-Drawn меню и \_ сообщение МЕАСУРЕИТЕМ WM

Прежде чем система выведет на экран элемент меню, рисуемый владельцем впервые, он отправляет сообщение [**WM \_ меасуреитем**](../controls/wm-measureitem.md) в оконную процедуру окна, которому принадлежит меню элемента. Это сообщение содержит указатель на структуру [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) , которая идентифицирует элемент и содержит данные элемента, которые могли быть назначены приложению. Процедура окна должна заполнить члены структуры **итемвидс** и **итемхеигхт** перед возвратом из обработки сообщения. Система использует информацию этих членов при создании ограничивающего прямоугольника, в котором приложение рисует пункт меню. Он также использует информацию для определения того, когда пользователь выбирает элемент.

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a>Owner-Drawn меню и \_ сообщение DRAWITEM WM

Каждый раз, когда элемент должен быть нарисован (например, когда он впервые отображается или когда пользователь выбирает его), система отправляет сообщение [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) в оконную процедуру окна "владелец" меню. Это сообщение содержит указатель на структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , которая содержит сведения об элементе, включая данные элемента, которые могли быть назначены приложению. Кроме того, **дравитемструкт** содержит флаги, указывающие состояние элемента (например, является ли он серым или выделенным), а также ограничивающий прямоугольник и контекст устройства, используемый приложением для рисования элемента.

При обработке сообщения [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) приложение должно выполнить следующие действия:

-   Определите необходимый тип рисунка. Для этого проверьте элемент **итемактион** структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .
-   Нарисуйте элемент меню соответствующим образом, используя ограничивающий прямоугольник и контекст устройства, полученные из структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . Приложение должно рисовать только в ограничивающем прямоугольнике. Из соображений производительности система не обрезает фрагменты изображения, рисуемые за пределами прямоугольника.
-   Восстановите все объекты GDI, выбранные для контекста устройства этого пункта меню.

Если пользователь выбирает пункт меню, система устанавливает для элемента **итемактион** структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) значение **Ода \_ SELECT** Value и устанавливает **\_ выбранное значение ODS** в элементе **ItemState** . Это подсказка приложения для перерисовки пункта меню, чтобы показать, что он выбран.

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a>Owner-Drawn меню и \_ сообщение МЕНУЧАР WM

В меню, отличном от рисуемых владельцем меню, можно указать клавишу меню, вставив знак подчеркивания рядом с символом в строке меню. Это позволяет пользователю выбрать меню, нажав клавишу ALT и нажимая клавишу «Menu». Однако в меню, рисуемых владельцем, при этом нельзя указать назначенную ему команду меню. Вместо этого приложение должно обработать сообщение [**WM \_ менучар**](wm-menuchar.md) , чтобы предоставить меню, рисуемое владельцем, с помощью мнемоник меню.

Сообщение [**WM \_ менучар**](wm-menuchar.md) отправляется, когда пользователь вводит назначенную клавишу меню, не совпадающую ни с одной из стандартных мнемоник текущего меню. Значение, содержащееся в параметре *wParam* , указывает символ ASCII, соответствующий ключу, который пользователь нажал с помощью клавиши ALT. Слово *wParam* с низким приоритетом определяет тип выбранного меню и может принимать одно из следующих значений:

-   **MF \_ Всплывающее окно** , если текущее меню является подменю.
-   **MF \_ СИСМЕНУ** , если меню является системным меню.

Слово « *wParam* » высокого порядка содержит маркер меню для текущего меню. Окно с меню, рисуемым владельцем, может обрабатывать [**WM \_ менучар**](wm-menuchar.md) следующим образом:


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



Два в слове с высоким порядком возвращаемого значения уведомляют систему о том, что младшее слово возвращаемого значения содержит Отсчитываемый от нуля индекс выбираемого элемента меню.

Следующие константы соответствуют возможным возвращаемым значениям из сообщения [**\_ менучар WM**](wm-menuchar.md) .



| Константа         | Значение | Значение                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **МНК \_ игнорировать**  | 0     | Система должна отказаться от нажатого пользователем символа и создать короткий звуковой сигнал на системном докладчике.                                                       |
| **МНК \_ Закрыть**   | 1     | Система должна закрыть активное меню.                                                                                                                      |
| **\_выполнение МНК** | 2     | Система должна выбрать элемент, указанный в младшем слове возвращаемого значения. Окно-владелец получает сообщение [**\_ командной строки WM**](wm-command.md) . |
| **МНК \_ SELECT**  | 3     | Система должна выбрать элемент, указанный в младшем слове возвращаемого значения.                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a>Установка шрифтов для Menu-Item текстовых строк

В этом разделе содержится пример из приложения, в котором используются элементы меню, рисуемые владельцем. Меню содержит элементы, устанавливающие атрибуты текущего шрифта, и элементы отображаются с помощью соответствующего атрибута Font.

Вот как это меню определено в файле определения ресурса. Обратите внимание, что строки для элементов меню обычный, полужирный, курсив и подчеркивание присваиваются во время выполнения, поэтому их строки в файле определения ресурсов пусты.


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



Окно приложения обрабатывает сообщения, участвующие в использовании элементов меню, рисуемых владельцем. Приложение использует сообщение о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) для следующих задач:

-   Установите флаг **MF \_ овнердрав** для пунктов меню.
-   Задайте текстовые строки для пунктов меню.
-   Получение дескрипторов шрифтов, используемых для рисования элементов.
-   Получение значений цвета текста и фона для выбранных пунктов меню.

Текстовые строки и дескрипторы шрифтов хранятся в массиве определяемых приложением структур МИТЕМ. Определяемая приложением функция Жетафонт создает шрифт, соответствующий указанному атрибуту Font, и возвращает маркер для шрифта. Дескрипторы уничтожаются во время обработки сообщения [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) .

Во время обработки сообщения [**WM \_ меасуреитем**](../controls/wm-measureitem.md) в примере получается ширина и высота строки элемента меню, и эти значения копируются в структуру [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) . Система использует значения Width и Height для вычисления размера меню.

Во время обработки сообщения [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) строка элемента меню рисуется с помощью комнаты слева рядом со строкой для точечного рисунка галочки. Если пользователь выбирает элемент, для рисования элемента используются выделенные цвета текста и фона.


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



### <a name="example-of-owner-drawn-menu-items"></a>Пример пунктов меню Owner-Drawn

В примере в этом разделе в меню используются элементы меню, рисуемые владельцем. Пункты меню выбирают конкретные атрибуты шрифта, и приложение отображает каждый элемент меню, используя шрифт с соответствующим атрибутом. Например, элемент меню **курсив** отображается курсивом. Откроется меню с **символами** в строке меню.

Строка меню и раскрывающееся меню определяются с помощью расширенного ресурса шаблона меню. Поскольку шаблон меню не может указывать элементы, рисуемые владельцем, меню изначально содержит четыре пункта текстового меню со следующими строками: "обычный", "полужирный", "Курсив" и "подчеркнутый". Процедура окна приложения изменяет их на рисуемые владельцем элементы при обработке сообщения о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) . При получении сообщения о **\_ создании WM** процедура Window вызывает функцию, определяемую приложением, которая выполняет следующие действия для каждого пункта меню:

-   Выделяет определенную приложением структуру МИТЕМ.
-   Возвращает текст пункта меню и сохраняет его в определяемой приложением структуре МИТЕМ.
-   Создает шрифт, используемый для вывода пункта меню, и сохраняет его маркер в определяемой приложением структуре МИТЕМ.
-   Изменяет тип элемента меню на **MFT \_ овнердрав** и сохраняет указатель на определенную приложением структуру митем в виде данных элемента.

Поскольку указатель на каждую определенную приложением структуру МИТЕМ сохраняется как данные элемента, он передается в процедуру окна вместе с сообщениями [**WM \_ Меасуреитем**](../controls/wm-measureitem.md) и [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) для соответствующего пункта меню. Указатель содержится в элементе **итемдата** в структурах [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) и [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .

Сообщение [**WM \_ меасуреитем**](../controls/wm-measureitem.md) отправляется для каждого элемента меню, рисуемого владельцем, при первом его отображении. Приложение обрабатывает это сообщение, выбирая шрифт для пункта меню в контексте устройства, а затем определяя пространство, необходимое для вывода текста пункта меню в этом шрифте. Текст шрифта и пункта меню определяется `MYITEM` структурой пункта меню (структурой, определенной приложением). Приложение определяет размер текста с помощью функции [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) .

Процедура окна обрабатывает сообщение [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) , отображая текст пункта меню соответствующим шрифтом. Текст шрифта и пункта меню задаются `MYITEM` структурой пункта меню. Приложение выбирает цвета текста и фона, соответствующие состоянию пункта меню.

Процедура Window обрабатывает сообщение [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) для уничтожения шрифтов и освобождения памяти. Приложение удаляет шрифт и освобождает структуру МИТЕМ, определяемую приложением, для каждого пункта меню.

Ниже приведены соответствующие части файла заголовка приложения.


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



Ниже приведены соответствующие части процедуры окна приложения и связанные с ней функции.


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



## <a name="using-custom-check-mark-bitmaps"></a>Использование пользовательских точечных рисунков

Система предоставляет растровое изображение галочки по умолчанию для отображения рядом с выбранным пунктом меню. Можно настроить отдельный элемент меню, предоставив пару точечных рисунков, чтобы заменить точечный рисунок галочки по умолчанию. Система отображает одно растровое изображение, когда элемент выбран и другой при его очистке. В этом разделе описываются шаги, связанные с созданием и использованием пользовательских точечных рисунков с галочкой.

-   [Создание пользовательских точечных рисунков с галочками](#creating-custom-check-mark-bitmaps)
-   [Связывание точечных рисунков с пунктом меню](#associating-bitmaps-with-a-menu-item)
-   [Установка атрибута галочки](#setting-the-check-mark-attribute)
-   [Имитация флажков в меню](#simulating-check-boxes-in-a-menu)
-   [Пример использования пользовательских точечных рисунков с галочкой](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a>Создание пользовательских точечных рисунков с галочками

Пользовательское растровое изображение галочки должно иметь тот же размер, что и точечный рисунок галочки по умолчанию. Вы можете получить размер отметки по умолчанию для точечного рисунка, вызвав функцию [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Слово с низким приоритетом возвращаемого значения этой функции указывает ширину; слово в высоком порядке указывает высоту.

Вы можете использовать ресурсы точечного рисунка для предоставления точечных рисунков галочки. Однако, поскольку требуемый размер растрового изображения зависит от типа дисплея, может потребоваться изменить размер растрового изображения во время выполнения с помощью функции [**стретчблт**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) . В зависимости от точечного рисунка искажение, вызванное изменением размера, может привести к неприемлемым результатам.

Вместо использования ресурса точечного рисунка можно создать точечный рисунок во время выполнения с помощью функций GDI.

**Создание точечного рисунка во время выполнения**

1.  Используйте функцию [**креатекомпатибледк**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) , чтобы создать контекст устройства, совместимый с тем, который используется главным окном приложения.

    В параметре *HDC* функции можно указать значение **null** или возврат из функции. [**Креатекомпатибледк**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) возвращает маркер для совместимого контекста устройства.

2.  Используйте функцию [**креатекомпатиблебитмап**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) , чтобы создать точечный рисунок, совместимый с главным окном приложения.

    Параметры *нвидс* и *нхеигхт* этой функции устанавливают размер растрового изображения. они должны указывать сведения о ширине и высоте, возвращаемые функцией [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .

    > [!Note]  
    > Для создания монохромного точечного рисунка можно также использовать функцию [**креатебитмап**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) .

     

3.  Используйте функцию [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) , чтобы выбрать точечный рисунок в совместимом контексте устройства.
4.  Используйте функции рисования GDI, такие как [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) и [**lineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), для рисования изображения в растровом изображении или для копирования изображения в растровое изображение с помощью таких функций, как [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) и [**стретчблт**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) .

Дополнительные сведения см. в разделе [точечные рисунки](/windows/desktop/gdi/bitmaps).

### <a name="associating-bitmaps-with-a-menu-item"></a>Связывание точечных рисунков с пунктом меню

Пара битов точечных рисунков связывается с пунктом меню путем передачи дескрипторов растровых изображений в функцию [**сетменуитембитмапс**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) . Параметр *хбитмапунчеккед* Определяет битовую карту, а параметр *хбитмапчеккед* определяет выбранный точечный рисунок. Если вы хотите удалить один или оба флажка из пункта меню, можно задать для параметра *хбитмапунчеккед* или *хбитмапчеккед* значение **null**.

### <a name="setting-the-check-mark-attribute"></a>Установка атрибута галочки

Функция [**чеккменуитем**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) задает для выбранного или сброшенного атрибута элемента меню флажок. Можно указать значение, установленное в параметре **MF \_** , чтобы присвоить атрибуту галочки значение выбрано, а **\_ непроверенное — MF** — очистить.

Вы также можете задать состояние проверки пункта меню с помощью функции [**сетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .

Иногда группа элементов меню представляет набор взаимоисключающих параметров. С помощью функции [**чеккменурадиоитем**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) можно проверить один пункт меню и одновременно снять флажок рядом с другими элементами меню в группе.

### <a name="simulating-check-boxes-in-a-menu"></a>Имитация флажков в меню

В этом разделе содержится пример, демонстрирующий имитацию флажков в меню. Этот пример содержит меню символов, элементы которого позволяют пользователю задать атрибуты полужирного начертания, курсива и подчеркивания текущего шрифта. Если атрибут Font действует, флажок рядом с соответствующим пунктом меню отображается галочкой. в противном случае рядом с элементом отображается пустой флажок.

В примере точечный рисунок галочки по умолчанию заменен двумя точечными рисунками: точечный рисунок с выбранным флажком и точечный рисунок с пустым полем. Выделенное битовое изображение флажка отображается рядом с пунктом меню полужирный, курсив или подчеркнутый, если для атрибута элемента установлен флажок установить значение **MF \_**. Если атрибут галочки установлен в значение **MF \_** снят, отображается битовое изображение флажка очистить или пусто.

Система предоставляет предопределенный точечный рисунок, который содержит изображения, используемые для флажков и переключателей. В этом примере изолируются флажки "выбранные" и "пустые", они копируются в два отдельных точечных рисунка, а затем используются в качестве выделенных и очищенных растровых изображений для элементов в меню " **символ** ".

Чтобы получить маркер для точечного рисунка с флажком, в примере вызывается функция [**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) с указанием **значения NULL** в качестве параметра *HINSTANCE* и **ОБМ \_ CheckBox** в качестве параметра *лпбитмапнаме* . Поскольку изображения в точечном рисунке имеют одинаковый размер, в примере их можно изолировать, разделив ширину и высоту растрового изображения на количество изображений в их строках и столбцах.

В следующей части файла определения ресурсов показано, как определяются элементы меню в меню « **символ** ». Обратите внимание, что атрибуты шрифта изначально не действуют, поэтому атрибуту галочки для **обычного** элемента присваивается значение выбрано и по умолчанию атрибуту галочки оставшихся элементов присваивается значение Clear.


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



Ниже приведено соответствующее содержимое файла заголовка приложения.


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



В следующем примере показаны части процедуры окна, которые создают точечные рисунки с галочкой. Задайте атрибут галочки для пунктов меню **полужирный**, **курсив** и **Подчеркивание** . и уничтожать растровые изображения галочки.


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



### <a name="example-of-using-custom-check-mark-bitmaps"></a>Пример использования пользовательских точечных рисунков с галочкой

В примере, приведенном в этом разделе, к пунктам меню в двух меню присваиваются точечные рисунки с пользовательскими галочками. Пункты меню в первом меню указывают атрибуты символов: полужирный, курсив и подчеркнутый. Каждый пункт меню может быть выбран или снят. Для этих пунктов меню в примере используются точечные рисунки с галочками, которые похожи на выбранные и сброшенные состояния элемента управления "флажок".

Пункты меню во втором меню задают параметры выравнивания абзаца: слева, по центру и справа. В любое время выбирается только один из этих пунктов меню. Для этих пунктов меню в примере используются точечные рисунки с галочками, которые похожи на выбранные и четкие состояния элемента управления "переключатель".

Процедура окна обрабатывает сообщение о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) , вызывая функцию, определяемую приложением. `OnCreate` создает четыре точечных рисунка галочки и затем назначает их соответствующим пунктам меню с помощью функции [**сетменуитембитмапс**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .

Для создания каждого точечного рисунка OnCreate вызывает определяемую приложением функцию Креатеменубитмапс, указывая указатель на функцию рисования, относящуюся к точечному рисунку. Креатеменубитмапс создает монохромное растровое изображение требуемого размера, выбирает его в контексте устройства памяти и стирает фон. Затем вызывается указанная функция рисования для заполнения переднего плана.

Четыре определяемые приложением функции рисования: Дравчекк, Дравунчекк, **драврадиочекк** и драврадиаунчекк. Они нарисуют прямоугольник с символом X, пустым прямоугольником, эллипсом, содержащим меньший эллипс, и пустой эллипс соответственно.

Процедура Window обрабатывает сообщение [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) , удаляя точечные рисунки галочки. Он извлекает каждый растровый маркер с помощью функции [**жетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) , а затем передает в функцию маркер.

Когда пользователь выбирает пункт меню, в окно владельца отправляется [**\_ командное сообщение WM**](wm-command.md) . Для пунктов меню в меню " **символ** " процедура Window вызывает определяемую приложением функцию чеккчарактеритем. Для элементов в меню « **абзац** » процедура Window вызывает определяемую приложением функцию чеккпараграфитем.

Каждый элемент в меню « **символ** » можно выбирать и очищать независимо друг от друга. Таким образом, Чеккчарактеритем просто переключается на состояние проверки указанного элемента меню. Сначала функция вызывает функцию [**жетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) для получения текущего состояния элемента меню. Затем он переключает флаг **состояния \_ checked MFA** и устанавливает новое состояние, вызывая функцию [**сетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .

В отличие от атрибутов символов, одновременно можно выбрать только одно выравнивание абзаца. Таким образом, Чеккпараграфитем проверяет указанный пункт меню и снимает флажки для всех остальных элементов меню. Для этого вызывается функция [**чеккменурадиоитем**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) .

Ниже приведены соответствующие части файла заголовка приложения.


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



Ниже приведены соответствующие части процедуры окна приложения и связанные функции.


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



 

 