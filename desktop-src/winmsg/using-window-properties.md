---
description: В этом разделе объясняется, как выполнять следующие задачи, связанные со свойствами окна.
ms.assetid: cdf196ec-300c-4c7b-8a4f-68088c4a2507
title: Использование свойств окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 736682eb34191a061aa9753ef9d5e8c7e366fbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105711974"
---
# <a name="using-window-properties"></a>Использование свойств окна

В этом разделе объясняется, как выполнять следующие задачи, связанные со свойствами окна.

-   [Добавление свойства окна](#adding-a-window-property)
-   [Получение свойства окна](#retrieving-a-window-property)
-   [Свойства окна списка для заданного окна](#listing-window-properties-for-a-given-window)
-   [Удаление свойства окна](#deleting-a-window-property)

## <a name="adding-a-window-property"></a>Добавление свойства окна

В следующем примере загружается значок, а затем курсор и выделяется память для буфера. Затем в примере используется функция [**сбой setprop**](/windows/win32/api/winuser/nf-winuser-setpropa) для присвоения результирующего значка, курсора и дескрипторов памяти в качестве свойств окна, определяемого определяемой приложением переменной хвндсубкласс. Свойства определяются значком PROP строки, параметром prop \_ \_ и \_ буфером prop.


```
#define BUFFER 4096 
 
HINSTANCE hinst;       // handle of current instance 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIcon, hCursor; 
HGLOBAL hMem; 
char *lpMem; 
TCHAR tchPath[] = "c:\\winnt\\samples\\winprop.c";
HRESULT hResult; 
 
// Load resources. 
 
hIcon = LoadIcon(hinst, MAKEINTRESOURCE(400)); 
hCursor = LoadCursor(hinst, MAKEINTRESOURCE(220)); 
 
// Allocate and fill a memory buffer. 
 
hMem = GlobalAlloc(GPTR, BUFFER); 
lpMem = GlobalLock(hMem);
if (lpMem == NULL)
{
// TODO: write error handler
}
hResult = StringCchCopy(lpMem, STRSAFE_MAX_CCH, tchPath);
if (FAILED(hResult))
{
// TO DO: write error handler if function fails.
} 
GlobalUnlock(hMem); 
 
// Set the window properties for hwndSubclass. 
 
SetProp(hwndSubclass, "PROP_ICON", hIcon); 
SetProp(hwndSubclass, "PROP_CURSOR", hCursor); 
SetProp(hwndSubclass, "PROP_BUFFER", hMem); 
```



## <a name="retrieving-a-window-property"></a>Получение свойства окна

Окно может создавать дескрипторы для данных свойств окна и использовать данные для любых целей. В следующем примере используется функция " [**предл**](/windows/win32/api/winuser/nf-winuser-getpropa) " для получения дескрипторов свойств окна, определенных \_ значком Prop, Prop \_ cursor и \_ buffer prop. В примере отображается содержимое только что полученного буфера памяти, курсора и значка в клиентской области окна.


```
#define PATHLENGTH 256 
 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIconProp, hCursProp; 
HGLOBAL hMemProp; 
char *lpFilename; 
TCHAR tchBuffer[PATHLENGTH]; 
size_t * nSize; 
HDC hdc;
HRESULT hResult; 
 
// Get the window properties, then use the data. 
 
hIconProp = (HICON) GetProp(hwndSubclass, "PROP_ICON"); 
TextOut(hdc, 10, 40, "PROP_ICON", 9); 
DrawIcon(hdc, 90, 40, hIconProp); 
 
hCursProp = (HCURSOR) GetProp(hwndSubclass, "PROP_CURSOR"); 
TextOut(hdc, 10, 85, "PROP_CURSOR", 9); 
DrawIcon(hdc, 110, 85, hCursProp); 
 
hMemProp = (HGLOBAL) GetProp(hwndSubclass, "PROP_BUFFER"); 
lpFilename = GlobalLock(hMemProp);
hResult = StringCchPrintf(tchBuffer, PATHLENGTH, 
    "Path to file:  %s", lpFilename);
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
hResult = StringCchLength(tchBuffer, PATHLENGTH, nSize)
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
TextOut(hdc, 10, 10, tchBuffer, *nSize); 
```



## <a name="listing-window-properties-for-a-given-window"></a>Свойства окна списка для заданного окна

В следующем примере функция [**енумпропсекс**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) перечисляет идентификаторы строк свойств окна для окна, определяемого определяемой приложением переменной хвндсубкласс. Эта функция использует определяемую приложением функцию обратного вызова Винпроппрок для вывода строк в клиентской области окна.


```
EnumPropsEx(hwndSubclass, WinPropProc, NULL); 
 
// WinPropProc is an application-defined callback function 
// that lists a window property. 
 
BOOL CALLBACK WinPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    static int nProp = 1;    // property counter 
    TCHAR tchBuffer[BUFFER]; // expanded-string buffer 
    size_t * nSize;          // size of string in buffer 
    HDC hdc;                 // device-context handle
    HRESULT hResult; 
 
    hdc = GetDC(hwndSubclass); 
 
    // Display window property string in client area.
    hResult = StringCchPrintf(tchBuffer, BUFFER, "WinProp %d:  %s", nProp++, lpszString);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    }
    hResult = StringCchLength(tchBuffer, BUFFER, nSize);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    } 
    TextOut(hdc, 10, nProp * 20, tchBuffer, *nSize); 
 
    ReleaseDC(hwndSubclass, hdc); 
 
    return TRUE; 
} 
```



## <a name="deleting-a-window-property"></a>Удаление свойства окна

При уничтожении окна оно должно уничтожить все заданные свойства окна. В следующем примере используется функция [**енумпропсекс**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) и определяемая приложением функция обратного вызова делпроппрок для уничтожения свойств, связанных с окном, определяемым определяемой приложением переменной хвндсубкласс. Также показана функция обратного вызова, которая использует функцию [**ремовепроп**](/windows/win32/api/winuser/nf-winuser-removepropa) .


```
case WM_DESTROY: 
 
    EnumPropsEx(hwndSubclass, DelPropProc, NULL); 
 
    PostQuitMessage(0); 
    break; 
 
// DelPropProc is an application-defined callback function 
// that deletes a window property. 
 
BOOL CALLBACK DelPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    hData = RemoveProp(hwndSubclass, lpszString); 
//
// if appropriate, free the handle hData
//
 
    return TRUE; 
}
```



 

 
