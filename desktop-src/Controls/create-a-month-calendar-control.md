---
title: Создание элемента управления "месячный календарь"
description: В этом разделе показано, как динамически создать элемент управления "месячный календарь" с помощью функции CreateWindowEx.
ms.assetid: 35ADDA85-5D7D-46F4-A637-99FEE4592B3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f3824618e9801b68eb67b13c64c638a5057481
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797335"
---
# <a name="how-to-create-a-month-calendar-control"></a>Создание элемента управления "месячный календарь"

В этом разделе показано, как динамически создать элемент управления "месячный календарь" с помощью функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции


Чтобы создать элемент управления "месячный календарь", используйте функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указав [**\_ класс монскал**](common-control-window-classes.md) в качестве класса Window. Сначала необходимо зарегистрировать класс окна, вызвав функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , указав бит ICC для **\_ \_ классов даты** в сопутствующей структуре [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .

В следующем примере показано, как создать элемент управления "месячный календарь" в существующем немодальном диалоговом окне. Обратите внимание, что значения размера, передаваемые в [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , являются нулями. Поскольку минимальный требуемый размер зависит от шрифта, используемого элементом управления, в примере используется макрос [**монскал \_ жетминрекрект**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) для запроса сведений о размере, а затем изменяется размер элемента управления путем вызова [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Если впоследствии изменить шрифт с помощью [**WM \_ сетфонт**](/windows/desktop/winmsg/wm-setfont), размеры элемента управления не изменятся. Необходимо снова вызвать **монскал \_ жетминрекрект** и изменить размер элемента управления в соответствии с новым шрифтом.



```C++
// Child window identifier of the month calendar.
#define IDC_MONTHCAL 101

// Symbols used by SetWindowPos function (arbitrary values).
#define LEFT 35
#define TOP  40

// Description:
//   Creates a month calendar control in a dialog box.  
// Parameters:
//   hwndOwner - handle of the owner window.
// Nonlocal variables:
//   MonthCalDlgProc - window procedure of the dialog box that 
//     contains the month calendar.
//   g_hInst - global instance handle.
//
HRESULT CreateMonthCalDialog(HWND hwndOwner)
{
    RECT rc;
    INITCOMMONCONTROLSEX icex;
    HWND hwndDlg = NULL;
    HWND hwndMonthCal = NULL;

    // Return an error code if the owner handle is invalid.
    if (hwndOwner == NULL)
        return E_INVALIDARG;

    // Load the window class.
    icex.dwSize = sizeof(icex);
    icex.dwICC  = ICC_DATE_CLASSES;
    InitCommonControlsEx(&icex);

    // Create a modeless dialog box to hold the control.
    hwndDlg = CreateDialog(g_hInst,
                    MAKEINTRESOURCE(IDD_DATE_PICKER),
                    hwndOwner,
                    MonthCalDlgProc);
   
    // Return if creating the dialog box failed. 
    if (hwndDlg == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                        
    // Create the month calendar.
    hwndMonthCal  = CreateWindowEx(0,
                    MONTHCAL_CLASS,
                    L"",
                    WS_BORDER | WS_CHILD | WS_VISIBLE | MCS_DAYSTATE,
                    0,0,0,0, // resize it later
                    hwndDlg,
                    (HMENU) IDC_MONTHCAL,
                    g_hInst,
                    NULL);

    // Return if creating the month calendar failed. 
    if (hwndMonthCal == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                     
    // Get the size required to show an entire month.
    MonthCal_GetMinReqRect(hwndMonthCal, &rc);

    // Resize the control now that the size values have been obtained.
    SetWindowPos(hwndMonthCal, NULL, LEFT, TOP, 
        rc.right, rc.bottom, SWP_NOZORDER);

    // Set the calendar to the annual view.
    MonthCal_SetCurrentView(hwndMonthCal, MCMV_YEAR);

    // Make the window visible.
    ShowWindow(hwndDlg, SW_SHOW);

    return S_OK;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по управлению календарем месяца](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Элементы управления "календарь месяца"](month-calendar-controls.md)
</dt> <dt>

[Использование элементов управления "календарь месяца"](using-month-calendar-controls.md)
</dt> </dl>

 

 