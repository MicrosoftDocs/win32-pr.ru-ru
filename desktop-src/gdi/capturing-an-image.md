---
description: Можно использовать точечный рисунок для записи изображения, а захваченный образ можно сохранить в памяти, отобразить его в другом расположении в окне приложения или отобразить в другом окне.
ms.assetid: 672fc2e4-c35c-4d5d-98fa-85f2ad56d9b0
title: Захват образа
ms.topic: article
ms.date: 12/03/2020
ms.custom: contperf-fy21q2
ms.openlocfilehash: b6029ec18a39ea034ca22e4c3d6c2d1e659635cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263692"
---
# <a name="capturing-an-image"></a><span data-ttu-id="59dc3-103">Захват образа</span><span class="sxs-lookup"><span data-stu-id="59dc3-103">Capturing an Image</span></span>

<span data-ttu-id="59dc3-104">Можно использовать точечный рисунок для записи изображения, а захваченный образ можно сохранить в памяти, отобразить его в другом расположении в окне приложения или отобразить в другом окне.</span><span class="sxs-lookup"><span data-stu-id="59dc3-104">You can use a bitmap to capture an image, and you can store the captured image in memory, display it at a different location in your application's window, or display it in another window.</span></span>

<span data-ttu-id="59dc3-105">В некоторых случаях может потребоваться, чтобы приложение захватывать образы и сохранять их только временно.</span><span class="sxs-lookup"><span data-stu-id="59dc3-105">In some cases, you may want your application to capture images and store them only temporarily.</span></span> <span data-ttu-id="59dc3-106">Например, при масштабировании или масштабировании изображения, созданного в приложении для рисования, приложение должно временно сохранить нормальное представление изображения и отобразить увеличенное представление.</span><span class="sxs-lookup"><span data-stu-id="59dc3-106">For example, when you scale or zoom a picture created in a drawing application, the application must temporarily save the normal view of the image and display the zoomed view.</span></span> <span data-ttu-id="59dc3-107">Позже, когда пользователь выбирает нормальное представление, приложение должно заменить измененное изображение копией нормального представления, которое он временно сохранил.</span><span class="sxs-lookup"><span data-stu-id="59dc3-107">Later, when the user selects the normal view, the application must replace the zoomed image with a copy of the normal view that it temporarily saved.</span></span>

<span data-ttu-id="59dc3-108">Чтобы временно сохранить образ, приложение должно вызвать [**креатекомпатибледк**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) , чтобы создать контроллер домена, совместимый с текущим окном DC.</span><span class="sxs-lookup"><span data-stu-id="59dc3-108">To store an image temporarily, your application must call [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) to create a DC that is compatible with the current window DC.</span></span> <span data-ttu-id="59dc3-109">После создания совместимого контроллера домена создайте точечный рисунок с соответствующими размерами, вызвав функцию [**креатекомпатиблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , а затем выбрав ее в этом контексте устройства, вызвав функцию [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="59dc3-109">After you create a compatible DC, you create a bitmap with the appropriate dimensions by calling the [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function and then select it into this device context by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span>

<span data-ttu-id="59dc3-110">После создания совместимого контекста устройства и выбора в нем соответствующего растрового изображения можно записать образ.</span><span class="sxs-lookup"><span data-stu-id="59dc3-110">After the compatible device context is created and the appropriate bitmap has been selected into it, you can capture the image.</span></span> <span data-ttu-id="59dc3-111">Функция [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) фиксирует образы.</span><span class="sxs-lookup"><span data-stu-id="59dc3-111">The [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) function captures images.</span></span> <span data-ttu-id="59dc3-112">Эта функция выполняет блочный блок, т. е. копирует данные из исходного растрового изображения в точечный рисунок назначения.</span><span class="sxs-lookup"><span data-stu-id="59dc3-112">This function performs a bit block transfer that is, it copies data from a source bitmap into a destination bitmap.</span></span> <span data-ttu-id="59dc3-113">Однако два аргумента этой функции не являются маркерами точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="59dc3-113">However, the two arguments to this function are not bitmap handles.</span></span> <span data-ttu-id="59dc3-114">Вместо этого **BitBlt** получает дескрипторы, которые обозначают два контекста устройств и копирует растровые данные из растрового изображения, выбранного в исходный контроллер домена, в точечный рисунок, выбранный в качестве целевого контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="59dc3-114">Instead, **BitBlt** receives handles that identify two device contexts and copies the bitmap data from a bitmap selected into the source DC into a bitmap selected into the target DC.</span></span> <span data-ttu-id="59dc3-115">В этом случае целевой контроллер домена является совместимым контроллером домена, поэтому когда **BitBlt** завершает перенос, образ сохраняется в памяти.</span><span class="sxs-lookup"><span data-stu-id="59dc3-115">In this case, the target DC is the compatible DC, so when **BitBlt** completes the transfer, the image has been stored in memory.</span></span> <span data-ttu-id="59dc3-116">Чтобы повторно отобразить изображение, вызовите **BitBlt** во второй раз, указав СОВМЕСТИМЫй контроллер домена в качестве исходного контроллера домена и окна (или принтера) DC в качестве целевого контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="59dc3-116">To redisplay the image, call **BitBlt** a second time, specifying the compatible DC as the source DC and a window (or printer) DC as the target DC.</span></span>

## <a name="code-example"></a><span data-ttu-id="59dc3-117">Пример кода</span><span class="sxs-lookup"><span data-stu-id="59dc3-117">Code example</span></span>

<span data-ttu-id="59dc3-118">В этом разделе содержится пример кода, который фиксирует изображение всего рабочего стола, масштабирует его до текущего размера окна, а затем сохраняет его в файл (а также в клиентской области).</span><span class="sxs-lookup"><span data-stu-id="59dc3-118">This section contains a code example that captures an image of the entire desktop, scales it down to the current window size, and then saves it to a file (as well as displaying it in the client area).</span></span>

<span data-ttu-id="59dc3-119">Чтобы испытать пример кода, начните с создания нового проекта в Visual Studio на основе шаблона проекта **классического приложения Windows** .</span><span class="sxs-lookup"><span data-stu-id="59dc3-119">To try out the code example, begin by creating a new project in Visual Studio based on the **Windows Desktop Application** project template.</span></span> <span data-ttu-id="59dc3-120">Важно присвоить новому проекту имя `GDI_CapturingAnImage` , чтобы скомпилировать приведенный ниже код (например, он включает `GDI_CapturingAnImage.h` , что будет существовать в новом проекте, если вы назовите его как предложенное).</span><span class="sxs-lookup"><span data-stu-id="59dc3-120">It's important to name the new project `GDI_CapturingAnImage` so that the code listing below will compile (for example, it includes `GDI_CapturingAnImage.h`, which will exist in your new project if you name it as suggested).</span></span>

<span data-ttu-id="59dc3-121">Откройте `GDI_CapturingAnImage.cpp` файл исходного кода в новом проекте и замените его содержимое приведенным ниже списком.</span><span class="sxs-lookup"><span data-stu-id="59dc3-121">Open the `GDI_CapturingAnImage.cpp` source code file in your new project, and replace its contents with the listing below.</span></span> <span data-ttu-id="59dc3-122">Затем выполните сборку и запуск.</span><span class="sxs-lookup"><span data-stu-id="59dc3-122">Then build and run.</span></span> <span data-ttu-id="59dc3-123">Каждый раз при изменении размера окна вы увидите захваченный снимок экрана, отображаемый в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="59dc3-123">Each time you resize the window, you'll see the captured screenshot displayed in the client area.</span></span>

```cpp
// GDI_CapturingAnImage.cpp : Defines the entry point for the application.
//

#include "framework.h"
#include "GDI_CapturingAnImage.h"

#define MAX_LOADSTRING 100

// Global Variables:
HINSTANCE hInst;                                // current instance
WCHAR szTitle[MAX_LOADSTRING];                  // The title bar text
WCHAR szWindowClass[MAX_LOADSTRING];            // the main window class name

// Forward declarations of functions included in this code module:
ATOM                MyRegisterClass(HINSTANCE hInstance);
BOOL                InitInstance(HINSTANCE, int);
LRESULT CALLBACK    WndProc(HWND, UINT, WPARAM, LPARAM);
INT_PTR CALLBACK    About(HWND, UINT, WPARAM, LPARAM);

int APIENTRY wWinMain(_In_ HINSTANCE hInstance,
    _In_opt_ HINSTANCE hPrevInstance,
    _In_ LPWSTR    lpCmdLine,
    _In_ int       nCmdShow)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    // TODO: Place code here.

    // Initialize global strings
    LoadStringW(hInstance, IDS_APP_TITLE, szTitle, MAX_LOADSTRING);
    LoadStringW(hInstance, IDC_GDICAPTURINGANIMAGE, szWindowClass, MAX_LOADSTRING);
    MyRegisterClass(hInstance);

    // Perform application initialization:
    if (!InitInstance(hInstance, nCmdShow))
    {
        return FALSE;
    }

    HACCEL hAccelTable = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDC_GDICAPTURINGANIMAGE));

    MSG msg;

    // Main message loop:
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    return (int)msg.wParam;
}

//
//  FUNCTION: MyRegisterClass()
//
//  PURPOSE: Registers the window class.
//
ATOM MyRegisterClass(HINSTANCE hInstance)
{
    WNDCLASSEXW wcex;

    wcex.cbSize = sizeof(WNDCLASSEX);

    wcex.style = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc = WndProc;
    wcex.cbClsExtra = 0;
    wcex.cbWndExtra = 0;
    wcex.hInstance = hInstance;
    wcex.hIcon = LoadIcon(hInstance, MAKEINTRESOURCE(IDI_GDICAPTURINGANIMAGE));
    wcex.hCursor = LoadCursor(nullptr, IDC_ARROW);
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW + 1);
    wcex.lpszMenuName = MAKEINTRESOURCEW(IDC_GDICAPTURINGANIMAGE);
    wcex.lpszClassName = szWindowClass;
    wcex.hIconSm = LoadIcon(wcex.hInstance, MAKEINTRESOURCE(IDI_SMALL));

    return RegisterClassExW(&wcex);
}

//
//   FUNCTION: InitInstance(HINSTANCE, int)
//
//   PURPOSE: Saves instance handle and creates main window
//
//   COMMENTS:
//
//        In this function, we save the instance handle in a global variable and
//        create and display the main program window.
//
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
    hInst = hInstance; // Store instance handle in our global variable

    HWND hWnd = CreateWindowW(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, nullptr, nullptr, hInstance, nullptr);

    if (!hWnd)
    {
        return FALSE;
    }

    ShowWindow(hWnd, nCmdShow);
    UpdateWindow(hWnd);

    return TRUE;
}

// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

//
//   FUNCTION: CaptureAnImage(HWND hWnd)
//
//   PURPOSE: Captures a screenshot into a window ,and then saves it in a .bmp file.
//
//   COMMENTS: 
//
//      Note: This function attempts to create a file called captureqwsx.bmp 
//        

int CaptureAnImage(HWND hWnd)
{
    HDC hdcScreen;
    HDC hdcWindow;
    HDC hdcMemDC = NULL;
    HBITMAP hbmScreen = NULL;
    BITMAP bmpScreen;
    DWORD dwBytesWritten = 0;
    DWORD dwSizeofDIB = 0;
    HANDLE hFile = NULL;
    char* lpbitmap = NULL;
    HANDLE hDIB = NULL;
    DWORD dwBmpSize = 0;

    // Retrieve the handle to a display device context for the client 
    // area of the window. 
    hdcScreen = GetDC(NULL);
    hdcWindow = GetDC(hWnd);

    // Create a compatible DC, which is used in a BitBlt from the window DC.
    hdcMemDC = CreateCompatibleDC(hdcWindow);

    if (!hdcMemDC)
    {
        MessageBox(hWnd, L"CreateCompatibleDC has failed", L"Failed", MB_OK);
        goto done;
    }

    // Get the client area for size calculation.
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    // This is the best stretch mode.
    SetStretchBltMode(hdcWindow, HALFTONE);

    // The source DC is the entire screen, and the destination DC is the current window (HWND).
    if (!StretchBlt(hdcWindow,
        0, 0,
        rcClient.right, rcClient.bottom,
        hdcScreen,
        0, 0,
        GetSystemMetrics(SM_CXSCREEN),
        GetSystemMetrics(SM_CYSCREEN),
        SRCCOPY))
    {
        MessageBox(hWnd, L"StretchBlt has failed", L"Failed", MB_OK);
        goto done;
    }

    // Create a compatible bitmap from the Window DC.
    hbmScreen = CreateCompatibleBitmap(hdcWindow, rcClient.right - rcClient.left, rcClient.bottom - rcClient.top);

    if (!hbmScreen)
    {
        MessageBox(hWnd, L"CreateCompatibleBitmap Failed", L"Failed", MB_OK);
        goto done;
    }

    // Select the compatible bitmap into the compatible memory DC.
    SelectObject(hdcMemDC, hbmScreen);

    // Bit block transfer into our compatible memory DC.
    if (!BitBlt(hdcMemDC,
        0, 0,
        rcClient.right - rcClient.left, rcClient.bottom - rcClient.top,
        hdcWindow,
        0, 0,
        SRCCOPY))
    {
        MessageBox(hWnd, L"BitBlt has failed", L"Failed", MB_OK);
        goto done;
    }

    // Get the BITMAP from the HBITMAP.
    GetObject(hbmScreen, sizeof(BITMAP), &bmpScreen);

    BITMAPFILEHEADER   bmfHeader;
    BITMAPINFOHEADER   bi;

    bi.biSize = sizeof(BITMAPINFOHEADER);
    bi.biWidth = bmpScreen.bmWidth;
    bi.biHeight = bmpScreen.bmHeight;
    bi.biPlanes = 1;
    bi.biBitCount = 32;
    bi.biCompression = BI_RGB;
    bi.biSizeImage = 0;
    bi.biXPelsPerMeter = 0;
    bi.biYPelsPerMeter = 0;
    bi.biClrUsed = 0;
    bi.biClrImportant = 0;

    dwBmpSize = ((bmpScreen.bmWidth * bi.biBitCount + 31) / 32) * 4 * bmpScreen.bmHeight;

    // Starting with 32-bit Windows, GlobalAlloc and LocalAlloc are implemented as wrapper functions that 
    // call HeapAlloc using a handle to the process's default heap. Therefore, GlobalAlloc and LocalAlloc 
    // have greater overhead than HeapAlloc.
    hDIB = GlobalAlloc(GHND, dwBmpSize);
    lpbitmap = (char*)GlobalLock(hDIB);

    // Gets the "bits" from the bitmap, and copies them into a buffer 
    // that's pointed to by lpbitmap.
    GetDIBits(hdcWindow, hbmScreen, 0,
        (UINT)bmpScreen.bmHeight,
        lpbitmap,
        (BITMAPINFO*)&bi, DIB_RGB_COLORS);

    // A file is created, this is where we will save the screen capture.
    hFile = CreateFile(L"captureqwsx.bmp",
        GENERIC_WRITE,
        0,
        NULL,
        CREATE_ALWAYS,
        FILE_ATTRIBUTE_NORMAL, NULL);

    // Add the size of the headers to the size of the bitmap to get the total file size.
    dwSizeofDIB = dwBmpSize + sizeof(BITMAPFILEHEADER) + sizeof(BITMAPINFOHEADER);

    // Offset to where the actual bitmap bits start.
    bmfHeader.bfOffBits = (DWORD)sizeof(BITMAPFILEHEADER) + (DWORD)sizeof(BITMAPINFOHEADER);

    // Size of the file.
    bmfHeader.bfSize = dwSizeofDIB;

    // bfType must always be BM for Bitmaps.
    bmfHeader.bfType = 0x4D42; // BM.

    WriteFile(hFile, (LPSTR)&bmfHeader, sizeof(BITMAPFILEHEADER), &dwBytesWritten, NULL);
    WriteFile(hFile, (LPSTR)&bi, sizeof(BITMAPINFOHEADER), &dwBytesWritten, NULL);
    WriteFile(hFile, (LPSTR)lpbitmap, dwBmpSize, &dwBytesWritten, NULL);

    // Unlock and Free the DIB from the heap.
    GlobalUnlock(hDIB);
    GlobalFree(hDIB);

    // Close the handle for the file that was created.
    CloseHandle(hFile);

    // Clean up.
done:
    DeleteObject(hbmScreen);
    DeleteObject(hdcMemDC);
    ReleaseDC(NULL, hdcScreen);
    ReleaseDC(hWnd, hdcWindow);

    return 0;
}

//
//  FUNCTION: WndProc(HWND, UINT, WPARAM, LPARAM)
//
//  PURPOSE: Processes messages for the main window.
//
//  WM_COMMAND  - process the application menu
//  WM_PAINT    - Paint the main window
//  WM_DESTROY  - post a quit message and return
//
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_COMMAND:
    {
        int wmId = LOWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
    }
    break;
    case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hWnd, &ps);
        CaptureAnImage(hWnd);
        EndPaint(hWnd, &ps);
    }
    break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

// Message handler for about box.
INT_PTR CALLBACK About(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    UNREFERENCED_PARAMETER(lParam);
    switch (message)
    {
    case WM_INITDIALOG:
        return (INT_PTR)TRUE;

    case WM_COMMAND:
        if (LOWORD(wParam) == IDOK || LOWORD(wParam) == IDCANCEL)
        {
            EndDialog(hDlg, LOWORD(wParam));
            return (INT_PTR)TRUE;
        }
        break;
    }
    return (INT_PTR)FALSE;
}
```
