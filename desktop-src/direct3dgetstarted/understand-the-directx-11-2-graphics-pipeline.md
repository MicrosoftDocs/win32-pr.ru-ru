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
# <a name="understand-the-direct3d-11-rendering-pipeline"></a>Общие сведения о конвейере визуализации Direct3D 11

Ранее вы рассматривали создание окна, которое можно использовать для рисования в [работе с ресурсами устройств DirectX](work-with-dxgi.md). Теперь вы узнаете, как создать графический конвейер и к нему можно присоединиться.

Вы помните, что существует два интерфейса Direct3D, которые определяют конвейер графики: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), который обеспечивает виртуальное представление GPU и его ресурсов. и [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), который представляет обработку графики для конвейера. Как правило, экземпляр **ID3D11Device** используется для настройки и получения ресурсов GPU, необходимых для начала обработки графики в сцене, и используется **ссылку ID3D11DeviceContext** для обработки этих ресурсов на каждом соответствующем этапе шейдера в графическом конвейере. Обычно методы **ID3D11Device** вызываются редко, т. е. только при настройке сцены или при изменении устройства. С другой стороны, вы вызываете **ссылку ID3D11DeviceContext** каждый раз при обработке кадра для вывода.

В этом примере создается и настраивается минимальный графический конвейер, подходящий для отображения простого цикличного Куба, затененного вершиной. Он демонстрирует приблизительно минимальный набор ресурсов, необходимых для вывода. При чтении этих сведений Обратите внимание на ограничения данного примера, где может потребоваться расширить его для поддержки сцены, которую нужно визуализировать.

В этом примере рассматриваются два класса C++ для графики: класс диспетчера ресурсов устройства и класс модуля подготовки 3D-сцены. В этом разделе особое внимание уделяется модулю визуализации 3D-сцены.

## <a name="what-does-the-cube-renderer-do"></a>Что делает модуль подготовки Куба?

Графический конвейер определяется классом модуля подготовки 3D-сцены. Модуль подготовки сцены может:

-   Определите постоянные буферы для хранения единообразных данных.
-   Определите буферы вершин для хранения данных вершин объекта и соответствующие буферы индексов, чтобы позволить шейдеру вершин правильно проанализировать треугольники.
-   Создание ресурсов текстуры и представлений ресурсов.
-   Загрузите объекты шейдера.
-   Обновите графические данные, чтобы отобразить каждый кадр.
-   Отрисовка (прорисовка) графики в цепочке буферов.

Первые четыре процесса обычно используют методы интерфейса [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) для инициализации графических ресурсов и управления ими, а последние два используют методы интерфейса [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) для управления и выполнения графического конвейера.

Экземпляр класса модуля **подготовки** отчетов создается и управляется как переменная-член в основном классе проекта. Экземпляр **DeviceResources** управляется как общий указатель на несколько классов, включая главный класс проекта, класс представления **приложения** и модуль **подготовки** отчетов. При замене модуля **подготовки** отчетов на собственный класс рассмотрите возможность объявления и назначения экземпляра **DeviceResources** в качестве совместно используемого элемента указателя:

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

Перед созданием экземпляра **DeviceResources** в методе **Initialize** класса **app** просто передайте указатель в конструктор класса (или другой метод инициализации). Можно также передать **слабую \_ ptr** -ссылку, если вместо этого требуется, чтобы главный класс полностью владеет экземпляром **DeviceResources** .

## <a name="create-the-cube-renderer"></a>Создание модуля подготовки Куба

В этом примере класс модуля подготовки сцены организован с помощью следующих методов:

-   **Креатедевицедепендентресаурцес**: вызывается всякий раз, когда необходимо инициализировать или перезапустить сцену. Этот метод загружает начальные данные вершин, текстуры, шейдеры и другие ресурсы, а также конструирует исходные константы и буферы вершин. Как правило, большая часть работы выполняется с помощью методов [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) , а не [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) методов.
-   **Креатевиндовсизедепендентресаурцес**: вызывается при каждом изменении состояния окна, например, при изменении размера или ориентации. Этот метод перестраивает матрицы преобразования, например, для камеры.
-   **Обновление**: обычно вызывается из части программы, которая управляет состоянием немедленной игры; в этом примере мы просто вызываем его из класса **Main** . Этот метод должен считывать сведения о состоянии игры, которые влияют на отрисовку, такие как обновление расположения объекта или кадров анимации, а также любые глобальные данные игры, такие как легкие или изменения в физике игры. Эти входные данные используются для обновления покадровых буферов констант и данных объектов.
-   **Render**: обычно вызывается из части программы, которая управляет циклом игры; в этом случае он вызывается из класса **Main** . Этот метод создает графический конвейер: привязывает шейдеры, привязывает буферы и ресурсы к этапам шейдера и вызывает Рисование для текущего кадра.

Эти методы состоят из текста поведений для визуализации сцены с помощью Direct3D с использованием ваших ресурсов. Если расширить этот пример с помощью нового класса отрисовки, объявите его в основном классе проекта. Таким образом:

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

становится

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

Обратите внимание, что в этом примере предполагается, что методы имеют одинаковые сигнатуры в вашей реализации. Если подписи были изменены, проверьте **главный** цикл и внесите соответствующие изменения.

Давайте более подробно рассмотрим методы отрисовки сцены.

## <a name="create-device-dependent-resources"></a>Создание ресурсов, зависящих от устройства

**Креатедевицедепендентресаурцес** объединяет все операции для инициализации сцены и ее ресурсов с помощью вызовов [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) . Этот метод предполагает, что устройство Direct3D только что было инициализировано (или создано повторно) для сцены. Он воссоздает или перезагружает все графические ресурсы, относящиеся к сцене, такие как шейдер вершин и текстуры, буферы вершин и индексов для объектов, а также любые другие ресурсы (например, текстуры и соответствующие представления).

Вот пример кода для **креатедевицедепендентресаурцес**:


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



Каждый раз при загрузке ресурсов с диска — такие ресурсы, как скомпилированные объекты шейдера (CSO или CSO), делают это асинхронно. Это позволяет выполнять другие операции одновременно (например, другие задачи установки), а поскольку главный цикл не блокируется, вы можете отображать визуально интересующие пользователя данные (например, анимацию загрузки для игры). В этом примере используется API Concurrency:: Tasks, доступный начиная с Windows 8; Обратите внимание на синтаксис лямбда-выражений, используемый для инкапсуляции задач асинхронной загрузки. Эти лямбда-выражения представляют функции, называемые «за пределами потока», поэтому явным образом фиксируется указатель на текущий объект класса (**this**).

Ниже приведен пример того, как можно загрузить байтовый код шейдера:


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



Ниже приведен пример создания буферов вершин и индексов.


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



В этом примере не загружаются ни сетки, ни текстуры. Необходимо создать методы для загрузки сетки и типов текстур, относящихся к игре, и вызывать их асинхронно.

Здесь также заполните начальные значения для буферов констант на сцене. Примерами буфера констант на сцене являются фиксированные огни или другие статические элементы сцены и данные.

## <a name="implement-the-createwindowsizedependentresources-method"></a>Реализация метода Креатевиндовсизедепендентресаурцес

Методы **креатевиндовсизедепендентресаурцес** вызываются каждый раз при изменении размера, ориентации или разрешения окна.

Ресурсы размера окна обновляются следующим образом: статическая процедура сообщения получает одно из нескольких возможных событий, указывающих на изменение состояния окна. Затем ваш главный цикл уведомляется о событии и вызывает **креатевиндовсизедепендентресаурцес** в основном экземпляре класса, который затем вызывает реализацию **креатевиндовсизедепендентресаурцес** в классе визуализатора сцены.

Основная задача этого метода — гарантировать, что в результате изменения свойств окна визуальные объекты не станут беспорядочными или недействительными. В этом примере мы обновляем матрицы проекта с помощью нового поля View (фов) для измененного или переориентированного окна.

Мы уже видели код для создания оконных ресурсов в **DeviceResources** , который был цепочкой подкачки (с задним буфером) и представлением целевого объекта отрисовки. Ниже показано, как модуль подготовки отчетов создает преобразования, зависимые от пропорций:


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



Если сцена имеет определенную структуру компонентов, которые зависят от пропорций, это место для их изменения в соответствии с пропорциями. Здесь также может потребоваться изменить конфигурацию поведения после обработки.

## <a name="implement-the-update-method"></a>Реализация метода Update

Метод **Update** вызывается один раз для каждого цикла игры. в этом примере он вызывается методом основного класса с тем же именем. Она имеет простую цель: обновление геометрии сцены и состояния игры на основе количества затраченного времени (или шагов, затраченного на период) с момента предыдущего кадра. В этом примере мы просто поворотим куб по одному разу для каждого кадра. В реальной игровой сцене этот метод содержит гораздо больше кода для проверки состояния игры, обновления отдельных (или других динамических) буферов констант, геометрических буферов и других ресурсов в памяти соответственно. Так как взаимодействие между ЦП и GPU вызывает дополнительные издержки, убедитесь, что обновлены только буферы, которые действительно изменились с момента последнего кадра. буферы констант можно сгруппировать или разделить, чтобы сделать это более эффективным.


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



В этом случае при **повороте** происходит обновление буфера констант с помощью новой матрицы преобразования для куба. Матрица будет умножена на вершину на этапе шейдера вершин. Поскольку этот метод вызывается с каждым кадром, это хорошее место для агрегирования любых методов, которые обновляют динамические константы и буферы вершин, или для выполнения любых других операций, подготавливающих объекты в сцене для преобразования с помощью графического конвейера.

## <a name="implement-the-render-method"></a>Реализация метода Render

Этот метод вызывается один раз для каждого цикла игры после вызова **Update**. Как и **Обновление**, метод **Render** также вызывается из класса Main. Это метод, в котором графический конвейер создается и обрабатывается для фрейма с помощью методов в экземпляре [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) . Это итогом в последнем вызове [**ссылку ID3D11DeviceContext::D равиндексед**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed). Важно понимать, что этот вызов (или другие аналогичные вызовы функции **Draw \* *_, определенные в _* ссылку ID3D11DeviceContext**) фактически выполняет конвейер. В частности, это происходит, когда Direct3D обменивается данными с графическим процессором для установки состояния рисования, выполняет каждую стадию конвейера и записывает результаты пикселя в буфер целевого буфера подготовки для отображения в цепочке подкачки. Так как взаимодействие между ЦП и GPU приводит к излишней нагрузке, объедините несколько вызовов Draw в одну, если это возможно, особенно если сцена имеет большой объем готовых к просмотру объектов.


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



Рекомендуется задавать различные этапы графического конвейера в контексте по порядку. Как правило, порядок:

-   При необходимости обновите ресурсы постоянного буфера новыми данными (используя данные из **обновления**).
-   Входная сборка (IA). здесь мы соединяем буферы вершин и индексов, которые определяют геометрию сцены. Необходимо присоединить каждую вершину и буфер индексов для каждого объекта в сцене. Поскольку этот пример содержит только куб, он довольно прост.
-   Шейдер вершин (VS): присоединение любых шейдеров вершин, которые будут преобразовывать данные в буферах вершин, и присоединение буферов констант для шейдера вершин.
-   Шейдер пикселей (PS): присоединение любых шейдеров пикселей, которые будут выполнять операции в растровой сцене, и присоединение ресурсов устройства для шейдера пикселей (константных буферов, текстур и т. д.).
-   Слияние выходных данных (OM): это этап смешивания пикселей после завершения шейдеров. Это исключение из правила, так как вы подключаете наборы элементов глубины и целевые объекты отрисовки перед установкой каких-либо других этапов. Если у вас есть дополнительные шейдеры вершин и точек, которые создают текстуры, такие как теневые карты, карты высоты или другие методы выборки, то у вас может быть несколько наборов элементов и целевых объектов.

Далее в последнем разделе ([Работа с шейдерами и ресурсами шейдеров](work-with-shaders-and-shader-resources.md)) мы рассмотрим шейдеры и расскажу, как они выполняют эти задачи.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Далее**
</dt> <dt>

[Работа с шейдерами и ресурсами шейдера](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
