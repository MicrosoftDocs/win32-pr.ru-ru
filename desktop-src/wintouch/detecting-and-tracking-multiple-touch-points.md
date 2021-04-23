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
# <a name="detecting-and-tracking-multiple-touch-points"></a><span data-ttu-id="7d9f0-106">Обнаружение и отслеживание нескольких точек касания</span><span class="sxs-lookup"><span data-stu-id="7d9f0-106">Detecting and Tracking Multiple Touch Points</span></span>

<span data-ttu-id="7d9f0-107">Ниже описаны действия по отслеживанию нескольких сенсорных точек с помощью технологии Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-107">The following steps explain how to track multiple touch points using Windows Touch.</span></span>

1.  <span data-ttu-id="7d9f0-108">Создание приложения и включение технологии Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-108">Create an application and enable Windows Touch.</span></span>
2.  <span data-ttu-id="7d9f0-109">Добавление обработчика для [**точек \_ касания**](wm-touchdown.md) и трассировки WM.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-109">Add a handler for [**WM\_TOUCH**](wm-touchdown.md) and track points.</span></span>
3.  <span data-ttu-id="7d9f0-110">Нарисуйте точки.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-110">Draw the points.</span></span>

<span data-ttu-id="7d9f0-111">После запуска приложения он будет отображать круги при каждом касании.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-111">After you have your application running, it will render circles under each touch.</span></span> <span data-ttu-id="7d9f0-112">На следующем снимке экрана показано, как приложение может выглядеть во время работы.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-112">The following screen shot shows how your application might look while running.</span></span>

![снимок экрана, показывающий приложение, которое отображает сенсорные точки как зеленые и желтые кружки](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a><span data-ttu-id="7d9f0-114">Создание приложения и включение технологии Windows Touch</span><span class="sxs-lookup"><span data-stu-id="7d9f0-114">Create an Application and Enable Windows Touch</span></span>

<span data-ttu-id="7d9f0-115">Начните работу с приложением Microsoft Win32 с помощью мастера Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-115">Start with a Microsoft Win32 application using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="7d9f0-116">После завершения работы мастера добавьте поддержку сообщений Touch Windows, задав версию Windows в targetver. h, включая Windows. h и виндовскс. h в приложении.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-116">After you have completed the wizard, add support for Windows Touch messages by setting the Windows version in targetver.h and including windows.h and windowsx.h in your application.</span></span> <span data-ttu-id="7d9f0-117">В следующем коде показано, как задать версию Windows в targetver. h.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-117">The following code shows how to set the Windows version in targetver.h.</span></span>


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



<span data-ttu-id="7d9f0-118">В следующем коде показано, как следует добавлять директивы include.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-118">The following code shows how your include directives should be added.</span></span> <span data-ttu-id="7d9f0-119">Кроме того, можно создать некоторые глобальные переменные, которые будут использоваться позже.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-119">Also, you can create some global variables that will be used later.</span></span>


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



## <a name="add-handler-for-wm_touch-and-track-points"></a><span data-ttu-id="7d9f0-120">Добавление обработчика для \_ точек управления WM Touch и Track</span><span class="sxs-lookup"><span data-stu-id="7d9f0-120">Add Handler for WM\_TOUCH and Track Points</span></span>

<span data-ttu-id="7d9f0-121">Сначала объявите некоторые переменные, используемые обработчиком [**WM \_ Touch**](wm-touchdown.md) в [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d9f0-121">First, declare some variables that are used by the [**WM\_TOUCH**](wm-touchdown.md) handler in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span></span>


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



<span data-ttu-id="7d9f0-122">Теперь Инициализируйте переменные, используемые для хранения точек касания, и зарегистрируйте окно для сенсорного ввода из метода **InitInstance** .</span><span class="sxs-lookup"><span data-stu-id="7d9f0-122">Now, initialize the variables used for storing touch points and register the window for touch input from the **InitInstance** method.</span></span>


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



<span data-ttu-id="7d9f0-123">Затем обработайте сообщение [**WM \_ Touch**](wm-touchdown.md) из метода [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7d9f0-123">Next, handle the [**WM\_TOUCH**](wm-touchdown.md) message from the [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) method.</span></span> <span data-ttu-id="7d9f0-124">В следующем коде показана реализация обработчика для **WM \_ Touch**.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-124">The following code shows an implementation of the handler for **WM\_TOUCH**.</span></span>


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
> <span data-ttu-id="7d9f0-125">Чтобы использовать функцию [**скринтоклиент**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , в приложении должна быть поддержка высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-125">In order to use the [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) function, you must have high DPI support in your application.</span></span> <span data-ttu-id="7d9f0-126">Дополнительные сведения о поддержке высокого DPI см. в разделе о [высоком уровне dpi]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) в MSDN.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-126">For more information on supporting high DPI, see the [High DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) section of MSDN.</span></span>

 

<span data-ttu-id="7d9f0-127">Теперь, когда пользователь касается экрана, позиции, на которые он или она касается, будут храниться в массиве points.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-127">Now when a user touches the screen, the positions that he or she is touching will be stored in the points array.</span></span> <span data-ttu-id="7d9f0-128">Элемент **ДВИД** структуры [**таучинпут**](/windows/win32/api/winuser/ns-winuser-touchinput) хранит идентификатор, который будет аппаратно зависимым.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-128">The **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure stores an identifier that will be hardware dependent.</span></span>

<span data-ttu-id="7d9f0-129">Чтобы устранить проблемы, связанные с тем, что член ДВИД зависит от оборудования, обработчик вариантов [**\_ касания WM**](wm-touchdown.md) использует функцию **жетконтактиндекс**, которая сопоставляет элемент **ДВИД** структуры [**таучинпут**](/windows/win32/api/winuser/ns-winuser-touchinput) с точкой, отображаемой на экране.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-129">To address the issue of the dwID member being dependent on hardware, the [**WM\_TOUCH**](wm-touchdown.md) case handler uses a function, **GetContactIndex**, that maps the **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure to a point that is drawn on the screen.</span></span> <span data-ttu-id="7d9f0-130">В следующем коде показана реализация этой функции.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-130">The following code shows an implementation of this function.</span></span>


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



## <a name="draw-the-points"></a><span data-ttu-id="7d9f0-131">Рисование точек</span><span class="sxs-lookup"><span data-stu-id="7d9f0-131">Draw the Points</span></span>

<span data-ttu-id="7d9f0-132">Объявите следующие переменные для подпрограммы рисования.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-132">Declare the following variables for the drawing routine.</span></span>


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



<span data-ttu-id="7d9f0-133">Контекст отображения памяти *мемдк* используется для хранения временного графического контекста, который перемещается с отображаемым контекстом отображения, *HDC*, чтобы устранить мерцание.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-133">The memory display context *memDC* is used for storing a temporary graphics context that is swapped with the rendered display context, *hdc*, to eliminate flickering.</span></span> <span data-ttu-id="7d9f0-134">Реализуйте подпрограммы рисования, которая принимает точки, которые вы сохранили, и рисует окружность в точках.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-134">Implement the drawing routine, which takes the points you have stored and draws a circle at the points.</span></span> <span data-ttu-id="7d9f0-135">В следующем коде показано, как можно реализовать обработчик [**\_ рисования WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="7d9f0-135">The following code shows how you could implement the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) handler.</span></span>


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



<span data-ttu-id="7d9f0-136">После запуска приложения в начале этого раздела он должен выглядеть примерно так, как показано на рисунке.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-136">When you run your application, it now should look something like the illustration at the beginning of this section.</span></span>

<span data-ttu-id="7d9f0-137">Для развлечения можно нарисовать несколько дополнительных линий вокруг точек касания.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-137">For fun, you can draw some extra lines around the touch points.</span></span> <span data-ttu-id="7d9f0-138">На следующем снимке экрана показано, как может выглядеть приложение с помощью нескольких дополнительных линий, нарисованных вокруг кругов.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-138">The following screen shot shows how the application could look with a few extra lines drawn around the circles.</span></span>

![снимок экрана, показывающий приложение, которое отображает сенсорные точки как круги с линиями через центры и пересекающиеся края точек касания](images/multitouchpointsfun.png)

## <a name="related-topics"></a><span data-ttu-id="7d9f0-140">См. также</span><span class="sxs-lookup"><span data-stu-id="7d9f0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d9f0-141">Сенсорный ввод Windows</span><span class="sxs-lookup"><span data-stu-id="7d9f0-141">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 