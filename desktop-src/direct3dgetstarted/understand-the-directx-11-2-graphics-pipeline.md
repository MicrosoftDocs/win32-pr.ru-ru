---
title: Общие сведения о конвейере визуализации Direct3D 11
description: Ранее вы рассматривали создание окна, которое можно использовать для рисования в работе с ресурсами устройств DirectX. Теперь вы узнаете, как создать графический конвейер и к нему можно присоединиться.
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50f9a387b2d44fe750abcf5a8856f75e6d0110e
ms.sourcegitcommit: 07b756a2f350efa5cfd5024a723ef392274ac3d9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "105720017"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a><span data-ttu-id="03e64-104">Общие сведения о конвейере визуализации Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="03e64-104">Understand the Direct3D 11 rendering pipeline</span></span>

<span data-ttu-id="03e64-105">Ранее вы рассматривали создание окна, которое можно использовать для рисования в [работе с ресурсами устройств DirectX](work-with-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="03e64-105">Previously, you looked at how to create a window you can use for drawing in [Work with DirectX device resources](work-with-dxgi.md).</span></span> <span data-ttu-id="03e64-106">Теперь вы узнаете, как создать графический конвейер и к нему можно присоединиться.</span><span class="sxs-lookup"><span data-stu-id="03e64-106">Now, you learn how to build the graphics pipeline, and where you can hook into it.</span></span>

<span data-ttu-id="03e64-107">Вы помните, что существует два интерфейса Direct3D, которые определяют конвейер графики: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), который обеспечивает виртуальное представление GPU и его ресурсов. и [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), который представляет обработку графики для конвейера.</span><span class="sxs-lookup"><span data-stu-id="03e64-107">You'll recall that there are two Direct3D interfaces that define the graphics pipeline: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), which provides a virtual representation of the GPU and its resources; and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), which represents the graphics processing for the pipeline.</span></span> <span data-ttu-id="03e64-108">Как правило, экземпляр **ID3D11Device** используется для настройки и получения ресурсов GPU, необходимых для начала обработки графики в сцене, и используется **ссылку ID3D11DeviceContext** для обработки этих ресурсов на каждом соответствующем этапе шейдера в графическом конвейере.</span><span class="sxs-lookup"><span data-stu-id="03e64-108">Typically, you use an instance of **ID3D11Device** to configure and obtain the GPU resources you need to start processing the graphics in a scene, and you use **ID3D11DeviceContext** to process those resources at each appropriate shader stage in the graphics pipeline.</span></span> <span data-ttu-id="03e64-109">Обычно методы **ID3D11Device** вызываются редко, т. е. только при настройке сцены или при изменении устройства.</span><span class="sxs-lookup"><span data-stu-id="03e64-109">You usually call **ID3D11Device** methods infrequently—that is, only when you set up a scene or when the device changes.</span></span> <span data-ttu-id="03e64-110">С другой стороны, вы вызываете **ссылку ID3D11DeviceContext** каждый раз при обработке кадра для вывода.</span><span class="sxs-lookup"><span data-stu-id="03e64-110">On the other hand, you'll call **ID3D11DeviceContext** every time you process a frame for display.</span></span>

<span data-ttu-id="03e64-111">В этом примере создается и настраивается минимальный графический конвейер, подходящий для отображения простого цикличного Куба, затененного вершиной.</span><span class="sxs-lookup"><span data-stu-id="03e64-111">This example creates and configures a minimal graphics pipeline suitable for displaying a simple spinning, vertex-shaded cube.</span></span> <span data-ttu-id="03e64-112">Он демонстрирует приблизительно минимальный набор ресурсов, необходимых для вывода.</span><span class="sxs-lookup"><span data-stu-id="03e64-112">It demonstrates approximately the smallest set of resources necessary for display.</span></span> <span data-ttu-id="03e64-113">При чтении этих сведений Обратите внимание на ограничения данного примера, где может потребоваться расширить его для поддержки сцены, которую нужно визуализировать.</span><span class="sxs-lookup"><span data-stu-id="03e64-113">As you read the info here, note the limitations of the given example where you may have to extend it to support the scene you want to render.</span></span>

<span data-ttu-id="03e64-114">В этом примере рассматриваются два класса C++ для графики: класс диспетчера ресурсов устройства и класс модуля подготовки 3D-сцены.</span><span class="sxs-lookup"><span data-stu-id="03e64-114">This example covers two C++ classes for graphics: a device resource manager class, and 3D scene renderer class.</span></span> <span data-ttu-id="03e64-115">В этом разделе особое внимание уделяется модулю визуализации 3D-сцены.</span><span class="sxs-lookup"><span data-stu-id="03e64-115">This topic focuses specifically on the 3D scene renderer.</span></span>

## <a name="what-does-the-cube-renderer-do"></a><span data-ttu-id="03e64-116">Что делает модуль подготовки Куба?</span><span class="sxs-lookup"><span data-stu-id="03e64-116">What does the cube renderer do?</span></span>

<span data-ttu-id="03e64-117">Графический конвейер определяется классом модуля подготовки 3D-сцены.</span><span class="sxs-lookup"><span data-stu-id="03e64-117">The graphics pipeline is defined by the 3D scene renderer class.</span></span> <span data-ttu-id="03e64-118">Модуль подготовки сцены может:</span><span class="sxs-lookup"><span data-stu-id="03e64-118">The scene renderer is able to:</span></span>

-   <span data-ttu-id="03e64-119">Определите постоянные буферы для хранения единообразных данных.</span><span class="sxs-lookup"><span data-stu-id="03e64-119">Define constant buffers to store your uniform data.</span></span>
-   <span data-ttu-id="03e64-120">Определите буферы вершин для хранения данных вершин объекта и соответствующие буферы индексов, чтобы позволить шейдеру вершин правильно проанализировать треугольники.</span><span class="sxs-lookup"><span data-stu-id="03e64-120">Define vertex buffers to hold your object vertex data, and corresponding index buffers to enable the vertex shader to walk the triangles correctly.</span></span>
-   <span data-ttu-id="03e64-121">Создание ресурсов текстуры и представлений ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03e64-121">Create texture resources and resource views.</span></span>
-   <span data-ttu-id="03e64-122">Загрузите объекты шейдера.</span><span class="sxs-lookup"><span data-stu-id="03e64-122">Load your shader objects.</span></span>
-   <span data-ttu-id="03e64-123">Обновите графические данные, чтобы отобразить каждый кадр.</span><span class="sxs-lookup"><span data-stu-id="03e64-123">Update the graphics data to display each frame.</span></span>
-   <span data-ttu-id="03e64-124">Отрисовка (прорисовка) графики в цепочке буферов.</span><span class="sxs-lookup"><span data-stu-id="03e64-124">Render (draw) the graphics to the swap chain.</span></span>

<span data-ttu-id="03e64-125">Первые четыре процесса обычно используют методы интерфейса [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) для инициализации графических ресурсов и управления ими, а последние два используют методы интерфейса [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) для управления и выполнения графического конвейера.</span><span class="sxs-lookup"><span data-stu-id="03e64-125">The first four processes typically use the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) interface methods for initializing and managing graphics resources, and the last two use the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) interface methods to manage and execute the graphics pipeline.</span></span>

<span data-ttu-id="03e64-126">Экземпляр класса модуля **подготовки** отчетов создается и управляется как переменная-член в основном классе проекта.</span><span class="sxs-lookup"><span data-stu-id="03e64-126">An instance of the **Renderer** class is created and managed as a member variable on the main project class.</span></span> <span data-ttu-id="03e64-127">Экземпляр **DeviceResources** управляется как общий указатель на несколько классов, включая главный класс проекта, класс представления **приложения** и модуль **подготовки** отчетов.</span><span class="sxs-lookup"><span data-stu-id="03e64-127">The **DeviceResources** instance is managed as a shared pointer across several classes, including the main project class, the **App** view-provider class, and **Renderer**.</span></span> <span data-ttu-id="03e64-128">При замене модуля **подготовки** отчетов на собственный класс рассмотрите возможность объявления и назначения экземпляра **DeviceResources** в качестве совместно используемого элемента указателя:</span><span class="sxs-lookup"><span data-stu-id="03e64-128">If you replace **Renderer** with your own class, consider declaring and assigning the **DeviceResources** instance as a shared pointer member as well:</span></span>

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

<span data-ttu-id="03e64-129">Перед созданием экземпляра **DeviceResources** в методе **Initialize** класса **app** просто передайте указатель в конструктор класса (или другой метод инициализации).</span><span class="sxs-lookup"><span data-stu-id="03e64-129">Just pass the pointer into the class constructor (or other initialization method) after the **DeviceResources** instance is created in the **Initialize** method of the **App** class.</span></span> <span data-ttu-id="03e64-130">Можно также передать **слабую \_ ptr** -ссылку, если вместо этого требуется, чтобы главный класс полностью владеет экземпляром **DeviceResources** .</span><span class="sxs-lookup"><span data-stu-id="03e64-130">You can also pass a **weak\_ptr** reference if, instead, you want your main class to completely own the **DeviceResources** instance.</span></span>

## <a name="create-the-cube-renderer"></a><span data-ttu-id="03e64-131">Создание модуля подготовки Куба</span><span class="sxs-lookup"><span data-stu-id="03e64-131">Create the cube renderer</span></span>

<span data-ttu-id="03e64-132">В этом примере класс модуля подготовки сцены организован с помощью следующих методов:</span><span class="sxs-lookup"><span data-stu-id="03e64-132">In this example, we organize the scene renderer class with the following methods:</span></span>

-   <span data-ttu-id="03e64-133">**Креатедевицедепендентресаурцес**: вызывается всякий раз, когда необходимо инициализировать или перезапустить сцену.</span><span class="sxs-lookup"><span data-stu-id="03e64-133">**CreateDeviceDependentResources**: Called whenever the scene must be initialized or restarted.</span></span> <span data-ttu-id="03e64-134">Этот метод загружает начальные данные вершин, текстуры, шейдеры и другие ресурсы, а также конструирует исходные константы и буферы вершин.</span><span class="sxs-lookup"><span data-stu-id="03e64-134">This method loads your initial vertex data, textures, shaders, and other resources, and constructs the initial constant and vertex buffers.</span></span> <span data-ttu-id="03e64-135">Как правило, большая часть работы выполняется с помощью методов [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) , а не [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) методов.</span><span class="sxs-lookup"><span data-stu-id="03e64-135">Typically, most of the work here is done with [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) methods, not [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) methods.</span></span>
-   <span data-ttu-id="03e64-136">**Креатевиндовсизедепендентресаурцес**: вызывается при каждом изменении состояния окна, например, при изменении размера или ориентации.</span><span class="sxs-lookup"><span data-stu-id="03e64-136">**CreateWindowSizeDependentResources**: Called whenever the window state changes, such as when resizing occurs or when orientation changes.</span></span> <span data-ttu-id="03e64-137">Этот метод перестраивает матрицы преобразования, например, для камеры.</span><span class="sxs-lookup"><span data-stu-id="03e64-137">This method rebuilds transform matrices, such as those for your camera.</span></span>
-   <span data-ttu-id="03e64-138">**Обновление**: обычно вызывается из части программы, которая управляет состоянием немедленной игры; в этом примере мы просто вызываем его из класса **Main** .</span><span class="sxs-lookup"><span data-stu-id="03e64-138">**Update**: Typically called from the part of the program that manages immediate game state; in this example, we just call it from the **Main** class.</span></span> <span data-ttu-id="03e64-139">Этот метод должен считывать сведения о состоянии игры, которые влияют на отрисовку, такие как обновление расположения объекта или кадров анимации, а также любые глобальные данные игры, такие как легкие или изменения в физике игры.</span><span class="sxs-lookup"><span data-stu-id="03e64-139">Have this method read from any game-state information that affects rendering, such as updates to object position or animation frames, plus any global game data like light levels or changes to game physics.</span></span> <span data-ttu-id="03e64-140">Эти входные данные используются для обновления покадровых буферов констант и данных объектов.</span><span class="sxs-lookup"><span data-stu-id="03e64-140">These inputs are used to update the per-frame constant buffers and object data.</span></span>
-   <span data-ttu-id="03e64-141">**Render**: обычно вызывается из части программы, которая управляет циклом игры; в этом случае он вызывается из класса **Main** .</span><span class="sxs-lookup"><span data-stu-id="03e64-141">**Render**: Typically called from the part of the program that manages the game loop; in this case, it's called from the **Main** class.</span></span> <span data-ttu-id="03e64-142">Этот метод создает графический конвейер: привязывает шейдеры, привязывает буферы и ресурсы к этапам шейдера и вызывает Рисование для текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="03e64-142">This method constructs the graphics pipeline: it binds shaders, binds buffers and resources to shader stages, and invokes drawing for the current frame.</span></span>

<span data-ttu-id="03e64-143">Эти методы состоят из текста поведений для визуализации сцены с помощью Direct3D с использованием ваших ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03e64-143">These methods comprise the body of behaviors for rendering a scene with Direct3D using your assets.</span></span> <span data-ttu-id="03e64-144">Если расширить этот пример с помощью нового класса отрисовки, объявите его в основном классе проекта.</span><span class="sxs-lookup"><span data-stu-id="03e64-144">If you extend this example with a new rendering class, declare it on the main project class.</span></span> <span data-ttu-id="03e64-145">Таким образом:</span><span class="sxs-lookup"><span data-stu-id="03e64-145">So this:</span></span>

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="03e64-146">становится</span><span class="sxs-lookup"><span data-stu-id="03e64-146">becomes this:</span></span>

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="03e64-147">Обратите внимание, что в этом примере предполагается, что методы имеют одинаковые сигнатуры в вашей реализации.</span><span class="sxs-lookup"><span data-stu-id="03e64-147">Again, note that this example assumes that the methods have the same signatures in your implementation.</span></span> <span data-ttu-id="03e64-148">Если подписи были изменены, проверьте **главный** цикл и внесите соответствующие изменения.</span><span class="sxs-lookup"><span data-stu-id="03e64-148">If the signatures have changed, review the **Main** loop and make the changes accordingly.</span></span>

<span data-ttu-id="03e64-149">Давайте более подробно рассмотрим методы отрисовки сцены.</span><span class="sxs-lookup"><span data-stu-id="03e64-149">Let's take a look at scene-rendering methods in more detail.</span></span>

## <a name="create-device-dependent-resources"></a><span data-ttu-id="03e64-150">Создание ресурсов, зависящих от устройства</span><span class="sxs-lookup"><span data-stu-id="03e64-150">Create device dependent resources</span></span>

<span data-ttu-id="03e64-151">**Креатедевицедепендентресаурцес** объединяет все операции для инициализации сцены и ее ресурсов с помощью вызовов [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) .</span><span class="sxs-lookup"><span data-stu-id="03e64-151">**CreateDeviceDependentResources** consolidates all the operations for initializing the scene and its resources using [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) calls.</span></span> <span data-ttu-id="03e64-152">Этот метод предполагает, что устройство Direct3D только что было инициализировано (или создано повторно) для сцены.</span><span class="sxs-lookup"><span data-stu-id="03e64-152">This method assumes that the Direct3D device has just been initialized (or has been recreated) for a scene.</span></span> <span data-ttu-id="03e64-153">Он воссоздает или перезагружает все графические ресурсы, относящиеся к сцене, такие как шейдер вершин и текстуры, буферы вершин и индексов для объектов, а также любые другие ресурсы (например, текстуры и соответствующие представления).</span><span class="sxs-lookup"><span data-stu-id="03e64-153">It recreates or reloads all scene-specific graphics resources, such as the vertex and pixel shaders, the vertex and index buffers for objects, and any other resources (for example, as textures and their corresponding views).</span></span>

<span data-ttu-id="03e64-154">Вот пример кода для **креатедевицедепендентресаурцес**:</span><span class="sxs-lookup"><span data-stu-id="03e64-154">Here's example code for **CreateDeviceDependentResources**:</span></span>


```C++
void Renderer::CreateDeviceDependentResources()
{
    // Compile shaders using the Effects library.
    auto CreateShadersTask = Concurrency::create_task(
            [this]( )
            {
                CreateShaders();
            }
        );

    // Load the geometry for the spinning cube.
    auto CreateCubeTask = CreateShadersTask.then(
            [this]()
            {
                CreateCube();
            }
        );
}

void Renderer::CreateWindowSizeDependentResources()
{
    // Create the view matrix and the perspective matrix.
    CreateViewAndPerspective();
}
```



<span data-ttu-id="03e64-155">Каждый раз при загрузке ресурсов с диска — такие ресурсы, как скомпилированные объекты шейдера (CSO или CSO), делают это асинхронно.</span><span class="sxs-lookup"><span data-stu-id="03e64-155">Any time you load resources from disk—resources like compiled shader object (CSO, or .cso) files or textures—do so asynchronously.</span></span> <span data-ttu-id="03e64-156">Это позволяет выполнять другие операции одновременно (например, другие задачи установки), а поскольку главный цикл не блокируется, вы можете отображать визуально интересующие пользователя данные (например, анимацию загрузки для игры).</span><span class="sxs-lookup"><span data-stu-id="03e64-156">This allows you to keep other work going at the same time (like other setup tasks), and because the main loop isn't blocked you can keep displaying something visually interesting to the user (like a loading animation for your game).</span></span> <span data-ttu-id="03e64-157">В этом примере используется API Concurrency:: Tasks, доступный начиная с Windows 8; Обратите внимание на синтаксис лямбда-выражений, используемый для инкапсуляции задач асинхронной загрузки.</span><span class="sxs-lookup"><span data-stu-id="03e64-157">This example uses the Concurrency::Tasks API that is available starting in Windows 8; note the lambda syntax used to encapsulate asynchronous loading tasks.</span></span> <span data-ttu-id="03e64-158">Эти лямбда-выражения представляют функции, называемые «за пределами потока», поэтому явным образом фиксируется указатель на текущий объект класса (**this**).</span><span class="sxs-lookup"><span data-stu-id="03e64-158">These lambdas represent the functions called off-thread, so a pointer to the current class object (**this**) is explicitly captured.</span></span>

<span data-ttu-id="03e64-159">Ниже приведен пример того, как можно загрузить байтовый код шейдера:</span><span class="sxs-lookup"><span data-stu-id="03e64-159">Here's an example of how you can load shader bytecode:</span></span>


```C++
HRESULT hr = S_OK;

// Use the Direct3D device to load resources into graphics memory.
ID3D11Device* device = m_deviceResources->GetDevice();

// You'll need to use a file loader to load the shader bytecode. In this
// example, we just use the standard library.
FILE* vShader, * pShader;
BYTE* bytes;

size_t destSize = 4096;
size_t bytesRead = 0;
bytes = new BYTE[destSize];

fopen_s(&vShader, "CubeVertexShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, vShader);
hr = device->CreateVertexShader(
    bytes,
    bytesRead,
    nullptr,
    &m_pVertexShader
    );

D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );

delete bytes;


bytes = new BYTE[destSize];
bytesRead = 0;
fopen_s(&pShader, "CubePixelShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, pShader);
hr = device->CreatePixelShader(
    bytes,
    bytesRead,
    nullptr,
    m_pPixelShader.GetAddressOf()
    );

delete bytes;

CD3D11_BUFFER_DESC cbDesc(
    sizeof(ConstantBufferStruct),
    D3D11_BIND_CONSTANT_BUFFER
    );

hr = device->CreateBuffer(
    &cbDesc,
    nullptr,
    m_pConstantBuffer.GetAddressOf()
    );

fclose(vShader);
fclose(pShader);
```



<span data-ttu-id="03e64-160">Ниже приведен пример создания буферов вершин и индексов.</span><span class="sxs-lookup"><span data-stu-id="03e64-160">Here's an example of how to create vertex and index buffers:</span></span>


```C++
HRESULT Renderer::CreateCube()
{
    HRESULT hr = S_OK;

    // Use the Direct3D device to load resources into graphics memory.
    ID3D11Device* device = m_deviceResources->GetDevice();

    // Create cube geometry.
    VertexPositionColor CubeVertices[] =
    {
        {DirectX::XMFLOAT3(-0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  0,   0,   0),},
        {DirectX::XMFLOAT3(-0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  0,   0,   1),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  0,   1,   0),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  0,   1,   1),},

        {DirectX::XMFLOAT3( 0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  1,   0,   0),},
        {DirectX::XMFLOAT3( 0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  1,   0,   1),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  1,   1,   0),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  1,   1,   1),},
    };
    
    // Create vertex buffer:
    
    CD3D11_BUFFER_DESC vDesc(
        sizeof(CubeVertices),
        D3D11_BIND_VERTEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA vData;
    ZeroMemory(&vData, sizeof(D3D11_SUBRESOURCE_DATA));
    vData.pSysMem = CubeVertices;
    vData.SysMemPitch = 0;
    vData.SysMemSlicePitch = 0;

    hr = device->CreateBuffer(
        &vDesc,
        &vData,
        &m_pVertexBuffer
        );

    // Create index buffer:
    unsigned short CubeIndices [] = 
    {
        0,2,1, // -x
        1,2,3,

        4,5,6, // +x
        5,7,6,

        0,1,5, // -y
        0,5,4,

        2,6,7, // +y
        2,7,3,

        0,4,6, // -z
        0,6,2,

        1,3,7, // +z
        1,7,5,
    };

    m_indexCount = ARRAYSIZE(CubeIndices);

    CD3D11_BUFFER_DESC iDesc(
        sizeof(CubeIndices),
        D3D11_BIND_INDEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA iData;
    ZeroMemory(&iData, sizeof(D3D11_SUBRESOURCE_DATA));
    iData.pSysMem = CubeIndices;
    iData.SysMemPitch = 0;
    iData.SysMemSlicePitch = 0;
    
    hr = device->CreateBuffer(
        &iDesc,
        &iData,
        &m_pIndexBuffer
        );

    return hr;
}
```



<span data-ttu-id="03e64-161">В этом примере не загружаются ни сетки, ни текстуры.</span><span class="sxs-lookup"><span data-stu-id="03e64-161">This example does not load any meshes or textures.</span></span> <span data-ttu-id="03e64-162">Необходимо создать методы для загрузки сетки и типов текстур, относящихся к игре, и вызывать их асинхронно.</span><span class="sxs-lookup"><span data-stu-id="03e64-162">You must create the methods for loading the mesh and texture types that are specific to your game, and call them asynchronously.</span></span>

<span data-ttu-id="03e64-163">Здесь также заполните начальные значения для буферов констант на сцене.</span><span class="sxs-lookup"><span data-stu-id="03e64-163">Populate initial values for your per-scene constant buffers here, too.</span></span> <span data-ttu-id="03e64-164">Примерами буфера констант на сцене являются фиксированные огни или другие статические элементы сцены и данные.</span><span class="sxs-lookup"><span data-stu-id="03e64-164">Examples of per-scene constant buffer include fixed lights, or other static scene elements and data.</span></span>

## <a name="implement-the-createwindowsizedependentresources-method"></a><span data-ttu-id="03e64-165">Реализация метода Креатевиндовсизедепендентресаурцес</span><span class="sxs-lookup"><span data-stu-id="03e64-165">Implement the CreateWindowSizeDependentResources method</span></span>

<span data-ttu-id="03e64-166">Методы **креатевиндовсизедепендентресаурцес** вызываются каждый раз при изменении размера, ориентации или разрешения окна.</span><span class="sxs-lookup"><span data-stu-id="03e64-166">**CreateWindowSizeDependentResources** methods are called every time the window size, orientation, or resolution changes.</span></span>

<span data-ttu-id="03e64-167">Ресурсы размера окна обновляются следующим образом: статическая процедура сообщения получает одно из нескольких возможных событий, указывающих на изменение состояния окна.</span><span class="sxs-lookup"><span data-stu-id="03e64-167">Window size resources are updated like so: The static message proc gets one of several possible events indicating a change in window state.</span></span> <span data-ttu-id="03e64-168">Затем ваш главный цикл уведомляется о событии и вызывает **креатевиндовсизедепендентресаурцес** в основном экземпляре класса, который затем вызывает реализацию **креатевиндовсизедепендентресаурцес** в классе визуализатора сцены.</span><span class="sxs-lookup"><span data-stu-id="03e64-168">Your main loop is then informed about the event and calls **CreateWindowSizeDependentResources** on the main class instance, which then calls the **CreateWindowSizeDependentResources** implementation on the scene renderer class.</span></span>

<span data-ttu-id="03e64-169">Основная задача этого метода — гарантировать, что в результате изменения свойств окна визуальные объекты не станут беспорядочными или недействительными.</span><span class="sxs-lookup"><span data-stu-id="03e64-169">The primary job of this method is to make sure the visuals don't become confused or invalid because of a change in window properties.</span></span> <span data-ttu-id="03e64-170">В этом примере мы обновляем матрицы проекта с помощью нового поля View (фов) для измененного или переориентированного окна.</span><span class="sxs-lookup"><span data-stu-id="03e64-170">In this example, we update the project matrices with a new field of view (FOV) for the resized or reoriented window.</span></span>

<span data-ttu-id="03e64-171">Мы уже видели код для создания оконных ресурсов в **DeviceResources** , который был цепочкой подкачки (с задним буфером) и представлением целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="03e64-171">We already saw the code for creating window resources in **DeviceResources** - that was the swap chain (with back buffer) and render target view.</span></span> <span data-ttu-id="03e64-172">Ниже показано, как модуль подготовки отчетов создает преобразования, зависимые от пропорций:</span><span class="sxs-lookup"><span data-stu-id="03e64-172">Here's how the renderer creates aspect ratio-dependent transforms:</span></span>


```C++
void Renderer::CreateViewAndPerspective()
{
    // Use DirectXMath to create view and perspective matrices.

    DirectX::XMVECTOR eye = DirectX::XMVectorSet(0.0f, 0.7f, 1.5f, 0.f);
    DirectX::XMVECTOR at  = DirectX::XMVectorSet(0.0f,-0.1f, 0.0f, 0.f);
    DirectX::XMVECTOR up  = DirectX::XMVectorSet(0.0f, 1.0f, 0.0f, 0.f);

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.view,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixLookAtRH(
                eye,
                at,
                up
                )
            )
        );

    float aspectRatioX = m_deviceResources->GetAspectRatio();
    float aspectRatioY = aspectRatioX < (16.0f / 9.0f) ? aspectRatioX / (16.0f / 9.0f) : 1.0f;

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.projection,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixPerspectiveFovRH(
                2.0f * std::atan(std::tan(DirectX::XMConvertToRadians(70) * 0.5f) / aspectRatioY),
                aspectRatioX,
                0.01f,
                100.0f
                )
            )
        );
}
```



<span data-ttu-id="03e64-173">Если сцена имеет определенную структуру компонентов, которые зависят от пропорций, это место для их изменения в соответствии с пропорциями.</span><span class="sxs-lookup"><span data-stu-id="03e64-173">If your scene has a specific layout of components that depends on the aspect ratio, this is the place to rearrange them to match that aspect ratio.</span></span> <span data-ttu-id="03e64-174">Здесь также может потребоваться изменить конфигурацию поведения после обработки.</span><span class="sxs-lookup"><span data-stu-id="03e64-174">You may want to change the configuration of post-processing behavior here also.</span></span>

## <a name="implement-the-update-method"></a><span data-ttu-id="03e64-175">Реализация метода Update</span><span class="sxs-lookup"><span data-stu-id="03e64-175">Implement the Update method</span></span>

<span data-ttu-id="03e64-176">Метод **Update** вызывается один раз для каждого цикла игры. в этом примере он вызывается методом основного класса с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="03e64-176">The **Update** method is called once per game loop - in this example, it is called by the main class's method of the same name.</span></span> <span data-ttu-id="03e64-177">Она имеет простую цель: обновление геометрии сцены и состояния игры на основе количества затраченного времени (или шагов, затраченного на период) с момента предыдущего кадра.</span><span class="sxs-lookup"><span data-stu-id="03e64-177">It has a simple purpose: update scene geometry and game state based on the amount of elapsed time (or elapsed time steps) since the previous frame.</span></span> <span data-ttu-id="03e64-178">В этом примере мы просто поворотим куб по одному разу для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="03e64-178">In this example, we simply rotate the cube once per frame.</span></span> <span data-ttu-id="03e64-179">В реальной игровой сцене этот метод содержит гораздо больше кода для проверки состояния игры, обновления отдельных (или других динамических) буферов констант, геометрических буферов и других ресурсов в памяти соответственно.</span><span class="sxs-lookup"><span data-stu-id="03e64-179">In a real game scene, this method contains a lot more code for checking game state, updating per-frame (or other dynamic) constant buffers, geometry buffers, and other in-memory assets accordingly.</span></span> <span data-ttu-id="03e64-180">Так как взаимодействие между ЦП и GPU вызывает дополнительные издержки, убедитесь, что обновлены только буферы, которые действительно изменились с момента последнего кадра. буферы констант можно сгруппировать или разделить, чтобы сделать это более эффективным.</span><span class="sxs-lookup"><span data-stu-id="03e64-180">Since communication between the CPU and GPU incurs overhead, make sure you only update buffers that have actually changed since the last frame - your constant buffers can be grouped, or split up, as needed to make this more efficient.</span></span>


```C++
void Renderer::Update()
{
    // Rotate the cube 1 degree per frame.
    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.world,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixRotationY(
                DirectX::XMConvertToRadians(
                    (float) m_frameCount++
                    )
                )
            )
        );

    if (m_frameCount == MAXUINT)  m_frameCount = 0;
}
```



<span data-ttu-id="03e64-181">В этом случае при **повороте** происходит обновление буфера констант с помощью новой матрицы преобразования для куба.</span><span class="sxs-lookup"><span data-stu-id="03e64-181">In this case, **Rotate** updates the constant buffer with a new transformation matrix for the cube.</span></span> <span data-ttu-id="03e64-182">Матрица будет умножена на вершину на этапе шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="03e64-182">The matrix will be multiplied per-vertex during the vertex shader stage.</span></span> <span data-ttu-id="03e64-183">Поскольку этот метод вызывается с каждым кадром, это хорошее место для агрегирования любых методов, которые обновляют динамические константы и буферы вершин, или для выполнения любых других операций, подготавливающих объекты в сцене для преобразования с помощью графического конвейера.</span><span class="sxs-lookup"><span data-stu-id="03e64-183">Since this method is called with every frame, this is a good place to aggregate any methods that update your dynamic constant and vertex buffers, or to perform any other operations that prepare the objects in the scene for transformation by the graphics pipeline.</span></span>

## <a name="implement-the-render-method"></a><span data-ttu-id="03e64-184">Реализация метода Render</span><span class="sxs-lookup"><span data-stu-id="03e64-184">Implement the Render method</span></span>

<span data-ttu-id="03e64-185">Этот метод вызывается один раз для каждого цикла игры после вызова **Update**.</span><span class="sxs-lookup"><span data-stu-id="03e64-185">This method is called once per game loop after calling **Update**.</span></span> <span data-ttu-id="03e64-186">Как и **Обновление**, метод **Render** также вызывается из класса Main.</span><span class="sxs-lookup"><span data-stu-id="03e64-186">Like **Update**, the **Render** method is also called from the main class.</span></span> <span data-ttu-id="03e64-187">Это метод, в котором графический конвейер создается и обрабатывается для фрейма с помощью методов в экземпляре [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .</span><span class="sxs-lookup"><span data-stu-id="03e64-187">This is the method where the graphics pipeline is constructed and processed for the frame using methods on the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) instance.</span></span> <span data-ttu-id="03e64-188">Это итогом в последнем вызове [**ссылку ID3D11DeviceContext::D равиндексед**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span><span class="sxs-lookup"><span data-stu-id="03e64-188">This culminates in a final call to [**ID3D11DeviceContext::DrawIndexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span></span> <span data-ttu-id="03e64-189">Важно понимать, что этот вызов (или другие аналогичные вызовы функции **Draw \* *_, определенные в _* ссылку ID3D11DeviceContext**) фактически выполняет конвейер.</span><span class="sxs-lookup"><span data-stu-id="03e64-189">It’s important to understand that this call (or other similar \**Draw\**_ calls defined on _\* ID3D11DeviceContext\*\*) actually executes the pipeline.</span></span> <span data-ttu-id="03e64-190">В частности, это происходит, когда Direct3D обменивается данными с графическим процессором для установки состояния рисования, выполняет каждую стадию конвейера и записывает результаты пикселя в буфер целевого буфера подготовки для отображения в цепочке подкачки.</span><span class="sxs-lookup"><span data-stu-id="03e64-190">Specifically, this is when Direct3D communicates with the GPU to set drawing state, runs each pipeline stage, and writes the pixel results into the render-target buffer resource for display by the swap chain.</span></span> <span data-ttu-id="03e64-191">Так как взаимодействие между ЦП и GPU приводит к излишней нагрузке, объедините несколько вызовов Draw в одну, если это возможно, особенно если сцена имеет большой объем готовых к просмотру объектов.</span><span class="sxs-lookup"><span data-stu-id="03e64-191">Since communication between the CPU and GPU incurs overhead, combine multiple draw calls into a single one if you can, especially if your scene has a lot of rendered objects.</span></span>


```C++
void Renderer::Render()
{
    // Use the Direct3D device context to draw.
    ID3D11DeviceContext* context = m_deviceResources->GetDeviceContext();

    ID3D11RenderTargetView* renderTarget = m_deviceResources->GetRenderTarget();
    ID3D11DepthStencilView* depthStencil = m_deviceResources->GetDepthStencil();

    context->UpdateSubresource(
        m_pConstantBuffer.Get(),
        0,
        nullptr,
        &m_constantBufferData,
        0,
        0
        );

    // Clear the render target and the z-buffer.
    const float teal [] = { 0.098f, 0.439f, 0.439f, 1.000f };
    context->ClearRenderTargetView(
        renderTarget,
        teal
        );
    context->ClearDepthStencilView(
        depthStencil,
        D3D11_CLEAR_DEPTH | D3D11_CLEAR_STENCIL,
        1.0f,
        0);

    // Set the render target.
    context->OMSetRenderTargets(
        1,
        &renderTarget,
        depthStencil
        );

    // Set up the IA stage by setting the input topology and layout.
    UINT stride = sizeof(VertexPositionColor);
    UINT offset = 0;

    context->IASetVertexBuffers(
        0,
        1,
        m_pVertexBuffer.GetAddressOf(),
        &stride,
        &offset
        );

    context->IASetIndexBuffer(
        m_pIndexBuffer.Get(),
        DXGI_FORMAT_R16_UINT,
        0
        );
    
    context->IASetPrimitiveTopology(
        D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST
        );

    context->IASetInputLayout(m_pInputLayout.Get());

    // Set up the vertex shader stage.
    context->VSSetShader(
        m_pVertexShader.Get(),
        nullptr,
        0
        );

    context->VSSetConstantBuffers(
        0,
        1,
        m_pConstantBuffer.GetAddressOf()
        );

    // Set up the pixel shader stage.
    context->PSSetShader(
        m_pPixelShader.Get(),
        nullptr,
        0
        );

    // Calling Draw tells Direct3D to start sending commands to the graphics device.
    context->DrawIndexed(
        m_indexCount,
        0,
        0
        );
}
```



<span data-ttu-id="03e64-192">Рекомендуется задавать различные этапы графического конвейера в контексте по порядку.</span><span class="sxs-lookup"><span data-stu-id="03e64-192">It's good practice to set the various graphics pipeline stages on the context in order.</span></span> <span data-ttu-id="03e64-193">Как правило, порядок:</span><span class="sxs-lookup"><span data-stu-id="03e64-193">Typically, the order is:</span></span>

-   <span data-ttu-id="03e64-194">При необходимости обновите ресурсы постоянного буфера новыми данными (используя данные из **обновления**).</span><span class="sxs-lookup"><span data-stu-id="03e64-194">Refresh constant buffer resources with new data as needed (using data from **Update**).</span></span>
-   <span data-ttu-id="03e64-195">Входная сборка (IA). здесь мы соединяем буферы вершин и индексов, которые определяют геометрию сцены.</span><span class="sxs-lookup"><span data-stu-id="03e64-195">Input assembly (IA): This is where we attach the vertex and index buffers that define the scene geometry.</span></span> <span data-ttu-id="03e64-196">Необходимо присоединить каждую вершину и буфер индексов для каждого объекта в сцене.</span><span class="sxs-lookup"><span data-stu-id="03e64-196">You need to attach each vertex and index buffer for each object in the scene.</span></span> <span data-ttu-id="03e64-197">Поскольку этот пример содержит только куб, он довольно прост.</span><span class="sxs-lookup"><span data-stu-id="03e64-197">Because this example has just the cube, it's pretty simple.</span></span>
-   <span data-ttu-id="03e64-198">Шейдер вершин (VS): присоединение любых шейдеров вершин, которые будут преобразовывать данные в буферах вершин, и присоединение буферов констант для шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="03e64-198">Vertex shader (VS): Attach any vertex shaders that will transform the data in the vertex buffers, and attach constant buffers for the vertex shader.</span></span>
-   <span data-ttu-id="03e64-199">Шейдер пикселей (PS): присоединение любых шейдеров пикселей, которые будут выполнять операции в растровой сцене, и присоединение ресурсов устройства для шейдера пикселей (константных буферов, текстур и т. д.).</span><span class="sxs-lookup"><span data-stu-id="03e64-199">Pixel shader (PS): Attach any pixel shaders that will perform per-pixel operations in the rasterized scene, and attach device resources for the pixel shader (constant buffers, textures, and so on).</span></span>
-   <span data-ttu-id="03e64-200">Слияние выходных данных (OM): это этап смешивания пикселей после завершения шейдеров.</span><span class="sxs-lookup"><span data-stu-id="03e64-200">Output merger (OM): This is the stage where pixels are blended, after the shaders are finished.</span></span> <span data-ttu-id="03e64-201">Это исключение из правила, так как вы подключаете наборы элементов глубины и целевые объекты отрисовки перед установкой каких-либо других этапов.</span><span class="sxs-lookup"><span data-stu-id="03e64-201">This is an exception to the rule, because you attach your depth stencils and render targets before setting any of the other stages.</span></span> <span data-ttu-id="03e64-202">Если у вас есть дополнительные шейдеры вершин и точек, которые создают текстуры, такие как теневые карты, карты высоты или другие методы выборки, то у вас может быть несколько наборов элементов и целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="03e64-202">You may have multiple stencils and targets if you have additional vertex and pixel shaders that generate textures such as shadow maps, height maps, or other sampling techniques - in this case, each drawing pass will need the appropriate target(s) set before you call a draw function.</span></span>

<span data-ttu-id="03e64-203">Далее в последнем разделе ([Работа с шейдерами и ресурсами шейдеров](work-with-shaders-and-shader-resources.md)) мы рассмотрим шейдеры и расскажу, как они выполняют эти задачи.</span><span class="sxs-lookup"><span data-stu-id="03e64-203">Next, in the final section ([Work with shaders and shader resources](work-with-shaders-and-shader-resources.md)), we'll look at the shaders and discuss how Direct3D executes them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03e64-204">См. также</span><span class="sxs-lookup"><span data-stu-id="03e64-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="03e64-205">**Далее**</span><span class="sxs-lookup"><span data-stu-id="03e64-205">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="03e64-206">Работа с шейдерами и ресурсами шейдера</span><span class="sxs-lookup"><span data-stu-id="03e64-206">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
