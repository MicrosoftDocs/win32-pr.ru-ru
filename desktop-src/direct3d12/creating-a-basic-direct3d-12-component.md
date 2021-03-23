---
title: Создание базового компонента Direct3D 12
description: В этом разделе описывается поток вызова для создания базового компонента Direct3D 12.
ms.assetid: A0FB108B-15C1-42AD-9277-D5CB63FA8329
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: d0c7ead9ce67ee23a0668304a006d6cd67fb3d67
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104758864"
---
# <a name="creating-a-basic-direct3d-12-component"></a>Создание базового компонента Direct3D 12

> [!NOTE]
> Примеры графики DirectX 12, в которых показано, как создавать ресурсоемкие приложения для Windows 10, см. в репозитории [примеров](https://github.com/Microsoft/DirectX-Graphics-Samples) с поддержкой графики DirectX.

В этом разделе описывается поток вызова для создания базового компонента Direct3D 12.

-   [Поток кода для простого приложения](#code-flow-for-a-simple-app)
    -   [Инициализация](#initialize)
    -   [Обновление](#update)
    -   [Render](#render)
    -   [Завершить](#destroy)
-   [Пример кода для простого приложения](#code-example-for-a-simple-app)
    -   [класс D3D12HelloTriangle](#class-d3d12hellotriangle)
    -   [OnInit ()](#oninit)
    -   [Лоадпипелине ()](#loadpipeline)
    -   [Лоадассетс ()](#loadassets)
    -   [OnUpdate ()](#onupdate)
    -   [OnRender ()](#onrender)
    -   [Популатекоммандлист ()](#populatecommandlist)
    -   [Ваитфорпревиаусфраме ()](#waitforpreviousframe)
    -   [OnDestroy ()](#ondestroy)
-   [Связанные темы](#related-topics)

## <a name="code-flow-for-a-simple-app"></a>Поток кода для простого приложения

Внешний цикл программы D3D 12 соответствует очень стандартному графическому процессу:

> [!TIP]
> За новыми функциями Direct3D 12 следует заметка.

-   [Инициализация](#initialize)
-   **Придется**
    -   [Обновление](#update)
    -   [Render](#render)
-   [Завершить](#destroy)

### <a name="initialize"></a>Инициализация

Инициализация включает в себя первую настройку глобальных переменных и классов, а функция Initialize должна подготовить конвейер и ресурсы.

-   Инициализируйте конвейер.
    -   Включение слоя отладки.
    -   Создайте устройство.
    -   Создайте очередь команд.
    -   Создайте цепочку буферов обмена.
    -   Создайте кучу дескрипторов представления целевого объекта отрисовки (РТВ).
        > [!Note]  
        > [Кучу дескрипторов](descriptor-heaps.md) можно рассматривать как массив [из дескрипторов.](descriptors.md) Где каждый дескриптор полностью описывает объект для GPU.

    -   Создание ресурсов фрейма (представление целевого объекта прорисовки для каждого кадра).
    -   Создайте распределитель команд.
        > [!Note]  
        > Распределитель команд управляет базовым хранилищем для [списков команд и пакетов](recording-command-lists-and-bundles.md).
         
-   Инициализация ресурсов.
    -   Создайте пустую корневую подпись.
        > [!Note]  
        > [Корневая подпись](root-signatures.md) графического элемента определяет, какие ресурсы привязаны к графическому конвейеру.

    -   Скомпилируйте шейдеры.
    -   Создайте макет ввода вершин.
    -   Создайте описание [объекта состояния конвейера](managing-graphics-pipeline-state-in-direct3d-12.md) , а затем создайте объект.
        > [!Note]  
        > Объект состояния конвейера поддерживает состояние всех заданных в данный момент шейдеров, а также определенные объекты фиксированного состояния функции (например, *входные ассемблеры*, *тесселатор*, средство *прорисовки* и *выход слияния*).

    -   Создайте список команд.
    -   Закройте список команд.
    -   Создание и загрузка буферов вершин.
    -   Создайте представления буфера вершин.
    -   Создайте ограждение.
        > [!Note]  
        > Ограждение используется для синхронизации ЦП с графическим процессором (см. раздел [Синхронизация с несколькими модулями](./user-mode-heap-synchronization.md)).

    -   Создайте обработчик событий.
    -   Дождитесь завершения работы GPU.
        > [!Note]  
        > Проверьте наличие ограждения.

См. [классы D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [лоадпипелине](#loadpipeline) и [лоадассетс](#loadassets).

### <a name="update"></a>Update

Обновите все, которое должно измениться с момента последнего кадра.

-   При необходимости измените константу, вершину, индексные буферы и все остальное.

См. инструкции по [обновлению](#onupdate).

### <a name="render"></a>Render

Нарисуйте новый мир.

-   Заполнение списка команд.
    -   Сброс распределителя списка команд.
        > [!Note]  
        > Повторно используйте память, связанную с распределителем команд.

         

    -   Сброс списка команд.
    -   Задайте корневую подпись графики.
        > [!Note]  
        > Задает корневую подпись графики, используемую для текущего списка команд.

         

    -   Задание окна просмотра и прямоугольных прямоугольников.
    -   Задайте барьер ресурсов, указывающий задний буфер для использования в качестве целевого объекта рендеринга.
        > [!Note]  
        > Барьеры ресурсов используются для управления переходами ресурсов.

         

    -   Запись команд в список команд.
    -   Указывает, что задний буфер будет использоваться для представления после выполнения списка команд.
        > [!Note]  
        > Еще один вызов для задания барьера ресурсов.

         

    -   Закройте список команд для дальнейшей записи.
-   Выполните список команд.
-   Представьте фрейм.
-   Дождитесь завершения работы GPU.
    > [!Note]  
    > Следите за обновлением и проверкой ограждения.

См. [OnRender](#onrender).

### <a name="destroy"></a>Уничтожить

Аккуратно закройте приложение.

-   Дождитесь завершения работы GPU.
    > [!Note]  
    > Окончательная проверка ограждения.

-   Закройте обработчик событий.

См. статью о [OnDestroy](#ondestroy).

## <a name="code-example-for-a-simple-app"></a>Пример кода для простого приложения

Следующий код расширяет приведенный выше поток кода, добавляя код, необходимый для простого примера.

### <a name="class-d3d12hellotriangle"></a>класс D3D12HelloTriangle

Сначала определите класс в файле заголовка, включая окно просмотра, прямоугольный прямоугольник и буфер вершин, используя структуры:

-   [**\_Окно просмотра D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [**D3D12 \_ Rect**](d3d12-rect.md)
-   [**\_ \_ Представление буфера вершин \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

```cpp
#include "DXSample.h"

using namespace DirectX;
using namespace Microsoft::WRL;

class D3D12HelloTriangle : public DXSample
{
public:
    D3D12HelloTriangle(UINT width, UINT height, std::wstring name);

    virtual void OnInit();
    virtual void OnUpdate();
    virtual void OnRender();
    virtual void OnDestroy();

private:
    static const UINT FrameCount = 2;

    struct Vertex
    {
        XMFLOAT3 position;
        XMFLOAT4 color;
    };

    // Pipeline objects.
    D3D12_VIEWPORT m_viewport;
    D3D12_RECT m_scissorRect;
    ComPtr<IDXGISwapChain3> m_swapChain;
    ComPtr<ID3D12Device> m_device;
    ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
    ComPtr<ID3D12CommandAllocator> m_commandAllocator;
    ComPtr<ID3D12CommandQueue> m_commandQueue;
    ComPtr<ID3D12RootSignature> m_rootSignature;
    ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
    ComPtr<ID3D12PipelineState> m_pipelineState;
    ComPtr<ID3D12GraphicsCommandList> m_commandList;
    UINT m_rtvDescriptorSize;

    // App resources.
    ComPtr<ID3D12Resource> m_vertexBuffer;
    D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;

    // Synchronization objects.
    UINT m_frameIndex;
    HANDLE m_fenceEvent;
    ComPtr<ID3D12Fence> m_fence;
    UINT64 m_fenceValue;

    void LoadPipeline();
    void LoadAssets();
    void PopulateCommandList();
    void WaitForPreviousFrame();
};
```

### <a name="oninit"></a>OnInit ()

В основном исходном файле проекта запустите инициализацию объектов:

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a>Лоадпипелине ()

Следующий код создает основы графического конвейера. Процесс создания устройств и цепочек подкачки очень похож на Direct3D 11.

-   Включение слоя отладки с вызовами:<dl>

[**D3D12GetDebugInterface**](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [**ID3D12Debug:: Енабледебуглайер**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   Создайте устройство:<dl>

[**CreateDXGIFactory1**](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   Заполните описание очереди команд, а затем создайте очередь команд:<dl>

[**D3D12 \_ команд \_ в очереди \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [**ID3D12Device:: Креатекоммандкуеуе**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   Заполните описание имеющуюся цепочку буферов, а затем создайте цепочку буферов обмена: <dl>

[**\_ \_ DESC цепочки подкачки \_**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [**Идксгифактори:: Креатесвапчаин**](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [**IDXGISwapChain3:: Жеткуррентбаккбуффериндекс**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   Заполните описание кучи. Затем создайте кучу дескрипторов: <dl>

[**Описание \_ кучи дескрипторов D3D12 \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [**ID3D12Device:: Креатедескрипторхеап**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [**ID3D12Device:: Жетдескрипторхандлеинкрементсизе**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   Создайте представление целевого объекта прорисовки: <dl>

[**\_ \_ Дескриптор дескриптора ЦП CD3DX12 \_**](cd3dx12-cpu-descriptor-handle.md)  
    [**жеткпудескрипторхандлефорхеапстарт**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**Идксгисвапчаин:: buffer**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [**ID3D12Device:: Креатерендертаржетвиев**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   Создайте распределитель команд: [**ID3D12Device:: креатекоммандаллокатор**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).

В последующих шагах списки команд получаются из распределителя команд и передаются в очередь команд.

Загрузите зависимости конвейера отрисовки (Обратите внимание, что создание программной деформации устройства является полностью необязательным).


```cpp
void D3D12HelloTriangle::LoadPipeline()
{
#if defined(_DEBUG)
    // Enable the D3D12 debug layer.
    {
        
        ComPtr<ID3D12Debug> debugController;
        if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&debugController))))
        {
            debugController->EnableDebugLayer();
        }
    }
#endif

    ComPtr<IDXGIFactory4> factory;
    ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&factory)));

    if (m_useWarpDevice)
    {
        ComPtr<IDXGIAdapter> warpAdapter;
        ThrowIfFailed(factory->EnumWarpAdapter(IID_PPV_ARGS(&warpAdapter)));

        ThrowIfFailed(D3D12CreateDevice(
            warpAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }
    else
    {
        ComPtr<IDXGIAdapter1> hardwareAdapter;
        GetHardwareAdapter(factory.Get(), &hardwareAdapter);

        ThrowIfFailed(D3D12CreateDevice(
            hardwareAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }

    // Describe and create the command queue.
    D3D12_COMMAND_QUEUE_DESC queueDesc = {};
    queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
    queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

    ThrowIfFailed(m_device->CreateCommandQueue(&queueDesc, IID_PPV_ARGS(&m_commandQueue)));

    // Describe and create the swap chain.
    DXGI_SWAP_CHAIN_DESC swapChainDesc = {};
    swapChainDesc.BufferCount = FrameCount;
    swapChainDesc.BufferDesc.Width = m_width;
    swapChainDesc.BufferDesc.Height = m_height;
    swapChainDesc.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
    swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
    swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_DISCARD;
    swapChainDesc.OutputWindow = Win32Application::GetHwnd();
    swapChainDesc.SampleDesc.Count = 1;
    swapChainDesc.Windowed = TRUE;

    ComPtr<IDXGISwapChain> swapChain;
    ThrowIfFailed(factory->CreateSwapChain(
        m_commandQueue.Get(),        // Swap chain needs the queue so that it can force a flush on it.
        &swapChainDesc,
        &swapChain
        ));

    ThrowIfFailed(swapChain.As(&m_swapChain));

    // This sample does not support fullscreen transitions.
    ThrowIfFailed(factory->MakeWindowAssociation(Win32Application::GetHwnd(), DXGI_MWA_NO_ALT_ENTER));

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();

    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
            rtvHandle.Offset(1, m_rtvDescriptorSize);
        }
    }

    ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
}
```



### <a name="loadassets"></a>Лоадассетс ()

Загрузка и подготовка ресурсов — длительный процесс. Многие из этих этапов похожи на D3D 11, хотя некоторые из них не знакомы с D3D 12.

В Direct3D 12 требуемое состояние конвейера прикрепляется к списку команд через [объект состояния конвейера](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO). В этом примере показано, как создать PSO. Вы можете сохранить PSO как переменную-член и использовать ее столько раз, сколько необходимо.

Куча дескрипторов определяет представления и способ доступа к ресурсам (например, представление целевого объекта прорисовки).

С помощью распределителя списка команд и PSO можно создать список фактических команд, который будет выполнен позже.

В ходе успеха вызываются следующие интерфейсы API и процессы.

-   Создайте пустую корневую подпись с помощью доступной вспомогательной структуры: <dl>

[**\_DESC корневой \_ подписи CD3DX12 \_**](cd3dx12-root-signature-desc.md)  
    [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [**ID3D12Device:: Креатерутсигнатуре**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   Загрузите и скомпилируйте шейдеры: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).
-   Создайте входной макет вершины: [**D3D12 \_ input \_ element \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).
-   Заполните описание состояния конвейера, используя доступные вспомогательные структуры, а затем создайте состояние графического конвейера: <dl>

[**D3D12 \_ графика \_ состояния графического конвейера \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [**CD3DX12 средство программной \_ прорисовки \_ DESC**](cd3dx12-rasterizer-desc.md)  
    [**CD3DX12 \_ Blend, \_ DESC**](cd3dx12-blend-desc.md)  
    [**ID3D12Device:: Креатеграфикспипелинестате**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   Создайте, а затем закройте список команд: <dl>

[**ID3D12Device:: Креатекоммандлист**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   Создайте буфер вершин: [**ID3D12Device:: креатекоммиттедресаурце**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).
-   Скопируйте данные вершин в буфер вершин:<dl>

[**ID3D12Resource:: Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [**ID3D12Resource:: отмена сопоставления**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   Инициализируйте представление буфера вершин: [**жетгпувиртуаладдресс**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).
-   Создайте и инициализируйте ограждение: [**ID3D12Device:: креатефенце**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).
-   Создайте обработчик событий для использования с синхронизацией кадров.
-   Дождитесь завершения работы GPU.


```cpp
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_UPLOAD);
        auto desc = CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize);
        ThrowIfFailed(m_device->CreateCommittedResource(
            &heapProps,
            D3D12_HEAP_FLAG_NONE,
            &desc,
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



### <a name="onupdate"></a>OnUpdate ()

В простом примере ничего не обновляется.


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a>OnRender ()

Во время установки переменная члена **m \_ коммандлист** была использована для записи и выполнения всех команд Set up. Теперь этот элемент можно использовать в основном цикле подготовки к просмотру.

Подготовка к просмотру включает вызов для заполнения списка команд, затем можно выполнить список команд и следующий буфер в приведенной цепочке буфера обмена:

-   Заполнение списка команд.
-   Выполните список команд: [**ID3D12CommandQueue:: ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).
-   [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) кадр.
-   Дождитесь завершения работы GPU.


```cpp
void D3D12HelloTriangle::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(1, 0));

    WaitForPreviousFrame();
}
```



### <a name="populatecommandlist"></a>Популатекоммандлист ()

Необходимо сбросить распределителя списка команд и список команд, прежде чем их можно будет использовать повторно. В более сложных сценариях может иметь смысл сбрасывать распределитель каждые несколько кадров. Память связана с распределительом, который не может быть освобожден сразу после выполнения списка команд. В этом примере показано, как сбросить распределитель после каждого кадра.

Теперь повторно используйте список команд для текущего кадра. Повторное подключение окна просмотра к списку команд (это необходимо делать при каждом сбросе списка команд и перед выполнением списка команд), указывать на то, что ресурс будет использоваться в качестве целевого объекта рендеринга, записывать команды, а затем указать, что целевой объект прорисовки будет использоваться для отображения при завершении выполнения списка команд.

Заполнение списков команд вызывает следующие методы и процессы в свою очередь:

-   Сброс распределителя команд и список команд: <dl>

[**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [**ID3D12GraphicsCommandList:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   Задать корневую подпись, окно просмотра и прямоугольники ножниц: <dl>

[**ID3D12GraphicsCommandList:: Сетграфиксрутсигнатуре**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [**ID3D12GraphicsCommandList:: Рссетвиевпортс**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [**ID3D12GraphicsCommandList:: РссетсЦиссорректс**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   Укажите, что задний буфер должен использоваться в качестве целевого объекта рендеринга: <dl>

[**ID3D12GraphicsCommandList:: Ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [**ID3D12DescriptorHeap:: Жеткпудескрипторхандлефорхеапстарт**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**ID3D12GraphicsCommandList:: Омсетрендертаржетс**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   Запишите команды:<dl>

[**ID3D12GraphicsCommandList:: Клеаррендертаржетвиев**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [**ID3D12GraphicsCommandList:: Иасетпримитиветопологи**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [**ID3D12GraphicsCommandList:: Иасетвертексбуфферс**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [**ID3D12GraphicsCommandList::D Равинстанцед**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   Укажите, что задний буфер теперь будет использоваться для представления: [**ID3D12GraphicsCommandList:: ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).
-   Закройте список команд: [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).


```cpp
void D3D12HelloTriangle::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocator->Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
    m_commandList->RSSetViewports(1, &m_viewport);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
    m_commandList->ResourceBarrier(1, &barrier);

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->DrawInstanced(3, 1, 0, 0);

    // Indicate that the back buffer will now be used to present.
    barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
    m_commandList->ResourceBarrier(1, &barrier);

    ThrowIfFailed(m_commandList->Close());
}
```



### <a name="waitforpreviousframe"></a>Ваитфорпревиаусфраме ()

В следующем коде показано чрезмерно упрощенное использование ограждений.

> [!Note]  
> Ожидание завершения кадра слишком эффективно для большинства приложений.

 

Следующие интерфейсы API и процессы вызываются по порядку:

-   [**ID3D12CommandQueue:: сигнал**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [**ID3D12Fence:: Жеткомплетедвалуе**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [**ID3D12Fence:: Сетевентонкомплетион**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   Дождитесь события.
-   Обновите индекс кадра: [**IDXGISwapChain3:: жеткуррентбаккбуффериндекс**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).


```cpp
void D3D12HelloTriangle::WaitForPreviousFrame()
{
    // WAITING FOR THE FRAME TO COMPLETE BEFORE CONTINUING IS NOT BEST PRACTICE.
    // This is code implemented as such for simplicity. More advanced samples 
    // illustrate how to use fences for efficient resource usage.

    // Signal and increment the fence value.
    const UINT64 fence = m_fenceValue;
    ThrowIfFailed(m_commandQueue->Signal(m_fence.Get(), fence));
    m_fenceValue++;

    // Wait until the previous frame is finished.
    if (m_fence->GetCompletedValue() < fence)
    {
        ThrowIfFailed(m_fence->SetEventOnCompletion(fence, m_fenceEvent));
        WaitForSingleObject(m_fenceEvent, INFINITE);
    }

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();
}
```



### <a name="ondestroy"></a>OnDestroy ()

Аккуратно закройте приложение.

-   Дождитесь завершения работы GPU.
-   Закройте событие.


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Основные сведения о Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Рабочие образцы](working-samples.md)
</dt> </dl>

 

 
