---
description: Кисть можно использовать для заполнения внутренней части практически любой фигуры с помощью функции интерфейса графических устройств (GDI).
ms.assetid: 64cd6e82-7a0d-4b5e-b491-450f37eea43a
title: Использование кистей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42e09dc5731ceba7961dfd66b296df531897f2915cff53ccdacf1b5b5740160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037502"
---
# <a name="using-brushes"></a>Использование кистей

Кисть можно использовать для заполнения внутренней части практически любой фигуры с помощью функции интерфейса графических устройств (GDI). Сюда входят внутренние области прямоугольников, эллипсов, многоугольников и контуров. В зависимости от требований приложения можно использовать сплошную кисть указанного цвета, геокисть, кисть штриховки или узорную кисть.

Этот раздел содержит примеры кода, демонстрирующие создание настраиваемых диалоговое окно кистью. Диалоговое окно содержит сетку, представляющую точечный рисунок, который система использует в качестве кисти. Пользователь может использовать эту сетку для создания точечного рисунка узорной кисти, а затем просмотреть пользовательский шаблон, нажав кнопку **тест шаблона** .

На следующем рисунке показан шаблон, созданный с помощью диалогового окна **Настраиваемая кисть** .

![снимок экрана диалогового окна "Настраиваемая кисть"](images/custbrush.png)

Чтобы отобразить диалоговое окно, необходимо сначала создать шаблон диалогового окна. В следующем шаблоне диалогового окна определяется диалоговое окно **Пользовательская кисть** .


```C++
CustBrush DIALOG 6, 18, 160, 118 
STYLE WS_DLGFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Custom Brush" 
FONT 8, "MS Sans Serif" 
BEGIN 
    CONTROL         "", IDD_GRID, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 3, 2, 83, 79 
    CONTROL         "", IDD_RECT, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 96, 11, 57, 28 
    PUSHBUTTON      "Test Pattern", IDD_PAINTRECT, 96, 47, 57, 14 
    PUSHBUTTON      "OK", IDD_OK, 29, 98, 40, 14 
    PUSHBUTTON      "Cancel", IDD_CANCEL, 92, 98, 40, 14 
END 
```



Диалоговое окно **Настраиваемая кисть** содержит пять элементов управления: окно точечного рисунка, окно просмотра узоров и три кнопки, помеченные как **шаблон тестирования**, **ОК** и **Отмена**. Кнопка **тестового шаблона** позволяет пользователю просмотреть шаблон. Шаблон диалогового окна задает общие размеры окна диалогового окна, присваивает значение каждому элементу управления, задает расположение каждого элемента управления и т. д. Дополнительные сведения см. в разделе [диалоговые окна](../dlgbox/dialog-boxes.md).

Значения элементов управления в шаблоне диалогового окна являются константами, которые были определены в файле заголовка приложения следующим образом.


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



После создания шаблона диалогового окна и включения его в файл определения ресурсов приложения необходимо написать процедуру диалогового окна. Эта процедура обрабатывает сообщения, которые система отправляет в диалоговое окно. В следующем фрагменте исходного кода приложения показана процедура диалогового окна для диалогового окна **Пользовательская кисть** и две определяемые приложением функции, которые она вызывает.


```C++
BOOL CALLBACK BrushDlgProc( HWND hdlg, UINT message, LONG wParam, 
                            LONG lParam) 
{ 
    static HWND hwndGrid;       // grid-window control  
    static HWND hwndBrush;      // pattern-brush control  
    static RECT rctGrid;        // grid-window rectangle  
    static RECT rctBrush;       // pattern-brush rectangle  
    static UINT bBrushBits[8];  // bitmap bits  
    static RECT rect[64];       // grid-cell array  
    static HBITMAP hbm;         // bitmap handle  
    HBRUSH hbrush;              // current brush  
    HBRUSH hbrushOld;           // default brush  
    HRGN hrgnCell;              // test-region handle  
    HDC hdc;                    // device context (DC) handle  
    int x, y, deltaX, deltaY;   // drawing coordinates  
    POINTS ptlHit;              // mouse coordinates  
    int i;                      // count variable  
 
    switch (message) 
        { 
        case WM_INITDIALOG: 
 
            // Retrieve a window handle for the grid-window and  
            // pattern-brush controls.  
 
            hwndGrid = GetDlgItem(hdlg, IDD_GRID); 
            hwndBrush = GetDlgItem(hdlg, IDD_RECT); 
 
            // Initialize the array of bits that defines the  
            // custom brush pattern with the value 1 to produce a  
            // solid white brush.  

            for (i=0; i<8; i++) 
                bBrushBits[i] = 0xFF; 
 
            // Retrieve dimensions for the grid-window and pattern- 
            // brush controls.  
 
            GetClientRect(hwndGrid, &rctGrid); 
            GetClientRect(hwndBrush, &rctBrush); 
 
            // Determine the width and height of a single cell.  
 
            deltaX = (rctGrid.right - rctGrid.left)/8; 
            deltaY = (rctGrid.bottom - rctGrid.top)/8; 
 
            // Initialize the array of cell rectangles.  
 
            for (y=rctGrid.top, i=0; y < rctGrid.bottom; y += deltaY)
            { 
                for(x=rctGrid.left; x < (rctGrid.right - 8) && i < 64; 
                        x += deltaX, i++) 
                { 
                    rect[i].left = x; rect[i].top = y; 
                    rect[i].right = x + deltaX; 
                    rect[i].bottom = y + deltaY; 
                } 
            } 
            return FALSE; 
 
 
        case WM_PAINT: 

            // Draw the grid.  
 
            hdc = GetDC(hwndGrid); 
 
            for (i=rctGrid.left; i<rctGrid.right; 
                 i+=(rctGrid.right - rctGrid.left)/8)
            { 
                 MoveToEx(hdc, i, rctGrid.top, NULL); 
                 LineTo(hdc, i, rctGrid.bottom); 
            } 
            for (i=rctGrid.top; i<rctGrid.bottom; 
                 i+=(rctGrid.bottom - rctGrid.top)/8)
            { 
                 MoveToEx(hdc, rctGrid.left, i, NULL); 
                 LineTo(hdc, rctGrid.right, i); 
            } 
            ReleaseDC(hwndGrid, hdc); 
            return FALSE; 
 
 
        case WM_LBUTTONDOWN: 
 
            // Store the mouse coordinates in a POINT structure.  
 
            ptlHit = MAKEPOINTS((POINTS FAR *)lParam); 
 
            // Create a rectangular region with dimensions and  
            // coordinates that correspond to those of the grid  
            // window.  
 
            hrgnCell = CreateRectRgn(rctGrid.left, rctGrid.top, 
                        rctGrid.right, rctGrid.bottom); 
 
            // Retrieve a window DC for the grid window.  
 
            hdc = GetDC(hwndGrid); 
 
            // Select the region into the DC.  
 
            SelectObject(hdc, hrgnCell); 
 
            // Test for a button click in the grid-window rectangle.  
 
            if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
            { 
                // A button click occurred in the grid-window  
                // rectangle; isolate the cell in which it occurred.  
 
                for(i=0; i<64; i++)
                { 
                    DeleteObject(hrgnCell); 
 
                    hrgnCell = CreateRectRgn(rect[i].left,  
                               rect[i].top, 
                               rect[i].right, rect[i].bottom); 
 
                    if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
                    { 
                        InvertRgn(hdc, hrgnCell); 
 
                        // Set the appropriate brush bits.  
 
                         if (i % 8 == 0) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x80; 
                         else if (i % 8 == 1) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x40; 
                         else if (i % 8 == 2) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x20; 
                         else if (i % 8 == 3) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x10; 
                         else if (i % 8 == 4) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x08; 
                         else if (i % 8 == 5) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x04; 
                         else if (i % 8 == 6) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x02; 
                         else if (i % 8 == 7) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x01; 
 
                      // Exit the "for" loop after the bit is set.  
 
                         break; 
                    } // end if  
 
                } // end for  
 
            } // end if  
 
            // Release the DC for the control.  
 
            ReleaseDC(hwndGrid, hdc); 
            return TRUE; 
 
 
        case WM_COMMAND: 
            switch (wParam)
            { 
               case IDD_PAINTRECT: 
 
                    hdc = GetDC(hwndBrush); 
 
                    // Create a monochrome bitmap.  
 
                    hbm = CreateBitmap(8, 8, 1, 1, 
                          (LPBYTE)bBrushBits); 
 
                    // Select the custom brush into the DC.  
 
                    hbrush = CreatePatternBrush(hbm); 
 
                    hbrushOld = SelectObject(hdc, hbrush); 
 
                    // Use the custom brush to fill the rectangle.  
 
                    Rectangle(hdc, rctBrush.left, rctBrush.top, 
                              rctBrush.right, rctBrush.bottom); 
 
                    // Clean up memory.  
                    SelectObject(hdc, hbrushOld); 
                    DeleteObject(hbrush); 
                    DeleteObject(hbm); 
 
                    ReleaseDC(hwndBrush, hdc); 
                    return TRUE; 
 
                case IDD_OK: 
 
                case IDD_CANCEL: 
                    EndDialog(hdlg, TRUE); 
                    return TRUE; 
 
            } // end switch  
            break; 
        default: 
            return FALSE; 
        } 
} 
 
 
int GetStrLngth(LPTSTR cArray) 
{ 
    int i = 0; 
 
    while (cArray[i++] != 0); 
    return i-1; 
 
} 
 
DWORD RetrieveWidth(LPTSTR cArray, int iLength) 
{ 
    int i, iTmp; 
    double dVal, dCount; 
 
    dVal = 0.0; 
    dCount = (double)(iLength-1); 
    for (i=0; i<iLength; i++)
    { 
        iTmp = cArray[i] - 0x30; 
        dVal = dVal + (((double)iTmp) * pow(10.0, dCount--)); 
    } 
 
    return (DWORD)dVal; 
} 
```



Процедура диалогового окна " **Пользовательская кисть** " обрабатывает четыре сообщения, как описано в следующей таблице.



| Message                                          | Действие                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md)   | Извлекает дескриптор окна и измерения для элементов управления "Сетка-окно" и "шаблон-кисть", вычисляет размеры отдельной ячейки в элементе управления "окно сетки" и инициализирует массив координат сетки-ячеек.                                                                                           |
| [**WM \_ Paint**](wm-paint.md)                    | Рисует шаблон сетки в элементе управления "окно сетки".                                                                                                                                                                                                                                                         |
| [**WM \_ лбуттондовн**](../inputdev/wm-lbuttondown.md) | Определяет, находится ли курсор в элементе управления "окно сетки" при нажатии пользователем левой кнопки мыши. В этом случае процедура диалогового окна инвертирует соответствующую ячейку сетки и записывает состояние этой ячейки в массиве битов, который используется для создания точечного рисунка для пользовательской кисти.              |
| [**\_команда WM**](../menurc/wm-command.md)         | Обрабатывает входные данные для трех элементов управления "Кнопка". Если пользователь нажимает кнопку **тестового шаблона** , процедура диалогового окна закрашивает элемент управления шаблоном тестирования новым пользовательским шаблоном кисти. Если пользователь нажмет кнопку **ОК** или **Отмена** , процедура диалогового окна выполняет соответствующие действия. |



 

Дополнительные сведения о сообщениях и обработке сообщений см. в разделе [сообщения и очереди сообщений](../winmsg/messages-and-message-queues.md).

После того как вы напишете процедуру диалогового окна, включите определение функции в файл заголовка приложения, а затем вызовите процедуру диалогового окна в соответствующей точке приложения.

В следующем фрагменте из файла заголовка приложения показано определение функции для процедуры диалогового окна и две функции, которые она вызывает.


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



Наконец, в следующем коде показано, как процедура диалогового окна вызывается из файла исходного кода приложения.


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



Этот вызов обычно выполняется в ответ на выбор пользователем параметра в меню приложения.

 

 
