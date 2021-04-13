---
title: Создание простого визуального дерева
description: В этом разделе показано, как создать простое визуальное дерево Microsoft DirectComposition. Пример в этом разделе создает и формирует визуальное дерево, состоящее из корневого визуального элемента и трех дочерних визуальных элементов.
ms.assetid: 86006C3C-67A8-4931-BE76-D0CA9DB19505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621e3f48f76b76be92dc464678dce23b08ebdbd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104412983"
---
# <a name="how-to-build-a-simple-visual-tree"></a>Создание простого визуального дерева

> [!NOTE]
> Для приложений в Windows 10 рекомендуется использовать интерфейсы API Windows. UI. компоновки вместо DirectComposition. Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).

В этом разделе показано, как создать простое визуальное дерево Microsoft DirectComposition. Пример в этом разделе создает и формирует визуальное дерево, состоящее из корневого визуального элемента и трех дочерних визуальных элементов. Содержимое корневого визуального элемента — это светло-синий точечный рисунок, служащий фоном для дочерних визуальных элементов. На этом рисунке показана композиция, созданная в примере кода в этой статье.

![композиция, состоящая из корневого точечного рисунка и трех дочерних растровых изображений](images/buildvisualtree.png)

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [DirectComposition](directcomposition-portal.md)
-   [Графика Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [Графическая инфраструктура DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Предварительные условия

Знания:

-   C/C++
-   Microsoft Win32
-   Модель COM

## <a name="instructions"></a>Инструкции

### <a name="step-1-initialize-the-device-and-composition-target-objects"></a>Шаг 1. Инициализация целевых объектов для устройства и композиции

Дополнительные сведения см. [в разделе как инициализировать DirectComposition](initialize-directcomposition.md).

### <a name="step-2-create-the-visual-objects-and-set-the-bitmap-content"></a>Шаг 2. Создание визуальных объектов и задание содержимого точечного рисунка

Используйте метод [**идкомпоситиондевице:: креатевисуал**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual) для создания визуальных элементов и метод [**Идкомпоситионвисуал:: сетконтент**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) для установки растрового содержимого визуальных элементов.

> [!NOTE]  
> В следующем примере первый элемент `m_hBitmaps` массива содержит битовую карту для корневого визуального элемента, а остальные элементы содержат точечные рисунки для дочерних визуальных элементов.

```cpp
#define NUM_VISUALS 4 // number of visuals in the composition
HBITMAP m_hBitmaps[NUM_VISUALS];
HRESULT hr = S_OK;

IDCompositionVisual *pVisuals[NUM_VISUALS]{ };
IDCompositionSurface *pSurface{ nullptr };

// Create a visual objects and set their content.   
for (int i = 0; i < NUM_VISUALS; i++)
{
    hr = m_pDevice->CreateVisual(&pVisuals[i]);
    if (SUCCEEDED(hr))
    {
        // This application-defined function creates a DirectComposition
        // surface and renders a GDI bitmap onto the surface. 
        hr = MyCreateGDIRenderedDCompSurface(m_hBitmaps[i], &pSurface);

        if (SUCCEEDED(hr))
        {
            // Set the bitmap content.  
            hr = pVisuals[i]->SetContent(pSurface);
        }

        SafeRelease(&pSurface);
    }

    if (FAILED(hr))
    {
        goto Cleanup;
    }
}
``` 

В следующей определяемой функции показано, как создать поверхность Microsoft DirectComposition и визуализировать на поверхности точечный рисунок Windows интерфейс графических устройств (GDI).

```cpp
// MyCreateGDIRenderedDCompSurface - Creates a DirectComposition surface and 
//   copies the bitmap to the surface. 
//
// Parameters:
//   hBitmap - a GDI bitmap.
//   ppSurface - the composition surface object.
//                                                                 
HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, IDCompositionSurface **ppSurface)
{
    HRESULT hr = S_OK;

    int bitmapWidth = 0;
    int bitmapHeight = 0;
    int bmpSize = 0;
     BITMAP bmp = { };
    HBITMAP hBitmapOld = NULL;

    HDC hSurfaceDC = NULL;  
    HDC hBitmapDC = NULL;

    IDXGISurface1 *pDXGISurface = nullptr;
    POINT pointOffset = { };

    hr =  hBitmap ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Get information about the bitmap.
        bmpSize = GetObject(hBitmap, sizeof(BITMAP), &bmp);
    }

    hr = bmpSize ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Save the bitmap dimensions.
        bitmapWidth = bmp.bmWidth;
        bitmapHeight = bmp.bmHeight;

        // Create a DirectComposition-compatible surface that is the same size 
        // as the bitmap.
        hr = m_pDevice->CreateSurface(bitmapWidth, bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, ppSurface);
    }

    hr = ppSurface ? S_OK : E_FAIL;
    if (SUCCEEDED(hr)) 
    {
        hr = (*ppSurface)->BeginDraw(NULL, __uuidof(IDXGISurface1), 
            reinterpret_cast<void**>(&pDXGISurface), &pointOffset);
    }

    if (SUCCEEDED(hr)) 
    {
        pDXGISurface->GetDC(FALSE, &hSurfaceDC);
    }

    hr = hSurfaceDC ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        hBitmapDC = CreateCompatibleDC(hSurfaceDC);
        if (hBitmapDC != NULL)
        {
            hBitmapOld = (HBITMAP)SelectObject(hBitmapDC, hBitmap);
            BitBlt(hSurfaceDC, pointOffset.x, pointOffset.y, 
                bitmapWidth, bitmapHeight, hBitmapDC, 0, 0, SRCCOPY);
            
            if (hBitmapOld)
            {
                SelectObject(hBitmapDC, hBitmapOld);
            }
            DeleteDC(hBitmapDC);
        }

        pDXGISurface->ReleaseDC(NULL);
    }

    (*ppSurface)->EndDraw();

    SafeRelease(&pDXGISurface);

    return hr;
}
```

### <a name="step-3-set-the-root-visual"></a>Шаг 3. Настройка корневого визуального элемента

Задайте горизонтальное и вертикальное смещение корневого визуального элемента, а затем добавьте его в визуальное дерево, вызвав метод [**идкомпоситионтаржет:: сетрут**](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot) .

```cpp
float xPosRoot = 50.0;
float yPosRoot = 50.0;

// Set the horizontal and vertical position of the root visual. 
pVisuals[0]->SetOffsetX(xPosRoot);
pVisuals[0]->SetOffsetY(yPosRoot);

// Set the root visual of the visual tree.          
hr = m_pCompTarget->SetRoot(pVisuals[0]);
```

### <a name="step-4-add-the-child-visuals-and-commit-the-composition"></a>Шаг 4. добавление дочерних визуальных элементов и фиксация композиции

Используйте методы, предоставляемые каждым интерфейсом [**идкомпоситионвисуал**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual) дочернего визуального элемента для установки содержимого растрового изображения и других свойств, а затем используйте метод [**Идкомпоситионвисуал:: аддвисуал**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-addvisual) корневого элемента, чтобы добавить дочерние визуальные элементы в корень визуального дерева. Вызовите метод [**идкомпоситиондевице:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) , чтобы зафиксировать пакет команд в DirectComposition для обработки. Полученная композиция появится в целевом окне.

```cpp
float xPosChild = 20.0f;
float yPosChild = 20.0f;

if (SUCCEEDED(hr))
{
    // Set the positions of the child visuals and add them to the visual tree.
    for (int i = 1; i < NUM_VISUALS; i++)
    {
        pVisuals[i]->SetOffsetX(xPosChild);
        pVisuals[i]->SetOffsetY(
            static_cast<float>((yPosChild * i) + (CHILD_BITMAP_HEIGHT * (i - 1))));

        // Add the child visuals as children of the root visual.
        pVisuals[0]->AddVisual(pVisuals[i], TRUE, nullptr);
    }
}

// Commit the visual to be composed and displayed.
hr = m_pDevice->Commit();
```

### <a name="step-5-free-the-directcomposition-objects"></a>Шаг 5. освобождение объектов DirectComposition

Освободите визуальные объекты, как только они больше не нужны. Следующий фрагмент кода вызывает макрос [**саферелеасе**](/windows/desktop/medfound/saferelease) , определяемый приложением, чтобы освободить визуальные объекты.

```cpp
Cleanup:
    // Free the visuals.
    for (int i = 0; i < NUM_VISUALS; i++) 
    {
        SafeRelease(&pVisuals[i]);
    }
```

Кроме того, не забудьте освободить целевые объекты устройства и композиции перед завершением работы приложения.

```cpp
SafeRelease(&m_pD3D11Device);
SafeRelease(&m_pDevice);
SafeRelease(&m_pCompTarget);
```

## <a name="complete-example"></a>Полный пример

```cpp
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

#pragma once
// Modify the following definitions if you need to target a platform prior to the ones specified below.
// Refer to MSDN for the latest info on corresponding values for different platforms.
#ifndef WINVER              // Allow use of features specific to Windows 7 or later.
#define WINVER 0x0700       // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT        // Allow use of features specific to Windows 7 or later.
#define _WIN32_WINNT 0x0700 // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN     // Exclude rarely-used items from Windows headers

// Windows Header Files:
#include <windows.h>

// C RunTime Header Files
#include <math.h>

#include <dcomp.h>
#include <d3d11.h>

/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
)
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}
#ifndef Assert
#if defined( DEBUG ) || defined( _DEBUG )
#define Assert(b) if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}
#else
#define Assert(b)
#endif //DEBUG || _DEBUG
#endif

#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

// Application-defined constants
#define NUM_VISUALS 4       // number of visuals in the composition
#define CHILD_BITMAP_HEIGHT 96    // height, in pixels, of a child visual
#define NUM_BITMAPS 4       // number of bitmaps in the composition

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT Initialize();

    void RunMessageLoop();

private:
    HRESULT InitializeDirectCompositionDevice();

    HRESULT CreateResources();
    void DiscardResources();

    HRESULT OnClientClick();

    HRESULT DemoApp::LoadResourceGDIBitmap(
        PCWSTR resourceName,
        HBITMAP &hbmp
    );
    HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, IDCompositionSurface **ppSurface);

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
    );

private:
    HWND m_hwnd;

    HBITMAP m_hBitmaps[NUM_VISUALS];
    ID3D11Device *m_pD3D11Device;
    IDCompositionDevice *m_pDevice;
    IDCompositionTarget *m_pCompTarget;
};
```

```cpp
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

// Instructions: Right-click in the client area to cause DirectCompostion
// to create a simple composition consisting a root visual and three child 
// visuals. The root visual provides the background bitmap for the 
// composition, and the three child visuals provide bitmaps that are 
// composed on top of the root. All bitmaps are GDI.

#include "SimpleVisualTree.h"

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE /* hInstance */,
    HINSTANCE /* hPrevInstance */,
    LPSTR /* lpCmdLine */,
    int /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
    // unlikely event that HeapSetInformation fails.
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);
    if (SUCCEEDED(CoInitialize(NULL)))
    {
        {
            DemoApp app;

            if (SUCCEEDED(app.Initialize()))
            {
                app.RunMessageLoop();
            }
        }
        CoUninitialize();
    }

    return 0;
}

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                         *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_hwnd(NULL),
    m_hBitmaps(),
    m_pD3D11Device(nullptr),
    m_pDevice(nullptr),
    m_pCompTarget(nullptr)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()
{
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pCompTarget);
}

/*******************************************************************
*                                                                  *
*  Create the application window.                                  *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::Initialize()
{
    HRESULT hr;

    // Register the window class.
    WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
    wcex.style         = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc   = DemoApp::WndProc;
    wcex.cbClsExtra    = 0;
    wcex.cbWndExtra    = sizeof(LONG_PTR);
    wcex.hInstance     = HINST_THISCOMPONENT;
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
    wcex.lpszMenuName  = NULL;
    wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wcex.lpszClassName = L"DirectCompDemoApp";

    RegisterClassEx(&wcex);

    // Create the application window.
    //
    // Because the CreateWindow function takes its size in pixels, we
    // obtain the system DPI and use it to scale the window size.
    int dpiX = 0;
    int dpiY = 0;
    HDC hdc = GetDC(NULL);
    if (hdc)
    {
        dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
        dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
        ReleaseDC(NULL, hdc);
    }

    m_hwnd = CreateWindow(
        L"DirectCompDemoApp",
        L"DirectComposition Demo Application",
        WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT,
        CW_USEDEFAULT,
        static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
        static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
        NULL,
        NULL,
        HINST_THISCOMPONENT,
        this
        );

    hr = m_hwnd ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        ShowWindow(m_hwnd, SW_SHOWNORMAL);
        UpdateWindow(m_hwnd);

        // Initialize DirectComposition resources, such as the
        // device object and composition target object.
        hr = InitializeDirectCompositionDevice();
    }

    if (SUCCEEDED(hr))
    {
        hr = CreateResources();
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the DirectComposition device object and    *
*  and the composition target object. These objects endure for    *
*  the lifetime of the application.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::InitializeDirectCompositionDevice()
{
    HRESULT hr = S_OK;

    D3D_FEATURE_LEVEL featureLevelSupported;
    IDXGIDevice *pDXGIDevice = nullptr;

    // Create the D3D device object.
    D3D11CreateDevice(
        nullptr,
        D3D_DRIVER_TYPE_HARDWARE,
        NULL,
        D3D11_CREATE_DEVICE_BGRA_SUPPORT,
        NULL,
        0,
        D3D11_SDK_VERSION,
        &m_pD3D11Device,
        &featureLevelSupported,
        NULL);

    hr = (m_pD3D11Device == nullptr) ? E_UNEXPECTED : S_OK;
    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = m_pD3D11Device->QueryInterface(&pDXGIDevice);
    }

    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, __uuidof(IDCompositionDevice), 
            reinterpret_cast<void **>(&m_pDevice));
    }

    if (SUCCEEDED(hr))
    {
        // Create the composition target object.
        hr = m_pDevice->CreateTargetForHwnd(m_hwnd, TRUE, &m_pCompTarget);   
    }

    SafeRelease(&pDXGIDevice);
    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the GDI bitmaps to be associated with      *
*  DirectComposition visual objects.                              *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateResources()
{
    HRESULT hr = S_OK;

    hr = LoadResourceGDIBitmap(L"Background", m_hBitmaps[0]);
    hr = LoadResourceGDIBitmap(L"BlkKnight", m_hBitmaps[1]);
    hr = LoadResourceGDIBitmap(L"BlkQueen", m_hBitmaps[2]);
    hr = LoadResourceGDIBitmap(L"BlkRook", m_hBitmaps[3]);
   
    return hr;
}

/******************************************************************
*                                                                 *
*  Discard device-specific resources.                             *
*                                                                 *
******************************************************************/

void DemoApp::DiscardResources()
{
    int i = 0;
    while (i < NUM_VISUALS) 
    {
        DeleteObject(m_hBitmaps[i++]);
    }
}

/******************************************************************
*                                                                 *
*  The main window&#39;s message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}

/******************************************************************
*                                                                 *
*  Called whenever the user clicks the client area of the main    *
*  window. This method builds a simple visual tree consisting of  *   
*  a root visual and three child visuals.                         *
******************************************************************/

HRESULT DemoApp::OnClientClick()
{
    HRESULT hr = S_OK;

    IDCompositionVisual *pVisuals[NUM_VISUALS] = { };
    IDCompositionSurface *pSurface = nullptr;
    
    // Create a visual objects and set their content.   
    for (int i = 0; i < NUM_VISUALS; i++)
    {
        hr = m_pDevice->CreateVisual(&pVisuals[i]); 
        if (SUCCEEDED(hr))
        {
            // This application-defined function creates a DirectComposition
            // surface and renders a GDI bitmap onto the surface. 
            hr = MyCreateGDIRenderedDCompSurface(m_hBitmaps[i], &pSurface);

            if (SUCCEEDED(hr))
            {
                // Set the bitmap content.  
                hr = pVisuals[i]->SetContent(pSurface);
            }

            SafeRelease(&pSurface);
        }

        if (FAILED(hr))
        {
            goto Cleanup;
        }
    }

    float xPosRoot = 50.0; 
    float yPosRoot = 50.0; 

    // Set the horizontal and vertical position of the root visual. 
    pVisuals[0]->SetOffsetX(xPosRoot);  
    pVisuals[0]->SetOffsetY(yPosRoot);  

    // Set the root visual of the visual tree.          
    hr = m_pCompTarget->SetRoot(pVisuals[0]);  

    float xPosChild = 20.0f;
    float yPosChild = 20.0f;

    if (SUCCEEDED(hr))
    {
        // Set the positions of the child visuals and add them to the visual tree.
        for (int i = 1; i < NUM_VISUALS; i++)
        {
            pVisuals[i]->SetOffsetX(xPosChild);
            pVisuals[i]->SetOffsetY(
                static_cast<float>((yPosChild * i) + (CHILD_BITMAP_HEIGHT * (i - 1))));

            // Add the child visuals as children of the root visual.
            pVisuals[0]->AddVisual(pVisuals[i], TRUE, nullptr);
        }
    }
    
    // Commit the visual to be composed and displayed.
    hr = m_pDevice->Commit();  

Cleanup:
    // Free the visuals.
    for (int i = 0; i < NUM_VISUALS; i++) 
    {
        SafeRelease(&pVisuals[i]);
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  The window&#39;s message handler.                                  *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
            );

        result = 1;
    }
    else
    {
        DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
            ::GetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA
                )));

        bool wasHandled = false;

        if (pDemoApp)
        {
            switch (message)
            {
            case WM_LBUTTONDOWN:
                {
                    pDemoApp->OnClientClick();
                }
 
            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                    pDemoApp->DiscardResources();
                }
                wasHandled = true;
                result = 1;
                break;
            }
        }

        if (!wasHandled)
        {
            result = DefWindowProc(hwnd, message, wParam, lParam);
        }
    }

    return result;
}

/******************************************************************
*                                                                 *
*  This method loads the specified GDI bitmap from the            *
*  application resources, creates a new bitmap that is in a       *
*  format that DirectComposition can use, and copies the contents *
*  of the original bitmap to the new bitmap.                      *
*                                                                 *
******************************************************************/

HRESULT DemoApp::LoadResourceGDIBitmap(PCWSTR resourceName, HBITMAP &hbmp)
{
    // Load the bitmap from the application resources.
    hbmp = static_cast<HBITMAP>(LoadImageW(HINST_THISCOMPONENT, resourceName, 
        IMAGE_BITMAP, 0, 0, LR_DEFAULTCOLOR));  
 
    return hbmp ? S_OK : E_FAIL;
}

// MyCreateGDIRenderedDCompSurface - Creates a DirectComposition surface and 
//   copies the bitmap to the surface. 
//
// Parameters:
//   hBitmap - a GDI bitmap.
//   ppSurface - the composition surface object.
//                                                                 
HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, IDCompositionSurface **ppSurface)
{
    HRESULT hr = S_OK;

    int bitmapWidth = 0;
    int bitmapHeight = 0;
    int bmpSize = 0;
     BITMAP bmp = { };
    HBITMAP hBitmapOld = NULL;

    HDC hSurfaceDC = NULL;  
    HDC hBitmapDC = NULL;

    IDXGISurface1 *pDXGISurface = nullptr;
    POINT pointOffset = { };

    hr =  hBitmap ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Get information about the bitmap.
        bmpSize = GetObject(hBitmap, sizeof(BITMAP), &bmp);
    }

    hr = bmpSize ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Save the bitmap dimensions.
        bitmapWidth = bmp.bmWidth;
        bitmapHeight = bmp.bmHeight;

        // Create a DirectComposition-compatible surface that is the same size 
        // as the bitmap.
        hr = m_pDevice->CreateSurface(bitmapWidth, bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, ppSurface);
    }

    hr = ppSurface ? S_OK : E_FAIL;
    if (SUCCEEDED(hr)) 
    {
        hr = (*ppSurface)->BeginDraw(NULL, __uuidof(IDXGISurface1), 
            reinterpret_cast<void**>(&pDXGISurface), &pointOffset);
    }

    if (SUCCEEDED(hr)) 
    {
        pDXGISurface->GetDC(FALSE, &hSurfaceDC);
    }

    hr = hSurfaceDC ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        hBitmapDC = CreateCompatibleDC(hSurfaceDC);
        if (hBitmapDC != NULL)
        {
            hBitmapOld = (HBITMAP)SelectObject(hBitmapDC, hBitmap);
            BitBlt(hSurfaceDC, pointOffset.x, pointOffset.y, 
                bitmapWidth, bitmapHeight, hBitmapDC, 0, 0, SRCCOPY);
            
            if (hBitmapOld)
            {
                SelectObject(hBitmapDC, hBitmapOld);
            }
            DeleteDC(hBitmapDC);
        }

        pDXGISurface->ReleaseDC(NULL);
    }

    (*ppSurface)->EndDraw();

    SafeRelease(&pDXGISurface);

    return hr;
}
```

## <a name="related-topics"></a>См. также

* [**дкомпоситионкреатедевице**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice)
* [**Идкомпоситиондевице:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
* [**Идкомпоситиондевице:: Креатетаржетфорхвнд**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd)
* [**Идкомпоситиондевице:: Креатевисуал**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual)
* [**Идкомпоситионтаржет:: Сетрут**](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot)
* [**Идкомпоситионвисуал:: Сетконтент**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent)
* [**саферелеасе**](/windows/desktop/medfound/saferelease)