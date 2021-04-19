---
title: Обнаружение и отслеживание нескольких точек касания
description: Обнаружение и отслеживание нескольких точек касания
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Касание Windows, несколько точек касания
- Обнаружение нескольких точек касания
- Отслеживание нескольких точек касания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13b9eaf665b850eea8925bd531ffd1e9ec3fcf40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488052"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a>Обнаружение и отслеживание нескольких точек касания

Ниже описаны действия по отслеживанию нескольких сенсорных точек с помощью технологии Windows Touch.

1.  Создание приложения и включение технологии Windows Touch.
2.  Добавление обработчика для [**точек \_ касания**](wm-touchdown.md) и трассировки WM.
3.  Нарисуйте точки.

После запуска приложения он будет отображать круги при каждом касании. На следующем снимке экрана показано, как приложение может выглядеть во время работы.

![снимок экрана, показывающий приложение, которое отображает сенсорные точки как зеленые и желтые кружки](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a>Создание приложения и включение технологии Windows Touch

Начните работу с приложением Microsoft Win32 с помощью мастера Microsoft Visual Studio. После завершения работы мастера добавьте поддержку сообщений Touch Windows, задав версию Windows в targetver. h, включая Windows. h и виндовскс. h в приложении. В следующем коде показано, как задать версию Windows в targetver. h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows 7.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows 7.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif     

#ifndef _WIN32_WINDOWS          // Specifies that the minimum required platform is Windows 98.
#define _WIN32_WINDOWS 0x0410 // Change this to the appropriate value to target Windows Me or later.
#endif

#ifndef _WIN32_IE                       // Specifies that the minimum required platform is Internet Explorer 7.0.
#define _WIN32_IE 0x0700        // Change this to the appropriate value to target other versions of IE.
#endif
```



В следующем коде показано, как следует добавлять директивы include. Кроме того, можно создать некоторые глобальные переменные, которые будут использоваться позже.


```C++
#include <windows.h>    // included for Windows Touch
#include <windowsx.h>   // included for point conversion

#define MAXPOINTS 10

// You will use this array to track touch points
int points[MAXPOINTS][2];

// You will use this array to switch the color / track ids
int idLookup[MAXPOINTS];


// You can make the touch points larger
// by changing this radius value
static int radius      = 50;

// There should be at least as many colors
// as there can be touch points so that you
// can have different colors for each point
COLORREF colors[] = { RGB(153,255,51), 
                      RGB(153,0,0), 
                      RGB(0,153,0), 
                      RGB(255,255,0), 
                      RGB(255,51,204), 
                      RGB(0,0,0),
                      RGB(0,153,0), 
                      RGB(153, 255, 255), 
                      RGB(153,153,255), 
                      RGB(0,51,153)
                    };

```



## <a name="add-handler-for-wm_touch-and-track-points"></a>Добавление обработчика для \_ точек управления WM Touch и Track

Сначала объявите некоторые переменные, используемые обработчиком [**WM \_ Touch**](wm-touchdown.md) в [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



Теперь Инициализируйте переменные, используемые для хранения точек касания, и зарегистрируйте окно для сенсорного ввода из метода **InitInstance** .


```C++
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd) {
      return FALSE;
   }

   // register the window for touch instead of gestures
   RegisterTouchWindow(hWnd, 0);  

   // the following code initializes the points
   for (int i=0; i< MAXPOINTS; i++){
     points[i][0] = -1;
     points[i][1] = -1;
     idLookup[i]  = -1;
   }  

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



Затем обработайте сообщение [**WM \_ Touch**](wm-touchdown.md) из метода [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . В следующем коде показана реализация обработчика для **WM \_ Touch**.


```C++
case WM_TOUCH:        
  cInputs = LOWORD(wParam);
  pInputs = new TOUCHINPUT[cInputs];
  if (pInputs){
    if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
      for (int i=0; i < static_cast<INT>(cInputs); i++){
        TOUCHINPUT ti = pInputs[i];
        index = GetContactIndex(ti.dwID);
        if (ti.dwID != 0 && index < MAXPOINTS){                            
          // Do something with your touch input handle
          ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
          ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
          ScreenToClient(hWnd, &ptInput);
          
          if (ti.dwFlags & TOUCHEVENTF_UP){                      
            points[index][0] = -1;
            points[index][1] = -1;                
          }else{
            points[index][0] = ptInput.x;
            points[index][1] = ptInput.y;                
          }
        }
      }
    }
    // If you handled the message and don't want anything else done with it, you can close it
    CloseTouchInputHandle((HTOUCHINPUT)lParam);
    delete [] pInputs;
  }else{
    // Handle the error here 
  }  
```



> [!Note]  
> Чтобы использовать функцию [**скринтоклиент**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , в приложении должна быть поддержка высокого разрешения. Дополнительные сведения о поддержке высокого DPI см. в разделе о [высоком уровне dpi]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) в MSDN.

 

Теперь, когда пользователь касается экрана, позиции, на которые он или она касается, будут храниться в массиве points. Элемент **ДВИД** структуры [**таучинпут**](/windows/win32/api/winuser/ns-winuser-touchinput) хранит идентификатор, который будет аппаратно зависимым.

Чтобы устранить проблемы, связанные с тем, что член ДВИД зависит от оборудования, обработчик вариантов [**\_ касания WM**](wm-touchdown.md) использует функцию **жетконтактиндекс**, которая сопоставляет элемент **ДВИД** структуры [**таучинпут**](/windows/win32/api/winuser/ns-winuser-touchinput) с точкой, отображаемой на экране. В следующем коде показана реализация этой функции.


```C++
// This function is used to return an index given an ID
int GetContactIndex(int dwID){
  for (int i=0; i < MAXPOINTS; i++){
    if (idLookup[i] == -1){
      idLookup[i] = dwID;
      return i;
    }else{
      if (idLookup[i] == dwID){
        return i;
      }
    }
  }
  // Out of contacts
  return -1;
}
```



## <a name="draw-the-points"></a>Рисование точек

Объявите следующие переменные для подпрограммы рисования.


```C++
    // For double buffering
    static HDC memDC       = 0;
    static HBITMAP hMemBmp = 0;
    HBITMAP hOldBmp        = 0;
   
    // For drawing / fills
    PAINTSTRUCT ps;
    HDC hdc;
    
    // For tracking dwId to points
    int index;
```



Контекст отображения памяти *мемдк* используется для хранения временного графического контекста, который перемещается с отображаемым контекстом отображения, *HDC*, чтобы устранить мерцание. Реализуйте подпрограммы рисования, которая принимает точки, которые вы сохранили, и рисует окружность в точках. В следующем коде показано, как можно реализовать обработчик [**\_ рисования WM**](/windows/desktop/gdi/wm-paint) .


```C++
  case WM_PAINT:
    hdc = BeginPaint(hWnd, &ps);    
    RECT client;
    GetClientRect(hWnd, &client);        
  
    // start double buffering
    if (!memDC){
      memDC = CreateCompatibleDC(hdc);
    }
    hMemBmp = CreateCompatibleBitmap(hdc, client.right, client.bottom);
    hOldBmp = (HBITMAP)SelectObject(memDC, hMemBmp);          
  
    FillRect(memDC, &client, CreateSolidBrush(RGB(255,255,255)));
     
    //Draw Touched Points                
    for (i=0; i < MAXPOINTS; i++){        
      SelectObject( memDC, CreateSolidBrush(colors[i]));           
      x = points[i][0];
      y = points[i][1];
      if  (x >0 && y>0){              
        Ellipse(memDC, x - radius, y - radius, x+ radius, y + radius);
      }
    }
  
    BitBlt(hdc, 0,0, client.right, client.bottom, memDC, 0,0, SRCCOPY);      

    EndPaint(hWnd, &ps);
    break;
```



После запуска приложения в начале этого раздела он должен выглядеть примерно так, как показано на рисунке.

Для развлечения можно нарисовать несколько дополнительных линий вокруг точек касания. На следующем снимке экрана показано, как может выглядеть приложение с помощью нескольких дополнительных линий, нарисованных вокруг кругов.

![снимок экрана, показывающий приложение, которое отображает сенсорные точки как круги с линиями через центры и пересекающиеся края точек касания](images/multitouchpointsfun.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сенсорный ввод Windows](guide-multi-touch-input.md)
</dt> </dl>

 

 