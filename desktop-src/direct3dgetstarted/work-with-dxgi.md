---
title: Работа с ресурсами устройств DirectX
description: Изучите роль графической инфраструктуры Microsoft DirectX (DXGI) в игре Windows Store DirectX.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096e2be6f957d99bc6e5055f845c14448ecd647f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487932"
---
# <a name="work-with-directx-device-resources"></a><span data-ttu-id="2c290-103">Работа с ресурсами устройств DirectX</span><span class="sxs-lookup"><span data-stu-id="2c290-103">Work with DirectX device resources</span></span>

<span data-ttu-id="2c290-104">Изучите роль графической инфраструктуры Microsoft DirectX (DXGI) в игре Windows Store DirectX.</span><span class="sxs-lookup"><span data-stu-id="2c290-104">Understand the role of the Microsoft DirectX Graphics Infrastructure (DXGI) in your Windows Store DirectX game.</span></span> <span data-ttu-id="2c290-105">DXGI — это набор API-интерфейсов, используемых для настройки и управления ресурсами графических и графических адаптеров низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="2c290-105">DXGI is a set of APIs used to configure and manage low-level graphics and graphics adapter resources.</span></span> <span data-ttu-id="2c290-106">Без этого у вас не будет возможности нарисовать графику игры в окне.</span><span class="sxs-lookup"><span data-stu-id="2c290-106">Without it, you'd have no way to draw your game's graphics to a window.</span></span>

<span data-ttu-id="2c290-107">Представьте себе DXGI таким образом: для прямого доступа к GPU и управления его ресурсами необходимо иметь способ описать его в приложении.</span><span class="sxs-lookup"><span data-stu-id="2c290-107">Think of DXGI this way: to directly access the GPU and manage its resources, you must have a way to describe it to your app.</span></span> <span data-ttu-id="2c290-108">Наиболее важной частью информации, необходимой для GPU, является место для рисования пикселов, которое может посылать эти пиксели на экран.</span><span class="sxs-lookup"><span data-stu-id="2c290-108">The most important piece of info you need about the GPU is the place to draw pixels so it can send those pixels to the screen.</span></span> <span data-ttu-id="2c290-109">Обычно это называется "задним буфером" — расположением в памяти GPU, в котором можно рисовать Пиксели, а затем развернутым или перенаправленным, а также отправкой на экран сигнала обновления.</span><span class="sxs-lookup"><span data-stu-id="2c290-109">Typically this is called the "back buffer"—a location in GPU memory where you can draw the pixels and then have it "flipped" or "swapped" and sent to the screen on a refresh signal.</span></span> <span data-ttu-id="2c290-110">DXGI позволяет получить это расположение и использовать этот буфер (называемый *цепочкой подкачки* , так как он является цепочкой буферов, поддерживающих буферизацию, что позволяет применять несколько стратегий использования буферов).</span><span class="sxs-lookup"><span data-stu-id="2c290-110">DXGI lets you acquire that location and the means to use that buffer (called a *swap chain* because it is a chain of swappable buffers, allowing for multiple buffering strategies).</span></span>

<span data-ttu-id="2c290-111">Для этого требуется доступ для записи в цепочку буферов и маркер окна, в котором будет отображаться текущий задний буфер для цепочки буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="2c290-111">To do this, you need access to write to the swap chain, and a handle to the window that will display the current back buffer for the swap chain.</span></span> <span data-ttu-id="2c290-112">Кроме того, необходимо подключить эти два объекта, чтобы операционная система обновляла окно с содержимым заднего буфера при запросе.</span><span class="sxs-lookup"><span data-stu-id="2c290-112">You also need to connect the two to ensure that the operating system will refresh the window with the contents of the back buffer when you request it to do so.</span></span>

<span data-ttu-id="2c290-113">Общий процесс рисования на экране выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2c290-113">The overall process for drawing to the screen is as follows:</span></span>

-   <span data-ttu-id="2c290-114">Получите [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) для своего приложения.</span><span class="sxs-lookup"><span data-stu-id="2c290-114">Get a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) for your app.</span></span>
-   <span data-ttu-id="2c290-115">Получите интерфейс для устройства и контекста Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2c290-115">Get an interface for the Direct3D device and context.</span></span>
-   <span data-ttu-id="2c290-116">Создайте цепочку буферов для отображения подготовленного образа в [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="2c290-116">Create the swap chain to display your rendered image in the [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>
-   <span data-ttu-id="2c290-117">Создайте целевой объект отрисовки для рисования и заполните его пикселами.</span><span class="sxs-lookup"><span data-stu-id="2c290-117">Create a render target for drawing and populate it with pixels.</span></span>
-   <span data-ttu-id="2c290-118">Представьте цепочку буферов.</span><span class="sxs-lookup"><span data-stu-id="2c290-118">Present the swap chain!</span></span>

## <a name="create-a-window-for-your-app"></a><span data-ttu-id="2c290-119">Создание окна для приложения</span><span class="sxs-lookup"><span data-stu-id="2c290-119">Create a window for your app</span></span>

<span data-ttu-id="2c290-120">Первое, что нам нужно сделать, — это создать окно.</span><span class="sxs-lookup"><span data-stu-id="2c290-120">The first thing we need to do is create a window.</span></span> <span data-ttu-id="2c290-121">Сначала создайте класс окна, заполнив экземпляр [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa), а затем зарегистрируйте его с помощью [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="2c290-121">First, create a window class by populating an instance of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa), then register it using [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="2c290-122">Класс Window содержит ключевые свойства окна, включая используемый им значок, функцию обработки статических сообщений (Подробнее об этом позже) и уникальное имя класса Window.</span><span class="sxs-lookup"><span data-stu-id="2c290-122">The window class contains essential properties of the window, including the icon it uses, the static message processing function (more on this later), and a unique name for the window class.</span></span>


```C++
if(m_hInstance == NULL) 
    m_hInstance = (HINSTANCE)GetModuleHandle(NULL);

HICON hIcon = NULL;
WCHAR szExePath[MAX_PATH];
    GetModuleFileName(NULL, szExePath, MAX_PATH);

// If the icon is NULL, then use the first one found in the exe
if(hIcon == NULL)
    hIcon = ExtractIcon(m_hInstance, szExePath, 0); 

// Register the windows class
WNDCLASS wndClass;
wndClass.style = CS_DBLCLKS;
wndClass.lpfnWndProc = MainClass::StaticWindowProc;
wndClass.cbClsExtra = 0;
wndClass.cbWndExtra = 0;
wndClass.hInstance = m_hInstance;
wndClass.hIcon = hIcon;
wndClass.hCursor = LoadCursor(NULL, IDC_ARROW);
wndClass.hbrBackground = (HBRUSH)GetStockObject(BLACK_BRUSH);
wndClass.lpszMenuName = NULL;
wndClass.lpszClassName = m_windowClassName.c_str();

if(!RegisterClass(&wndClass))
{
    DWORD dwError = GetLastError();
    if(dwError != ERROR_CLASS_ALREADY_EXISTS)
        return HRESULT_FROM_WIN32(dwError);
}
```



<span data-ttu-id="2c290-123">Затем создайте окно.</span><span class="sxs-lookup"><span data-stu-id="2c290-123">Next, you create the window.</span></span> <span data-ttu-id="2c290-124">Также необходимо предоставить сведения о размере окна и имени только что созданного класса Window.</span><span class="sxs-lookup"><span data-stu-id="2c290-124">We also need to provide size information for the window and the name of the window class we just created.</span></span> <span data-ttu-id="2c290-125">При вызове [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa)возвращается непрозрачный указатель на окно, именуемое HWND; необходимо будет оставаться указателем HWND и использовать его каждый раз, когда необходимо ссылаться на окно, включая его удаление или повторное создание, а также (особенно важно) при создании цепочки подкачки DXGI, используемой для рисования в окне.</span><span class="sxs-lookup"><span data-stu-id="2c290-125">When you call [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), you get back an opaque pointer to the window called an HWND; you'll need to keep the HWND pointer and use it any time you need to reference the window, including destroying or recreating it, and (especially important) when creating the DXGI swap chain you use to draw in the window.</span></span>


```C++
m_rc;
int x = CW_USEDEFAULT;
int y = CW_USEDEFAULT;

// No menu in this example.
m_hMenu = NULL;

// This example uses a non-resizable 640 by 480 viewport for simplicity.
int nDefaultWidth = 640;
int nDefaultHeight = 480;
SetRect(&m_rc, 0, 0, nDefaultWidth, nDefaultHeight);        
AdjustWindowRect(
    &m_rc,
    WS_OVERLAPPEDWINDOW,
    (m_hMenu != NULL) ? true : false
    );

// Create the window for our viewport.
m_hWnd = CreateWindow(
    m_windowClassName.c_str(),
    L"Cube11",
    WS_OVERLAPPEDWINDOW,
    x, y,
    (m_rc.right-m_rc.left), (m_rc.bottom-m_rc.top),
    0,
    m_hMenu,
    m_hInstance,
    0
    );

if(m_hWnd == NULL)
{
    DWORD dwError = GetLastError();
    return HRESULT_FROM_WIN32(dwError);
}
```



<span data-ttu-id="2c290-126">Модель классического приложения Windows включает в цикл обработки сообщений Windows обработчик.</span><span class="sxs-lookup"><span data-stu-id="2c290-126">The Windows desktop app model includes a hook into the Windows message loop.</span></span> <span data-ttu-id="2c290-127">Необходимо создать основной цикл программы для этого обработчика, написав функцию "Статиквиндовпрок" для обработки оконных событий.</span><span class="sxs-lookup"><span data-stu-id="2c290-127">You'll need to base your main program loop off of this hook by writing a "StaticWindowProc" function to process windowing events.</span></span> <span data-ttu-id="2c290-128">Это должна быть статическая функция, так как Windows будет вызывать ее за пределами контекста любого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="2c290-128">This must be a static function because Windows will call it outside of the context of any class instance.</span></span> <span data-ttu-id="2c290-129">Вот очень простой пример функции обработки статических сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c290-129">Here's a very simple example of a static message processing function.</span></span>


```C++
LRESULT CALLBACK MainClass::StaticWindowProc(
    HWND hWnd,
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam
    )
{
    switch(uMsg)
    {
        case WM_CLOSE:
        {
            HMENU hMenu;
            hMenu = GetMenu(hWnd);
            if (hMenu != NULL)
            {
                DestroyMenu(hMenu);
            }
            DestroyWindow(hWnd);
            UnregisterClass(
                m_windowClassName.c_str(),
                m_hInstance
                );
            return 0;
        }

        case WM_DESTROY:
            PostQuitMessage(0);
            break;
    }
    
    return DefWindowProc(hWnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="2c290-130">В этом простом примере выполняется проверка только условий выхода программы: [**WM \_ Close**](/windows/desktop/winmsg/wm-close), Sent, когда запрашивается закрытие окна, и [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy), который отправляется после фактического удаления окна с экрана.</span><span class="sxs-lookup"><span data-stu-id="2c290-130">This simple example only checks for program exit conditions: [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), sent when the window is requested to be closed, and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy), which is sent after the window is actually removed from the screen.</span></span> <span data-ttu-id="2c290-131">Полное, рабочее приложение также должно работать с другими событиями окон, а полный список событий для окон см. в разделе [уведомления окна](/windows/desktop/winmsg/window-notifications).</span><span class="sxs-lookup"><span data-stu-id="2c290-131">A full, production app needs to handle other windowing events too—for the complete list of windowing events, see [Window Notifications](/windows/desktop/winmsg/window-notifications).</span></span>

<span data-ttu-id="2c290-132">Основной цикл программы должен подтвердить сообщения Windows, разрешая Windows выполнить статическую процедуру сообщения.</span><span class="sxs-lookup"><span data-stu-id="2c290-132">The main program loop itself needs to acknowledge Windows messages by allowing Windows the opportunity to run the static message proc.</span></span> <span data-ttu-id="2c290-133">Помогите программе работать эффективно, развилкая поведение. Каждая итерация должна выбрать обработку новых сообщений Windows, если они доступны, и если в очереди нет сообщений, они должны визуализировать новый кадр.</span><span class="sxs-lookup"><span data-stu-id="2c290-133">Help the program run efficiently by forking the behavior: each iteration should choose to process new Windows messages if they are available, and if no messages are in the queue it should render a new frame.</span></span> <span data-ttu-id="2c290-134">Вот очень простой пример:</span><span class="sxs-lookup"><span data-stu-id="2c290-134">Here's a very simple example:</span></span>


```C++
bool bGotMsg;
MSG  msg;
msg.message = WM_NULL;
PeekMessage(&msg, NULL, 0U, 0U, PM_NOREMOVE);

while (WM_QUIT != msg.message)
{
    // Process window events.
    // Use PeekMessage() so we can use idle time to render the scene. 
    bGotMsg = (PeekMessage(&msg, NULL, 0U, 0U, PM_REMOVE) != 0);

    if (bGotMsg)
    {
        // Translate and dispatch the message
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
    else
    {
        // Update the scene.
        renderer->Update();

        // Render frames during idle time (when no messages are waiting).
        renderer->Render();

        // Present the frame to the screen.
        deviceResources->Present();
    }
}
```



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a><span data-ttu-id="2c290-135">Получение интерфейса для устройства и контекста Direct3D</span><span class="sxs-lookup"><span data-stu-id="2c290-135">Get an interface for the Direct3D device and context</span></span>

<span data-ttu-id="2c290-136">Первым шагом при использовании Direct3D является получение интерфейса для аппаратного обеспечения Direct3D (GPU), представленного в виде экземпляров [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) и [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2).</span><span class="sxs-lookup"><span data-stu-id="2c290-136">The first step to using Direct3D is to acquire an interface for the Direct3D hardware (the GPU), represented as instances of [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2).</span></span> <span data-ttu-id="2c290-137">Первое — это виртуальное представление ресурсов GPU, а второе — независимая от устройства абстракция конвейера и процесса отрисовки.</span><span class="sxs-lookup"><span data-stu-id="2c290-137">The former is a virtual representation of the GPU resources, and the latter is a device-agnostic abstraction of the rendering pipeline and process.</span></span> <span data-ttu-id="2c290-138">Вот простой способ представить его: **ID3D11Device** содержит графические методы, которые вызываются редко, как правило, перед отрисовкой, чтобы получить и настроить набор ресурсов, необходимых для начала рисования пикселов.</span><span class="sxs-lookup"><span data-stu-id="2c290-138">Here's an easy way to think of it: **ID3D11Device** contains the graphics methods you call infrequently, usually before any rendering occurs, to acquire and configure the set of resources you need to start drawing pixels.</span></span> <span data-ttu-id="2c290-139">**Ссылку ID3D11DeviceContext**, с другой стороны, содержит методы, которые вызывают каждый кадр: Загрузка в буферах и представлениях и других ресурсах, изменение состояния вывода и прорисовки, управление шейдерами, а также рисование результатов передачи этих ресурсов с помощью состояний и шейдеров.</span><span class="sxs-lookup"><span data-stu-id="2c290-139">**ID3D11DeviceContext**, on the other hand, contains the methods you call every frame: loading in buffers and views and other resources, changing output-merger and rasterizer state, managing shaders, and drawing the results of passing those resources through the states and shaders.</span></span>

<span data-ttu-id="2c290-140">Существует одна очень важная часть этого процесса: Настройка уровня компонента.</span><span class="sxs-lookup"><span data-stu-id="2c290-140">There's one very important part of this process: setting the feature level.</span></span> <span data-ttu-id="2c290-141">Уровень компонентов указывает DirectX на минимальную версию оборудования, поддерживаемого приложением, с \_ уровнем D3D \_ уровня \_ 9 \_ 1 минимальным набором функций и \_ уровнем возможностей \_ D3D \_ 11 \_ 1 в качестве текущего самого высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="2c290-141">The feature level tells DirectX the minimum level of hardware your app supports, with D3D\_FEATURE\_LEVEL\_9\_1 as the lowest feature set and D3D\_FEATURE\_LEVEL\_11\_1 as the current highest.</span></span> <span data-ttu-id="2c290-142">\_Если вы хотите получить доступ к самой широкой аудитории, в качестве минимума следует использовать 9 1.</span><span class="sxs-lookup"><span data-stu-id="2c290-142">You should support 9\_1 as the minimum if you want to reach the widest possible audience.</span></span> <span data-ttu-id="2c290-143">Уделите некоторое время для ознакомления с [уровнями функций](/previous-versions/windows/apps/hh994923(v=win.10)) Direct3D и оценки минимальных и максимальных уровней функций, которые должна поддерживать ваша игра, и для понимания возможных последствий.</span><span class="sxs-lookup"><span data-stu-id="2c290-143">Take some time to read up on Direct3D [feature levels](/previous-versions/windows/apps/hh994923(v=win.10)) and assess for yourself the minimum and maximum feature levels you want your game to support and to understand the implications of your choice.</span></span>

<span data-ttu-id="2c290-144">Получите ссылки (указатели) как для устройства Direct3D, так и для контекста устройства и сохраните их в виде переменных уровня класса в экземпляре **DeviceResources** (как смарт-указатели **ComPtr** ).</span><span class="sxs-lookup"><span data-stu-id="2c290-144">Obtain references (pointers) to both the Direct3D device and device context and store them as class-level variables on the **DeviceResources** instance (as **ComPtr** smart pointers).</span></span> <span data-ttu-id="2c290-145">Используйте эти ссылки при необходимости доступа к контексту устройства или устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2c290-145">Use these references whenever you need to access the Direct3D device or device context.</span></span>


```C++
D3D_FEATURE_LEVEL levels[] = {
    D3D_FEATURE_LEVEL_9_1,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_11_1
};

// This flag adds support for surfaces with a color-channel ordering different
// from the API default. It is required for compatibility with Direct2D.
UINT deviceFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;

#if defined(DEBUG) || defined(_DEBUG)
deviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif

// Create the Direct3D 11 API device object and a corresponding context.
Microsoft::WRL::ComPtr<ID3D11Device>        device;
Microsoft::WRL::ComPtr<ID3D11DeviceContext> context;

hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    deviceFlags,                // Set debug and Direct2D compatibility flags.
    levels,                     // List of feature levels this app can support.
    ARRAYSIZE(levels),          // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_featureLevel,            // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (FAILED(hr))
{
    // Handle device interface creation failure if it occurs.
    // For example, reduce the feature level requirement, or fail over 
    // to WARP rendering.
}

// Store pointers to the Direct3D 11.1 API device and immediate context.
device.As(&m_pd3dDevice);
context.As(&m_pd3dDeviceContext);
```



## <a name="create-the-swap-chain"></a><span data-ttu-id="2c290-146">Создание цепочки буферов</span><span class="sxs-lookup"><span data-stu-id="2c290-146">Create the swap chain</span></span>

<span data-ttu-id="2c290-147">Хорошо: у вас есть окно для рисования, и у вас есть интерфейс для отправки данных и предоставления команд GPU.</span><span class="sxs-lookup"><span data-stu-id="2c290-147">Okay: You have a window to draw in, and you have an interface to send data and give commands to the GPU.</span></span> <span data-ttu-id="2c290-148">Теперь давайте посмотрим, как их объединить.</span><span class="sxs-lookup"><span data-stu-id="2c290-148">Now let's see how to bring them together.</span></span>

<span data-ttu-id="2c290-149">Во первых, вы указываете DXGI, какие значения следует использовать для свойств цепочки буферов обмена.</span><span class="sxs-lookup"><span data-stu-id="2c290-149">First, you tell DXGI what values to use for the properties of the swap chain.</span></span> <span data-ttu-id="2c290-150">Это делается с помощью структуры для [**\_ \_ цепочки \_ буфера обмена DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) .</span><span class="sxs-lookup"><span data-stu-id="2c290-150">Do this using a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure.</span></span> <span data-ttu-id="2c290-151">Шесть полей особенно важны для классических приложений:</span><span class="sxs-lookup"><span data-stu-id="2c290-151">Six fields are particularly important for desktop apps:</span></span>

-   <span data-ttu-id="2c290-152">**Оконное**: указывает, находится ли цепочка подкачки в полноэкранном режиме или обрезана до окна.</span><span class="sxs-lookup"><span data-stu-id="2c290-152">**Windowed**: Indicates whether the swap chain is full-screen or clipped to the window.</span></span> <span data-ttu-id="2c290-153">Задайте значение TRUE, чтобы цепочка буфера обмена была размещена в созданном ранее окне.</span><span class="sxs-lookup"><span data-stu-id="2c290-153">Set this to TRUE to put the swap chain in the window you created earlier.</span></span>
-   <span data-ttu-id="2c290-154">**Буфферусаже**: задайте для этого параметра значение \_ Использование DXGI \_ \_ \_ . выходные данные целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="2c290-154">**BufferUsage**: Set this to DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT.</span></span> <span data-ttu-id="2c290-155">Это означает, что цепочка буфера обмена будет поверхностью рисования, что позволит использовать ее в качестве целевого объекта визуализации Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2c290-155">This indicates that the swap chain will be a drawing surface, allowing you to use it as a Direct3D render-target.</span></span>
-   <span data-ttu-id="2c290-156">**SwapEffect**: задайте для этого параметра \_ значение \_ отразить эффекты переключения DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2c290-156">**SwapEffect**: Set this to DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL.</span></span>
-   <span data-ttu-id="2c290-157">**Формат**: формат \_ B8G8R8A8 UNORM формата DXGI \_ \_ задает 32-разрядный цвет: 8 бит для каждого из трех цветовых каналов RGB и 8 бит для альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="2c290-157">**Format**: The DXGI\_FORMAT\_B8G8R8A8\_UNORM format specifies 32-bit color: 8 bits for each of the three RGB color channels, and 8 bits for the alpha channel.</span></span>
-   <span data-ttu-id="2c290-158">**BufferCount**: задайте значение 2 для традиционного двойного буферизации, чтобы избежать разрыва.</span><span class="sxs-lookup"><span data-stu-id="2c290-158">**BufferCount**: Set this to 2 for a traditional double-buffered behavior to avoid tearing.</span></span> <span data-ttu-id="2c290-159">Установите значение 3 для счетчика буферов, если содержимое графики занимает несколько циклов обновления монитора для отображения одного кадра (в 60 Гц, например, пороговое значение превышает 16 мс).</span><span class="sxs-lookup"><span data-stu-id="2c290-159">Set the buffer count to 3 if your graphics content takes more than one monitor refresh cycle to render a single frame (at 60 Hz for example, the threshold is more than 16 ms).</span></span>
-   <span data-ttu-id="2c290-160">**Сампледеск**: это поле управляет множественной выборкой.</span><span class="sxs-lookup"><span data-stu-id="2c290-160">**SampleDesc**: This field controls multisampling.</span></span> <span data-ttu-id="2c290-161">Задайте для **счетчика** значение 1 и **качество** , равное 0, для цепочек перестановки перелистывания моделей.</span><span class="sxs-lookup"><span data-stu-id="2c290-161">Set **Count** to 1 and **Quality** to 0 for flip-model swap chains.</span></span> <span data-ttu-id="2c290-162">(Чтобы использовать множественную выборку с цепочками перелистывания моделей, рисуйте на отдельном целевом объекте отрисовки с множественной выборкой, а затем разрешите эту цель в цепочку буферов непосредственно перед ее представлением.</span><span class="sxs-lookup"><span data-stu-id="2c290-162">(To use multisampling with flip-model swap chains, draw on a separate multisampled render target and then resolve that target to the swap chain just before presenting it.</span></span> <span data-ttu-id="2c290-163">Пример кода приведен в [многовыборочной выборки в приложениях для Магазина Windows](/previous-versions/windows/apps/dn458384(v=win.10)).)</span><span class="sxs-lookup"><span data-stu-id="2c290-163">Example code is provided in [Multisampling in Windows Store apps](/previous-versions/windows/apps/dn458384(v=win.10)).)</span></span>

<span data-ttu-id="2c290-164">После того как вы указали конфигурацию для цепочки буферов, необходимо использовать ту же фабрику DXGI, что и устройство Direct3D (и контекст устройства), чтобы создать цепочку буферов.</span><span class="sxs-lookup"><span data-stu-id="2c290-164">After you have specified a configuration for the swap chain, you must use the same DXGI factory that created the Direct3D device (and device context) in order to create the swap chain.</span></span>

<span data-ttu-id="2c290-165">**Краткая форма:  **</span><span class="sxs-lookup"><span data-stu-id="2c290-165">**Short form:  **</span></span>

<span data-ttu-id="2c290-166">Получите ссылку на [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) , созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="2c290-166">Get the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) reference you created previously.</span></span> <span data-ttu-id="2c290-167">Восведите его в [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (если вы еще этого не сделали), а затем вызовите [**идксгидевице::-Adapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) , чтобы получить адаптер DXGI.</span><span class="sxs-lookup"><span data-stu-id="2c290-167">Upcast it to [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (if you haven't already) and then call [**IDXGIDevice::GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) to acquire the DXGI adapter.</span></span> <span data-ttu-id="2c290-168">Получите родительскую фабрику для этого адаптера, вызвав [**IDXGIFactory2::**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) NoInherit ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) наследует от [**идксгиобжект**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)) — теперь вы можете использовать эту фабрику для создания цепочки буферов путем вызова [**креатесвапчаинфорхвнд**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="2c290-168">Get the parent factory for that adapter by calling [**IDXGIFactory2::GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) inherits from [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject))—now you can use that factory to create the swap chain by calling [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), as seen in the following code sample.</span></span>


```C++
DXGI_SWAP_CHAIN_DESC desc;
ZeroMemory(&desc, sizeof(DXGI_SWAP_CHAIN_DESC));
desc.Windowed = TRUE; // Sets the initial state of full-screen mode.
desc.BufferCount = 2;
desc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
desc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
desc.SampleDesc.Count = 1;      //multisampling setting
desc.SampleDesc.Quality = 0;    //vendor-specific flag
desc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL;
desc.OutputWindow = hWnd;

// Create the DXGI device object to use in other factories, such as Direct2D.
Microsoft::WRL::ComPtr<IDXGIDevice3> dxgiDevice;
m_pd3dDevice.As(&dxgiDevice);

// Create swap chain.
Microsoft::WRL::ComPtr<IDXGIAdapter> adapter;
Microsoft::WRL::ComPtr<IDXGIFactory> factory;

hr = dxgiDevice->GetAdapter(&adapter);

if (SUCCEEDED(hr))
{
    adapter->GetParent(IID_PPV_ARGS(&factory));

    hr = factory->CreateSwapChain(
        m_pd3dDevice.Get(),
        &desc,
        &m_pDXGISwapChain
        );
}
```



<span data-ttu-id="2c290-169">Если вы только начинаете, то, вероятно, лучше использовать описанную здесь конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="2c290-169">If you're just starting out, it's probably best to use the configuration shown here.</span></span> <span data-ttu-id="2c290-170">Теперь, если вы уже знакомы с предыдущими версиями DirectX, вы можете спросить: «почему мы не создаем устройство и цепочку буферов, вместо того чтобы проходить все эти классы?»</span><span class="sxs-lookup"><span data-stu-id="2c290-170">Now at this point, if you are already familiar with previous versions of DirectX you might be asking: "Why didn't we create the device and swap chain at the same time, instead of walking back through all of those classes?"</span></span> <span data-ttu-id="2c290-171">Ответ — это эффективность: цепочки обмена — это ресурсы устройства Direct3D, а ресурсы устройств привязаны к конкретному устройству Direct3D, которое их создало.</span><span class="sxs-lookup"><span data-stu-id="2c290-171">The answer is efficiency: swap chains are Direct3D device resources, and device resources are tied to the particular Direct3D device that created them.</span></span> <span data-ttu-id="2c290-172">При создании нового устройства с новой цепочкой подкачки необходимо повторно создать все ресурсы устройства с помощью нового устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2c290-172">If you create a new device with a new swap chain, you have to recreate all your device resources using the new Direct3D device.</span></span> <span data-ttu-id="2c290-173">Таким образом, создав цепочку подкачки с той же фабрикой (как показано выше), вы можете повторно создать цепочку буферов и продолжить использовать уже загруженные ресурсы устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2c290-173">So by creating the swap chain with the same factory (as shown above), you are able to recreate the swap chain and continue using the Direct3D device resources you already have loaded!</span></span>

<span data-ttu-id="2c290-174">Теперь у вас есть окно из операционной системы, способ доступа к GPU и его ресурсам, а также цепочку буферов для отображения результатов отрисовки.</span><span class="sxs-lookup"><span data-stu-id="2c290-174">Now you've got a window from the operating system, a way to access the GPU and its resources, and a swap chain to display the rendering results.</span></span> <span data-ttu-id="2c290-175">Все, что осталось, — это соединить все вместе!</span><span class="sxs-lookup"><span data-stu-id="2c290-175">All that's left is to wire the whole thing together!</span></span>

## <a name="create-a-render-target-for-drawing"></a><span data-ttu-id="2c290-176">Создание целевого объекта отрисовки для рисования</span><span class="sxs-lookup"><span data-stu-id="2c290-176">Create a render target for drawing</span></span>

<span data-ttu-id="2c290-177">Конвейеру шейдера требуется ресурс для рисования пикселов.</span><span class="sxs-lookup"><span data-stu-id="2c290-177">The shader pipeline needs a resource to draw pixels into.</span></span> <span data-ttu-id="2c290-178">Самый простой способ создать этот ресурс — определить ресурс [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) в качестве заднего буфера для рисования в построителе пикселей, а затем прочесть эту текстуру в цепочке буферов.</span><span class="sxs-lookup"><span data-stu-id="2c290-178">The simplest way to create this resource is to define a [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource as a back buffer for the pixel shader to draw into, and then read that texture into the swap chain.</span></span>

<span data-ttu-id="2c290-179">Для этого необходимо создать *представление* целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="2c290-179">To do this, you create a render-target *view*.</span></span> <span data-ttu-id="2c290-180">В Direct3D представление — это способ доступа к определенному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2c290-180">In Direct3D, a view is a way to access a specific resource.</span></span> <span data-ttu-id="2c290-181">В этом случае представление позволяет шейдеру пикселей выполнять запись в текстуру по мере завершения операций на пиксель.</span><span class="sxs-lookup"><span data-stu-id="2c290-181">In this case, the view enables the pixel shader to write into the texture as it completes its per-pixel operations.</span></span>

<span data-ttu-id="2c290-182">Рассмотрим код для этого.</span><span class="sxs-lookup"><span data-stu-id="2c290-182">Let's look at the code for this.</span></span> <span data-ttu-id="2c290-183">При установке \_ \_ \_ в цепочке буферов выходных данных целевого объекта визуализации использования DXGI, \_ который включает базовый ресурс Direct3D для использования в качестве поверхности рисования.</span><span class="sxs-lookup"><span data-stu-id="2c290-183">When you set DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT on the swap chain, that enabled the underlying Direct3D resource to be used as a drawing surface.</span></span> <span data-ttu-id="2c290-184">Чтобы получить представление целевого объекта прорисовки, нам нужно просто получить задний буфер из цепочки буферов и создать представление целевого объекта прорисовки, привязанное к ресурсу заднего буфера.</span><span class="sxs-lookup"><span data-stu-id="2c290-184">So to get our render target view, we just need to get the back buffer from the swap chain and create a render target view bound to the back buffer resource.</span></span>


```C++
hr = m_pDXGISwapChain->GetBuffer(
    0,
    __uuidof(ID3D11Texture2D),
    (void**) &m_pBackBuffer);

hr = m_pd3dDevice->CreateRenderTargetView(
    m_pBackBuffer.Get(),
    nullptr,
    m_pRenderTarget.GetAddressOf()
    );

m_pBackBuffer->GetDesc(&m_bbDesc);
```



<span data-ttu-id="2c290-185">Также создайте *буфер шаблона глубины*.</span><span class="sxs-lookup"><span data-stu-id="2c290-185">Also create a *depth-stencil buffer*.</span></span> <span data-ttu-id="2c290-186">Буфер шаблона глубины — это просто конкретная форма ресурса [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , которая обычно используется для определения того, какие пиксели имеют приоритет в процессе растрирования на основе расстояния объектов в сцене от камеры.</span><span class="sxs-lookup"><span data-stu-id="2c290-186">A depth-stencil buffer is just a particular form of [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource, which is typically used to determine which pixels have draw priority during rasterization based on the distance of the objects in the scene from the camera.</span></span> <span data-ttu-id="2c290-187">Буфер трафарета глубины также можно использовать для эффектов трафаретов, в которых определенные Пиксели отбрасываются или игнорируются во время растрирования.</span><span class="sxs-lookup"><span data-stu-id="2c290-187">A depth-stencil buffer can also be used for stencil effects, where specific pixels are discarded or ignored during rasterization.</span></span> <span data-ttu-id="2c290-188">Размер этого буфера должен совпадать с размером целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="2c290-188">This buffer must be the same size as the render target.</span></span> <span data-ttu-id="2c290-189">Обратите внимание, что невозможно выполнить чтение из или прорисовку текстуры буфера кадров — текстуру набора элементов, так как она используется исключительно в конвейере шейдера до и во время финальной растрирования.</span><span class="sxs-lookup"><span data-stu-id="2c290-189">Note that you cannot read from or render to the frame buffer depth-stencil texture because it is used exclusively by the shader pipeline before and during final rasterization.</span></span>

<span data-ttu-id="2c290-190">Также создайте представление для буфера шаблона глубины в виде [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="2c290-190">Also create a view for the depth-stencil buffer as an [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span></span> <span data-ttu-id="2c290-191">Представление сообщает конвейеру шейдера, как интерпретировать базовый ресурс [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) . так что если вы не укажете это представление, не будет выполнено тестирование глубины для каждого пикселя, и объекты в сцене могут показаться немного недоступными.</span><span class="sxs-lookup"><span data-stu-id="2c290-191">The view tells the shader pipeline how to interpret the underlying [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource - so if you don't supply this view no per-pixel depth testing is performed, and the objects in your scene may seem a bit inside-out at the very least!</span></span>


```C++
CD3D11_TEXTURE2D_DESC depthStencilDesc(
    DXGI_FORMAT_D24_UNORM_S8_UINT,
    static_cast<UINT> (m_bbDesc.Width),
    static_cast<UINT> (m_bbDesc.Height),
    1, // This depth stencil view has only one texture.
    1, // Use a single mipmap level.
    D3D11_BIND_DEPTH_STENCIL
    );

m_pd3dDevice->CreateTexture2D(
    &depthStencilDesc,
    nullptr,
    &m_pDepthStencil
    );

CD3D11_DEPTH_STENCIL_VIEW_DESC depthStencilViewDesc(D3D11_DSV_DIMENSION_TEXTURE2D);

m_pd3dDevice->CreateDepthStencilView(
    m_pDepthStencil.Get(),
    &depthStencilViewDesc,
    &m_pDepthStencilView
    );
```



<span data-ttu-id="2c290-192">Последним шагом является создание окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="2c290-192">The last step is to create a viewport.</span></span> <span data-ttu-id="2c290-193">Это определяет видимый прямоугольник заднего буфера, отображаемый на экране; можно изменить часть буфера, отображаемого на экране, изменив параметры окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="2c290-193">This defines the visible rectangle of the back buffer displayed on the screen; you can change the part of the buffer that is displayed on the screen by changing the parameters of the viewport.</span></span> <span data-ttu-id="2c290-194">Этот код предназначен для всего размера окна (или разрешения экрана) в случае с цепочкой полноэкранного переключения.</span><span class="sxs-lookup"><span data-stu-id="2c290-194">This code targets the whole window size—or the screen resolution, in the case of full-screen swap chains.</span></span> <span data-ttu-id="2c290-195">Для развлечения измените указанные значения координат и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="2c290-195">For fun, change the supplied coordinate values and observe the results.</span></span>


```C++
ZeroMemory(&m_viewport, sizeof(D3D11_VIEWPORT));
m_viewport.Height = (float) m_bbDesc.Height;
m_viewport.Width = (float) m_bbDesc.Width;
m_viewport.MinDepth = 0;
m_viewport.MaxDepth = 1;

m_pd3dDeviceContext->RSSetViewports(
    1,
    &m_viewport
    );
```



<span data-ttu-id="2c290-196">И вот как вы не можете рисовать Пиксели в окне!</span><span class="sxs-lookup"><span data-stu-id="2c290-196">And that's how you go from nothing to drawing pixels in a window!</span></span> <span data-ttu-id="2c290-197">Как вы начинаете, лучше познакомиться с тем, как DirectX с помощью DXGI управляет основными ресурсами, необходимыми для рисования пикселов.</span><span class="sxs-lookup"><span data-stu-id="2c290-197">As you start out, it's a good idea to become familiar with how DirectX, through DXGI, manages the core resources you need to start drawing pixels.</span></span>

<span data-ttu-id="2c290-198">Далее будет рассмотрена структура графического конвейера. см. раздел [понимание конвейера отрисовки шаблона приложения DirectX](understand-the-directx-11-2-graphics-pipeline.md).</span><span class="sxs-lookup"><span data-stu-id="2c290-198">Next you'll look at the structure of the graphics pipeline; see [Understand the DirectX app template's rendering pipeline](understand-the-directx-11-2-graphics-pipeline.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c290-199">См. также</span><span class="sxs-lookup"><span data-stu-id="2c290-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2c290-200">**Далее**</span><span class="sxs-lookup"><span data-stu-id="2c290-200">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="2c290-201">Работа с шейдерами и ресурсами шейдера</span><span class="sxs-lookup"><span data-stu-id="2c290-201">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 