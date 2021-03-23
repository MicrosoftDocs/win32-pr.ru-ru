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
# <a name="creating-a-basic-direct3d-12-component"></a><span data-ttu-id="e23ed-103">Создание базового компонента Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e23ed-103">Creating a basic Direct3D 12 component</span></span>

> [!NOTE]
> <span data-ttu-id="e23ed-104">Примеры графики DirectX 12, в которых показано, как создавать ресурсоемкие приложения для Windows 10, см. в репозитории [примеров](https://github.com/Microsoft/DirectX-Graphics-Samples) с поддержкой графики DirectX.</span><span class="sxs-lookup"><span data-stu-id="e23ed-104">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="e23ed-105">В этом разделе описывается поток вызова для создания базового компонента Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e23ed-105">This topic describes the call flow to create a basic Direct3D 12 component.</span></span>

-   [<span data-ttu-id="e23ed-106">Поток кода для простого приложения</span><span class="sxs-lookup"><span data-stu-id="e23ed-106">Code flow for a simple app</span></span>](#code-flow-for-a-simple-app)
    -   [<span data-ttu-id="e23ed-107">Инициализация</span><span class="sxs-lookup"><span data-stu-id="e23ed-107">Initialize</span></span>](#initialize)
    -   [<span data-ttu-id="e23ed-108">Обновление</span><span class="sxs-lookup"><span data-stu-id="e23ed-108">Update</span></span>](#update)
    -   [<span data-ttu-id="e23ed-109">Render</span><span class="sxs-lookup"><span data-stu-id="e23ed-109">Render</span></span>](#render)
    -   [<span data-ttu-id="e23ed-110">Завершить</span><span class="sxs-lookup"><span data-stu-id="e23ed-110">Destroy</span></span>](#destroy)
-   [<span data-ttu-id="e23ed-111">Пример кода для простого приложения</span><span class="sxs-lookup"><span data-stu-id="e23ed-111">Code example for a simple app</span></span>](#code-example-for-a-simple-app)
    -   [<span data-ttu-id="e23ed-112">класс D3D12HelloTriangle</span><span class="sxs-lookup"><span data-stu-id="e23ed-112">class D3D12HelloTriangle</span></span>](#class-d3d12hellotriangle)
    -   [<span data-ttu-id="e23ed-113">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-113">OnInit()</span></span>](#oninit)
    -   [<span data-ttu-id="e23ed-114">Лоадпипелине ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-114">LoadPipeline()</span></span>](#loadpipeline)
    -   [<span data-ttu-id="e23ed-115">Лоадассетс ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-115">LoadAssets()</span></span>](#loadassets)
    -   [<span data-ttu-id="e23ed-116">OnUpdate ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-116">OnUpdate()</span></span>](#onupdate)
    -   [<span data-ttu-id="e23ed-117">OnRender ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-117">OnRender()</span></span>](#onrender)
    -   [<span data-ttu-id="e23ed-118">Популатекоммандлист ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-118">PopulateCommandList()</span></span>](#populatecommandlist)
    -   [<span data-ttu-id="e23ed-119">Ваитфорпревиаусфраме ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-119">WaitForPreviousFrame()</span></span>](#waitforpreviousframe)
    -   [<span data-ttu-id="e23ed-120">OnDestroy ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-120">OnDestroy()</span></span>](#ondestroy)
-   [<span data-ttu-id="e23ed-121">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e23ed-121">Related topics</span></span>](#related-topics)

## <a name="code-flow-for-a-simple-app"></a><span data-ttu-id="e23ed-122">Поток кода для простого приложения</span><span class="sxs-lookup"><span data-stu-id="e23ed-122">Code flow for a simple app</span></span>

<span data-ttu-id="e23ed-123">Внешний цикл программы D3D 12 соответствует очень стандартному графическому процессу:</span><span class="sxs-lookup"><span data-stu-id="e23ed-123">The outermost loop of a D3D 12 program follows a very standard graphics process:</span></span>

> [!TIP]
> <span data-ttu-id="e23ed-124">За новыми функциями Direct3D 12 следует заметка.</span><span class="sxs-lookup"><span data-stu-id="e23ed-124">Features new to Direct3D 12 are followed by a note.</span></span>

-   [<span data-ttu-id="e23ed-125">Инициализация</span><span class="sxs-lookup"><span data-stu-id="e23ed-125">Initialize</span></span>](#initialize)
-   <span data-ttu-id="e23ed-126">**Придется**</span><span class="sxs-lookup"><span data-stu-id="e23ed-126">**Repeat**</span></span>
    -   [<span data-ttu-id="e23ed-127">Обновление</span><span class="sxs-lookup"><span data-stu-id="e23ed-127">Update</span></span>](#update)
    -   [<span data-ttu-id="e23ed-128">Render</span><span class="sxs-lookup"><span data-stu-id="e23ed-128">Render</span></span>](#render)
-   [<span data-ttu-id="e23ed-129">Завершить</span><span class="sxs-lookup"><span data-stu-id="e23ed-129">Destroy</span></span>](#destroy)

### <a name="initialize"></a><span data-ttu-id="e23ed-130">Инициализация</span><span class="sxs-lookup"><span data-stu-id="e23ed-130">Initialize</span></span>

<span data-ttu-id="e23ed-131">Инициализация включает в себя первую настройку глобальных переменных и классов, а функция Initialize должна подготовить конвейер и ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e23ed-131">Initialization involves first setting up the global variables and classes, and an initialize function must prepare the pipeline and assets.</span></span>

-   <span data-ttu-id="e23ed-132">Инициализируйте конвейер.</span><span class="sxs-lookup"><span data-stu-id="e23ed-132">Initialize the pipeline.</span></span>
    -   <span data-ttu-id="e23ed-133">Включение слоя отладки.</span><span class="sxs-lookup"><span data-stu-id="e23ed-133">Enable the debug layer.</span></span>
    -   <span data-ttu-id="e23ed-134">Создайте устройство.</span><span class="sxs-lookup"><span data-stu-id="e23ed-134">Create the device.</span></span>
    -   <span data-ttu-id="e23ed-135">Создайте очередь команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-135">Create the command queue.</span></span>
    -   <span data-ttu-id="e23ed-136">Создайте цепочку буферов обмена.</span><span class="sxs-lookup"><span data-stu-id="e23ed-136">Create the swap chain.</span></span>
    -   <span data-ttu-id="e23ed-137">Создайте кучу дескрипторов представления целевого объекта отрисовки (РТВ).</span><span class="sxs-lookup"><span data-stu-id="e23ed-137">Create a render target view (RTV) descriptor heap.</span></span>
        > [!Note]  
        > <span data-ttu-id="e23ed-138">[Кучу дескрипторов](descriptor-heaps.md) можно рассматривать как массив [из дескрипторов.](descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="e23ed-138">A [descriptor heap](descriptor-heaps.md) can be thought of as an array of [descriptors](descriptors.md).</span></span> <span data-ttu-id="e23ed-139">Где каждый дескриптор полностью описывает объект для GPU.</span><span class="sxs-lookup"><span data-stu-id="e23ed-139">Where each descriptor fully describes an object to the GPU.</span></span>

    -   <span data-ttu-id="e23ed-140">Создание ресурсов фрейма (представление целевого объекта прорисовки для каждого кадра).</span><span class="sxs-lookup"><span data-stu-id="e23ed-140">Create frame resources (a render target view for each frame).</span></span>
    -   <span data-ttu-id="e23ed-141">Создайте распределитель команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-141">Create a command allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="e23ed-142">Распределитель команд управляет базовым хранилищем для [списков команд и пакетов](recording-command-lists-and-bundles.md).</span><span class="sxs-lookup"><span data-stu-id="e23ed-142">A command allocator manages the underlying storage for [command lists and bundles](recording-command-lists-and-bundles.md).</span></span>
         
-   <span data-ttu-id="e23ed-143">Инициализация ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e23ed-143">Initialize the assets.</span></span>
    -   <span data-ttu-id="e23ed-144">Создайте пустую корневую подпись.</span><span class="sxs-lookup"><span data-stu-id="e23ed-144">Create an empty root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="e23ed-145">[Корневая подпись](root-signatures.md) графического элемента определяет, какие ресурсы привязаны к графическому конвейеру.</span><span class="sxs-lookup"><span data-stu-id="e23ed-145">A graphics [root signature](root-signatures.md) defines what resources are bound to the graphics pipeline.</span></span>

    -   <span data-ttu-id="e23ed-146">Скомпилируйте шейдеры.</span><span class="sxs-lookup"><span data-stu-id="e23ed-146">Compile the shaders.</span></span>
    -   <span data-ttu-id="e23ed-147">Создайте макет ввода вершин.</span><span class="sxs-lookup"><span data-stu-id="e23ed-147">Create the vertex input layout.</span></span>
    -   <span data-ttu-id="e23ed-148">Создайте описание [объекта состояния конвейера](managing-graphics-pipeline-state-in-direct3d-12.md) , а затем создайте объект.</span><span class="sxs-lookup"><span data-stu-id="e23ed-148">Create a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) description, then create the object.</span></span>
        > [!Note]  
        > <span data-ttu-id="e23ed-149">Объект состояния конвейера поддерживает состояние всех заданных в данный момент шейдеров, а также определенные объекты фиксированного состояния функции (например, *входные ассемблеры*, *тесселатор*, средство *прорисовки* и *выход слияния*).</span><span class="sxs-lookup"><span data-stu-id="e23ed-149">A pipeline state object maintains the state of all currently set shaders as well as certain fixed function state objects (such as the *input assembler*, *tesselator*, *rasterizer* and *output merger*).</span></span>

    -   <span data-ttu-id="e23ed-150">Создайте список команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-150">Create the command list.</span></span>
    -   <span data-ttu-id="e23ed-151">Закройте список команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-151">Close the command list.</span></span>
    -   <span data-ttu-id="e23ed-152">Создание и загрузка буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="e23ed-152">Create and load the vertex buffers.</span></span>
    -   <span data-ttu-id="e23ed-153">Создайте представления буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="e23ed-153">Create the vertex buffer views.</span></span>
    -   <span data-ttu-id="e23ed-154">Создайте ограждение.</span><span class="sxs-lookup"><span data-stu-id="e23ed-154">Create a fence.</span></span>
        > [!Note]  
        > <span data-ttu-id="e23ed-155">Ограждение используется для синхронизации ЦП с графическим процессором (см. раздел [Синхронизация с несколькими модулями](./user-mode-heap-synchronization.md)).</span><span class="sxs-lookup"><span data-stu-id="e23ed-155">A fence is used to synchronize the CPU with the GPU (see [Multi-engine synchronization](./user-mode-heap-synchronization.md)).</span></span>

    -   <span data-ttu-id="e23ed-156">Создайте обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="e23ed-156">Create an event handle.</span></span>
    -   <span data-ttu-id="e23ed-157">Дождитесь завершения работы GPU.</span><span class="sxs-lookup"><span data-stu-id="e23ed-157">Wait for the GPU to finish.</span></span>
        > [!Note]  
        > <span data-ttu-id="e23ed-158">Проверьте наличие ограждения.</span><span class="sxs-lookup"><span data-stu-id="e23ed-158">Check on the fence!</span></span>

<span data-ttu-id="e23ed-159">См. [классы D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [лоадпипелине](#loadpipeline) и [лоадассетс](#loadassets).</span><span class="sxs-lookup"><span data-stu-id="e23ed-159">Refer to [class D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) and [LoadAssets](#loadassets).</span></span>

### <a name="update"></a><span data-ttu-id="e23ed-160">Update</span><span class="sxs-lookup"><span data-stu-id="e23ed-160">Update</span></span>

<span data-ttu-id="e23ed-161">Обновите все, которое должно измениться с момента последнего кадра.</span><span class="sxs-lookup"><span data-stu-id="e23ed-161">Update everything that should change since the last frame.</span></span>

-   <span data-ttu-id="e23ed-162">При необходимости измените константу, вершину, индексные буферы и все остальное.</span><span class="sxs-lookup"><span data-stu-id="e23ed-162">Modify the constant, vertex, index buffers, and everything else, as necessary.</span></span>

<span data-ttu-id="e23ed-163">См. инструкции по [обновлению](#onupdate).</span><span class="sxs-lookup"><span data-stu-id="e23ed-163">Refer to [OnUpdate](#onupdate).</span></span>

### <a name="render"></a><span data-ttu-id="e23ed-164">Render</span><span class="sxs-lookup"><span data-stu-id="e23ed-164">Render</span></span>

<span data-ttu-id="e23ed-165">Нарисуйте новый мир.</span><span class="sxs-lookup"><span data-stu-id="e23ed-165">Draw the new world.</span></span>

-   <span data-ttu-id="e23ed-166">Заполнение списка команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-166">Populate the command list.</span></span>
    -   <span data-ttu-id="e23ed-167">Сброс распределителя списка команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-167">Reset the command list allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="e23ed-168">Повторно используйте память, связанную с распределителем команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-168">Re-use the memory that is associated with the command allocator.</span></span>

         

    -   <span data-ttu-id="e23ed-169">Сброс списка команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-169">Reset the command list.</span></span>
    -   <span data-ttu-id="e23ed-170">Задайте корневую подпись графики.</span><span class="sxs-lookup"><span data-stu-id="e23ed-170">Set the graphics root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="e23ed-171">Задает корневую подпись графики, используемую для текущего списка команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-171">Sets the graphics root signature to use for the current command list.</span></span>

         

    -   <span data-ttu-id="e23ed-172">Задание окна просмотра и прямоугольных прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="e23ed-172">Set the viewport and scissor rectangles.</span></span>
    -   <span data-ttu-id="e23ed-173">Задайте барьер ресурсов, указывающий задний буфер для использования в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="e23ed-173">Set a resource barrier, indicating the back buffer is to be used as a render target.</span></span>
        > [!Note]  
        > <span data-ttu-id="e23ed-174">Барьеры ресурсов используются для управления переходами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e23ed-174">Resource barriers are used to manage resource transitions.</span></span>

         

    -   <span data-ttu-id="e23ed-175">Запись команд в список команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-175">Record commands into the command list.</span></span>
    -   <span data-ttu-id="e23ed-176">Указывает, что задний буфер будет использоваться для представления после выполнения списка команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-176">Indicate the back buffer will be used to present after the command list has executed.</span></span>
        > [!Note]  
        > <span data-ttu-id="e23ed-177">Еще один вызов для задания барьера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e23ed-177">Another call to set a resource barrier.</span></span>

         

    -   <span data-ttu-id="e23ed-178">Закройте список команд для дальнейшей записи.</span><span class="sxs-lookup"><span data-stu-id="e23ed-178">Close the command list to further recording.</span></span>
-   <span data-ttu-id="e23ed-179">Выполните список команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-179">Execute the command list.</span></span>
-   <span data-ttu-id="e23ed-180">Представьте фрейм.</span><span class="sxs-lookup"><span data-stu-id="e23ed-180">Present the frame.</span></span>
-   <span data-ttu-id="e23ed-181">Дождитесь завершения работы GPU.</span><span class="sxs-lookup"><span data-stu-id="e23ed-181">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="e23ed-182">Следите за обновлением и проверкой ограждения.</span><span class="sxs-lookup"><span data-stu-id="e23ed-182">Keep updating and checking the fence.</span></span>

<span data-ttu-id="e23ed-183">См. [OnRender](#onrender).</span><span class="sxs-lookup"><span data-stu-id="e23ed-183">Refer to [OnRender](#onrender).</span></span>

### <a name="destroy"></a><span data-ttu-id="e23ed-184">Уничтожить</span><span class="sxs-lookup"><span data-stu-id="e23ed-184">Destroy</span></span>

<span data-ttu-id="e23ed-185">Аккуратно закройте приложение.</span><span class="sxs-lookup"><span data-stu-id="e23ed-185">Cleanly close down the app.</span></span>

-   <span data-ttu-id="e23ed-186">Дождитесь завершения работы GPU.</span><span class="sxs-lookup"><span data-stu-id="e23ed-186">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="e23ed-187">Окончательная проверка ограждения.</span><span class="sxs-lookup"><span data-stu-id="e23ed-187">Final check on the fence.</span></span>

-   <span data-ttu-id="e23ed-188">Закройте обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="e23ed-188">Close the event handle.</span></span>

<span data-ttu-id="e23ed-189">См. статью о [OnDestroy](#ondestroy).</span><span class="sxs-lookup"><span data-stu-id="e23ed-189">Refer to [OnDestroy](#ondestroy).</span></span>

## <a name="code-example-for-a-simple-app"></a><span data-ttu-id="e23ed-190">Пример кода для простого приложения</span><span class="sxs-lookup"><span data-stu-id="e23ed-190">Code example for a simple app</span></span>

<span data-ttu-id="e23ed-191">Следующий код расширяет приведенный выше поток кода, добавляя код, необходимый для простого примера.</span><span class="sxs-lookup"><span data-stu-id="e23ed-191">The following expands the code flow above to include the code required for a basic sample.</span></span>

### <a name="class-d3d12hellotriangle"></a><span data-ttu-id="e23ed-192">класс D3D12HelloTriangle</span><span class="sxs-lookup"><span data-stu-id="e23ed-192">class D3D12HelloTriangle</span></span>

<span data-ttu-id="e23ed-193">Сначала определите класс в файле заголовка, включая окно просмотра, прямоугольный прямоугольник и буфер вершин, используя структуры:</span><span class="sxs-lookup"><span data-stu-id="e23ed-193">First define the class in a header file, including a viewport, scissor rectangle and vertex buffer using the structures:</span></span>

-   [<span data-ttu-id="e23ed-194">**\_Окно просмотра D3D12**</span><span class="sxs-lookup"><span data-stu-id="e23ed-194">**D3D12\_VIEWPORT**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [<span data-ttu-id="e23ed-195">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="e23ed-195">**D3D12\_RECT**</span></span>](d3d12-rect.md)
-   [<span data-ttu-id="e23ed-196">**\_ \_ Представление буфера вершин \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="e23ed-196">**D3D12\_VERTEX\_BUFFER\_VIEW**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

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

### <a name="oninit"></a><span data-ttu-id="e23ed-197">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-197">OnInit()</span></span>

<span data-ttu-id="e23ed-198">В основном исходном файле проекта запустите инициализацию объектов:</span><span class="sxs-lookup"><span data-stu-id="e23ed-198">In the projects main source file, start initializing the objects:</span></span>

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a><span data-ttu-id="e23ed-199">Лоадпипелине ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-199">LoadPipeline()</span></span>

<span data-ttu-id="e23ed-200">Следующий код создает основы графического конвейера.</span><span class="sxs-lookup"><span data-stu-id="e23ed-200">The following code creates the basics for a graphics pipeline.</span></span> <span data-ttu-id="e23ed-201">Процесс создания устройств и цепочек подкачки очень похож на Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="e23ed-201">The process of creating devices and swap chains is very similar to Direct3D 11.</span></span>

-   <span data-ttu-id="e23ed-202">Включение слоя отладки с вызовами:</span><span class="sxs-lookup"><span data-stu-id="e23ed-202">Enable the debug layer, with calls to:</span></span><dl>

[<span data-ttu-id="e23ed-203">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="e23ed-203">**D3D12GetDebugInterface**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [<span data-ttu-id="e23ed-204">**ID3D12Debug:: Енабледебуглайер**</span><span class="sxs-lookup"><span data-stu-id="e23ed-204">**ID3D12Debug::EnableDebugLayer**</span></span>](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   <span data-ttu-id="e23ed-205">Создайте устройство:</span><span class="sxs-lookup"><span data-stu-id="e23ed-205">Create the device:</span></span><dl>

[<span data-ttu-id="e23ed-206">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="e23ed-206">**CreateDXGIFactory1**</span></span>](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [<span data-ttu-id="e23ed-207">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="e23ed-207">**D3D12CreateDevice**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   <span data-ttu-id="e23ed-208">Заполните описание очереди команд, а затем создайте очередь команд:</span><span class="sxs-lookup"><span data-stu-id="e23ed-208">Fill out a command queue description, then create the command queue:</span></span><dl>

[<span data-ttu-id="e23ed-209">**D3D12 \_ команд \_ в очереди \_**</span><span class="sxs-lookup"><span data-stu-id="e23ed-209">**D3D12\_COMMAND\_QUEUE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [<span data-ttu-id="e23ed-210">**ID3D12Device:: Креатекоммандкуеуе**</span><span class="sxs-lookup"><span data-stu-id="e23ed-210">**ID3D12Device::CreateCommandQueue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   <span data-ttu-id="e23ed-211">Заполните описание имеющуюся цепочку буферов, а затем создайте цепочку буферов обмена:</span><span class="sxs-lookup"><span data-stu-id="e23ed-211">Fill out a swapchain description, then create the swap chain:</span></span> <dl>

[<span data-ttu-id="e23ed-212">**\_ \_ DESC цепочки подкачки \_**</span><span class="sxs-lookup"><span data-stu-id="e23ed-212">**DXGI\_SWAP\_CHAIN\_DESC**</span></span>](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [<span data-ttu-id="e23ed-213">**Идксгифактори:: Креатесвапчаин**</span><span class="sxs-lookup"><span data-stu-id="e23ed-213">**IDXGIFactory::CreateSwapChain**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [<span data-ttu-id="e23ed-214">**IDXGISwapChain3:: Жеткуррентбаккбуффериндекс**</span><span class="sxs-lookup"><span data-stu-id="e23ed-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span></span>](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   <span data-ttu-id="e23ed-215">Заполните описание кучи.</span><span class="sxs-lookup"><span data-stu-id="e23ed-215">Fill out a heap description.</span></span> <span data-ttu-id="e23ed-216">Затем создайте кучу дескрипторов:</span><span class="sxs-lookup"><span data-stu-id="e23ed-216">then create a descriptor heap:</span></span> <dl>

[<span data-ttu-id="e23ed-217">**Описание \_ кучи дескрипторов D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e23ed-217">**D3D12\_DESCRIPTOR\_HEAP\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [<span data-ttu-id="e23ed-218">**ID3D12Device:: Креатедескрипторхеап**</span><span class="sxs-lookup"><span data-stu-id="e23ed-218">**ID3D12Device::CreateDescriptorHeap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [<span data-ttu-id="e23ed-219">**ID3D12Device:: Жетдескрипторхандлеинкрементсизе**</span><span class="sxs-lookup"><span data-stu-id="e23ed-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   <span data-ttu-id="e23ed-220">Создайте представление целевого объекта прорисовки:</span><span class="sxs-lookup"><span data-stu-id="e23ed-220">Create the render target view:</span></span> <dl>

[<span data-ttu-id="e23ed-221">**\_ \_ Дескриптор дескриптора ЦП CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="e23ed-221">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE**</span></span>](cd3dx12-cpu-descriptor-handle.md)  
    [<span data-ttu-id="e23ed-222">**жеткпудескрипторхандлефорхеапстарт**</span><span class="sxs-lookup"><span data-stu-id="e23ed-222">**GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="e23ed-223">**Идксгисвапчаин:: buffer**</span><span class="sxs-lookup"><span data-stu-id="e23ed-223">**IDXGISwapChain::GetBuffer**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [<span data-ttu-id="e23ed-224">**ID3D12Device:: Креатерендертаржетвиев**</span><span class="sxs-lookup"><span data-stu-id="e23ed-224">**ID3D12Device::CreateRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   <span data-ttu-id="e23ed-225">Создайте распределитель команд: [**ID3D12Device:: креатекоммандаллокатор**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span><span class="sxs-lookup"><span data-stu-id="e23ed-225">Create the command allocator: [**ID3D12Device::CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span></span>

<span data-ttu-id="e23ed-226">В последующих шагах списки команд получаются из распределителя команд и передаются в очередь команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-226">In later steps, command lists are obtained from the command allocator and submitted to the command queue.</span></span>

<span data-ttu-id="e23ed-227">Загрузите зависимости конвейера отрисовки (Обратите внимание, что создание программной деформации устройства является полностью необязательным).</span><span class="sxs-lookup"><span data-stu-id="e23ed-227">Load the rendering pipeline dependencies (note that the creation of a software WARP device is entirely optional).</span></span>


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



### <a name="loadassets"></a><span data-ttu-id="e23ed-228">Лоадассетс ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-228">LoadAssets()</span></span>

<span data-ttu-id="e23ed-229">Загрузка и подготовка ресурсов — длительный процесс.</span><span class="sxs-lookup"><span data-stu-id="e23ed-229">Loading and preparing assets is a lengthy process.</span></span> <span data-ttu-id="e23ed-230">Многие из этих этапов похожи на D3D 11, хотя некоторые из них не знакомы с D3D 12.</span><span class="sxs-lookup"><span data-stu-id="e23ed-230">Many of these stages are similar to D3D 11, though some are new to D3D 12.</span></span>

<span data-ttu-id="e23ed-231">В Direct3D 12 требуемое состояние конвейера прикрепляется к списку команд через [объект состояния конвейера](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO).</span><span class="sxs-lookup"><span data-stu-id="e23ed-231">In Direct3D 12, required pipeline state is attached to a command list via a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO).</span></span> <span data-ttu-id="e23ed-232">В этом примере показано, как создать PSO.</span><span class="sxs-lookup"><span data-stu-id="e23ed-232">This example shows how to create a PSO.</span></span> <span data-ttu-id="e23ed-233">Вы можете сохранить PSO как переменную-член и использовать ее столько раз, сколько необходимо.</span><span class="sxs-lookup"><span data-stu-id="e23ed-233">You can store the PSO as a member variable and reuse it as many times as needed.</span></span>

<span data-ttu-id="e23ed-234">Куча дескрипторов определяет представления и способ доступа к ресурсам (например, представление целевого объекта прорисовки).</span><span class="sxs-lookup"><span data-stu-id="e23ed-234">A descriptor heap defines the views and how to access resources (for example, a render target view).</span></span>

<span data-ttu-id="e23ed-235">С помощью распределителя списка команд и PSO можно создать список фактических команд, который будет выполнен позже.</span><span class="sxs-lookup"><span data-stu-id="e23ed-235">With the command list allocator and PSO, you can create the actual command list, which will be executed at a later time.</span></span>

<span data-ttu-id="e23ed-236">В ходе успеха вызываются следующие интерфейсы API и процессы.</span><span class="sxs-lookup"><span data-stu-id="e23ed-236">The following APIs and processes are called in succession.</span></span>

-   <span data-ttu-id="e23ed-237">Создайте пустую корневую подпись с помощью доступной вспомогательной структуры:</span><span class="sxs-lookup"><span data-stu-id="e23ed-237">Create an empty root signature, using the available helper structure:</span></span> <dl>

[<span data-ttu-id="e23ed-238">**\_DESC корневой \_ подписи CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="e23ed-238">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md)  
    [<span data-ttu-id="e23ed-239">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="e23ed-239">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [<span data-ttu-id="e23ed-240">**ID3D12Device:: Креатерутсигнатуре**</span><span class="sxs-lookup"><span data-stu-id="e23ed-240">**ID3D12Device::CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   <span data-ttu-id="e23ed-241">Загрузите и скомпилируйте шейдеры: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span><span class="sxs-lookup"><span data-stu-id="e23ed-241">Load and compile the shaders: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span></span>
-   <span data-ttu-id="e23ed-242">Создайте входной макет вершины: [**D3D12 \_ input \_ element \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="e23ed-242">Create the vertex input layout: [**D3D12\_INPUT\_ELEMENT\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span></span>
-   <span data-ttu-id="e23ed-243">Заполните описание состояния конвейера, используя доступные вспомогательные структуры, а затем создайте состояние графического конвейера:</span><span class="sxs-lookup"><span data-stu-id="e23ed-243">Fill out a pipeline state description, using the helper structures available, then create the graphics pipeline state:</span></span> <dl>

[<span data-ttu-id="e23ed-244">**D3D12 \_ графика \_ состояния графического конвейера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e23ed-244">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [<span data-ttu-id="e23ed-245">**CD3DX12 средство программной \_ прорисовки \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="e23ed-245">**CD3DX12\_RASTERIZER\_DESC**</span></span>](cd3dx12-rasterizer-desc.md)  
    [<span data-ttu-id="e23ed-246">**CD3DX12 \_ Blend, \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="e23ed-246">**CD3DX12\_BLEND\_DESC**</span></span>](cd3dx12-blend-desc.md)  
    [<span data-ttu-id="e23ed-247">**ID3D12Device:: Креатеграфикспипелинестате**</span><span class="sxs-lookup"><span data-stu-id="e23ed-247">**ID3D12Device::CreateGraphicsPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   <span data-ttu-id="e23ed-248">Создайте, а затем закройте список команд:</span><span class="sxs-lookup"><span data-stu-id="e23ed-248">Create, then close, a command list:</span></span> <dl>

[<span data-ttu-id="e23ed-249">**ID3D12Device:: Креатекоммандлист**</span><span class="sxs-lookup"><span data-stu-id="e23ed-249">**ID3D12Device::CreateCommandList**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [<span data-ttu-id="e23ed-250">**ID3D12GraphicsCommandList:: Close**</span><span class="sxs-lookup"><span data-stu-id="e23ed-250">**ID3D12GraphicsCommandList::Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   <span data-ttu-id="e23ed-251">Создайте буфер вершин: [**ID3D12Device:: креатекоммиттедресаурце**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="e23ed-251">Create the vertex buffer: [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>
-   <span data-ttu-id="e23ed-252">Скопируйте данные вершин в буфер вершин:</span><span class="sxs-lookup"><span data-stu-id="e23ed-252">Copy the vertex data to the vertex buffer:</span></span><dl>

[<span data-ttu-id="e23ed-253">**ID3D12Resource:: Map**</span><span class="sxs-lookup"><span data-stu-id="e23ed-253">**ID3D12Resource::Map**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [<span data-ttu-id="e23ed-254">**ID3D12Resource:: отмена сопоставления**</span><span class="sxs-lookup"><span data-stu-id="e23ed-254">**ID3D12Resource::Unmap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   <span data-ttu-id="e23ed-255">Инициализируйте представление буфера вершин: [**жетгпувиртуаладдресс**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span><span class="sxs-lookup"><span data-stu-id="e23ed-255">Initialize the vertex buffer view: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span></span>
-   <span data-ttu-id="e23ed-256">Создайте и инициализируйте ограждение: [**ID3D12Device:: креатефенце**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span><span class="sxs-lookup"><span data-stu-id="e23ed-256">Create and initialize the fence: [**ID3D12Device::CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span></span>
-   <span data-ttu-id="e23ed-257">Создайте обработчик событий для использования с синхронизацией кадров.</span><span class="sxs-lookup"><span data-stu-id="e23ed-257">Create an event handle for use with frame synchronization.</span></span>
-   <span data-ttu-id="e23ed-258">Дождитесь завершения работы GPU.</span><span class="sxs-lookup"><span data-stu-id="e23ed-258">Wait for the GPU to finish.</span></span>


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



### <a name="onupdate"></a><span data-ttu-id="e23ed-259">OnUpdate ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-259">OnUpdate()</span></span>

<span data-ttu-id="e23ed-260">В простом примере ничего не обновляется.</span><span class="sxs-lookup"><span data-stu-id="e23ed-260">For a simple example, nothing is updated.</span></span>


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a><span data-ttu-id="e23ed-261">OnRender ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-261">OnRender()</span></span>

<span data-ttu-id="e23ed-262">Во время установки переменная члена **m \_ коммандлист** была использована для записи и выполнения всех команд Set up.</span><span class="sxs-lookup"><span data-stu-id="e23ed-262">During set up, the member variable **m\_commandList** was used to record and execute all of the set up commands.</span></span> <span data-ttu-id="e23ed-263">Теперь этот элемент можно использовать в основном цикле подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="e23ed-263">You can now reuse that member in the main render loop.</span></span>

<span data-ttu-id="e23ed-264">Подготовка к просмотру включает вызов для заполнения списка команд, затем можно выполнить список команд и следующий буфер в приведенной цепочке буфера обмена:</span><span class="sxs-lookup"><span data-stu-id="e23ed-264">Rendering involves a call to populate the command list, then the command list can be executed and the next buffer in the swap chain presented:</span></span>

-   <span data-ttu-id="e23ed-265">Заполнение списка команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-265">Populate the command list.</span></span>
-   <span data-ttu-id="e23ed-266">Выполните список команд: [**ID3D12CommandQueue:: ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="e23ed-266">Execute the command list: [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>
-   <span data-ttu-id="e23ed-267">[**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) кадр.</span><span class="sxs-lookup"><span data-stu-id="e23ed-267">[**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) the frame.</span></span>
-   <span data-ttu-id="e23ed-268">Дождитесь завершения работы GPU.</span><span class="sxs-lookup"><span data-stu-id="e23ed-268">Wait on the GPU to finish.</span></span>


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



### <a name="populatecommandlist"></a><span data-ttu-id="e23ed-269">Популатекоммандлист ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-269">PopulateCommandList()</span></span>

<span data-ttu-id="e23ed-270">Необходимо сбросить распределителя списка команд и список команд, прежде чем их можно будет использовать повторно.</span><span class="sxs-lookup"><span data-stu-id="e23ed-270">You must reset the command list allocator and the command list itself before you can reuse them.</span></span> <span data-ttu-id="e23ed-271">В более сложных сценариях может иметь смысл сбрасывать распределитель каждые несколько кадров.</span><span class="sxs-lookup"><span data-stu-id="e23ed-271">In more advanced scenarios it might make sense to reset the allocator every several frames.</span></span> <span data-ttu-id="e23ed-272">Память связана с распределительом, который не может быть освобожден сразу после выполнения списка команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-272">Memory is associated with the allocator that can't be released immediately after executing a command list.</span></span> <span data-ttu-id="e23ed-273">В этом примере показано, как сбросить распределитель после каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="e23ed-273">This example shows how to reset the allocator after every frame.</span></span>

<span data-ttu-id="e23ed-274">Теперь повторно используйте список команд для текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="e23ed-274">Now, reuse the command list for the current frame.</span></span> <span data-ttu-id="e23ed-275">Повторное подключение окна просмотра к списку команд (это необходимо делать при каждом сбросе списка команд и перед выполнением списка команд), указывать на то, что ресурс будет использоваться в качестве целевого объекта рендеринга, записывать команды, а затем указать, что целевой объект прорисовки будет использоваться для отображения при завершении выполнения списка команд.</span><span class="sxs-lookup"><span data-stu-id="e23ed-275">Reattach the viewport to the command list (which must be done whenever a command list is reset, and before the command list is executed), indicate that the resource will be in use as a render target, record commands, and then indicate that the render target will be used to present when the command list is done executing.</span></span>

<span data-ttu-id="e23ed-276">Заполнение списков команд вызывает следующие методы и процессы в свою очередь:</span><span class="sxs-lookup"><span data-stu-id="e23ed-276">Populating command lists calls the following methods and processes in turn:</span></span>

-   <span data-ttu-id="e23ed-277">Сброс распределителя команд и список команд:</span><span class="sxs-lookup"><span data-stu-id="e23ed-277">Reset the command allocator, and command list:</span></span> <dl>

[<span data-ttu-id="e23ed-278">**ID3D12CommandAllocator:: Reset**</span><span class="sxs-lookup"><span data-stu-id="e23ed-278">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [<span data-ttu-id="e23ed-279">**ID3D12GraphicsCommandList:: Reset**</span><span class="sxs-lookup"><span data-stu-id="e23ed-279">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   <span data-ttu-id="e23ed-280">Задать корневую подпись, окно просмотра и прямоугольники ножниц:</span><span class="sxs-lookup"><span data-stu-id="e23ed-280">Set the root signature, viewport and scissors rectangles:</span></span> <dl>

[<span data-ttu-id="e23ed-281">**ID3D12GraphicsCommandList:: Сетграфиксрутсигнатуре**</span><span class="sxs-lookup"><span data-stu-id="e23ed-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [<span data-ttu-id="e23ed-282">**ID3D12GraphicsCommandList:: Рссетвиевпортс**</span><span class="sxs-lookup"><span data-stu-id="e23ed-282">**ID3D12GraphicsCommandList::RSSetViewports**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [<span data-ttu-id="e23ed-283">**ID3D12GraphicsCommandList:: РссетсЦиссорректс**</span><span class="sxs-lookup"><span data-stu-id="e23ed-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   <span data-ttu-id="e23ed-284">Укажите, что задний буфер должен использоваться в качестве целевого объекта рендеринга:</span><span class="sxs-lookup"><span data-stu-id="e23ed-284">Indicate that the back buffer is to be used as a render target:</span></span> <dl>

[<span data-ttu-id="e23ed-285">**ID3D12GraphicsCommandList:: Ресаурцебарриер**</span><span class="sxs-lookup"><span data-stu-id="e23ed-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [<span data-ttu-id="e23ed-286">**ID3D12DescriptorHeap:: Жеткпудескрипторхандлефорхеапстарт**</span><span class="sxs-lookup"><span data-stu-id="e23ed-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="e23ed-287">**ID3D12GraphicsCommandList:: Омсетрендертаржетс**</span><span class="sxs-lookup"><span data-stu-id="e23ed-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   <span data-ttu-id="e23ed-288">Запишите команды:</span><span class="sxs-lookup"><span data-stu-id="e23ed-288">Record the commands:</span></span><dl>

[<span data-ttu-id="e23ed-289">**ID3D12GraphicsCommandList:: Клеаррендертаржетвиев**</span><span class="sxs-lookup"><span data-stu-id="e23ed-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [<span data-ttu-id="e23ed-290">**ID3D12GraphicsCommandList:: Иасетпримитиветопологи**</span><span class="sxs-lookup"><span data-stu-id="e23ed-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [<span data-ttu-id="e23ed-291">**ID3D12GraphicsCommandList:: Иасетвертексбуфферс**</span><span class="sxs-lookup"><span data-stu-id="e23ed-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [<span data-ttu-id="e23ed-292">**ID3D12GraphicsCommandList::D Равинстанцед**</span><span class="sxs-lookup"><span data-stu-id="e23ed-292">**ID3D12GraphicsCommandList::DrawInstanced**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   <span data-ttu-id="e23ed-293">Укажите, что задний буфер теперь будет использоваться для представления: [**ID3D12GraphicsCommandList:: ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="e23ed-293">Indicate the back buffer will now be used to present: [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>
-   <span data-ttu-id="e23ed-294">Закройте список команд: [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span><span class="sxs-lookup"><span data-stu-id="e23ed-294">Close the command list: [**ID3D12GraphicsCommandList::Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span></span>


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



### <a name="waitforpreviousframe"></a><span data-ttu-id="e23ed-295">Ваитфорпревиаусфраме ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-295">WaitForPreviousFrame()</span></span>

<span data-ttu-id="e23ed-296">В следующем коде показано чрезмерно упрощенное использование ограждений.</span><span class="sxs-lookup"><span data-stu-id="e23ed-296">The following code shows an over-simplified use of fences.</span></span>

> [!Note]  
> <span data-ttu-id="e23ed-297">Ожидание завершения кадра слишком эффективно для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="e23ed-297">Waiting for a frame to complete is too inefficient for most apps.</span></span>

 

<span data-ttu-id="e23ed-298">Следующие интерфейсы API и процессы вызываются по порядку:</span><span class="sxs-lookup"><span data-stu-id="e23ed-298">The following APIs and processes are called in order:</span></span>

-   [<span data-ttu-id="e23ed-299">**ID3D12CommandQueue:: сигнал**</span><span class="sxs-lookup"><span data-stu-id="e23ed-299">**ID3D12CommandQueue::Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [<span data-ttu-id="e23ed-300">**ID3D12Fence:: Жеткомплетедвалуе**</span><span class="sxs-lookup"><span data-stu-id="e23ed-300">**ID3D12Fence::GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [<span data-ttu-id="e23ed-301">**ID3D12Fence:: Сетевентонкомплетион**</span><span class="sxs-lookup"><span data-stu-id="e23ed-301">**ID3D12Fence::SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   <span data-ttu-id="e23ed-302">Дождитесь события.</span><span class="sxs-lookup"><span data-stu-id="e23ed-302">Wait for the event.</span></span>
-   <span data-ttu-id="e23ed-303">Обновите индекс кадра: [**IDXGISwapChain3:: жеткуррентбаккбуффериндекс**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span><span class="sxs-lookup"><span data-stu-id="e23ed-303">Update the frame index: [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span></span>


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



### <a name="ondestroy"></a><span data-ttu-id="e23ed-304">OnDestroy ()</span><span class="sxs-lookup"><span data-stu-id="e23ed-304">OnDestroy()</span></span>

<span data-ttu-id="e23ed-305">Аккуратно закройте приложение.</span><span class="sxs-lookup"><span data-stu-id="e23ed-305">Cleanly close down the app.</span></span>

-   <span data-ttu-id="e23ed-306">Дождитесь завершения работы GPU.</span><span class="sxs-lookup"><span data-stu-id="e23ed-306">Wait for the GPU to finish.</span></span>
-   <span data-ttu-id="e23ed-307">Закройте событие.</span><span class="sxs-lookup"><span data-stu-id="e23ed-307">Close the event.</span></span>


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a><span data-ttu-id="e23ed-308">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e23ed-308">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e23ed-309">Основные сведения о Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e23ed-309">Understanding Direct3D 12</span></span>](directx-12-getting-started.md)
</dt> <dt>

[<span data-ttu-id="e23ed-310">Рабочие образцы</span><span class="sxs-lookup"><span data-stu-id="e23ed-310">Working Samples</span></span>](working-samples.md)
</dt> </dl>

 

 
