---
title: Создание Owner-Drawn поля со списком
description: В этом разделе показано, как использовать поле со списком, рисуемое владельцем.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5355dd33fe0067165308e9e6e5885b76edbe7ceb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070655"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a>Создание Owner-Drawn поля со списком

В этом разделе показано, как использовать поле со списком, рисуемое владельцем. В примере кода C++ используется раскрывающийся список, рисуемый владельцем, для отображения четырех групп продуктов, каждый из которых представлен точечным рисунком и именем. Выбор группы продуктов питания приводит к тому, что продуктов в этой группе появятся в списке.

![снимок экрана с диалоговым окном со списком и развернутым раскрывающимся списком, отображающим значок и метку для каждого элемента](images/cscbx-01.png)

Диалоговое окно также содержит список (IDLIST) и две кнопки: **ОК** (идок) и **Отмена** (идканцел). Константы ИДОК и ИДКАНЦЕЛ определяются файлами заголовков пакета SDK. Константа IDLIST определяется в файле заголовка приложения, как и идентификатор элемента управления ИДКОМБО. Дополнительные сведения о диалоговых окнах см. в разделе [диалоговые окна](/windows/desktop/dlgbox/dialog-boxes).

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="step-1-create-the-owner-drawn-dialog-box"></a>Шаг 1. Создание диалогового окна «Owner-Drawn»

В примере кода используется функция [**диалогбокс**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) для создания модального диалогового окна. Шаблон диалогового окна Идд \_ скмеал определяет стили окна, кнопки и идентификаторы элементов управления для поля со списком. В поле со списком в этом примере используются [**Стили \_ CBS**](combo-box-styles.md), [**CBS \_ овнердравфиксед**](combo-box-styles.md), [**CBS \_ Sort**](combo-box-styles.md), [**CBS \_ хасстрингс**](combo-box-styles.md), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)и [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a>Шаг 2. Обработка сообщений WM \_ инитдиалог и WM \_ destroy в диалоговом окне.

При использовании поля со списком в диалоговом окне, как правило, вы отвечаете на сообщение [**WM \_ инитдиалог**](/windows/desktop/dlgbox/wm-initdialog) , инициализируя поле со списком. Приложение загружает точечные рисунки, используемые для рисуемого владельцем поля со списком, а затем вызывает определяемую приложением `InitGroupList` функцию для инициализации поля со списком. Он также выбирает первый элемент списка в поле со списком, а затем вызывает определяемую приложением `InitFoodList` функцию для инициализации списка.

В этом примере поле со списком, рисуемым владельцем, представляет собой раскрывающийся список, содержащий имена всех четырех групп продуктов. `InitGroupList` Добавляет имя каждой группы продуктов и использует сообщение [**\_ сетитемдата CB**](cb-setitemdata.md) для связывания маркера точечного рисунка с каждым элементом списка, идентифицирующим группу продуктов.

Список в примере содержит имена продуктов в выбранной группе продуктов. **Инитфудлист** сбрасывает содержимое списка, а затем добавляет имена текущего выбора продуктов в раскрывающийся список текущая группа продуктов.


```C++
case WM_INITDIALOG:

    // Call an application-defined function to load bitmap resources.
    if (!LoadIconBitmaps())
    {
        EndDialog(hDlg, -1);
        break;
    }

    // Initialize the food groups combo box and select the first item.
    InitGroupList(hDlg);
    SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

    // Initialize the food list box and select the first item.
    InitFoodList(hDlg);
    SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

     return (INT_PTR)TRUE;
```



При получении сообщения [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) приложение удаляет точечные рисунки в поле со списком, рисуемом владельцем.


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a>Шаг 3. обработка сообщения WM \_ меасуреитем.

Поле со списком, рисуемое владельцем, отправляет сообщение [**WM \_ меасуреитем**](wm-measureitem.md) в свое родительское окно или процедуру диалогового окна, чтобы приложение может задать размеры каждого элемента списка. Так как поле со списком "пример" имеет стиль [**CBS \_ овнердравфиксед**](combo-box-styles.md) , система отправляет сообщение **WM \_ меасуреитем** только один раз. Поля со списком в стиле [**CBS \_ овнердраввариабле**](combo-box-styles.md) отправляют сообщение **WM \_ меасуреитем** для каждого элемента списка.

Параметр *lParam* является указателем на структуру [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) , определяющую элемент управления и элемент списка. Он также содержит измерения по умолчанию для элемента списка. В примере изменяется элемент структуры **итемхеигхт** , чтобы гарантировать, что элементы списка достаточно высоки для размещения растровых изображений группы продуктов.


```C++
case WM_MEASUREITEM:
    {
    // Set the height of the items in the food groups combo box.
    LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

    if (lpmis->itemHeight < CY_BITMAP + 2)
        lpmis->itemHeight = CY_BITMAP + 2;

    break;
    }
```



### <a name="step-4-process-the-wm_drawitem-message"></a>Шаг 4. обработка сообщения WM \_ DRAWITEM.

Поле со списком, рисуемое владельцем, отправляет сообщение [**WM \_ DRAWITEM**](wm-drawitem.md) в свое родительское окно или процедуру диалогового окна каждый раз, когда приложение должно перерисовывать элемент списка. Параметр *lParam* является указателем на структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , определяющую элемент управления и элемент списка. Он также содержит сведения, необходимые для рисования элемента.

В примере приложения отображается текст элемента списка и точечный рисунок, связанный с группой пищи. Если элемент имеет фокус, он также рисует прямоугольник фокуса. Перед отображением текста в примере задаются цвета переднего плана и фона на основе выбранного элемента. Так как поле со списком имеет стиль [**CBS \_ хасстрингс**](combo-box-styles.md) , поле со списком поддерживает текст для каждого элемента списка, который можно получить с помощью сообщения [**\_ жетлбтекст CB**](cb-getlbtext.md) .

Точечные рисунки, используемые для элемента списка, зависят от группы продуктов. `InitGroupList` использует сообщение [**\_ сетитемдата CB**](cb-setitemdata.md) для связывания маркера точечного рисунка с каждым элементом списка. Процедура окна Извлекает маркер растрового изображения из элемента **итемдата** структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . Система использует два точечных рисунка для каждого символа группы пищи: монохромное растровое изображение с растровой операцией СРКАНД для стирания неправильного региона за изображением и цветовой точечный рисунок с растровой операцией СРКПАИНТ для рисования изображения.


```C++
case WM_DRAWITEM:
    {
    COLORREF clrBackground;
    COLORREF clrForeground;
    TEXTMETRIC tm;
    int x;
    int y;
    HRESULT hr;
    size_t cch;

    LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
       
    if (lpdis->itemID == -1) // Empty item)
        break;

    // Get the food icon from the item data.
    hbmIcon = (HBITMAP) lpdis->itemData;

    // The colors depend on whether the item is selected.
    clrForeground = SetTextColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

    clrBackground = SetBkColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHT : COLOR_WINDOW));

    // Calculate the vertical and horizontal position.
    GetTextMetrics(lpdis->hDC, &tm);
    y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
    x = LOWORD(GetDialogBaseUnits()) / 4;

    // Get and display the text for the list item.
    SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
        lpdis->itemID, (LPARAM) achTemp);

    hr = StringCchLength(achTemp, 256, &cch);
    if (FAILED(hr))
    {
        // TODO: Write error handler.
    }

    ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
        ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
        achTemp, (UINT)cch, NULL);

    // Restore the previous colors.
    SetTextColor(lpdis->hDC, clrForeground);
    SetBkColor(lpdis->hDC, clrBackground);
    
    //  Draw the food icon for the item. 
    HDC hdc = CreateCompatibleDC(lpdis->hDC); 
    if (hdc == NULL) 
        break; 
 
    SelectObject(hdc, hbmMask); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
    SelectObject(hdc, hbmIcon); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
    DeleteDC(hdc); 
  
    // If the item has the focus, draw the focus rectangle.
    if (lpdis->itemState & ODS_FOCUS)
        DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

    break;
    }
```



### <a name="step-5-process-the-wm_command-message"></a>Шаг 5. Обработка \_ командного сообщения WM.

При возникновении события в элементе управления диалогового окна элемент управления уведомляет процедуру диалогового окна с помощью [**\_ командного сообщения WM**](/windows/desktop/menurc/wm-command) . Пример обрабатывает сообщения уведомления из поля со списком, списка и кнопки **ОК** . Идентификатор элемента управления находится в младшем слове *wParam*, а код уведомления — в слове *wParam* с высоким порядком.

Если идентификатор элемента управления — ИДКОМБО, в поле со списком возникло событие. В ответ процедура диалогового окна игнорирует все другие события поля со списком, кроме [**КБН \_ селендок**](cbn-selendok.md), что означает, что был сделан выбор, раскрывающийся список был закрыт и внесенные изменения должны быть приняты. В диалоговом окне вызывается процедура `InitFoodList` для сброса содержимого списка и добавления имен текущего выбора в раскрывающемся списке.

Если идентификатор элемента управления — IDLIST, в списке произошло событие. Это приводит к тому, что процедура диалогового окна пропускает все события списка, кроме [**ЛБН \_ дблклк**](lbn-dblclk.md), что означает, что пользователь дважды щелкнул элемент списка. Это событие обрабатывается так же, как если бы была выбрана кнопка **ОК** .

Если идентификатор элемента управления — ИДОК, пользователь выбрал кнопку **ОК** . В ответ процедура диалогового окна вставляет имя выбранного пищи в многострочный элемент управления "поле ввода", а затем вызывает функцию [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) для закрытия этого диалогового окна.

Если идентификатор элемента управления — ИДКАНЦЕЛ, пользователь нажмет кнопку **Отмена** . В ответ процедура диалогового окна вызывает метод [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) , чтобы закрыть диалоговое окно.


```C++
case WM_COMMAND:
        switch (LOWORD(wParam)) 
        { 
            case IDCOMBO: 
                if (HIWORD(wParam) == CBN_SELENDOK) 
                { 
                    InitFoodList(hDlg); 
                    SendDlgItemMessage(hDlg, IDLIST, 
                        LB_SETCURSEL, 0, 0); 
                } 
                break; 
 
            case IDLIST: 
                if (HIWORD(wParam) != LBN_DBLCLK) 
                    break; 
 
            // For a double-click, process the OK case. 
            case IDOK: 
 
                // Get the text for the selected list item. 
                hwnd = GetDlgItem(hDlg, IDLIST); 

                // Here it is assumed the text can fit into achTemp.
                // If there is doubt, call LB_GETTEXTLENGTH first.
                SendMessage(hwnd, LB_GETTEXT, 
                    SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                    (LPARAM) achTemp); 
 
                // TODO: Do something with the selected text.
 
                EndDialog(hDlg, 0); 
                break; 
 
            case IDCANCEL: 
                hwnd = GetDlgItem(hDlg, IDCOMBO); 
                if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                    SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                else EndDialog(hDlg, 0); 
        } 
        break; 
```



## <a name="complete-example"></a>Полный пример

Ниже приведена процедура диалогового окна и вспомогательные функции для диалогового окна « **квадратный еды** ».


```C++
#define ID_BREAD 0
#define ID_DAIRY 1
#define ID_FRUIT 2
#define ID_MEAT  3

#define CX_BITMAP 24
#define CY_BITMAP 24

HBITMAP hbmBread;
HBITMAP hbmDairy;
HBITMAP hbmMeat;
HBITMAP hbmFruit;
HBITMAP hbmMask;

HBITMAP hbmIcon;
```

```C++
// Message handler for Square Meal dialog box.
INT_PTR CALLBACK FoodDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam)
{
    UNREFERENCED_PARAMETER(lParam);
    TCHAR achTemp[256];
    HWND hwnd;

    switch (message)
    {
    case WM_INITDIALOG:

        // Call an application-defined function to load bitmap resources.
        if (!LoadIconBitmaps())
        {
            EndDialog(hDlg, -1);
            break;
        }

        // Initialize the food groups combo box and select the first item.
        InitGroupList(hDlg);
        SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

        // Initialize the food list box and select the first item.
        InitFoodList(hDlg);
        SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

         return (INT_PTR)TRUE;
   
    case WM_MEASUREITEM:
        {
        // Set the height of the items in the food groups combo box.
        LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

        if (lpmis->itemHeight < CY_BITMAP + 2)
            lpmis->itemHeight = CY_BITMAP + 2;

        break;
        }

    case WM_DRAWITEM:
        {
        COLORREF clrBackground;
        COLORREF clrForeground;
        TEXTMETRIC tm;
        int x;
        int y;
        HRESULT hr;
        size_t cch;

        LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
           
        if (lpdis->itemID == -1) // Empty item)
            break;

        // Get the food icon from the item data.
        hbmIcon = (HBITMAP) lpdis->itemData;

        // The colors depend on whether the item is selected.
        clrForeground = SetTextColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

        clrBackground = SetBkColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHT : COLOR_WINDOW));

        // Calculate the vertical and horizontal position.
        GetTextMetrics(lpdis->hDC, &tm);
        y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
        x = LOWORD(GetDialogBaseUnits()) / 4;

        // Get and display the text for the list item.
        SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
            lpdis->itemID, (LPARAM) achTemp);

        hr = StringCchLength(achTemp, 256, &cch);
        if (FAILED(hr))
        {
            // TODO: Write error handler.
        }

        ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
            ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
            achTemp, (UINT)cch, NULL);

        // Restore the previous colors.
        SetTextColor(lpdis->hDC, clrForeground);
        SetBkColor(lpdis->hDC, clrBackground);
        
        //  Draw the food icon for the item. 
        HDC hdc = CreateCompatibleDC(lpdis->hDC); 
        if (hdc == NULL) 
            break; 
 
        SelectObject(hdc, hbmMask); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
        SelectObject(hdc, hbmIcon); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
        DeleteDC(hdc); 
      
        // If the item has the focus, draw the focus rectangle.
        if (lpdis->itemState & ODS_FOCUS)
            DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

        break;
        }

    case WM_COMMAND:
            switch (LOWORD(wParam)) 
            { 
                case IDCOMBO: 
                    if (HIWORD(wParam) == CBN_SELENDOK) 
                    { 
                        InitFoodList(hDlg); 
                        SendDlgItemMessage(hDlg, IDLIST, 
                            LB_SETCURSEL, 0, 0); 
                    } 
                    break; 
 
                case IDLIST: 
                    if (HIWORD(wParam) != LBN_DBLCLK) 
                        break; 
 
                // For a double-click, process the OK case. 
                case IDOK: 
 
                    // Get the text for the selected list item. 
                    hwnd = GetDlgItem(hDlg, IDLIST); 

                    // Here it is assumed the text can fit into achTemp.
                    // If there is doubt, call LB_GETTEXTLENGTH first.
                    SendMessage(hwnd, LB_GETTEXT, 
                        SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                        (LPARAM) achTemp); 
 
                    // TODO: Do something with the selected text.
 
                    EndDialog(hDlg, 0); 
                    break; 
 
                case IDCANCEL: 
                    hwnd = GetDlgItem(hDlg, IDCOMBO); 
                    if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                        SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                    else EndDialog(hDlg, 0); 
            } 
            break; 

    case WM_DESTROY:

        // Call the application-defined function to free the bitmap resources.
        DeleteIconBitmaps();
        break;
    }
    return (INT_PTR)FALSE;
}

// Loads string resources and adds them as items to the drop-down list of
//   the food groups combo box. The bitmap handle of each item&#39;s icon is
//   stored as item data for easy access when the item needs to be drawn.
// 
void InitGroupList(HWND hDlg)
{
    TCHAR achTemp[256];
    DWORD dwIndex;

    // Get the handle of the food groups combo box.
    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);

    LoadString(hInst, IDS_BREAD, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmBread);
    
    LoadString(hInst, IDS_DAIRY, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmDairy);

    LoadString(hInst, IDS_FRUIT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmFruit); 

    LoadString(hInst, IDS_MEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmMeat);

    return;
}

// Fills the food list based on the selected item in the food groups
//   combo box.
void InitFoodList(HWND hDlg)
{
    TCHAR achTemp[256];

    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);
    HWND hwndFoodList = GetDlgItem(hDlg, IDLIST);

    // Clear the list contents.
    SendMessage(hwndFoodList, LB_RESETCONTENT, 0, 0);

    // Find out which food group is selected.
    int idFoodGroup = SendMessage(hwndGroupsBox, CB_GETCURSEL, 0, 0);

    switch (idFoodGroup)
    {
    case ID_BREAD:
        LoadString(hInst, IDS_OAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_WHEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_RYE, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        break;

    case ID_DAIRY:
        LoadString(hInst, IDS_CHEDDAR, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_MILK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PROCESSED, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_SWISS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        
        break;

    case ID_FRUIT:
        LoadString(hInst, IDS_APPLES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_BANANAS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_ORANGES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    case ID_MEAT:
        LoadString(hInst, IDS_BEEF, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_CHICKEN, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PORK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    default:
        break;
    }

    return;
}

// Loads the food icon bitmaps from the application resources.
//
BOOL LoadIconBitmaps(void)
{
    hbmBread = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_BREAD));

    if (hbmBread != NULL)
         hbmDairy = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_DAIRY));

    if (hbmDairy != NULL)
         hbmMeat = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MEAT));

    if (hbmMeat != NULL)
        hbmFruit = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_FRUIT));
    
    if (hbmFruit != NULL)
        hbmMask = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MASK));

    if (hbmMask != NULL)
        return TRUE;
        
    return FALSE;
}

// Frees the icon bitmps.
//
void DeleteIconBitmaps(void)
{
    FreeResource(reinterpret_cast<HGLOBAL>(hbmBread));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmDairy));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMeat));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmFruit));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMask));
}
```


## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование полей со списком](using-combo-boxes.md)
</dt> </dl>

 

 