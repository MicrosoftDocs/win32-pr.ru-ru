---
description: В этом разделе показано, как нарисовать линию с помощью GDI и.
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: Рисование линии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5284a178baab624633dd427cad84b35933a72fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985184"
---
# <a name="drawing-a-line"></a><span data-ttu-id="8a1d3-103">Рисование линии</span><span class="sxs-lookup"><span data-stu-id="8a1d3-103">Drawing a Line</span></span>

<span data-ttu-id="8a1d3-104">В этом разделе показано, как нарисовать линию с помощью GDI и.</span><span class="sxs-lookup"><span data-stu-id="8a1d3-104">This topic demonstrates how to draw a line using GDI Plus.</span></span>

<span data-ttu-id="8a1d3-105">Для рисования линии в Windows GDI+ необходим [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект, объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) и объект [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="8a1d3-105">To draw a line in Windows GDI+ you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="8a1d3-106">Объект **Graphics** предоставляет метод [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) , а объект **Pen** содержит атрибуты линии, такие как цвет и ширина.</span><span class="sxs-lookup"><span data-stu-id="8a1d3-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object holds attributes of the line, such as color and width.</span></span> <span data-ttu-id="8a1d3-107">Адрес объекта **Pen** передается в качестве аргумента в метод **DrawLine** .</span><span class="sxs-lookup"><span data-stu-id="8a1d3-107">The address of the **Pen** object is passed as an argument to the **DrawLine** method.</span></span>

<span data-ttu-id="8a1d3-108">Следующая программа, которая рисует строку от (0, 0) до (200, 100), состоит из трех функций: **WinMain**, **WndProc** и **onpain**.</span><span class="sxs-lookup"><span data-stu-id="8a1d3-108">The following program, which draws a line from (0, 0) to (200, 100), consists of three functions: **WinMain**, **WndProc**, and **OnPaint**.</span></span> <span data-ttu-id="8a1d3-109">Функции **WinMain** и **WndProc** предоставляют фундаментальный код, который является общим для большинства приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="8a1d3-109">The **WinMain** and **WndProc** functions provide the fundamental code common to most Windows applications.</span></span> <span data-ttu-id="8a1d3-110">В функции **WndProc** отсутствует код GDI+.</span><span class="sxs-lookup"><span data-stu-id="8a1d3-110">There is no GDI+ code in the **WndProc** function.</span></span> <span data-ttu-id="8a1d3-111">Функция **WinMain** имеет небольшой объем кода GDI+, а именно, необходимые вызовы [**гдиплусстартуп**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) и [**гдиплусшутдовн**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown).</span><span class="sxs-lookup"><span data-stu-id="8a1d3-111">The **WinMain** function has a small amount of GDI+ code, namely the required calls to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) and [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown).</span></span> <span data-ttu-id="8a1d3-112">Код GDI+, который фактически создает [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и рисует линию, находится в функции **onpain** .</span><span class="sxs-lookup"><span data-stu-id="8a1d3-112">The GDI+ code that actually creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and draws a line is in the **OnPaint** function.</span></span>

<span data-ttu-id="8a1d3-113">Функция **onpain** получает указатель на контекст устройства и передает этот обработчик [**графическому**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) конструктору.</span><span class="sxs-lookup"><span data-stu-id="8a1d3-113">The **OnPaint** function receives a handle to a device context and passes that handle to a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="8a1d3-114">Аргумент, передаваемый конструктору [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , является ссылкой на объект [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="8a1d3-114">The argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor is a reference to a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="8a1d3-115">Четыре числа, передаваемые конструктору Color, представляют собой альфа-, красный, зеленый и синий компоненты цвета.</span><span class="sxs-lookup"><span data-stu-id="8a1d3-115">The four numbers passed to the color constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="8a1d3-116">Альфа-компонент определяет прозрачность цвета. 0 является полностью прозрачным, а 255 — полностью непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="8a1d3-116">The alpha component determines the transparency of the color; 0 is fully transparent and 255 is fully opaque.</span></span> <span data-ttu-id="8a1d3-117">Четыре числа, передаваемые методу [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) , представляют начальную точку (0, 0) и конечную точку (200, 100) строки.</span><span class="sxs-lookup"><span data-stu-id="8a1d3-117">The four numbers passed to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method represent the starting point (0, 0) and the ending point (200, 100) of the line.</span></span>


```C++
#include <stdafx.h>
#include <windows.h>
#include <objidl.h>
#include <gdiplus.h>
using namespace Gdiplus;
#pragma comment (lib,"Gdiplus.lib")

VOID OnPaint(HDC hdc)
{
   Graphics graphics(hdc);
   Pen      pen(Color(255, 0, 0, 255));
   graphics.DrawLine(&pen, 0, 0, 200, 100);
}

LRESULT CALLBACK WndProc(HWND, UINT, WPARAM, LPARAM);

INT WINAPI WinMain(HINSTANCE hInstance, HINSTANCE, PSTR, INT iCmdShow)
{
   HWND                hWnd;
   MSG                 msg;
   WNDCLASS            wndClass;
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR           gdiplusToken;
   
   // Initialize GDI+.
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   
   wndClass.style          = CS_HREDRAW | CS_VREDRAW;
   wndClass.lpfnWndProc    = WndProc;
   wndClass.cbClsExtra     = 0;
   wndClass.cbWndExtra     = 0;
   wndClass.hInstance      = hInstance;
   wndClass.hIcon          = LoadIcon(NULL, IDI_APPLICATION);
   wndClass.hCursor        = LoadCursor(NULL, IDC_ARROW);
   wndClass.hbrBackground  = (HBRUSH)GetStockObject(WHITE_BRUSH);
   wndClass.lpszMenuName   = NULL;
   wndClass.lpszClassName  = TEXT("GettingStarted");
   
   RegisterClass(&wndClass);
   
   hWnd = CreateWindow(
      TEXT("GettingStarted"),   // window class name
      TEXT("Getting Started"),  // window caption
      WS_OVERLAPPEDWINDOW,      // window style
      CW_USEDEFAULT,            // initial x position
      CW_USEDEFAULT,            // initial y position
      CW_USEDEFAULT,            // initial x size
      CW_USEDEFAULT,            // initial y size
      NULL,                     // parent window handle
      NULL,                     // window menu handle
      hInstance,                // program instance handle
      NULL);                    // creation parameters
      
   ShowWindow(hWnd, iCmdShow);
   UpdateWindow(hWnd);
   
   while(GetMessage(&msg, NULL, 0, 0))
   {
      TranslateMessage(&msg);
      DispatchMessage(&msg);
   }
   
   GdiplusShutdown(gdiplusToken);
   return msg.wParam;
}  // WinMain

LRESULT CALLBACK WndProc(HWND hWnd, UINT message, 
   WPARAM wParam, LPARAM lParam)
{
   HDC          hdc;
   PAINTSTRUCT  ps;
   
   switch(message)
   {
   case WM_PAINT:
      hdc = BeginPaint(hWnd, &ps);
      OnPaint(hdc);
      EndPaint(hWnd, &ps);
      return 0;
   case WM_DESTROY:
      PostQuitMessage(0);
      return 0;
   default:
      return DefWindowProc(hWnd, message, wParam, lParam);
   }
} // WndProc
```



<span data-ttu-id="8a1d3-118">Обратите внимание на вызов [**гдиплусстартуп**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) в функции **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="8a1d3-118">Note the call to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) in the **WinMain** function.</span></span> <span data-ttu-id="8a1d3-119">Первым параметром функции **гдиплусстартуп** является адрес типа ulong \_ .</span><span class="sxs-lookup"><span data-stu-id="8a1d3-119">The first parameter of the **GdiplusStartup** function is the address of a ULONG\_PTR.</span></span> <span data-ttu-id="8a1d3-120">**Гдиплусстартуп** заполняет переменную токеном, который позже передается в функцию [**гдиплусшутдовн**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) .</span><span class="sxs-lookup"><span data-stu-id="8a1d3-120">**GdiplusStartup** fills that variable with a token that is later passed to the [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) function.</span></span> <span data-ttu-id="8a1d3-121">Вторым параметром функции **гдиплусстартуп** является адрес структуры [**гдиплусстартупинпут**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) .</span><span class="sxs-lookup"><span data-stu-id="8a1d3-121">The second parameter of the **GdiplusStartup** function is the address of a [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) structure.</span></span> <span data-ttu-id="8a1d3-122">Приведенный выше код полагается на конструктор **гдиплусстартупинпут** по умолчанию, чтобы правильно задать элементы структуры.</span><span class="sxs-lookup"><span data-stu-id="8a1d3-122">The preceding code relies on the default **GdiplusStartupInput** constructor to set the structure members appropriately.</span></span>

 

 



