---
title: Использование буфера обмена
description: В этом разделе приведены примеры кода для следующих задач.
ms.assetid: 377fb2cc-5b46-481a-8222-9291e504ae2c
keywords:
- буфер обмена, вырезание данных
- буфер обмена, копирование данных
- буфер обмена, вставленные данные
- буфер обмена, выбор данных
- буфер обмена, команды меню "Правка"
- буфер обмена, средства просмотра
- буфер обмена, окна средства просмотра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b2b0a12af9bac8c1bbe7c895a1951c9c02513bc8222ace107e39b23bf3d6ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811560"
---
# <a name="using-the-clipboard"></a>Использование буфера обмена

В этом разделе приведены примеры кода для следующих задач:

-   [Реализация команд вырезания, копирования и вставки](#implementing-the-cut-copy-and-paste-commands)
    -   [Выбор данных](#selecting-data)
    -   [Создание меню "Правка"](#creating-an-edit-menu)
    -   [Обработка сообщения WM \_ инитменупопуп](#processing-the-wm_initmenupopup-message)
    -   [Обработка \_ командного сообщения WM](#processing-the-wm_command-message)
    -   [Копирование данных в буфер обмена](#copying-information-to-the-clipboard)
    -   [Вставлены сведения из буфера обмена](#pasting-information-from-the-clipboard)
    -   [Регистрация формата буфера обмена](#registering-a-clipboard-format)
    -   [Обработка сообщений WM \_ RENDERFORMAT и WM \_ рендераллформатс](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [Обработка сообщения WM \_ дестройклипбоард](#processing-the-wm_destroyclipboard-message)
    -   [Использование формата буфера обмена Owner-Display](#using-the-owner-display-clipboard-format)
-   [Мониторинг содержимого буфера обмена](#monitoring-clipboard-contents)
-   [Запрос порядкового номера буфера обмена](#querying-the-clipboard-sequence-number)
-   [Создание прослушивателя формата буфера обмена](#creating-a-clipboard-format-listener)
-   [Создание окна средства просмотра буфера обмена](#creating-a-clipboard-viewer-window)
-   [Добавление окна в цепочку средства просмотра буфера обмена](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [Обработка сообщения WM \_ чанжекбчаин](#processing-the-wm_changecbchain-message)
    -   [Удаление окна из цепочки окна просмотра буфера обмена](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [Обработка сообщения WM \_ дравклипбоард](#processing-the-wm_drawclipboard-message)
    -   [Пример средства просмотра буфера обмена](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a>Реализация команд вырезания, копирования и вставки

В этом разделе описывается, как стандартные команды **вырезания**, **копирования** и **вставки** реализуются в приложении. В примере в этом разделе эти методы используются для размещения данных в буфере обмена с помощью зарегистрированного формата буфера обмена, формата **\_ овнердисплай CF** и **\_ текстового формата CF** . Зарегистрированный формат используется для представления прямоугольных или эллиптических текстовых окон, называемых метками.

### <a name="selecting-data"></a>Выбор данных

Прежде чем копировать данные в буфер обмена, пользователь должен выбрать определенные данные для копирования или вырезания. Приложение должно предоставлять пользователю возможность выбора информации в документе и какого-либо визуального отзыва для указания выбранных данных.

### <a name="creating-an-edit-menu"></a>Создание меню "Правка"

Приложение должно загрузить таблицу сочетаний клавиш, содержащую стандартные сочетания клавиш для команд меню " **Правка** ". Чтобы сочетания клавиш вступили в силу, необходимо добавить функцию [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) в цикл обработки сообщений приложения. Дополнительные сведения о сочетаниях клавиш см. в разделе [сочетания](/windows/desktop/menurc/keyboard-accelerators)клавиш.

### <a name="processing-the-wm_initmenupopup-message"></a>Обработка сообщения WM \_ инитменупопуп

Не все команды буфера обмена доступны пользователю в любое заданное время. Приложение должно обработать сообщение [**WM \_ инитменупопуп**](/windows/desktop/menurc/wm-initmenupopup) , чтобы включить пункты меню для доступных команд и отключить недоступные команды.

Ниже приведен регистр [**WM \_ инитменупопуп**](/windows/desktop/menurc/wm-initmenupopup) для приложения с именем Label.


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



Функция Инитмену определяется следующим образом.


```
void WINAPI InitMenu(HMENU hmenu) 
{ 
    int  cMenuItems = GetMenuItemCount(hmenu); 
    int  nPos; 
    UINT id; 
    UINT fuFlags; 
    PLABELBOX pbox = (hwndSelected == NULL) ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    for (nPos = 0; nPos < cMenuItems; nPos++) 
    { 
        id = GetMenuItemID(hmenu, nPos); 
 
        switch (id) 
        { 
            case IDM_CUT: 
            case IDM_COPY: 
            case IDM_DELETE: 
                if (pbox == NULL || !pbox->fSelected) 
                    fuFlags = MF_BYCOMMAND | MF_GRAYED; 
                else if (pbox->fEdit) 
                    fuFlags = (id != IDM_DELETE && pbox->ichSel 
                            == pbox->ichCaret) ? 
                        MF_BYCOMMAND | MF_GRAYED : 
                        MF_BYCOMMAND | MF_ENABLED; 
                else 
                    fuFlags = MF_BYCOMMAND | MF_ENABLED; 
 
                EnableMenuItem(hmenu, id, fuFlags); 
                break; 
 
            case IDM_PASTE: 
                if (pbox != NULL && pbox->fEdit) 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable(CF_TEXT) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
                else 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable( 
                                uLabelFormat) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
 
        } 
    } 
}
```



### <a name="processing-the-wm_command-message"></a>Обработка \_ командного сообщения WM

Чтобы обработать команды меню, добавьте [**\_ командный сценарий WM**](/windows/desktop/menurc/wm-command) в главную оконную процедуру приложения. Ниже приведен пример **\_ команды WM** для процедуры окна приложения Label.


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_CUT: 
            if (EditCopy()) 
                EditDelete(); 
            break; 
 
        case IDM_COPY: 
            EditCopy(); 
            break; 
 
        case IDM_PASTE: 
            EditPaste(); 
            break; 
 
        case IDM_DELETE: 
            EditDelete(); 
            break; 
 
        case IDM_EXIT: 
            DestroyWindow(hwnd); 
    } 
    break; 
```



Для выполнения команд **Copy** и **Cut** процедура Window вызывает определяемую приложением функцию едиткопи. Дополнительные сведения см. в разделе [копирование данных в буфер обмена](#copying-information-to-the-clipboard). Для выполнения команды **Paste** процедура Window вызывает определяемую приложением функцию едитпасте. Дополнительные сведения о функции Едитпасте см. в разделе [о вставлении данных из буфера обмена](#pasting-information-from-the-clipboard).

### <a name="copying-information-to-the-clipboard"></a>Копирование данных в буфер обмена

В приложении-метке функция Едиткопи, определяемая приложением, копирует текущее выделение в буфер обмена. Эта функция выполняет следующие действия:

1.  Открывает буфер обмена, вызывая функцию [**опенклипбоард**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .
2.  Очищает буфер обмена, вызывая функцию [**емптиклипбоард**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) .
3.  Вызывает функцию [**сетклипбоарддата**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) один раз для каждого формата буфера обмена, предоставляемого приложением.
4.  Закрывает буфер обмена, вызывая функцию [**клосеклипбоард**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

В зависимости от текущего выбора функция Едиткопи копирует диапазон текста или копирует определенную приложением структуру, представляющую всю метку. Структура, именуемая ЛАБЕЛБОКС, определяется следующим образом.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



Ниже приведена функция Едиткопи.


```
BOOL WINAPI EditCopy(VOID) 
{ 
    PLABELBOX pbox; 
    LPTSTR  lptstrCopy; 
    HGLOBAL hglbCopy; 
    int ich1, ich2, cch; 
 
    if (hwndSelected == NULL) 
        return FALSE; 
 
    // Open the clipboard, and empty it. 
 
    if (!OpenClipboard(hwndMain)) 
        return FALSE; 
    EmptyClipboard(); 
 
    // Get a pointer to the structure for the selected label. 
 
    pbox = (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If text is selected, copy it using the CF_TEXT format. 
 
    if (pbox->fEdit) 
    { 
        if (pbox->ichSel == pbox->ichCaret)     // zero length
        {   
            CloseClipboard();                   // selection 
            return FALSE; 
        } 
 
        if (pbox->ichSel < pbox->ichCaret) 
        { 
            ich1 = pbox->ichSel; 
            ich2 = pbox->ichCaret; 
        } 
        else 
        { 
            ich1 = pbox->ichCaret; 
            ich2 = pbox->ichSel; 
        } 
        cch = ich2 - ich1; 
 
        // Allocate a global memory object for the text. 
 
        hglbCopy = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglbCopy == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
 
        // Lock the handle and copy the text to the buffer. 
 
        lptstrCopy = GlobalLock(hglbCopy); 
        memcpy(lptstrCopy, &pbox->atchLabel[ich1], 
            cch * sizeof(TCHAR)); 
        lptstrCopy[cch] = (TCHAR) 0;    // null character 
        GlobalUnlock(hglbCopy); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglbCopy); 
    } 
 
    // If no text is selected, the label as a whole is copied. 
 
    else 
    { 
        // Save a copy of the selected label as a local memory 
        // object. This copy is used to render data on request. 
        // It is freed in response to the WM_DESTROYCLIPBOARD 
        // message. 
 
        pboxLocalClip = (PLABELBOX) LocalAlloc( 
            LMEM_FIXED, 
            sizeof(LABELBOX) 
        ); 
        if (pboxLocalClip == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
        memcpy(pboxLocalClip, pbox, sizeof(LABELBOX)); 
        pboxLocalClip->fSelected = FALSE; 
        pboxLocalClip->fEdit = FALSE; 
 
        // Place a registered clipboard format, the owner-display 
        // format, and the CF_TEXT format on the clipboard using 
        // delayed rendering. 
 
        SetClipboardData(uLabelFormat, NULL); 
        SetClipboardData(CF_OWNERDISPLAY, NULL); 
        SetClipboardData(CF_TEXT, NULL); 
    } 
 
    // Close the clipboard. 
 
    CloseClipboard(); 
 
    return TRUE; 
}
```



### <a name="pasting-information-from-the-clipboard"></a>Вставлены сведения из буфера обмена

В приложении Label функция Едитпасте, определяемая приложением, вставит содержимое буфера обмена. Эта функция выполняет следующие действия:

1.  Открывает буфер обмена, вызывая функцию [**опенклипбоард**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .
2.  Определяет, какой из доступных форматов буфера обмена требуется извлечь.
3.  Извлекает маркер для данных в выбранном формате путем вызова функции [**жетклипбоарддата**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) .
4.  Вставляет копию данных в документ.

    Маркер, возвращенный [**жетклипбоарддата**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) , по-прежнему принадлежит буферу обмена, поэтому приложение не должно освободить его или оставить заблокированным.

5.  Закрывает буфер обмена, вызывая функцию [**клосеклипбоард**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

Если метка выбрана и содержит точку вставки, функция Едитпасте вставляет текст из буфера обмена в точку вставки. Если ничего не выделено или если метка выбрана, функция создает новую метку, используя определяемую приложением структуру ЛАБЕЛБОКС в буфере обмена. Структура ЛАБЕЛБОКС помещается в буфер обмена с помощью зарегистрированного формата буфера обмена.

Структура, именуемая ЛАБЕЛБОКС, определяется следующим образом.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



Ниже приведена функция Едитпасте.


```
VOID WINAPI EditPaste(VOID) 
{ 
    PLABELBOX pbox; 
    HGLOBAL   hglb; 
    LPTSTR    lptstr; 
    PLABELBOX pboxCopy; 
    int cx, cy; 
    HWND hwnd; 
 
    pbox = hwndSelected == NULL ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If the application is in edit mode, 
    // get the clipboard text. 
 
    if (pbox != NULL && pbox->fEdit) 
    { 
        if (!IsClipboardFormatAvailable(CF_TEXT)) 
            return; 
        if (!OpenClipboard(hwndMain)) 
            return; 
 
        hglb = GetClipboardData(CF_TEXT); 
        if (hglb != NULL) 
        { 
            lptstr = GlobalLock(hglb); 
            if (lptstr != NULL) 
            { 
                // Call the application-defined ReplaceSelection 
                // function to insert the text and repaint the 
                // window. 
 
                ReplaceSelection(hwndSelected, pbox, lptstr); 
                GlobalUnlock(hglb); 
            } 
        } 
        CloseClipboard(); 
 
        return; 
    } 
 
    // If the application is not in edit mode, 
    // create a label window. 
 
    if (!IsClipboardFormatAvailable(uLabelFormat)) 
        return; 
    if (!OpenClipboard(hwndMain)) 
        return; 
 
    hglb = GetClipboardData(uLabelFormat); 
    if (hglb != NULL) 
    { 
        pboxCopy = GlobalLock(hglb); 
        if (pboxCopy != NULL) 
        { 
            cx = pboxCopy->rcText.right + CX_MARGIN; 
            cy = pboxCopy->rcText.top * 2 + cyText; 
 
            hwnd = CreateWindowEx( 
                WS_EX_NOPARENTNOTIFY | WS_EX_TRANSPARENT, 
                atchClassChild, NULL, WS_CHILD, 0, 0, cx, cy, 
                hwndMain, NULL, hinst, NULL 
            ); 
            if (hwnd != NULL) 
            { 
                pbox = (PLABELBOX) GetWindowLong(hwnd, 0); 
                memcpy(pbox, pboxCopy, sizeof(LABELBOX)); 
                ShowWindow(hwnd, SW_SHOWNORMAL); 
                SetFocus(hwnd); 
            } 
            GlobalUnlock(hglb); 
        } 
    } 
    CloseClipboard(); 
}
```



### <a name="registering-a-clipboard-format"></a>Регистрация формата буфера обмена

Чтобы зарегистрировать формат буфера обмена, добавьте вызов функции [**регистерклипбоардформат**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) в функцию инициализации экземпляра приложения, как показано ниже.


```
// Register a clipboard format. 
 
// We assume that atchTemp can contain the format name and
// a null-terminator, otherwise it is truncated.
//
LoadString(hinstCurrent, IDS_FORMATNAME, atchTemp, 
    sizeof(atchTemp)/sizeof(TCHAR)); 
uLabelFormat = RegisterClipboardFormat(atchTemp); 
if (uLabelFormat == 0) 
    return FALSE;
```



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a>Обработка сообщений WM \_ RENDERFORMAT и WM \_ рендераллформатс

Если окно передает в функцию [**сетклипбоарддата**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) маркер **со значением NULL** , он должен обрабатывать сообщения [**WM \_ RENDERFORMAT**](wm-renderformat.md) и [**WM \_ рендераллформатс**](wm-renderallformats.md) для отрисовки данных по запросу.

Если окно задерживает Отображение определенного формата, а затем другое приложение запрашивает данные в этом формате, то в окно отправляется сообщение [**WM \_ RENDERFORMAT**](wm-renderformat.md) . Кроме того, если окно задерживает визуализацию одного или нескольких форматов, и если некоторые из этих форматов остаются невидимыми, когда окно собирается уничтожиться, то сообщение [**WM \_ рендераллформатс**](wm-renderallformats.md) отправляется в окно перед его уничтожением.

Чтобы отобразить формат буфера обмена, процедура Window должна помещаться в буфер обмена с помощью функции [**сетклипбоарддата**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) , не **имеющей значение NULL** . Если процедура окна представляет формат в ответ на сообщение [**\_ RENDERFORMAT WM**](wm-renderformat.md) , он не должен открывать буфер обмена перед вызовом **сетклипбоарддата**. Но если он выводит один или несколько форматов в ответ на сообщение [**\_ рендераллформатс WM**](wm-renderallformats.md) , он должен открыть буфер обмена и убедиться, что окно по-прежнему владеет буфером обмена перед вызовом **сетклипбоарддата**, и он должен закрыть буфер обмена перед возвратом.

Приложение Label обрабатывает сообщения [**WM \_ RENDERFORMAT**](wm-renderformat.md) и [**WM \_ рендераллформатс**](wm-renderallformats.md) следующим образом.


```
case WM_RENDERFORMAT: 
    RenderFormat((UINT) wParam); 
    break; 
 
case WM_RENDERALLFORMATS:
    if (OpenClipboard(hwnd))
    {
        if (GetClipboardOwner() == hwnd)
        {
            RenderFormat(uLabelFormat);
            RenderFormat(CF_TEXT);
        }
        CloseClipboard();
    }
    break;
```



В обоих случаях процедура Window вызывает определяемую приложением функцию RenderFormat, определенную следующим образом.

Структура, именуемая ЛАБЕЛБОКС, определяется следующим образом.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```




```
void WINAPI RenderFormat(UINT uFormat) 
{ 
    HGLOBAL hglb; 
    PLABELBOX pbox; 
    LPTSTR  lptstr; 
    int cch; 
 
    if (pboxLocalClip == NULL) 
        return; 
 
    if (uFormat == CF_TEXT) 
    { 
        // Allocate a buffer for the text. 
 
        cch = pboxLocalClip->cchLabel; 
        hglb = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglb == NULL) 
            return; 
 
        // Copy the text from pboxLocalClip. 
 
        lptstr = GlobalLock(hglb); 
        memcpy(lptstr, pboxLocalClip->atchLabel, 
            cch * sizeof(TCHAR)); 
        lptstr[cch] = (TCHAR) 0; 
        GlobalUnlock(hglb); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglb); 
    } 
    else if (uFormat == uLabelFormat) 
    { 
        hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(LABELBOX)); 
        if (hglb == NULL) 
            return; 
        pbox = GlobalLock(hglb); 
        memcpy(pbox, pboxLocalClip, sizeof(LABELBOX)); 
        GlobalUnlock(hglb); 
 
        SetClipboardData(uLabelFormat, hglb); 
    } 
}
```



### <a name="processing-the-wm_destroyclipboard-message"></a>Обработка сообщения WM \_ дестройклипбоард

Окно может обработать сообщение [**WM \_ дестройклипбоард**](wm-destroyclipboard.md) , чтобы освободить все ресурсы, которые были заданы для поддержки отложенной отрисовки. Например, приложение Label при копировании метки в буфер обмена выделяет объект локальной памяти. Затем этот объект освобождается в ответ на сообщение **\_ дестройклипбоард WM** , как показано ниже.


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a>Использование формата буфера обмена Owner-Display

Если окно помещает сведения в буфер обмена с помощью формата буфера обмена **CF \_ овнердисплай** , оно должно выполнять следующие действия:

-   Обработайте сообщение [**WM \_ паинтклипбоард**](wm-paintclipboard.md) . Это сообщение отправляется владельцу буфера обмена, когда часть окна средства просмотра буфера обмена должна быть перерисована.

-   Обработайте сообщение [**WM \_ сизеклипбоард**](wm-sizeclipboard.md) . Это сообщение отправляется владельцу буфера обмена при изменении размера окна буфера обмена или его содержимого.

    Как правило, окно отвечает на это сообщение, устанавливая позиции прокрутки и диапазоны для окна средства просмотра буфера обмена. В ответ на это сообщение приложение Label также обновляет структуру [**размера**](/previous-versions//dd145106(v=vs.85)) окна средства просмотра буфера обмена.

-   Обработка сообщений [**WM \_ Хскроллклипбоард**](wm-hscrollclipboard.md) и [**WM \_ вскроллклипбоард**](wm-vscrollclipboard.md) . Эти сообщения отправляются владельцу буфера обмена при возникновении события полосы прокрутки в окне средства просмотра буфера обмена.

-   Обработайте сообщение [**WM \_ асккбформатнаме**](wm-askcbformatname.md) . Окно просмотра буфера обмена отправляет это сообщение приложению для получения имени формата, отображаемого владельцем.

Процедура Window для приложения Label обрабатывает эти сообщения следующим образом.


```
LRESULT CALLBACK MainWindowProc(hwnd, msg, wParam, lParam) 
HWND hwnd; 
UINT msg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static RECT rcViewer; 
 
    RECT rc; 
    LPRECT lprc; 
    LPPAINTSTRUCT lpps; 
 
    switch (msg) 
    { 
        //
        // Handle other messages.
        //
        case WM_PAINTCLIPBOARD: 
            // Determine the dimensions of the label. 
 
            SetRect(&rc, 0, 0, 
                pboxLocalClip->rcText.right + CX_MARGIN, 
                pboxLocalClip->rcText.top * 2 + cyText 
            ); 
 
            // Center the image in the clipboard viewer window. 
 
            if (rc.right < rcViewer.right) 
            { 
                rc.left = (rcViewer.right - rc.right) / 2; 
                rc.right += rc.left; 
            } 
            if (rc.bottom < rcViewer.bottom) 
            { 
                rc.top = (rcViewer.bottom - rc.bottom) / 2; 
                rc.bottom += rc.top; 
            } 
 
            // Paint the image, using the specified PAINTSTRUCT 
            // structure, by calling the application-defined 
            // PaintLabel function. 
 
            lpps = (LPPAINTSTRUCT) GlobalLock((HGLOBAL) lParam); 
            PaintLabel(lpps, pboxLocalClip, &rc); 
            GlobalUnlock((HGLOBAL) lParam); 
            break; 
 
        case WM_SIZECLIPBOARD: 
            // Save the dimensions of the window in a static 
            // RECT structure. 
 
            lprc = (LPRECT) GlobalLock((HGLOBAL) lParam); 
            memcpy(&rcViewer, lprc, sizeof(RECT)); 
            GlobalUnlock((HGLOBAL) lParam); 
 
            // Set the scroll ranges to zero (thus eliminating 
            // the need to process the WM_HSCROLLCLIPBOARD and 
            // WM_VSCROLLCLIPBOARD messages). 
 
            SetScrollRange((HWND) wParam, SB_HORZ, 0, 0, TRUE); 
            SetScrollRange((HWND) wParam, SB_VERT, 0, 0, TRUE); 
 
            break; 
 
        case WM_ASKCBFORMATNAME: 
            LoadString(hinst, IDS_OWNERDISPLAY, 
                (LPSTR) lParam, wParam); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
}
```



## <a name="monitoring-clipboard-contents"></a>Мониторинг содержимого буфера обмена

Существует три способа мониторинга изменений в буфере обмена. Самый старый способ — создать окно средства просмотра буфера обмена. Windows 2000 добавлена возможность запрашивать порядковый номер буфера обмена, а Windows Vista добавлена поддержка прослушивателей формата буфера обмена. Окна буфера обмена поддерживаются для обеспечения обратной совместимости с более ранними версиями Windows. Новые программы должны использовать прослушиватели формата буфера обмена или порядковый номер буфера обмена.

## <a name="querying-the-clipboard-sequence-number"></a>Запрос порядкового номера буфера обмена

Каждый раз, когда содержимое буфера обмена изменяется, увеличивается 32-разрядное значение, известное как порядковый номер буфера обмена. Программа может получить текущий порядковый номер буфера обмена, вызвав функцию [**жетклипбоардсекуенценумбер**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) . Сравнивая значение, возвращаемое для значения, возвращенного предыдущим вызовом **жетклипбоардсекуенценумбер**, программа может определить, изменилось ли содержимое буфера обмена. Этот метод лучше подходит для программ, которые кэшируют результаты на основе текущего содержимого буфера обмена и должны знать, являются ли вычисления допустимыми, прежде чем использовать результаты из этого кэша. Обратите внимание, что это не метод уведомления, и его не следует использовать в цикле опроса. Чтобы получать уведомления об изменении содержимого буфера обмена, используйте прослушиватель формата буфера обмена или средство просмотра буфера обмена.

## <a name="creating-a-clipboard-format-listener"></a>Создание прослушивателя формата буфера обмена

Прослушиватель формата буфера обмена — это окно, зарегистрированное для уведомления об изменении содержимого буфера обмена. Этот метод рекомендуется использовать вместо создания окна средства просмотра буфера обмена, так как его проще реализовать и избежать проблем, если программы не смогут правильно поддерживать цепочку просмотра буфера обмена или если окно в цепочке просмотра буфера обмена перестает отвечать на сообщения.

Окно регистрируется в качестве прослушивателя формата буфера обмена путем вызова функции [**аддклипбоардформатлистенер**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) . При изменении содержимого буфера обмена окно отправляет сообщение [**WM \_ клипбоардупдате**](wm-clipboardupdate.md) . Регистрация остается действительной до тех пор, пока окно не будет отменено, вызвав функцию [**ремовеклипбоардформатлистенер**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) .

## <a name="creating-a-clipboard-viewer-window"></a>Создание окна средства просмотра буфера обмена

Окно просмотра буфера обмена отображает текущее содержимое буфера обмена и получает сообщения при изменении содержимого буфера обмена. Чтобы создать окно средства просмотра буфера обмена, приложение должно выполнить следующие действия.

-   Добавьте окно в цепочку средства просмотра буфера обмена.
-   Обработайте сообщение [**WM \_ чанжекбчаин**](wm-changecbchain.md) .
-   Обработайте сообщение [**WM \_ дравклипбоард**](wm-drawclipboard.md) .
-   Удалите окно из цепочки окна просмотра буфера обмена, прежде чем оно будет уничтожено.

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a>Добавление окна в цепочку средства просмотра буфера обмена

Окно добавляет себя в цепочку средства просмотра буфера обмена путем вызова функции [**сетклипбоардвиевер**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) . Возвращаемое значение — это обработчик следующего окна в цепочке. Окно должно отследить это значение, например путем его сохранения в статической переменной с именем *хвнднекствиевер*.

В следующем примере окно добавляется в цепочку окна просмотра буфера обмена в ответ на сообщение о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) .


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



Фрагменты кода отображаются для следующих задач:

-   [Обработка сообщения WM \_ чанжекбчаин](/windows)
-   [Удаление окна из цепочки окна просмотра буфера обмена](#removing-a-window-from-the-clipboard-viewer-chain)
-   [Обработка сообщения WM \_ дравклипбоард](/windows)
-   [Пример средства просмотра буфера обмена](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a>Обработка сообщения WM \_ чанжекбчаин

Окно просмотра буфера обмена получает сообщение [**WM \_ чанжекбчаин**](wm-changecbchain.md) , когда другое окно удаляет себя из цепочки средства просмотра буфера обмена. Если удаляемое окно является следующим окном в цепочке, окно, получающее сообщение, должно удалить связь со следующим окном из цепочки. В противном случае это сообщение должно быть передано в следующее окно в цепочке.

В следующем примере показана обработка сообщения [**WM \_ чанжекбчаин**](wm-changecbchain.md) .


```
case WM_CHANGECBCHAIN: 
 
    // If the next window is closing, repair the chain. 
 
    if ((HWND) wParam == hwndNextViewer) 
        hwndNextViewer = (HWND) lParam; 
 
    // Otherwise, pass the message to the next link. 
 
    else if (hwndNextViewer != NULL) 
        SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
    break;
```



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a>Удаление окна из цепочки окна просмотра буфера обмена

Чтобы удалить себя из цепочки средства просмотра буфера обмена, окно вызывает функцию [**чанжеклипбоардчаин**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) . В следующем примере удаляется окно из цепочки окна буфера просмотра в ответ на сообщение [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) .


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a>Обработка сообщения WM \_ дравклипбоард

Сообщение [**WM \_ дравклипбоард**](wm-drawclipboard.md) уведомляет окно средства просмотра буфера обмена о том, что содержимое буфера обмена изменилось. При обработке сообщения **WM \_ дравклипбоард** в окне необходимо выполнить следующие действия:

1.  Определите, какой из доступных форматов буфера обмена нужно отобразить.
2.  Извлеките данные из буфера обмена и отобразите их в окне. Или если формат буфера обмена — **CF \_ овнердисплай**, отправьте сообщение [**WM \_ паинтклипбоард**](wm-paintclipboard.md) владельцу буфера обмена.
3.  Отправка сообщения в следующее окно в цепочке окна просмотра буфера обмена.

Пример обработки сообщения [**WM \_ дравклипбоард**](wm-drawclipboard.md) см. в примере, приведенном в [примере средства просмотра буфера обмена](#example-of-a-clipboard-viewer).

### <a name="example-of-a-clipboard-viewer"></a>Пример средства просмотра буфера обмена

В следующем примере показано простое приложение просмотра буфера обмена.


```
HINSTANCE hinst; 
UINT uFormat = (UINT)(-1); 
BOOL fAuto = TRUE; 
 
LRESULT APIENTRY MainWndProc(hwnd, uMsg, wParam, lParam) 
HWND hwnd; 
UINT uMsg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static HWND hwndNextViewer; 
 
    HDC hdc; 
    HDC hdcMem; 
    PAINTSTRUCT ps; 
    LPPAINTSTRUCT lpps; 
    RECT rc; 
    LPRECT lprc; 
    HGLOBAL hglb; 
    LPSTR lpstr; 
    HBITMAP hbm; 
    HENHMETAFILE hemf; 
    HWND hwndOwner; 
 
    switch (uMsg) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
 
            // Branch depending on the clipboard format. 
 
            switch (uFormat) 
            { 
                case CF_OWNERDISPLAY: 
                    hwndOwner = GetClipboardOwner(); 
                    hglb = GlobalAlloc(GMEM_MOVEABLE, 
                        sizeof(PAINTSTRUCT)); 
                    lpps = GlobalLock(hglb);
                    memcpy(lpps, &ps, sizeof(PAINTSTRUCT)); 
                    GlobalUnlock(hglb); 
 
                    SendMessage(hwndOwner, WM_PAINTCLIPBOARD, 
                        (WPARAM) hwnd, (LPARAM) hglb); 
 
                    GlobalFree(hglb); 
                    break; 
 
                case CF_BITMAP: 
                    hdcMem = CreateCompatibleDC(hdc); 
                    if (hdcMem != NULL) 
                    { 
                        if (OpenClipboard(hwnd)) 
                        { 
                            hbm = (HBITMAP) 
                                GetClipboardData(uFormat); 
                            SelectObject(hdcMem, hbm); 
                            GetClientRect(hwnd, &rc); 
 
                            BitBlt(hdc, 0, 0, rc.right, rc.bottom, 
                                hdcMem, 0, 0, SRCCOPY); 
                            CloseClipboard(); 
                        } 
                        DeleteDC(hdcMem); 
                    } 
                    break; 
 
                case CF_TEXT: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hglb = GetClipboardData(uFormat); 
                        lpstr = GlobalLock(hglb); 
 
                        GetClientRect(hwnd, &rc); 
                        DrawText(hdc, lpstr, -1, &rc, DT_LEFT); 
 
                        GlobalUnlock(hglb); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case CF_ENHMETAFILE: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hemf = GetClipboardData(uFormat); 
                        GetClientRect(hwnd, &rc); 
                        PlayEnhMetaFile(hdc, hemf, &rc); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case 0: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "The clipboard is empty.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
                    break; 
 
                default: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "Unable to display format.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
            } 
            EndPaint(hwnd, &ps); 
            break; 
 
        case WM_SIZE: 
            if (uFormat == CF_OWNERDISPLAY) 
            { 
                hwndOwner = GetClipboardOwner(); 
                hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(RECT)); 
                lprc = GlobalLock(hglb); 
                GetClientRect(hwnd, lprc); 
                GlobalUnlock(hglb); 
 
                SendMessage(hwndOwner, WM_SIZECLIPBOARD, 
                    (WPARAM) hwnd, (LPARAM) hglb); 
 
                GlobalFree(hglb); 
            } 
            break; 
 
        case WM_CREATE: 
 
            // Add the window to the clipboard viewer chain. 
 
            hwndNextViewer = SetClipboardViewer(hwnd); 
            break; 
 
        case WM_CHANGECBCHAIN: 
 
            // If the next window is closing, repair the chain. 
 
            if ((HWND) wParam == hwndNextViewer) 
                hwndNextViewer = (HWND) lParam; 
 
            // Otherwise, pass the message to the next link. 
 
            else if (hwndNextViewer != NULL) 
                SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
            break; 
 
        case WM_DESTROY: 
            ChangeClipboardChain(hwnd, hwndNextViewer); 
            PostQuitMessage(0); 
            break; 
 
        case WM_DRAWCLIPBOARD:  // clipboard contents changed. 
 
            // Update the window by using Auto clipboard format. 
 
            SetAutoView(hwnd); 
 
            // Pass the message to the next window in clipboard 
            // viewer chain. 
 
            SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
            break; 
 
        case WM_INITMENUPOPUP: 
            if (!HIWORD(lParam)) 
                InitMenu(hwnd, (HMENU) wParam); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_EXIT: 
                    DestroyWindow(hwnd); 
                    break; 
 
                case IDM_AUTO: 
                    SetAutoView(hwnd); 
                    break; 
 
                default: 
                    fAuto = FALSE; 
                    uFormat = LOWORD(wParam); 
                    InvalidateRect(hwnd, NULL, TRUE); 
            } 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return (LRESULT) NULL; 
} 
 
void WINAPI SetAutoView(HWND hwnd) 
{ 
    static UINT auPriorityList[] = { 
        CF_OWNERDISPLAY, 
        CF_TEXT, 
        CF_ENHMETAFILE, 
        CF_BITMAP 
    }; 
 
    uFormat = GetPriorityClipboardFormat(auPriorityList, 4); 
    fAuto = TRUE; 
 
    InvalidateRect(hwnd, NULL, TRUE); 
    UpdateWindow(hwnd); 
} 
 
void WINAPI InitMenu(HWND hwnd, HMENU hmenu) 
{ 
    UINT uFormat; 
    char szFormatName[80]; 
    LPCSTR lpFormatName; 
    UINT fuFlags; 
    UINT idMenuItem; 
 
    // If a menu is not the display menu, no initialization is necessary. 
 
    if (GetMenuItemID(hmenu, 0) != IDM_AUTO) 
        return; 
 
    // Delete all menu items except the first. 
 
    while (GetMenuItemCount(hmenu) > 1) 
        DeleteMenu(hmenu, 1, MF_BYPOSITION); 
 
    // Check or uncheck the Auto menu item. 
 
    fuFlags = fAuto ? MF_BYCOMMAND | MF_CHECKED : 
        MF_BYCOMMAND | MF_UNCHECKED; 
    CheckMenuItem(hmenu, IDM_AUTO, fuFlags); 
 
    // If there are no clipboard formats, return. 
 
    if (CountClipboardFormats() == 0) 
        return; 
 
    // Open the clipboard. 
 
    if (!OpenClipboard(hwnd)) 
        return; 
 
    // Add a separator and then a menu item for each format. 
 
    AppendMenu(hmenu, MF_SEPARATOR, 0, NULL); 
    uFormat = EnumClipboardFormats(0); 
 
    while (uFormat) 
    { 
        // Call an application-defined function to get the name 
        // of the clipboard format. 
 
        lpFormatName = GetPredefinedClipboardFormatName(uFormat); 
 
        // For registered formats, get the registered name. 
 
        if (lpFormatName == NULL) 
        {

        // Note that, if the format name is larger than the
        // buffer, it is truncated. 
            if (GetClipboardFormatName(uFormat, szFormatName, 
                    sizeof(szFormatName))) 
                lpFormatName = szFormatName; 
            else 
                lpFormatName = "(unknown)"; 
        } 
 
        // Add a menu item for the format. For displayable 
        // formats, use the format ID for the menu ID. 
 
        if (IsDisplayableFormat(uFormat)) 
        { 
            fuFlags = MF_STRING; 
            idMenuItem = uFormat; 
        } 
        else 
        { 
            fuFlags = MF_STRING | MF_GRAYED; 
            idMenuItem = 0; 
        } 
        AppendMenu(hmenu, fuFlags, idMenuItem, lpFormatName); 
 
        uFormat = EnumClipboardFormats(uFormat); 
    } 
    CloseClipboard(); 
 
} 
 
BOOL WINAPI IsDisplayableFormat(UINT uFormat) 
{ 
    switch (uFormat) 
    { 
        case CF_OWNERDISPLAY: 
        case CF_TEXT: 
        case CF_ENHMETAFILE: 
        case CF_BITMAP: 
            return TRUE; 
    } 
    return FALSE; 
} 
```



 

 