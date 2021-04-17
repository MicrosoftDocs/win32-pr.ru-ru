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
ms.openlocfilehash: 9d7c7e7d6db6f25bc1016eefbcc5afc9f5e0db44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337908"
---
# <a name="using-the-clipboard"></a><span data-ttu-id="24650-110">Использование буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-110">Using the Clipboard</span></span>

<span data-ttu-id="24650-111">В этом разделе приведены примеры кода для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="24650-111">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="24650-112">Реализация команд вырезания, копирования и вставки</span><span class="sxs-lookup"><span data-stu-id="24650-112">Implementing the Cut, Copy, and Paste Commands</span></span>](#implementing-the-cut-copy-and-paste-commands)
    -   [<span data-ttu-id="24650-113">Выбор данных</span><span class="sxs-lookup"><span data-stu-id="24650-113">Selecting Data</span></span>](#selecting-data)
    -   [<span data-ttu-id="24650-114">Создание меню "Правка"</span><span class="sxs-lookup"><span data-stu-id="24650-114">Creating an Edit Menu</span></span>](#creating-an-edit-menu)
    -   [<span data-ttu-id="24650-115">Обработка сообщения WM \_ инитменупопуп</span><span class="sxs-lookup"><span data-stu-id="24650-115">Processing the WM\_INITMENUPOPUP Message</span></span>](#processing-the-wm_initmenupopup-message)
    -   [<span data-ttu-id="24650-116">Обработка \_ командного сообщения WM</span><span class="sxs-lookup"><span data-stu-id="24650-116">Processing the WM\_COMMAND Message</span></span>](#processing-the-wm_command-message)
    -   [<span data-ttu-id="24650-117">Копирование данных в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="24650-117">Copying Information to the Clipboard</span></span>](#copying-information-to-the-clipboard)
    -   [<span data-ttu-id="24650-118">Вставлены сведения из буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-118">Pasting Information from the Clipboard</span></span>](#pasting-information-from-the-clipboard)
    -   [<span data-ttu-id="24650-119">Регистрация формата буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-119">Registering a Clipboard Format</span></span>](#registering-a-clipboard-format)
    -   [<span data-ttu-id="24650-120">Обработка сообщений WM \_ RENDERFORMAT и WM \_ рендераллформатс</span><span class="sxs-lookup"><span data-stu-id="24650-120">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [<span data-ttu-id="24650-121">Обработка сообщения WM \_ дестройклипбоард</span><span class="sxs-lookup"><span data-stu-id="24650-121">Processing the WM\_DESTROYCLIPBOARD Message</span></span>](#processing-the-wm_destroyclipboard-message)
    -   [<span data-ttu-id="24650-122">Использование формата буфера обмена Owner-Display</span><span class="sxs-lookup"><span data-stu-id="24650-122">Using the Owner-Display Clipboard Format</span></span>](#using-the-owner-display-clipboard-format)
-   [<span data-ttu-id="24650-123">Мониторинг содержимого буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-123">Monitoring Clipboard Contents</span></span>](#monitoring-clipboard-contents)
-   [<span data-ttu-id="24650-124">Запрос порядкового номера буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-124">Querying the Clipboard Sequence Number</span></span>](#querying-the-clipboard-sequence-number)
-   [<span data-ttu-id="24650-125">Создание прослушивателя формата буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-125">Creating a Clipboard Format Listener</span></span>](#creating-a-clipboard-format-listener)
-   [<span data-ttu-id="24650-126">Создание окна средства просмотра буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-126">Creating a Clipboard Viewer Window</span></span>](#creating-a-clipboard-viewer-window)
-   [<span data-ttu-id="24650-127">Добавление окна в цепочку средства просмотра буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-127">Adding a Window to the Clipboard Viewer Chain</span></span>](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="24650-128">Обработка сообщения WM \_ чанжекбчаин</span><span class="sxs-lookup"><span data-stu-id="24650-128">Processing the WM\_CHANGECBCHAIN Message</span></span>](#processing-the-wm_changecbchain-message)
    -   [<span data-ttu-id="24650-129">Удаление окна из цепочки окна просмотра буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-129">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="24650-130">Обработка сообщения WM \_ дравклипбоард</span><span class="sxs-lookup"><span data-stu-id="24650-130">Processing the WM\_DRAWCLIPBOARD Message</span></span>](#processing-the-wm_drawclipboard-message)
    -   [<span data-ttu-id="24650-131">Пример средства просмотра буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-131">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a><span data-ttu-id="24650-132">Реализация команд вырезания, копирования и вставки</span><span class="sxs-lookup"><span data-stu-id="24650-132">Implementing the Cut, Copy, and Paste Commands</span></span>

<span data-ttu-id="24650-133">В этом разделе описывается, как стандартные команды **вырезания**, **копирования** и **вставки** реализуются в приложении.</span><span class="sxs-lookup"><span data-stu-id="24650-133">This section describes how standard **Cut**, **Copy**, and **Paste** commands are implemented in an application.</span></span> <span data-ttu-id="24650-134">В примере в этом разделе эти методы используются для размещения данных в буфере обмена с помощью зарегистрированного формата буфера обмена, формата **\_ овнердисплай CF** и **\_ текстового формата CF** .</span><span class="sxs-lookup"><span data-stu-id="24650-134">The example in this section uses these methods to place data on the clipboard using a registered clipboard format, the **CF\_OWNERDISPLAY** format, and the **CF\_TEXT** format.</span></span> <span data-ttu-id="24650-135">Зарегистрированный формат используется для представления прямоугольных или эллиптических текстовых окон, называемых метками.</span><span class="sxs-lookup"><span data-stu-id="24650-135">The registered format is used to represent rectangular or elliptical text windows, called labels.</span></span>

### <a name="selecting-data"></a><span data-ttu-id="24650-136">Выбор данных</span><span class="sxs-lookup"><span data-stu-id="24650-136">Selecting Data</span></span>

<span data-ttu-id="24650-137">Прежде чем копировать данные в буфер обмена, пользователь должен выбрать определенные данные для копирования или вырезания.</span><span class="sxs-lookup"><span data-stu-id="24650-137">Before information can be copied to the clipboard, the user must select specific information to be copied or cut.</span></span> <span data-ttu-id="24650-138">Приложение должно предоставлять пользователю возможность выбора информации в документе и какого-либо визуального отзыва для указания выбранных данных.</span><span class="sxs-lookup"><span data-stu-id="24650-138">An application should provide a means for the user to select information within a document and some kind of visual feedback to indicate selected data.</span></span>

### <a name="creating-an-edit-menu"></a><span data-ttu-id="24650-139">Создание меню "Правка"</span><span class="sxs-lookup"><span data-stu-id="24650-139">Creating an Edit Menu</span></span>

<span data-ttu-id="24650-140">Приложение должно загрузить таблицу сочетаний клавиш, содержащую стандартные сочетания клавиш для команд меню " **Правка** ".</span><span class="sxs-lookup"><span data-stu-id="24650-140">An application should load an accelerator table containing the standard keyboard accelerators for the **Edit** menu commands.</span></span> <span data-ttu-id="24650-141">Чтобы сочетания клавиш вступили в силу, необходимо добавить функцию [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) в цикл обработки сообщений приложения.</span><span class="sxs-lookup"><span data-stu-id="24650-141">The [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function must be added to the application's message loop for the accelerators to take effect.</span></span> <span data-ttu-id="24650-142">Дополнительные сведения о сочетаниях клавиш см. в разделе [сочетания](/windows/desktop/menurc/keyboard-accelerators)клавиш.</span><span class="sxs-lookup"><span data-stu-id="24650-142">For more information about keyboard accelerators, see [Keyboard Accelerators](/windows/desktop/menurc/keyboard-accelerators).</span></span>

### <a name="processing-the-wm_initmenupopup-message"></a><span data-ttu-id="24650-143">Обработка сообщения WM \_ инитменупопуп</span><span class="sxs-lookup"><span data-stu-id="24650-143">Processing the WM\_INITMENUPOPUP Message</span></span>

<span data-ttu-id="24650-144">Не все команды буфера обмена доступны пользователю в любое заданное время.</span><span class="sxs-lookup"><span data-stu-id="24650-144">Not all clipboard commands are available to the user at any given time.</span></span> <span data-ttu-id="24650-145">Приложение должно обработать сообщение [**WM \_ инитменупопуп**](/windows/desktop/menurc/wm-initmenupopup) , чтобы включить пункты меню для доступных команд и отключить недоступные команды.</span><span class="sxs-lookup"><span data-stu-id="24650-145">An application should process the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message to enable the menu items for available commands and disable unavailable commands.</span></span>

<span data-ttu-id="24650-146">Ниже приведен регистр [**WM \_ инитменупопуп**](/windows/desktop/menurc/wm-initmenupopup) для приложения с именем Label.</span><span class="sxs-lookup"><span data-stu-id="24650-146">Following is the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) case for an application named Label.</span></span>


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



<span data-ttu-id="24650-147">Функция Инитмену определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="24650-147">The InitMenu function is defined as follows.</span></span>


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



### <a name="processing-the-wm_command-message"></a><span data-ttu-id="24650-148">Обработка \_ командного сообщения WM</span><span class="sxs-lookup"><span data-stu-id="24650-148">Processing the WM\_COMMAND Message</span></span>

<span data-ttu-id="24650-149">Чтобы обработать команды меню, добавьте [**\_ командный сценарий WM**](/windows/desktop/menurc/wm-command) в главную оконную процедуру приложения.</span><span class="sxs-lookup"><span data-stu-id="24650-149">To process menu commands, add the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) case to your application's main window procedure.</span></span> <span data-ttu-id="24650-150">Ниже приведен пример **\_ команды WM** для процедуры окна приложения Label.</span><span class="sxs-lookup"><span data-stu-id="24650-150">Following is the **WM\_COMMAND** case for the Label application's window procedure.</span></span>


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



<span data-ttu-id="24650-151">Для выполнения команд **Copy** и **Cut** процедура Window вызывает определяемую приложением функцию едиткопи.</span><span class="sxs-lookup"><span data-stu-id="24650-151">To carry out the **Copy** and **Cut** commands, the window procedure calls the application-defined EditCopy function.</span></span> <span data-ttu-id="24650-152">Дополнительные сведения см. в разделе [копирование данных в буфер обмена](#copying-information-to-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="24650-152">For more information, see [Copying Information to the Clipboard](#copying-information-to-the-clipboard).</span></span> <span data-ttu-id="24650-153">Для выполнения команды **Paste** процедура Window вызывает определяемую приложением функцию едитпасте.</span><span class="sxs-lookup"><span data-stu-id="24650-153">To carry out the **Paste** command, the window procedure calls the application-defined EditPaste function.</span></span> <span data-ttu-id="24650-154">Дополнительные сведения о функции Едитпасте см. в разделе [о вставлении данных из буфера обмена](#pasting-information-from-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="24650-154">For more information about the EditPaste function, see [Pasting Information from the Clipboard](#pasting-information-from-the-clipboard).</span></span>

### <a name="copying-information-to-the-clipboard"></a><span data-ttu-id="24650-155">Копирование данных в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="24650-155">Copying Information to the Clipboard</span></span>

<span data-ttu-id="24650-156">В приложении-метке функция Едиткопи, определяемая приложением, копирует текущее выделение в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-156">In the Label application, the application-defined EditCopy function copies the current selection to the clipboard.</span></span> <span data-ttu-id="24650-157">Эта функция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="24650-157">This function does the following:</span></span>

1.  <span data-ttu-id="24650-158">Открывает буфер обмена, вызывая функцию [**опенклипбоард**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .</span><span class="sxs-lookup"><span data-stu-id="24650-158">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="24650-159">Очищает буфер обмена, вызывая функцию [**емптиклипбоард**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) .</span><span class="sxs-lookup"><span data-stu-id="24650-159">Empties the clipboard by calling the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function.</span></span>
3.  <span data-ttu-id="24650-160">Вызывает функцию [**сетклипбоарддата**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) один раз для каждого формата буфера обмена, предоставляемого приложением.</span><span class="sxs-lookup"><span data-stu-id="24650-160">Calls the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function once for each clipboard format the application provides.</span></span>
4.  <span data-ttu-id="24650-161">Закрывает буфер обмена, вызывая функцию [**клосеклипбоард**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .</span><span class="sxs-lookup"><span data-stu-id="24650-161">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="24650-162">В зависимости от текущего выбора функция Едиткопи копирует диапазон текста или копирует определенную приложением структуру, представляющую всю метку.</span><span class="sxs-lookup"><span data-stu-id="24650-162">Depending on the current selection, the EditCopy function either copies a range of text or copies an application-defined structure representing an entire label.</span></span> <span data-ttu-id="24650-163">Структура, именуемая ЛАБЕЛБОКС, определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="24650-163">The structure, called LABELBOX, is defined as follows.</span></span>


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



<span data-ttu-id="24650-164">Ниже приведена функция Едиткопи.</span><span class="sxs-lookup"><span data-stu-id="24650-164">Following is the EditCopy function.</span></span>


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



### <a name="pasting-information-from-the-clipboard"></a><span data-ttu-id="24650-165">Вставлены сведения из буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-165">Pasting Information from the Clipboard</span></span>

<span data-ttu-id="24650-166">В приложении Label функция Едитпасте, определяемая приложением, вставит содержимое буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-166">In the Label application, the application-defined EditPaste function pastes the content of the clipboard.</span></span> <span data-ttu-id="24650-167">Эта функция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="24650-167">This function does the following:</span></span>

1.  <span data-ttu-id="24650-168">Открывает буфер обмена, вызывая функцию [**опенклипбоард**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .</span><span class="sxs-lookup"><span data-stu-id="24650-168">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="24650-169">Определяет, какой из доступных форматов буфера обмена требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="24650-169">Determines which of the available clipboard formats to retrieve.</span></span>
3.  <span data-ttu-id="24650-170">Извлекает маркер для данных в выбранном формате путем вызова функции [**жетклипбоарддата**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="24650-170">Retrieves the handle to the data in the selected format by calling the [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) function.</span></span>
4.  <span data-ttu-id="24650-171">Вставляет копию данных в документ.</span><span class="sxs-lookup"><span data-stu-id="24650-171">Inserts a copy of the data into the document.</span></span>

    <span data-ttu-id="24650-172">Маркер, возвращенный [**жетклипбоарддата**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) , по-прежнему принадлежит буферу обмена, поэтому приложение не должно освободить его или оставить заблокированным.</span><span class="sxs-lookup"><span data-stu-id="24650-172">The handle returned by [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) is still owned by the clipboard, so an application must not free it or leave it locked.</span></span>

5.  <span data-ttu-id="24650-173">Закрывает буфер обмена, вызывая функцию [**клосеклипбоард**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .</span><span class="sxs-lookup"><span data-stu-id="24650-173">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="24650-174">Если метка выбрана и содержит точку вставки, функция Едитпасте вставляет текст из буфера обмена в точку вставки.</span><span class="sxs-lookup"><span data-stu-id="24650-174">If a label is selected and contains an insertion point, the EditPaste function inserts the text from the clipboard at the insertion point.</span></span> <span data-ttu-id="24650-175">Если ничего не выделено или если метка выбрана, функция создает новую метку, используя определяемую приложением структуру ЛАБЕЛБОКС в буфере обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-175">If there is no selection or if a label is selected, the function creates a new label, using the application-defined LABELBOX structure on the clipboard.</span></span> <span data-ttu-id="24650-176">Структура ЛАБЕЛБОКС помещается в буфер обмена с помощью зарегистрированного формата буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-176">The LABELBOX structure is placed on the clipboard by using a registered clipboard format.</span></span>

<span data-ttu-id="24650-177">Структура, именуемая ЛАБЕЛБОКС, определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="24650-177">The structure, called LABELBOX, is defined as follows.</span></span>


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



<span data-ttu-id="24650-178">Ниже приведена функция Едитпасте.</span><span class="sxs-lookup"><span data-stu-id="24650-178">Following is the EditPaste function.</span></span>


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



### <a name="registering-a-clipboard-format"></a><span data-ttu-id="24650-179">Регистрация формата буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-179">Registering a Clipboard Format</span></span>

<span data-ttu-id="24650-180">Чтобы зарегистрировать формат буфера обмена, добавьте вызов функции [**регистерклипбоардформат**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) в функцию инициализации экземпляра приложения, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="24650-180">To register a clipboard format, add a call to the [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) function to your application's instance initialization function, as follows.</span></span>


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



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a><span data-ttu-id="24650-181">Обработка сообщений WM \_ RENDERFORMAT и WM \_ рендераллформатс</span><span class="sxs-lookup"><span data-stu-id="24650-181">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>

<span data-ttu-id="24650-182">Если окно передает в функцию [**сетклипбоарддата**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) маркер **со значением NULL** , он должен обрабатывать сообщения [**WM \_ RENDERFORMAT**](wm-renderformat.md) и [**WM \_ рендераллформатс**](wm-renderallformats.md) для отрисовки данных по запросу.</span><span class="sxs-lookup"><span data-stu-id="24650-182">If a window passes a **NULL** handle to the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function, it must process the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages to render data upon request.</span></span>

<span data-ttu-id="24650-183">Если окно задерживает Отображение определенного формата, а затем другое приложение запрашивает данные в этом формате, то в окно отправляется сообщение [**WM \_ RENDERFORMAT**](wm-renderformat.md) .</span><span class="sxs-lookup"><span data-stu-id="24650-183">If a window delays rendering a specific format and then another application requests data in that format, then a [**WM\_RENDERFORMAT**](wm-renderformat.md) message is sent to the window.</span></span> <span data-ttu-id="24650-184">Кроме того, если окно задерживает визуализацию одного или нескольких форматов, и если некоторые из этих форматов остаются невидимыми, когда окно собирается уничтожиться, то сообщение [**WM \_ рендераллформатс**](wm-renderallformats.md) отправляется в окно перед его уничтожением.</span><span class="sxs-lookup"><span data-stu-id="24650-184">In addition, if a window delays rendering one or more formats, and if some of those formats remain unrendered when the window is about to be destroyed, then a [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message is sent to the window before its destruction.</span></span>

<span data-ttu-id="24650-185">Чтобы отобразить формат буфера обмена, процедура Window должна помещаться в буфер обмена с помощью функции [**сетклипбоарддата**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) , не **имеющей значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="24650-185">To render a clipboard format, the window procedure should place a non-**NULL** data handle on the clipboard using the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function.</span></span> <span data-ttu-id="24650-186">Если процедура окна представляет формат в ответ на сообщение [**\_ RENDERFORMAT WM**](wm-renderformat.md) , он не должен открывать буфер обмена перед вызовом **сетклипбоарддата**.</span><span class="sxs-lookup"><span data-stu-id="24650-186">If the window procedure is rendering a format in response to the [**WM\_RENDERFORMAT**](wm-renderformat.md) message, it must not open the clipboard before calling **SetClipboardData**.</span></span> <span data-ttu-id="24650-187">Но если он выводит один или несколько форматов в ответ на сообщение [**\_ рендераллформатс WM**](wm-renderallformats.md) , он должен открыть буфер обмена и убедиться, что окно по-прежнему владеет буфером обмена перед вызовом **сетклипбоарддата**, и он должен закрыть буфер обмена перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="24650-187">But if it is rendering one or more formats in response to the [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message, it must open the clipboard and check that the window still owns the clipboard before calling **SetClipboardData**, and it must close the clipboard before returning.</span></span>

<span data-ttu-id="24650-188">Приложение Label обрабатывает сообщения [**WM \_ RENDERFORMAT**](wm-renderformat.md) и [**WM \_ рендераллформатс**](wm-renderallformats.md) следующим образом.</span><span class="sxs-lookup"><span data-stu-id="24650-188">The Label application processes the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages as follows.</span></span>


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



<span data-ttu-id="24650-189">В обоих случаях процедура Window вызывает определяемую приложением функцию RenderFormat, определенную следующим образом.</span><span class="sxs-lookup"><span data-stu-id="24650-189">In both cases, the window procedure calls the application-defined RenderFormat function, defined as follows.</span></span>

<span data-ttu-id="24650-190">Структура, именуемая ЛАБЕЛБОКС, определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="24650-190">The structure, called LABELBOX, is defined as follows.</span></span>


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



### <a name="processing-the-wm_destroyclipboard-message"></a><span data-ttu-id="24650-191">Обработка сообщения WM \_ дестройклипбоард</span><span class="sxs-lookup"><span data-stu-id="24650-191">Processing the WM\_DESTROYCLIPBOARD Message</span></span>

<span data-ttu-id="24650-192">Окно может обработать сообщение [**WM \_ дестройклипбоард**](wm-destroyclipboard.md) , чтобы освободить все ресурсы, которые были заданы для поддержки отложенной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="24650-192">A window can process the [**WM\_DESTROYCLIPBOARD**](wm-destroyclipboard.md) message in order to free any resources that it set aside to support delayed rendering.</span></span> <span data-ttu-id="24650-193">Например, приложение Label при копировании метки в буфер обмена выделяет объект локальной памяти.</span><span class="sxs-lookup"><span data-stu-id="24650-193">For example the Label application, when copying a label to the clipboard, allocates a local memory object.</span></span> <span data-ttu-id="24650-194">Затем этот объект освобождается в ответ на сообщение **\_ дестройклипбоард WM** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="24650-194">It then frees this object in response to the **WM\_DESTROYCLIPBOARD** message, as follows.</span></span>


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a><span data-ttu-id="24650-195">Использование формата буфера обмена Owner-Display</span><span class="sxs-lookup"><span data-stu-id="24650-195">Using the Owner-Display Clipboard Format</span></span>

<span data-ttu-id="24650-196">Если окно помещает сведения в буфер обмена с помощью формата буфера обмена **CF \_ овнердисплай** , оно должно выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="24650-196">If a window places information on the clipboard by using the **CF\_OWNERDISPLAY** clipboard format, it must do the following:</span></span>

-   <span data-ttu-id="24650-197">Обработайте сообщение [**WM \_ паинтклипбоард**](wm-paintclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="24650-197">Process the [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message.</span></span> <span data-ttu-id="24650-198">Это сообщение отправляется владельцу буфера обмена, когда часть окна средства просмотра буфера обмена должна быть перерисована.</span><span class="sxs-lookup"><span data-stu-id="24650-198">This message is sent to the clipboard owner when a portion of the clipboard viewer window must be repainted.</span></span>

-   <span data-ttu-id="24650-199">Обработайте сообщение [**WM \_ сизеклипбоард**](wm-sizeclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="24650-199">Process the [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span> <span data-ttu-id="24650-200">Это сообщение отправляется владельцу буфера обмена при изменении размера окна буфера обмена или его содержимого.</span><span class="sxs-lookup"><span data-stu-id="24650-200">This message is sent to the clipboard owner when the clipboard viewer window has been resized or its content has changed.</span></span>

    <span data-ttu-id="24650-201">Как правило, окно отвечает на это сообщение, устанавливая позиции прокрутки и диапазоны для окна средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-201">Typically, a window responds to this message by setting the scroll positions and ranges for the clipboard viewer window.</span></span> <span data-ttu-id="24650-202">В ответ на это сообщение приложение Label также обновляет структуру [**размера**](/previous-versions//dd145106(v=vs.85)) окна средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-202">In response to this message, the Label application also updates a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure for the clipboard viewer window.</span></span>

-   <span data-ttu-id="24650-203">Обработка сообщений [**WM \_ Хскроллклипбоард**](wm-hscrollclipboard.md) и [**WM \_ вскроллклипбоард**](wm-vscrollclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="24650-203">Process the [**WM\_HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) and [**WM\_VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) messages.</span></span> <span data-ttu-id="24650-204">Эти сообщения отправляются владельцу буфера обмена при возникновении события полосы прокрутки в окне средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-204">These messages are sent to the clipboard owner when a scroll bar event occurs in the clipboard viewer window.</span></span>

-   <span data-ttu-id="24650-205">Обработайте сообщение [**WM \_ асккбформатнаме**](wm-askcbformatname.md) .</span><span class="sxs-lookup"><span data-stu-id="24650-205">Process the [**WM\_ASKCBFORMATNAME**](wm-askcbformatname.md) message.</span></span> <span data-ttu-id="24650-206">Окно просмотра буфера обмена отправляет это сообщение приложению для получения имени формата, отображаемого владельцем.</span><span class="sxs-lookup"><span data-stu-id="24650-206">The clipboard viewer window sends this message to an application to retrieve the name of the owner-display format.</span></span>

<span data-ttu-id="24650-207">Процедура Window для приложения Label обрабатывает эти сообщения следующим образом.</span><span class="sxs-lookup"><span data-stu-id="24650-207">The window procedure for the Label application processes these messages, as follows.</span></span>


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



## <a name="monitoring-clipboard-contents"></a><span data-ttu-id="24650-208">Мониторинг содержимого буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-208">Monitoring Clipboard Contents</span></span>

<span data-ttu-id="24650-209">Существует три способа мониторинга изменений в буфере обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-209">There are three ways of monitoring changes to the clipboard.</span></span> <span data-ttu-id="24650-210">Самый старый способ — создать окно средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-210">The oldest method is to create a clipboard viewer window.</span></span> <span data-ttu-id="24650-211">В Windows 2000 добавлена возможность запрашивать порядковый номер буфера обмена, а в Windows Vista добавлена поддержка прослушивателей формата буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-211">Windows 2000 added the ability to query the clipboard sequence number, and Windows Vista added support for clipboard format listeners.</span></span> <span data-ttu-id="24650-212">Окна буфера обмена поддерживаются для обеспечения обратной совместимости с более ранними версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="24650-212">Clipboard viewer windows are supported for backward compatibility with earlier versions of Windows.</span></span> <span data-ttu-id="24650-213">Новые программы должны использовать прослушиватели формата буфера обмена или порядковый номер буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-213">New programs should use clipboard format listeners or the clipboard sequence number.</span></span>

## <a name="querying-the-clipboard-sequence-number"></a><span data-ttu-id="24650-214">Запрос порядкового номера буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-214">Querying the Clipboard Sequence Number</span></span>

<span data-ttu-id="24650-215">Каждый раз, когда содержимое буфера обмена изменяется, увеличивается 32-разрядное значение, известное как порядковый номер буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-215">Each time the contents of the clipboard change, a 32-bit value known as the clipboard sequence number is incremented.</span></span> <span data-ttu-id="24650-216">Программа может получить текущий порядковый номер буфера обмена, вызвав функцию [**жетклипбоардсекуенценумбер**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) .</span><span class="sxs-lookup"><span data-stu-id="24650-216">A program can retrieve the current clipboard sequence number by calling the [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) function.</span></span> <span data-ttu-id="24650-217">Сравнивая значение, возвращаемое для значения, возвращенного предыдущим вызовом **жетклипбоардсекуенценумбер**, программа может определить, изменилось ли содержимое буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-217">By comparing the value returned against a value returned by a previous call to **GetClipboardSequenceNumber**, a program can determine whether the clipboard contents have changed.</span></span> <span data-ttu-id="24650-218">Этот метод лучше подходит для программ, которые кэшируют результаты на основе текущего содержимого буфера обмена и должны знать, являются ли вычисления допустимыми, прежде чем использовать результаты из этого кэша.</span><span class="sxs-lookup"><span data-stu-id="24650-218">This method is more suitable to programs which cache results based on the current clipboard contents and need to know whether the calculations are still valid before using the results from that cache.</span></span> <span data-ttu-id="24650-219">Обратите внимание, что это не метод уведомления, и его не следует использовать в цикле опроса.</span><span class="sxs-lookup"><span data-stu-id="24650-219">Note that this is a not a notification method and should not be used in a polling loop.</span></span> <span data-ttu-id="24650-220">Чтобы получать уведомления об изменении содержимого буфера обмена, используйте прослушиватель формата буфера обмена или средство просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-220">To be notified when clipboard contents change, use a clipboard format listener or a clipboard viewer.</span></span>

## <a name="creating-a-clipboard-format-listener"></a><span data-ttu-id="24650-221">Создание прослушивателя формата буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-221">Creating a Clipboard Format Listener</span></span>

<span data-ttu-id="24650-222">Прослушиватель формата буфера обмена — это окно, зарегистрированное для уведомления об изменении содержимого буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-222">A clipboard format listener is a window which has registered to be notified when the contents of the clipboard has changed.</span></span> <span data-ttu-id="24650-223">Этот метод рекомендуется использовать вместо создания окна средства просмотра буфера обмена, так как его проще реализовать и избежать проблем, если программы не смогут правильно поддерживать цепочку просмотра буфера обмена или если окно в цепочке просмотра буфера обмена перестает отвечать на сообщения.</span><span class="sxs-lookup"><span data-stu-id="24650-223">This method is recommended over creating a clipboard viewer window because it is simpler to implement and avoids problems if programs fail to maintain the clipboard viewer chain properly or if a window in the clipboard viewer chain stops responding to messages.</span></span>

<span data-ttu-id="24650-224">Окно регистрируется в качестве прослушивателя формата буфера обмена путем вызова функции [**аддклипбоардформатлистенер**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="24650-224">A window registers as a clipboard format listener by calling the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span> <span data-ttu-id="24650-225">При изменении содержимого буфера обмена окно отправляет сообщение [**WM \_ клипбоардупдате**](wm-clipboardupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="24650-225">When the contents of the clipboard change, the window is posted a [**WM\_CLIPBOARDUPDATE**](wm-clipboardupdate.md) message.</span></span> <span data-ttu-id="24650-226">Регистрация остается действительной до тех пор, пока окно не будет отменено, вызвав функцию [**ремовеклипбоардформатлистенер**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="24650-226">The registration remains valid until the window unregister itself by calling the [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) function.</span></span>

## <a name="creating-a-clipboard-viewer-window"></a><span data-ttu-id="24650-227">Создание окна средства просмотра буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-227">Creating a Clipboard Viewer Window</span></span>

<span data-ttu-id="24650-228">Окно просмотра буфера обмена отображает текущее содержимое буфера обмена и получает сообщения при изменении содержимого буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-228">A clipboard viewer window displays the current content of the clipboard, and receives messages when the clipboard content changes.</span></span> <span data-ttu-id="24650-229">Чтобы создать окно средства просмотра буфера обмена, приложение должно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="24650-229">To create a clipboard viewer window, your application must do the following:</span></span>

-   <span data-ttu-id="24650-230">Добавьте окно в цепочку средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-230">Add the window to the clipboard viewer chain.</span></span>
-   <span data-ttu-id="24650-231">Обработайте сообщение [**WM \_ чанжекбчаин**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="24650-231">Process the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>
-   <span data-ttu-id="24650-232">Обработайте сообщение [**WM \_ дравклипбоард**](wm-drawclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="24650-232">Process the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message.</span></span>
-   <span data-ttu-id="24650-233">Удалите окно из цепочки окна просмотра буфера обмена, прежде чем оно будет уничтожено.</span><span class="sxs-lookup"><span data-stu-id="24650-233">Remove the window from the clipboard viewer chain before it is destroyed.</span></span>

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a><span data-ttu-id="24650-234">Добавление окна в цепочку средства просмотра буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-234">Adding a Window to the Clipboard Viewer Chain</span></span>

<span data-ttu-id="24650-235">Окно добавляет себя в цепочку средства просмотра буфера обмена путем вызова функции [**сетклипбоардвиевер**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="24650-235">A window adds itself to the clipboard viewer chain by calling the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span> <span data-ttu-id="24650-236">Возвращаемое значение — это обработчик следующего окна в цепочке.</span><span class="sxs-lookup"><span data-stu-id="24650-236">The return value is the handle to the next window in the chain.</span></span> <span data-ttu-id="24650-237">Окно должно отследить это значение, например путем его сохранения в статической переменной с именем *хвнднекствиевер*.</span><span class="sxs-lookup"><span data-stu-id="24650-237">A window must keep track of this value — for example, by saving it in a static variable named *hwndNextViewer*.</span></span>

<span data-ttu-id="24650-238">В следующем примере окно добавляется в цепочку окна просмотра буфера обмена в ответ на сообщение о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="24650-238">The following example adds a window to the clipboard viewer chain in response to the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span>


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



<span data-ttu-id="24650-239">Фрагменты кода отображаются для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="24650-239">Code snippets are shown for the following tasks:</span></span>

-   [<span data-ttu-id="24650-240">Обработка сообщения WM \_ чанжекбчаин</span><span class="sxs-lookup"><span data-stu-id="24650-240">Processing the WM\_CHANGECBCHAIN Message</span></span>](/windows)
-   [<span data-ttu-id="24650-241">Удаление окна из цепочки окна просмотра буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-241">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
-   [<span data-ttu-id="24650-242">Обработка сообщения WM \_ дравклипбоард</span><span class="sxs-lookup"><span data-stu-id="24650-242">Processing the WM\_DRAWCLIPBOARD Message</span></span>](/windows)
-   [<span data-ttu-id="24650-243">Пример средства просмотра буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-243">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a><span data-ttu-id="24650-244">Обработка сообщения WM \_ чанжекбчаин</span><span class="sxs-lookup"><span data-stu-id="24650-244">Processing the WM\_CHANGECBCHAIN Message</span></span>

<span data-ttu-id="24650-245">Окно просмотра буфера обмена получает сообщение [**WM \_ чанжекбчаин**](wm-changecbchain.md) , когда другое окно удаляет себя из цепочки средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-245">A clipboard viewer window receives the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message when another window is removing itself from the clipboard viewer chain.</span></span> <span data-ttu-id="24650-246">Если удаляемое окно является следующим окном в цепочке, окно, получающее сообщение, должно удалить связь со следующим окном из цепочки.</span><span class="sxs-lookup"><span data-stu-id="24650-246">If the window being removed is the next window in the chain, the window receiving the message must unlink the next window from the chain.</span></span> <span data-ttu-id="24650-247">В противном случае это сообщение должно быть передано в следующее окно в цепочке.</span><span class="sxs-lookup"><span data-stu-id="24650-247">Otherwise, this message should be passed to the next window in the chain.</span></span>

<span data-ttu-id="24650-248">В следующем примере показана обработка сообщения [**WM \_ чанжекбчаин**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="24650-248">The following example shows the processing of the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>


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



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a><span data-ttu-id="24650-249">Удаление окна из цепочки окна просмотра буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-249">Removing a Window from the Clipboard Viewer Chain</span></span>

<span data-ttu-id="24650-250">Чтобы удалить себя из цепочки средства просмотра буфера обмена, окно вызывает функцию [**чанжеклипбоардчаин**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) .</span><span class="sxs-lookup"><span data-stu-id="24650-250">To remove itself from the clipboard viewer chain, a window calls the [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) function.</span></span> <span data-ttu-id="24650-251">В следующем примере удаляется окно из цепочки окна буфера просмотра в ответ на сообщение [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="24650-251">The following example removes a window from the clipboard viewer chain in response to the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a><span data-ttu-id="24650-252">Обработка сообщения WM \_ дравклипбоард</span><span class="sxs-lookup"><span data-stu-id="24650-252">Processing the WM\_DRAWCLIPBOARD Message</span></span>

<span data-ttu-id="24650-253">Сообщение [**WM \_ дравклипбоард**](wm-drawclipboard.md) уведомляет окно средства просмотра буфера обмена о том, что содержимое буфера обмена изменилось.</span><span class="sxs-lookup"><span data-stu-id="24650-253">The [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message notifies a clipboard viewer window that the content of the clipboard has changed.</span></span> <span data-ttu-id="24650-254">При обработке сообщения **WM \_ дравклипбоард** в окне необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="24650-254">A window should do the following when processing the **WM\_DRAWCLIPBOARD** message:</span></span>

1.  <span data-ttu-id="24650-255">Определите, какой из доступных форматов буфера обмена нужно отобразить.</span><span class="sxs-lookup"><span data-stu-id="24650-255">Determine which of the available clipboard formats to display.</span></span>
2.  <span data-ttu-id="24650-256">Извлеките данные из буфера обмена и отобразите их в окне.</span><span class="sxs-lookup"><span data-stu-id="24650-256">Retrieve the clipboard data and display it in the window.</span></span> <span data-ttu-id="24650-257">Или если формат буфера обмена — **CF \_ овнердисплай**, отправьте сообщение [**WM \_ паинтклипбоард**](wm-paintclipboard.md) владельцу буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-257">Or if the clipboard format is **CF\_OWNERDISPLAY**, send a [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message to the clipboard owner.</span></span>
3.  <span data-ttu-id="24650-258">Отправка сообщения в следующее окно в цепочке окна просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-258">Send the message to the next window in the clipboard viewer chain.</span></span>

<span data-ttu-id="24650-259">Пример обработки сообщения [**WM \_ дравклипбоард**](wm-drawclipboard.md) см. в примере, приведенном в [примере средства просмотра буфера обмена](#example-of-a-clipboard-viewer).</span><span class="sxs-lookup"><span data-stu-id="24650-259">For an example of processing the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message, see the example listing in [Example of a Clipboard Viewer](#example-of-a-clipboard-viewer).</span></span>

### <a name="example-of-a-clipboard-viewer"></a><span data-ttu-id="24650-260">Пример средства просмотра буфера обмена</span><span class="sxs-lookup"><span data-stu-id="24650-260">Example of a Clipboard Viewer</span></span>

<span data-ttu-id="24650-261">В следующем примере показано простое приложение просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="24650-261">The following example shows a simple clipboard viewer application.</span></span>


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



 

 