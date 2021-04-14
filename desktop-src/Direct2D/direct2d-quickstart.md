---
title: Создание простого приложения Direct2D
description: Описывает процесс создания окна, которое визуализирует содержимое Direct2D.
ms.assetid: a627523e-417a-40cd-82c0-4f0380a3a0b1
keywords:
- Direct2D, учебник
- Direct2D, пошаговое руководство
- Direct2D, создание приложений
- Direct2D, приложения
- приложения для Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d023e348e30b4e421ffe177f30c0c55a344fba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104564796"
---
# <a name="creating-a-simple-direct2d-application"></a><span data-ttu-id="cc285-108">Создание простого приложения Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc285-108">Creating a Simple Direct2D Application</span></span>

<span data-ttu-id="cc285-109">В этом разделе описывается процесс создания класса DemoApp, который создает окно и использует Direct2D для рисования сетки и двух прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="cc285-109">This topic walks you through the process of creating the DemoApp class, which creates a window and uses Direct2D to draw a grid and two rectangles.</span></span> <span data-ttu-id="cc285-110">В этом руководстве вы узнаете, как создавать ресурсы Direct2D и вырисовывать базовые фигуры.</span><span class="sxs-lookup"><span data-stu-id="cc285-110">In this tutorial, you learn how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="cc285-111">Вы также узнаете, как структурировать приложение, чтобы повысить производительность, минимизируя создание ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc285-111">You also learn how to structure your application to enhance performance by minimizing resource creation.</span></span>

<span data-ttu-id="cc285-112">Чтобы проследить за этим руководством, можно использовать Microsoft Visual Studio 2008 для создания проекта Win32, а затем заменить код в главном заголовке приложения и CPP-файл кодом, описанным в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="cc285-112">To follow the tutorial, you can use Microsoft Visual Studio 2008 to create a Win32 project and then replace the code in the main application header and cpp file with the code described in this tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="cc285-113">Если вы хотите создать приложение для Магазина Windows, использующее Direct2D, см. раздел [Краткое руководство по Direct2D для Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="cc285-113">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="cc285-114">Общие сведения об интерфейсах, которые можно использовать для создания содержимого Direct2D, см. в [обзоре API Direct2D](the-direct2d-api.md).</span><span class="sxs-lookup"><span data-stu-id="cc285-114">For an overview of the interfaces you can use to create Direct2D content, see the [Direct2D API Overview](the-direct2d-api.md).</span></span>

<span data-ttu-id="cc285-115">Этот учебник содержит следующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="cc285-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="cc285-116">Часть 1. Создание заголовка DemoApp</span><span class="sxs-lookup"><span data-stu-id="cc285-116">Part 1: Create the DemoApp Header</span></span>](#part-1-create-the-demoapp-header)
-   [<span data-ttu-id="cc285-117">Часть 2. Реализация инфраструктуры класса</span><span class="sxs-lookup"><span data-stu-id="cc285-117">Part 2: Implement the Class Infrastructure</span></span>](#part-2-implement-the-class-infrastructure)
-   [<span data-ttu-id="cc285-118">Часть 3. Создание ресурсов Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc285-118">Part 3: Create Direct2D Resources</span></span>](#part-3-create-direct2d-resources)
-   [<span data-ttu-id="cc285-119">Часть 4. прорисовка содержимого Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc285-119">Part 4: Render Direct2D Content</span></span>](#part-4-render-direct2d-content)
-   [<span data-ttu-id="cc285-120">Сводка</span><span class="sxs-lookup"><span data-stu-id="cc285-120">Summary</span></span>](#summary)
-   [<span data-ttu-id="cc285-121">См. также</span><span class="sxs-lookup"><span data-stu-id="cc285-121">Related topics</span></span>](#related-topics)

<span data-ttu-id="cc285-122">После завершения класс DemoApp выдает выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="cc285-122">Upon completion, the DemoApp class produces the output shown in the following illustration.</span></span>

![Иллюстрация двух прямоугольников на фоне сетки](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a><span data-ttu-id="cc285-124">Часть 1. Создание заголовка DemoApp</span><span class="sxs-lookup"><span data-stu-id="cc285-124">Part 1: Create the DemoApp Header</span></span>

<span data-ttu-id="cc285-125">На этом шаге вы настроите приложение для использования Direct2D, добавив необходимые заголовки и макросы.</span><span class="sxs-lookup"><span data-stu-id="cc285-125">In this step, you set up your application to use Direct2D by adding the necessary headers and macros.</span></span> <span data-ttu-id="cc285-126">Вы также объявляете методы и члены данных, которые будут использоваться в последующих частях этого руководства.</span><span class="sxs-lookup"><span data-stu-id="cc285-126">You also declare the methods and data members you'll use in later parts of this tutorial.</span></span>

1.  <span data-ttu-id="cc285-127">В файле заголовка приложения добавьте следующие часто используемые заголовки.</span><span class="sxs-lookup"><span data-stu-id="cc285-127">In your application header file, include the following frequently used headers.</span></span>
```C++
    // Windows Header Files:
    #include <windows.h>

    // C RunTime Header Files:
    #include <stdlib.h>
    #include <malloc.h>
    #include <memory.h>
    #include <wchar.h>
    #include <math.h>

    #include <d2d1.h>
    #include <d2d1helper.h>
    #include <dwrite.h>
    #include <wincodec.h>
```

    

2.  <span data-ttu-id="cc285-128">Объявите дополнительные функции для освобождения интерфейсов и макросов для обработки ошибок и получения базового адреса модуля.</span><span class="sxs-lookup"><span data-stu-id="cc285-128">Declare additional functions for releasing interfaces and macros for error handling and retrieving the module's base address.</span></span>
```C++
    template<class Interface>
    inline void SafeRelease(
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
    #define Assert(b) do {if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}} while(0)
    #else
    #define Assert(b)
    #endif //DEBUG || _DEBUG
    #endif



    #ifndef HINST_THISCOMPONENT
    EXTERN_C IMAGE_DOS_HEADER __ImageBase;
    #define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
    #endif
```

    

3.  <span data-ttu-id="cc285-129">Объявите методы для инициализации класса, создания и отмены ресурсов, обработки цикла сообщений, отрисовки содержимого и процедуры Windows.</span><span class="sxs-lookup"><span data-stu-id="cc285-129">Declare methods for initializing the class, creating and discarding resources, handling the message loop, rendering content, and the windows procedure.</span></span>
```C++
    class DemoApp
    {
    public:
        DemoApp();
        ~DemoApp();

        // Register the window class and call methods for instantiating drawing resources
        HRESULT Initialize();

        // Process and dispatch messages
        void RunMessageLoop();

    private:
        // Initialize device-independent resources.
        HRESULT CreateDeviceIndependentResources();

        // Initialize device-dependent resources.
        HRESULT CreateDeviceResources();

        // Release device-dependent resource.
        void DiscardDeviceResources();

        // Draw content.
        HRESULT OnRender();

        // Resize the render target.
        void OnResize(
            UINT width,
            UINT height
            );

        // The windows procedure.
        static LRESULT CALLBACK WndProc(
            HWND hWnd,
            UINT message,
            WPARAM wParam,
            LPARAM lParam
            );

    
};
```



    

4.  <span data-ttu-id="cc285-130">Объявите указатели для объекта [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , объекта [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) и двух объектов [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) в качестве членов класса.</span><span class="sxs-lookup"><span data-stu-id="cc285-130">Declare pointers for an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object, and two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) objects as class members.</span></span>
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a><span data-ttu-id="cc285-131">Часть 2. Реализация инфраструктуры класса</span><span class="sxs-lookup"><span data-stu-id="cc285-131">Part 2: Implement the Class Infrastructure</span></span>

<span data-ttu-id="cc285-132">В этой части реализуется конструктор и деструктор DemoApp, методы циклов инициализации и обработки сообщений, а также функция WinMain.</span><span class="sxs-lookup"><span data-stu-id="cc285-132">In this part, you implement the DemoApp constructor and destructor, its initialization and message looping methods, and the WinMain function.</span></span> <span data-ttu-id="cc285-133">Большинство этих методов выглядят так же, как и в любом другом приложении Win32.</span><span class="sxs-lookup"><span data-stu-id="cc285-133">Most of these methods look the same as those found in any other Win32 application.</span></span> <span data-ttu-id="cc285-134">Единственным исключением является метод Initialize, который вызывает метод Креатедевицеиндепендентресаурцес (определяемый в следующей части), который создает несколько ресурсов Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cc285-134">The only exception is the Initialize method, which calls the CreateDeviceIndependentResources method (which you define in the next part) that creates several Direct2D resources.</span></span>

1.  <span data-ttu-id="cc285-135">В файле реализации класса реализуйте конструктор класса и деструктор.</span><span class="sxs-lookup"><span data-stu-id="cc285-135">In the class implementation file, implement the class constructor and destructor.</span></span> <span data-ttu-id="cc285-136">Конструктор должен инициализировать свои члены **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="cc285-136">The constructor should initialize its members to **NULL**.</span></span> <span data-ttu-id="cc285-137">Деструктор должен освобождать любые интерфейсы, хранящиеся как члены класса.</span><span class="sxs-lookup"><span data-stu-id="cc285-137">The destructor should release any interfaces stored as class members.</span></span>
```C++
    DemoApp::DemoApp() :
        m_hwnd(NULL),
        m_pDirect2dFactory(NULL),
        m_pRenderTarget(NULL),
        m_pLightSlateGrayBrush(NULL),
        m_pCornflowerBlueBrush(NULL)
    {
    }

    
DemoApp::~DemoApp()
    {
        SafeRelease(&m_pDirect2dFactory);
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);

    }
```



    

2.  <span data-ttu-id="cc285-138">Реализуйте метод DemoApp:: Рунмессажелуп, который преобразует и отправляет сообщения.</span><span class="sxs-lookup"><span data-stu-id="cc285-138">Implement the DemoApp::RunMessageLoop method that translates and dispatches messages.</span></span>
```C++
    void DemoApp::RunMessageLoop()
    {
        MSG msg;

        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```

    

3.  <span data-ttu-id="cc285-139">Реализуйте метод Initialize, который создает окно, отображает его и вызывает метод DemoApp:: Креатедевицеиндепендентресаурцес.</span><span class="sxs-lookup"><span data-stu-id="cc285-139">Implement the Initialize method that creates the window, shows it, and calls the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="cc285-140">Метод Креатедевицеиндепендентресаурцес реализуется в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="cc285-140">You implement the CreateDeviceIndependentResources method in the next section.</span></span>
```C++
    HRESULT DemoApp::Initialize()
    {
        HRESULT hr;

        // Initialize device-indpendent resources, such
        // as the Direct2D factory.
        hr = CreateDeviceIndependentResources();

        if (SUCCEEDED(hr))
        {
            // Register the window class.
            WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
            wcex.style         = CS_HREDRAW | CS_VREDRAW;
            wcex.lpfnWndProc   = DemoApp::WndProc;
            wcex.cbClsExtra    = 0;
            wcex.cbWndExtra    = sizeof(LONG_PTR);
            wcex.hInstance     = HINST_THISCOMPONENT;
            wcex.hbrBackground = NULL;
            wcex.lpszMenuName  = NULL;
            wcex.hCursor       = LoadCursor(NULL, IDI_APPLICATION);
            wcex.lpszClassName = L"D2DDemoApp";

            RegisterClassEx(&wcex);


            // Because the CreateWindow function takes its size in pixels,
            // obtain the system DPI and use it to scale the window size.
            FLOAT dpiX, dpiY;

            // The factory returns the current system DPI. This is also the value it will use
            // to create its own windows.
            m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


            // Create the window.
            m_hwnd = CreateWindow(
                L"D2DDemoApp",
                L"Direct2D Demo App",
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
            }
        }

        return hr;
    }
```

    

4.  <span data-ttu-id="cc285-141">Создайте метод WinMain, который выступает в качестве точки входа приложения.</span><span class="sxs-lookup"><span data-stu-id="cc285-141">Create the WinMain method that serves as the application entry point.</span></span> <span data-ttu-id="cc285-142">Инициализируйте экземпляр класса DemoApp и начните его цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc285-142">Initialize an instance of the DemoApp class and begin its message loop.</span></span>
```C++
    int WINAPI WinMain(
        HINSTANCE /* hInstance */,
        HINSTANCE /* hPrevInstance */,
        LPSTR /* lpCmdLine */,
        int /* nCmdShow */
        )
    {
        // Use HeapSetInformation to specify that the process should
        // terminate if the heap manager detects an error in any heap used
        // by the process.
        // The return value is ignored, because we want to continue running in the
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
```

    

## <a name="part-3-create-direct2d-resources"></a><span data-ttu-id="cc285-143">Часть 3. Создание ресурсов Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc285-143">Part 3: Create Direct2D Resources</span></span>

<span data-ttu-id="cc285-144">В этой части создаются ресурсы Direct2D, которые используются для рисования.</span><span class="sxs-lookup"><span data-stu-id="cc285-144">In this part, you create the Direct2D resources that you use to draw.</span></span> <span data-ttu-id="cc285-145">Direct2D предоставляет два типа ресурсов: ресурсы, независимые от устройства, которые могут быть в последнее время в течение всего приложения, и ресурсы, зависящие от устройства.</span><span class="sxs-lookup"><span data-stu-id="cc285-145">Direct2D provides two types of resources: device-independent resources that can last for the duration of the application, and device-dependent resources.</span></span> <span data-ttu-id="cc285-146">Ресурсы, зависящие от устройства, связаны с конкретным устройством отрисовки и перестают функционировать, если это устройство будет удалено.</span><span class="sxs-lookup"><span data-stu-id="cc285-146">Device-dependent resources are associated with a particular rendering device and will cease to function if that device is removed.</span></span>

1.  <span data-ttu-id="cc285-147">Реализуйте метод DemoApp:: Креатедевицеиндепендентресаурцес.</span><span class="sxs-lookup"><span data-stu-id="cc285-147">Implement the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="cc285-148">В методе создайте [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), аппаратно-независимый ресурс для создания других ресурсов Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cc285-148">In the method, create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), a device-independent resource, for creating other Direct2D resources.</span></span> <span data-ttu-id="cc285-149">Используйте член класса **m \_ pDirect2DdFactory** для хранения фабрики.</span><span class="sxs-lookup"><span data-stu-id="cc285-149">Use the **m\_pDirect2DdFactory** class member to store the factory.</span></span>
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  <span data-ttu-id="cc285-150">Реализуйте метод DemoApp:: Креатедевицересаурцес.</span><span class="sxs-lookup"><span data-stu-id="cc285-150">Implement the DemoApp::CreateDeviceResources method.</span></span> <span data-ttu-id="cc285-151">Этот метод создает ресурсы окна, зависящие от устройства, цель отрисовки и две кисти.</span><span class="sxs-lookup"><span data-stu-id="cc285-151">This method creates the window's device-dependent resources, a render target, and two brushes.</span></span> <span data-ttu-id="cc285-152">Получите размер клиентской области и создайте [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) с тем же размером, который визуализируется в **HWND** окна.</span><span class="sxs-lookup"><span data-stu-id="cc285-152">Retrieve the size of the client area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of the same size that renders to the window's **HWND**.</span></span> <span data-ttu-id="cc285-153">Сохраните целевой объект отрисовки в элементе класса **m \_ прендертаржет** .</span><span class="sxs-lookup"><span data-stu-id="cc285-153">Store the render target in the **m\_pRenderTarget** class member.</span></span>
```C++
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );
    
```

    

3.  <span data-ttu-id="cc285-154">Используйте целевой объект Render для создания серого [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) и Васильковый Blue **ID2D1SolidColorBrush**.</span><span class="sxs-lookup"><span data-stu-id="cc285-154">Use the render target to create a gray [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) and a cornflower blue **ID2D1SolidColorBrush**.</span></span>
```C++
            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
```

    

4.  <span data-ttu-id="cc285-155">Поскольку этот метод будет вызываться повторно, добавьте оператор if, чтобы проверить, существует ли уже целевой объект прорисовки (**m \_ прендертаржет** ).</span><span class="sxs-lookup"><span data-stu-id="cc285-155">Because this method will be called repeatedly, add an if statement to check whether the render target (**m\_pRenderTarget** ) already exists.</span></span> <span data-ttu-id="cc285-156">В следующем коде показан полный метод Креатедевицересаурцес.</span><span class="sxs-lookup"><span data-stu-id="cc285-156">The following code shows the complete CreateDeviceResources method.</span></span>
```C++
    HRESULT DemoApp::CreateDeviceResources()
    {
        HRESULT hr = S_OK;

        if (!m_pRenderTarget)
        {
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );


            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
        }

        return hr;
    }
```

    

5.  <span data-ttu-id="cc285-157">Реализуйте метод DemoApp::D Искарддевицересаурцес.</span><span class="sxs-lookup"><span data-stu-id="cc285-157">Implement the DemoApp::DiscardDeviceResources method.</span></span> <span data-ttu-id="cc285-158">В этом методе Освободите целевой объект отрисовки и две кисти, созданные в методе DemoApp:: Креатедевицересаурцес.</span><span class="sxs-lookup"><span data-stu-id="cc285-158">In this method, release the render target and the two brushes you created in the DemoApp::CreateDeviceResources method.</span></span>
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a><span data-ttu-id="cc285-159">Часть 4. прорисовка содержимого Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc285-159">Part 4: Render Direct2D Content</span></span>

<span data-ttu-id="cc285-160">В этой части реализуется процедура Windows, метод OnRender, который Закрашивает содержимое, и метод Онресизе, который корректирует размер целевого объекта отрисовки при изменении размера окна.</span><span class="sxs-lookup"><span data-stu-id="cc285-160">In this part, you implement the windows procedure, the OnRender method that paints content, and the OnResize method that adjusts the size of the render target when the window is resized.</span></span>

1.  <span data-ttu-id="cc285-161">Реализуйте метод DemoApp:: WndProc для управления сообщениями окна.</span><span class="sxs-lookup"><span data-stu-id="cc285-161">Implement the DemoApp::WndProc method to handle window messages.</span></span> <span data-ttu-id="cc285-162">Для сообщения [**с \_ размером WM**](../winmsg/wm-size.md) вызовите метод DemoApp:: онресизе и передайте ему новую ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="cc285-162">For the [**WM\_SIZE**](../winmsg/wm-size.md) message, call the DemoApp::OnResize method and pass it the new width and height.</span></span> <span data-ttu-id="cc285-163">Для сообщений [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) и [**WM \_ дисплайчанже**](/windows/desktop/gdi/wm-displaychange) вызовите метод DemoApp:: OnRender, чтобы закрасить окно.</span><span class="sxs-lookup"><span data-stu-id="cc285-163">For the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) messages, call the DemoApp::OnRender method to paint the window.</span></span> <span data-ttu-id="cc285-164">Методы OnRender и Онресизе реализуются в следующих шагах.</span><span class="sxs-lookup"><span data-stu-id="cc285-164">You implement the OnRender and OnResize methods in the steps that follow.</span></span>
```C++
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
                reinterpret_cast<LONG_PTR>(pDemoApp)
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
                case WM_SIZE:
                    {
                        UINT width = LOWORD(lParam);
                        UINT height = HIWORD(lParam);
                        pDemoApp->OnResize(width, height);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DISPLAYCHANGE:
                    {
                        InvalidateRect(hwnd, NULL, FALSE);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_PAINT:
                    {
                        pDemoApp->OnRender();
                        ValidateRect(hwnd, NULL);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DESTROY:
                    {
                        PostQuitMessage(0);
                    }
                    result = 1;
                    wasHandled = true;
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
    
```

    

2.  <span data-ttu-id="cc285-165">Реализуйте метод DemoApp:: OnRender.</span><span class="sxs-lookup"><span data-stu-id="cc285-165">Implement the DemoApp::OnRender method.</span></span> <span data-ttu-id="cc285-166">Сначала создайте **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cc285-166">First, create an **HRESULT**.</span></span> <span data-ttu-id="cc285-167">Затем вызовите метод Креатедевицересаурце.</span><span class="sxs-lookup"><span data-stu-id="cc285-167">Then call the CreateDeviceResource method.</span></span> <span data-ttu-id="cc285-168">Этот метод вызывается каждый раз при рисовании окна.</span><span class="sxs-lookup"><span data-stu-id="cc285-168">This method is called every time the window is painted.</span></span> <span data-ttu-id="cc285-169">Вспомним, что на шаге 4 части 3 был добавлен оператор **If** , чтобы метод не выполнял никакой работы, если целевой объект прорисовки уже существует.</span><span class="sxs-lookup"><span data-stu-id="cc285-169">Recall that, in step 4 of Part 3, you added an **if** statement to prevent the method from doing any work if the render target already exists.</span></span>
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  <span data-ttu-id="cc285-170">Убедитесь, что метод Креатедевицересаурце был создан.</span><span class="sxs-lookup"><span data-stu-id="cc285-170">Verify that the CreateDeviceResource method succeeded.</span></span> <span data-ttu-id="cc285-171">Если это не так, никакие рисунки не выполняются.</span><span class="sxs-lookup"><span data-stu-id="cc285-171">If it didn't, don't perform any drawing.</span></span>
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  <span data-ttu-id="cc285-172">В только что созданном операторе **If** инициируйте рисование, вызвав метод бегиндрав целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="cc285-172">Inside the **if** statement you just created, initiate drawing by calling the render target's BeginDraw method.</span></span> <span data-ttu-id="cc285-173">Задайте преобразование целевого объекта отрисовки в матрицу идентификаторов и очистите окно.</span><span class="sxs-lookup"><span data-stu-id="cc285-173">Set the render target's transform to the identity matrix, and clear the window.</span></span>
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  <span data-ttu-id="cc285-174">Получение размера области рисования.</span><span class="sxs-lookup"><span data-stu-id="cc285-174">Retrieve the size of the drawing area.</span></span>
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  <span data-ttu-id="cc285-175">Рисование фона сетки с помощью цикла **for** и метода [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) целевого объекта прорисовки для рисования ряда линий.</span><span class="sxs-lookup"><span data-stu-id="cc285-175">Draw a grid background by using a **for** loop and the render target's [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) method to draw a series of lines.</span></span>
```C++
            // Draw a grid background.
            int width = static_cast<int>(rtSize.width);
            int height = static_cast<int>(rtSize.height);

            for (int x = 0; x < width; x += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                    D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }

            for (int y = 0; y < height; y += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                    D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }
```

    

7.  <span data-ttu-id="cc285-176">Создайте два прямоугольных примитива, центрированных на экране.</span><span class="sxs-lookup"><span data-stu-id="cc285-176">Create two rectangle primitives that are centered on the screen.</span></span>
```C++
            // Draw two rectangles.
            D2D1_RECT_F rectangle1 = D2D1::RectF(
                rtSize.width/2 - 50.0f,
                rtSize.height/2 - 50.0f,
                rtSize.width/2 + 50.0f,
                rtSize.height/2 + 50.0f
                );

            D2D1_RECT_F rectangle2 = D2D1::RectF(
                rtSize.width/2 - 100.0f,
                rtSize.height/2 - 100.0f,
                rtSize.width/2 + 100.0f,
                rtSize.height/2 + 100.0f
                );
    
```

    

8.  <span data-ttu-id="cc285-177">Используйте метод [**филлректангле**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) целевого объекта рендеринга для заполнения внутренней части первого прямоугольника серой кистью.</span><span class="sxs-lookup"><span data-stu-id="cc285-177">Use the render target's [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the first rectangle with the gray brush.</span></span>
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  <span data-ttu-id="cc285-178">Используйте метод [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) целевого объекта рендеринга, чтобы закрасить контур второго прямоугольника с помощью синей кисти Васильковый.</span><span class="sxs-lookup"><span data-stu-id="cc285-178">Use the render target's [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the second rectangle with the cornflower blue brush.</span></span>
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. <span data-ttu-id="cc285-179">Вызовите метод [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="cc285-179">Call the render target's [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="cc285-180">Метод **EndDraw** возвращает **значение HRESULT** , указывающее, были ли операции рисования успешными.</span><span class="sxs-lookup"><span data-stu-id="cc285-180">The **EndDraw** method returns an **HRESULT** to indicate whether the drawing operations were successful.</span></span> <span data-ttu-id="cc285-181">Закройте оператор **If** , который вы начали на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="cc285-181">Close the **if** statement you began in Step 3.</span></span>
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. <span data-ttu-id="cc285-182">Проверьте **значение HRESULT** , возвращенное [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="cc285-182">Check the **HRESULT** returned by [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span> <span data-ttu-id="cc285-183">Если он указывает на необходимость повторного создания целевого объекта отрисовки, вызовите метод DemoApp::D Искарддевицересаурцес, чтобы освободить его. Он будет создан заново при следующем получении сообщения [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) или [**WM \_ дисплайчанже**](/windows/desktop/gdi/wm-displaychange) .</span><span class="sxs-lookup"><span data-stu-id="cc285-183">If it indicates that the render target needs to be recreated, call the DemoApp::DiscardDeviceResources method to release it; it will be recreated the next time the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) or [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span>
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. <span data-ttu-id="cc285-184">Возвращайте значение **HRESULT** и закройте метод.</span><span class="sxs-lookup"><span data-stu-id="cc285-184">Return the **HRESULT** and close the method.</span></span>
```C++
        return hr;
    }
```

    

13. <span data-ttu-id="cc285-185">Реализуйте метод DemoApp:: Онресизе, чтобы он изменяет размер целевого объекта отрисовки на новый размер окна.</span><span class="sxs-lookup"><span data-stu-id="cc285-185">Implement the DemoApp::OnResize method so that it resizes the render target to the new size of the window.</span></span>
```C++
    void DemoApp::OnResize(UINT width, UINT height)
    {
        if (m_pRenderTarget)
        {
            // Note: This method can fail, but it's okay to ignore the
            // error here, because the error will be returned again
            // the next time EndDraw is called.
            m_pRenderTarget->Resize(D2D1::SizeU(width, height));
        }
    }
```

    

<span data-ttu-id="cc285-186">Вы завершили работу с руководством.</span><span class="sxs-lookup"><span data-stu-id="cc285-186">You've completed the tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="cc285-187">Чтобы использовать Direct2D, убедитесь, что приложение содержит файл заголовка D2D1. h и компилируется в библиотеке D2D1. lib.</span><span class="sxs-lookup"><span data-stu-id="cc285-187">To use Direct2D, ensure that your application includes the d2d1.h header file and compiles against the d2d1.lib library.</span></span> <span data-ttu-id="cc285-188">В [пакете средств разработки программного обеспечения (SDK) для Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx)можно найти D2D1. h и D2D1. lib.</span><span class="sxs-lookup"><span data-stu-id="cc285-188">You can find d2d1.h and d2d1.lib in [Windows Software Development Kit (SDK) for Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

 

## <a name="summary"></a><span data-ttu-id="cc285-189">Сводка</span><span class="sxs-lookup"><span data-stu-id="cc285-189">Summary</span></span>

<span data-ttu-id="cc285-190">В этом руководстве вы узнали, как создавать ресурсы Direct2D и вырисовывать базовые фигуры.</span><span class="sxs-lookup"><span data-stu-id="cc285-190">In this tutorial, you learned how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="cc285-191">Вы также узнали, как структурировать приложение, чтобы повысить производительность, минимизируя создание ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc285-191">You also learned how to structure your application to enhance performance by minimizing resource creation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc285-192">См. также</span><span class="sxs-lookup"><span data-stu-id="cc285-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc285-193">Обзор API Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc285-193">Direct2D API Overview</span></span>](the-direct2d-api.md)
</dt> <dt>

[<span data-ttu-id="cc285-194">Повышение производительности Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc285-194">Improving the Performance of Direct2D</span></span>](improving-direct2d-performance.md)
</dt> </dl>

 

 