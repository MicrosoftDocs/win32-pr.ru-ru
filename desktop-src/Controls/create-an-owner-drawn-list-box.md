---
title: Создание списка Owner-Drawn
description: В этом разделе показано, как реализовать рисуемый владельцем список.
ms.assetid: AE6E8943-DC03-4A21-9F0A-9C70C6BD7481
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b48a56ca188fb2c277cc822dcb9a343205a331
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988023"
---
# <a name="how-to-create-an-owner-drawn-list-box"></a>Создание списка Owner-Drawn

В этом разделе показано, как реализовать рисуемый владельцем список.

В примере кода C++ в этом разделе показано, как нарисовать список, содержащий пять элементов, рисуемых владельцем: четыре реализации рисования и вилка. Каждый элемент списка отображается в виде точечного рисунка, за которым следует имя объекта. Кнопка предлагает пользователю выбрать один элемент, который не похож на другие. При нажатии кнопки с выбранным разветвленным выводится «вы верно». сообщение и закрывает диалоговое окно. При нажатии кнопки с любым другим выбранным элементом списка отображается сообщение "повторить попытку!" .

В списке имеются стили [**фунта \_ Овнердравфиксед**](list-box-styles.md) и [**фунта \_**](list-box-styles.md) , а также стандартные стили списка.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции


Чтобы инициализировать список, рисуемый владельцем, приложение должно загрузить текстовую строку и связанный точечный рисунок для каждого элемента списка.

В следующем примере кода C++ процедура диалогового окна инициализирует список, **\_ список \_ IDC**, отправляя сообщение [**\_ ADDSTRING**](lb-addstring.md) для установки текста, а затем отправляет сообщение [**\_ сетитемдата балансировки нагрузки**](lb-setitemdata.md) , чтобы связать точечный рисунок с каждым элементом списка. Код также задает высоту каждого элемента списка путем обработки сообщения [**WM \_ меасуреитем**](wm-measureitem.md) и рисует текст и точечный рисунок для каждого элемента, обрабатывая сообщение [**WM \_ DRAWITEM**](wm-drawitem.md) .



```C++
#define XBITMAP 48 
#define YBITMAP 48 
 
#define BUFFER MAX_PATH 
 
HBITMAP hbmpPencil, hbmpCrayon, hbmpMarker, hbmpPen, hbmpFork; 
HBITMAP hbmpPicture, hbmpOld; 
 
void AddItem(HWND hwnd, PTSTR pstr, HBITMAP hbmp) 
{ 
    int lbItem; 
 
    lbItem = SendMessage(hwnd, LB_ADDSTRING, 0, (LPARAM)pstr); 
    SendMessage(hwnd, LB_SETITEMDATA, (WPARAM)lbItem, (LPARAM)hbmp); 
} 
 
INT_PTR CALLBACK DlgDrawProc(HWND hDlg, UINT message,
        UINT wParam, LONG lParam) 
{ 
    HWND hListBox; 
    PMEASUREITEMSTRUCT pmis; 
    PDRAWITEMSTRUCT pdis; 
    HDC hdcMem; 
       HBITMAP hbmp; 
    TCHAR achBuffer[BUFFER];
    size_t cch;
    int yPos; 
    int lbItem; 
    TEXTMETRIC tm; 
    RECT rcBitmap;
    HRESULT hr; 
    
    switch (message) 
    { 
         case WM_INITDIALOG: 
 
            // Load the bitmaps. g_hInst is the global HINSTANCE handle.
            hbmpPencil = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_PENCIL)); 
            hbmpCrayon = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_CRAYON)); 
            hbmpMarker = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_MARKER)); 
            hbmpPen = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_PEN)); 
            hbmpFork = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_FORK)); 
 
            // Retrieve the list box handle. 
            hListBox = GetDlgItem(hDlg, IDC_LIST_STUFF); 
 
            // Initialize the list box text and associate a bitmap 
            // with each list box item. 
            AddItem(hListBox, L"pencil", hbmpPencil); 
            AddItem(hListBox, L"crayon", hbmpCrayon); 
            AddItem(hListBox, L"marker", hbmpMarker); 
            AddItem(hListBox, L"pen",    hbmpPen); 
            AddItem(hListBox, L"fork",   hbmpFork); 
 
            SetFocus(hListBox); 
            SendMessage(hListBox, LB_SETCURSEL, 0, 0); 
            return TRUE; 
 
        case WM_MEASUREITEM: 
 
            pmis = (PMEASUREITEMSTRUCT) lParam; 
 
            // Set the height of the list box items. 
            pmis->itemHeight = YBITMAP;

            return TRUE; 
 
        case WM_DRAWITEM: 
 
            pdis = (PDRAWITEMSTRUCT) lParam; 
 
            // If there are no list box items, skip this message. 
            if (pdis->itemID == -1) 
            { 
                break; 
            } 
 
            // Draw the bitmap and text for the list box item. Draw a 
            // rectangle around the bitmap if it is selected. 
            switch (pdis->itemAction) 
            { 
                case ODA_SELECT: 
                case ODA_DRAWENTIRE: 
 
                    // Draw the bitmap associated with the item. 
                    //
                    // Get the item bitmap.
                    hbmpPicture = (HBITMAP)SendMessage(pdis->hwndItem, 
                        LB_GETITEMDATA, pdis->itemID, 0); 
 
                    // Create a compatible device context. 
                    hdcMem = CreateCompatibleDC(pdis->hDC); 

                    // Select the item bitmap into the compatible device
                    // context and save the old bitmap.
                    hbmpOld = (HBITMAP) SelectObject(hdcMem, hbmpPicture); 
 
                    // Copy the bitmap into the compatible device context.
                    BitBlt(pdis->hDC, 
                        pdis->rcItem.left, pdis->rcItem.top, 
                        pdis->rcItem.right - pdis->rcItem.left, 
                        pdis->rcItem.bottom - pdis->rcItem.top, 
                        hdcMem, 0, 0, SRCCOPY); 
 
                    // Draw the string associated with the item. 
                    //
                    // Get the item string from the list box.
                    SendMessage(pdis->hwndItem, LB_GETTEXT, 
                        pdis->itemID, (LPARAM)achBuffer); 
 
                    // Get the metrics for the current font.
                    GetTextMetrics(pdis->hDC, &tm); 

                    // Calculate the vertical position for the item string 
                    // so that the string will be vertically centered in the 
                    // item rectangle.
                    yPos = (pdis->rcItem.bottom + pdis->rcItem.top - 
                        tm.tmHeight) / 2;
                        
                    // Get the character length of the item string.
                    hr = StringCchLength(achBuffer, BUFFER, &cch);
                    if (FAILED(hr))
                    {
                        // TODO: Handle error.
                    }
 
                    // Draw the string in the item rectangle, leaving a six
                    // pixel gap between the item bitmap and the string.
                    TextOut(pdis->hDC, XBITMAP + 6, yPos, achBuffer, cch);                         
 
                    // Clean up.
                    SelectObject(hdcMem, hbmpOld); 
                    DeleteDC(hdcMem); 
 
                    // Is the item selected? 
                    if (pdis->itemState & ODS_SELECTED) 
                    { 
                        // Set RECT coordinates to surround only the 
                        // bitmap. 
                        rcBitmap.left = pdis->rcItem.left; 
                        rcBitmap.top = pdis->rcItem.top; 
                        rcBitmap.right = pdis->rcItem.left + XBITMAP; 
                        rcBitmap.bottom = pdis->rcItem.top + YBITMAP; 
 
                        // Draw a rectangle around bitmap to indicate 
                        // the selection. 
                        DrawFocusRect(pdis->hDC, &rcBitmap); 
                    } 
                    break; 
 
                case ODA_FOCUS: 
 
                    // Do not process focus changes. The focus caret 
                    // (outline rectangle) indicates the selection. 
                    // The IDOK button indicates the final 
                    // selection. 
                    break; 
            } 
            return TRUE; 
 
        case WM_COMMAND: 
 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    // Get the selected item's text. 
                    lbItem = SendMessage(GetDlgItem(hDlg, IDC_LIST_STUFF), 
                        LB_GETCURSEL, 0, 0); 

                    // Get the selected item's bitmap. 
                    hbmp = (HBITMAP) SendMessage(GetDlgItem(hDlg, IDC_LIST_STUFF), 
                         LB_GETITEMDATA, lbItem, 0); 
 
                    // If the item is not the correct answer, tell the 
                    // user to try again. 
                    //
                    // If the item is the correct answer, congratulate 
                    // the user and destroy the dialog box. 
                    if (hbmp != hbmpFork) 
                    { 
                        MessageBox(hDlg, L"Try again!", L"Oops", MB_OK); 
                        return FALSE; 
                    } 
                    else 
                    { 
                        MessageBox(hDlg, L"You're right!", 
                            L"Congratulations.", MB_OK); 
 
                      // Fall through. 
                    } 
 
                case IDCANCEL: 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
 
                default: 
 
                    return FALSE; 
            } 
 
        case WM_DESTROY: 
 
            // Free the bitmap resources. 
            DeleteObject(hbmpPencil); 
            DeleteObject(hbmpCrayon); 
            DeleteObject(hbmpMarker); 
            DeleteObject(hbmpPen); 
            DeleteObject(hbmpFork); 
 
            return TRUE; 
 
        default: 
            return FALSE; 
 
    } 
    return FALSE; 
} 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по элементу управления "список"](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Сведения о списках](about-list-boxes.md)
</dt> <dt>

[Использование списков](using-list-boxes.md)
</dt> </dl>

 

 




