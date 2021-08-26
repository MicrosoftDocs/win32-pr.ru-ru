---
title: Работа с ресурсами устройств DirectX
description: сведения о роли графической инфраструктуры Microsoft DirectX (DXGI) в Windows магазине DirectX.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600af9c5ca2d2ba8ce8a7b078c769e195c4a7898384d102a21be3aaaf2c936bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068664"
---
# <a name="work-with-directx-device-resources"></a>Работа с ресурсами устройств DirectX

сведения о роли графической инфраструктуры Microsoft DirectX (DXGI) в Windows магазине DirectX. DXGI — это набор API-интерфейсов, используемых для настройки и управления ресурсами графических и графических адаптеров низкого уровня. Без этого у вас не будет возможности нарисовать графику игры в окне.

Представьте себе DXGI таким образом: для прямого доступа к GPU и управления его ресурсами необходимо иметь способ описать его в приложении. Наиболее важной частью информации, необходимой для GPU, является место для рисования пикселов, которое может посылать эти пиксели на экран. Обычно это называется "задним буфером" — расположением в памяти GPU, в котором можно рисовать Пиксели, а затем развернутым или перенаправленным, а также отправкой на экран сигнала обновления. DXGI позволяет получить это расположение и использовать этот буфер (называемый *цепочкой подкачки* , так как он является цепочкой буферов, поддерживающих буферизацию, что позволяет применять несколько стратегий использования буферов).

Для этого требуется доступ для записи в цепочку буферов и маркер окна, в котором будет отображаться текущий задний буфер для цепочки буфера обмена. Кроме того, необходимо подключить эти два объекта, чтобы операционная система обновляла окно с содержимым заднего буфера при запросе.

Общий процесс рисования на экране выглядит следующим образом:

-   Получите [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) для своего приложения.
-   Получите интерфейс для устройства и контекста Direct3D.
-   Создайте цепочку буферов для отображения подготовленного образа в [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).
-   Создайте целевой объект отрисовки для рисования и заполните его пикселами.
-   Представьте цепочку буферов.

## <a name="create-a-window-for-your-app"></a>Создание окна для приложения

Первое, что нам нужно сделать, — это создать окно. Сначала создайте класс окна, заполнив экземпляр [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa), а затем зарегистрируйте его с помощью [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa). Класс Window содержит ключевые свойства окна, включая используемый им значок, функцию обработки статических сообщений (Подробнее об этом позже) и уникальное имя класса Window.


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



Затем создайте окно. Также необходимо предоставить сведения о размере окна и имени только что созданного класса Window. При вызове [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa)возвращается непрозрачный указатель на окно, именуемое HWND; необходимо будет оставаться указателем HWND и использовать его каждый раз, когда необходимо ссылаться на окно, включая его удаление или повторное создание, а также (особенно важно) при создании цепочки подкачки DXGI, используемой для рисования в окне.


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



модель классического приложения Windows включает в себя обработчик сообщений Windows. Необходимо создать основной цикл программы для этого обработчика, написав функцию "Статиквиндовпрок" для обработки оконных событий. это должна быть статическая функция, так как Windows будет вызывать ее вне контекста любого экземпляра класса. Вот очень простой пример функции обработки статических сообщений.


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



В этом простом примере выполняется проверка только условий выхода программы: [**WM \_ Close**](/windows/desktop/winmsg/wm-close), Sent, когда запрашивается закрытие окна, и [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy), который отправляется после фактического удаления окна с экрана. Полное, рабочее приложение также должно работать с другими событиями окон, а полный список событий для окон см. в разделе [уведомления окна](/windows/desktop/winmsg/window-notifications).

основной цикл программы должен подтверждать Windows сообщения, разрешая Windows возможность выполнения статической процедуры сообщения. помогите программе работать эффективно, развилкая поведение. каждая итерация должна выбрать обработку новых Windows сообщений, если они доступны, и если в очереди нет сообщений, они должны визуализировать новый кадр. Вот очень простой пример:


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



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a>Получение интерфейса для устройства и контекста Direct3D

Первым шагом при использовании Direct3D является получение интерфейса для аппаратного обеспечения Direct3D (GPU), представленного в виде экземпляров [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) и [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2). Первое — это виртуальное представление ресурсов GPU, а второе — независимая от устройства абстракция конвейера и процесса отрисовки. Вот простой способ представить его: **ID3D11Device** содержит графические методы, которые вызываются редко, как правило, перед отрисовкой, чтобы получить и настроить набор ресурсов, необходимых для начала рисования пикселов. **Ссылку ID3D11DeviceContext**, с другой стороны, содержит методы, которые вызывают каждый кадр: Загрузка в буферах и представлениях и других ресурсах, изменение состояния вывода и прорисовки, управление шейдерами, а также рисование результатов передачи этих ресурсов с помощью состояний и шейдеров.

Существует одна очень важная часть этого процесса: Настройка уровня компонента. Уровень компонентов указывает DirectX на минимальную версию оборудования, поддерживаемого приложением, с \_ уровнем D3D \_ уровня \_ 9 \_ 1 минимальным набором функций и \_ уровнем возможностей \_ D3D \_ 11 \_ 1 в качестве текущего самого высокого уровня. \_Если вы хотите получить доступ к самой широкой аудитории, в качестве минимума следует использовать 9 1. Уделите некоторое время для ознакомления с [уровнями функций](/previous-versions/windows/apps/hh994923(v=win.10)) Direct3D и оценки минимальных и максимальных уровней функций, которые должна поддерживать ваша игра, и для понимания возможных последствий.

Получите ссылки (указатели) как для устройства Direct3D, так и для контекста устройства и сохраните их в виде переменных уровня класса в экземпляре **DeviceResources** (как смарт-указатели **ComPtr** ). Используйте эти ссылки при необходимости доступа к контексту устройства или устройства Direct3D.


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



## <a name="create-the-swap-chain"></a>Создание цепочки буферов

Хорошо: у вас есть окно для рисования, и у вас есть интерфейс для отправки данных и предоставления команд GPU. Теперь давайте посмотрим, как их объединить.

Во первых, вы указываете DXGI, какие значения следует использовать для свойств цепочки буферов обмена. Это делается с помощью структуры для [**\_ \_ цепочки \_ буфера обмена DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) . Шесть полей особенно важны для классических приложений:

-   **Оконное**: указывает, находится ли цепочка подкачки в полноэкранном режиме или обрезана до окна. Задайте значение TRUE, чтобы цепочка буфера обмена была размещена в созданном ранее окне.
-   **Буфферусаже**: задайте для этого параметра значение \_ Использование DXGI \_ \_ \_ . выходные данные целевого объекта прорисовки. Это означает, что цепочка буфера обмена будет поверхностью рисования, что позволит использовать ее в качестве целевого объекта визуализации Direct3D.
-   **SwapEffect**: задайте для этого параметра \_ значение \_ отразить эффекты переключения DXGI \_ \_ .
-   **Формат**: формат \_ B8G8R8A8 UNORM формата DXGI \_ \_ задает 32-разрядный цвет: 8 бит для каждого из трех цветовых каналов RGB и 8 бит для альфа-канала.
-   **BufferCount**: задайте значение 2 для традиционного двойного буферизации, чтобы избежать разрыва. Установите значение 3 для счетчика буферов, если содержимое графики занимает несколько циклов обновления монитора для отображения одного кадра (в 60 Гц, например, пороговое значение превышает 16 мс).
-   **Сампледеск**: это поле управляет множественной выборкой. Задайте для **счетчика** значение 1 и **качество** , равное 0, для цепочек перестановки перелистывания моделей. (Чтобы использовать множественную выборку с цепочками перелистывания моделей, рисуйте на отдельном целевом объекте отрисовки с множественной выборкой, а затем разрешите эту цель в цепочку буферов непосредственно перед ее представлением. пример кода приведен в [многовыборочной выборке в приложениях Windows Store](/previous-versions/windows/apps/dn458384(v=win.10)).)

После того как вы указали конфигурацию для цепочки буферов, необходимо использовать ту же фабрику DXGI, что и устройство Direct3D (и контекст устройства), чтобы создать цепочку буферов.

* * Краткая форма: * *

Получите ссылку на [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) , созданную ранее. Восведите его в [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (если вы еще этого не сделали), а затем вызовите [**идксгидевице::-Adapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) , чтобы получить адаптер DXGI. Получите родительскую фабрику для этого адаптера, вызвав [**IDXGIFactory2::**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) NoInherit ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) наследует от [**идксгиобжект**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)) — теперь вы можете использовать эту фабрику для создания цепочки буферов путем вызова [**креатесвапчаинфорхвнд**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), как показано в следующем примере кода.


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



Если вы только начинаете, то, вероятно, лучше использовать описанную здесь конфигурацию. Теперь, если вы уже знакомы с предыдущими версиями DirectX, вы можете спросить: «почему мы не создаем устройство и цепочку буферов, вместо того чтобы проходить все эти классы?» Ответ — это эффективность: цепочки обмена — это ресурсы устройства Direct3D, а ресурсы устройств привязаны к конкретному устройству Direct3D, которое их создало. При создании нового устройства с новой цепочкой подкачки необходимо повторно создать все ресурсы устройства с помощью нового устройства Direct3D. Таким образом, создав цепочку подкачки с той же фабрикой (как показано выше), вы можете повторно создать цепочку буферов и продолжить использовать уже загруженные ресурсы устройства Direct3D.

Теперь у вас есть окно из операционной системы, способ доступа к GPU и его ресурсам, а также цепочку буферов для отображения результатов отрисовки. Все, что осталось, — это соединить все вместе!

## <a name="create-a-render-target-for-drawing"></a>Создание целевого объекта отрисовки для рисования

Конвейеру шейдера требуется ресурс для рисования пикселов. Самый простой способ создать этот ресурс — определить ресурс [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) в качестве заднего буфера для рисования в построителе пикселей, а затем прочесть эту текстуру в цепочке буферов.

Для этого необходимо создать *представление* целевого объекта рендеринга. В Direct3D представление — это способ доступа к определенному ресурсу. В этом случае представление позволяет шейдеру пикселей выполнять запись в текстуру по мере завершения операций на пиксель.

Рассмотрим код для этого. При установке \_ \_ \_ в цепочке буферов выходных данных целевого объекта визуализации использования DXGI, \_ который включает базовый ресурс Direct3D для использования в качестве поверхности рисования. Чтобы получить представление целевого объекта прорисовки, нам нужно просто получить задний буфер из цепочки буферов и создать представление целевого объекта прорисовки, привязанное к ресурсу заднего буфера.


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



Также создайте *буфер шаблона глубины*. Буфер шаблона глубины — это просто конкретная форма ресурса [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , которая обычно используется для определения того, какие пиксели имеют приоритет в процессе растрирования на основе расстояния объектов в сцене от камеры. Буфер трафарета глубины также можно использовать для эффектов трафаретов, в которых определенные Пиксели отбрасываются или игнорируются во время растрирования. Размер этого буфера должен совпадать с размером целевого объекта рендеринга. Обратите внимание, что невозможно выполнить чтение из или прорисовку текстуры буфера кадров — текстуру набора элементов, так как она используется исключительно в конвейере шейдера до и во время финальной растрирования.

Также создайте представление для буфера шаблона глубины в виде [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview). Представление сообщает конвейеру шейдера, как интерпретировать базовый ресурс [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) . так что если вы не укажете это представление, не будет выполнено тестирование глубины для каждого пикселя, и объекты в сцене могут показаться немного недоступными.


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



Последним шагом является создание окна просмотра. Это определяет видимый прямоугольник заднего буфера, отображаемый на экране; можно изменить часть буфера, отображаемого на экране, изменив параметры окна просмотра. Этот код предназначен для всего размера окна (или разрешения экрана) в случае с цепочкой полноэкранного переключения. Для развлечения измените указанные значения координат и просмотрите результаты.


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



И вот как вы не можете рисовать Пиксели в окне! Как вы начинаете, лучше познакомиться с тем, как DirectX с помощью DXGI управляет основными ресурсами, необходимыми для рисования пикселов.

Далее будет рассмотрена структура графического конвейера. см. раздел [понимание конвейера отрисовки шаблона приложения DirectX](understand-the-directx-11-2-graphics-pipeline.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Далее**
</dt> <dt>

[Работа с шейдерами и ресурсами шейдера](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 