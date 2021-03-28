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
# <a name="drawing-a-line"></a>Рисование линии

В этом разделе показано, как нарисовать линию с помощью GDI и.

Для рисования линии в Windows GDI+ необходим [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект, объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) и объект [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Объект **Graphics** предоставляет метод [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) , а объект **Pen** содержит атрибуты линии, такие как цвет и ширина. Адрес объекта **Pen** передается в качестве аргумента в метод **DrawLine** .

Следующая программа, которая рисует строку от (0, 0) до (200, 100), состоит из трех функций: **WinMain**, **WndProc** и **onpain**. Функции **WinMain** и **WndProc** предоставляют фундаментальный код, который является общим для большинства приложений Windows. В функции **WndProc** отсутствует код GDI+. Функция **WinMain** имеет небольшой объем кода GDI+, а именно, необходимые вызовы [**гдиплусстартуп**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) и [**гдиплусшутдовн**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). Код GDI+, который фактически создает [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и рисует линию, находится в функции **onpain** .

Функция **onpain** получает указатель на контекст устройства и передает этот обработчик [**графическому**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) конструктору. Аргумент, передаваемый конструктору [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , является ссылкой на объект [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Четыре числа, передаваемые конструктору Color, представляют собой альфа-, красный, зеленый и синий компоненты цвета. Альфа-компонент определяет прозрачность цвета. 0 является полностью прозрачным, а 255 — полностью непрозрачным. Четыре числа, передаваемые методу [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) , представляют начальную точку (0, 0) и конечную точку (200, 100) строки.


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



Обратите внимание на вызов [**гдиплусстартуп**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) в функции **WinMain** . Первым параметром функции **гдиплусстартуп** является адрес типа ulong \_ . **Гдиплусстартуп** заполняет переменную токеном, который позже передается в функцию [**гдиплусшутдовн**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) . Вторым параметром функции **гдиплусстартуп** является адрес структуры [**гдиплусстартупинпут**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) . Приведенный выше код полагается на конструктор **гдиплусстартупинпут** по умолчанию, чтобы правильно задать элементы структуры.

 

 



