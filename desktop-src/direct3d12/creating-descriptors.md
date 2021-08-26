---
title: Создание дескрипторов
description: Описывает и показывает примеры создания представлений индекса, вершины и буфера констант. ресурс шейдера, целевой объект прорисовки, неупорядоченный доступ, потоковый выход и представления элементов глубины; и пробы. Все методы для создания дескрипторов являются свободными потоками.
ms.assetid: 0D360A7C-8A2F-49E1-A5CC-98C958B59D1C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 915cf1d92165f6d802bf4e8698180675a3edb32bd77da0510f4d9b52d6e044b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069714"
---
# <a name="creating-descriptors"></a>Создание дескрипторов

Описывает и показывает примеры создания представлений индекса, вершины и буфера констант. ресурс шейдера, целевой объект прорисовки, неупорядоченный доступ, потоковый выход и представления элементов глубины; и пробы. Все методы для создания дескрипторов являются свободными потоками.

-   [Представление буфера индекса](#index-buffer-view)
-   [Представление буфера вершин](#vertex-buffer-view)
-   [представление ресурсов шейдера](#shader-resource-view)
-   [Представление буфера констант](#constant-buffer-view)
-   [Образец](#sampler)
-   [Представление неупорядоченного доступа](#unordered-access-view)
-   [Представление потока вывода](#stream-output-view)
-   [Представление целевого объекта прорисовки](#render-target-view)
-   [Представление трафарета глубины](#depth-stencil-view)
-   [Связанные темы](#related-topics)

## <a name="index-buffer-view"></a>Представление буфера индекса

Чтобы создать представление буфера индекса, заполните структуру [**\_ \_ \_ представления буфера D3D12 index**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view) .

``` syntax
typedef struct D3D12_INDEX_BUFFER_VIEW
{
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
    UINT SizeInBytes;
    DXGI_FORMAT Format;
}   D3D12_INDEX_BUFFER_VIEW;
```

Задайте расположение (Call [**жетгпувиртуаладдресс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) и размер буфера, указывая, что \_ виртуальный адрес D3D12 GPU \_ \_ определен как:

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

См. перечисление в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) . Как правило, для буфера индекса может использоваться следующее определение:

`const DXGI_FORMAT StandardIndexFormat = DXGI_FORMAT_R32_UINT;`

Наконец, вызовите [**ID3D12GraphicsCommandList:: иасетиндексбуффер**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer).

Например,


```C++
// Initialize the index buffer view.
m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
```



## <a name="vertex-buffer-view"></a>Представление буфера вершин

Чтобы создать представление буфера вершин, заполните структуру [**\_ \_ \_ представления буфера вершин D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view) :

``` syntax
typedef struct D3D12_VERTEX_BUFFER_VIEW {
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;  
    UINT SizeInBytes;  
    UINT StrideInBytes;  
} D3D12_VERTEX_BUFFER_VIEW;
```

Задайте расположение (Call [**жетгпувиртуаладдресс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) и размер буфера, указывая, что \_ виртуальный адрес D3D12 GPU \_ \_ определен как:

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

Этот шаг обычно является размером структуры данных с одной вершиной, такой как `sizeof(Vertex);` , а затем вызывается [**ID3D12GraphicsCommandList:: иасетвертексбуфферс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers).

Например,


```C++
// Initialize the vertex buffer view.
m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
m_vertexBufferView.SizeInBytes = SampleAssets::VertexDataSize;
m_vertexBufferView.StrideInBytes = SampleAssets::StandardVertexStride;
```



## <a name="shader-resource-view"></a>представление ресурсов шейдера

Чтобы создать представление ресурсов шейдера, заполните структуру [**D3D12 в \_ \_ \_ представлении \_ ресурсов шейдера**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) .

``` syntax
typedef struct D3D12_SHADER_RESOURCE_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_SRV_DIMENSION ViewDimension;  
    UINT Shader4ComponentMapping;  
    union   
        {  
        D3D12_BUFFER_SRV Buffer;  
        D3D12_TEX1D_SRV Texture1D;  
        D3D12_TEX1D_ARRAY_SRV Texture1DArray;  
        D3D12_TEX2D_SRV Texture2D;  
        D3D12_TEX2D_ARRAY_SRV Texture2DArray;  
        D3D12_TEX2DMS_SRV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_SRV Texture2DMSArray;  
        D3D12_TEX3D_SRV Texture3D;  
        D3D12_TEXCUBE_SRV TextureCube;  
        D3D12_TEXCUBE_ARRAY_SRV TextureCubeArray;  
        }   ;  
    }   D3D12_SHADER_RESOURCE_VIEW_DESC; 
```

`ViewDimension`Поле имеет значение 0 или одно из значений перечисления [**\_ \_ \_ флагов SRV для буфера D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags) .

Перечисления и структуры, на которые ссылается [**\_ \_ представление ресурсов шейдера \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) , имеют следующие типы:

-   [**\_Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ буфера \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv)
-   [**D3D12 \_ TEX1D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv)
-   [**D3D12 \_ TEX1D \_ массив \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ массив \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv)
-   [**D3D12 \_ TEX2DMS \_ массив \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX3D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv)
-   [**D3D12 \_ текскубе \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv)
-   [**D3D12 \_ текскубе \_ массив \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv)

Обратите внимание, что `ResourceMinLODClamp` в СРВС для Tex1D/2D/3D/Cube было добавлено значение float. В D3D11 это свойство ресурса, но оно не соответствует его реализации в оборудовании. `StructureByteStride` был добавлен в буфер СРВС, где в D3D11 это свойство ресурса. Если шаг не равен нулю, то он указывает на представление структурированного буфера, а формат должен быть задан как \_ \_ неизвестный формат DXGI.

Наконец, чтобы создать представление ресурсов шейдера, вызовите метод [**ID3D12Device:: креатешадерресаурцевиев**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview).

Например,


```C++
// Describe and create an SRV.
D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
srvDesc.Format = tex.Format;
srvDesc.Texture2D.MipLevels = tex.MipLevels;
srvDesc.Texture2D.MostDetailedMip = 0;
srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);
```



## <a name="constant-buffer-view"></a>Представление буфера констант

Чтобы создать представление буфера констант, заполните структуру [**D3D12 \_ константного \_ \_ представления буфера \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc) :

``` syntax
typedef struct D3D12_CONSTANT_BUFFER_VIEW_DESC {
  D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
  UINT   SizeInBytes;
} D3D12_CONSTANT_BUFFER_VIEW_DESC;
```

Затем вызовите [**ID3D12Device:: креатеконстантбуффервиев**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview).

Например,


```C++
// Describe and create a constant buffer view.
D3D12_CONSTANT_BUFFER_VIEW_DESC cbvDesc = {};
cbvDesc.BufferLocation = m_constantBuffer->GetGPUVirtualAddress();
cbvDesc.SizeInBytes = (sizeof(ConstantBuffer) + 255) & ~255;    // CB size is required to be 256-byte aligned.
m_device->CreateConstantBufferView(&cbvDesc, m_cbvHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="sampler"></a>Образец

Чтобы создать пример, заполните [**D3D12 \_ образец \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc) в виде структуры:

``` syntax
typedef struct D3D12_SAMPLER_DESC
{
    D3D12_FILTER Filter;
    D3D12_TEXTURE_ADDRESS_MODE AddressU;
    D3D12_TEXTURE_ADDRESS_MODE AddressV;
    D3D12_TEXTURE_ADDRESS_MODE AddressW;
    FLOAT MipLODBias;
    UINT MaxAnisotropy;
    D3D12_COMPARISON_FUNC ComparisonFunc;
    FLOAT BorderColor[4]; // RGBA
    FLOAT MinLOD;
    FLOAT MaxLOD;
} D3D12_SAMPLER_DESC;
```

Чтобы заполнить эту структуру, см. следующие перечисления:

-   [**\_Фильтр D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)
-   [**\_Тип фильтра \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_type)
-   [**\_ \_ Тип уменьшения фильтра \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_reduction_type)
-   [**\_ \_ Режим адресации текстуры D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)
-   [**\_Сравнение D3D12 \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

Наконец, вызовите [**ID3D12Device:: креатесамплер**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler).

Например,


```C++
// Describe and create a sampler.
D3D12_SAMPLER_DESC samplerDesc = {};
samplerDesc.Filter = D3D12_FILTER_MIN_MAG_MIP_LINEAR;
samplerDesc.AddressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.AddressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.AddressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.MinLOD = 0;
samplerDesc.MaxLOD = D3D12_FLOAT32_MAX;
samplerDesc.MipLODBias = 0.0f;
samplerDesc.MaxAnisotropy = 1;
samplerDesc.ComparisonFunc = D3D12_COMPARISON_FUNC_ALWAYS;
m_device->CreateSampler(&samplerDesc, m_samplerHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="unordered-access-view"></a>Представление неупорядоченного доступа

Чтобы создать представление неупорядоченного доступа, заполните структуру [**D3D12 \_ неупорядоченный \_ доступ к структуре \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc) :

``` syntax
typedef struct D3D12_UNORDERED_ACCESS_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_UAV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_UAV Buffer;
        D3D12_TEX1D_UAV Texture1D;
        D3D12_TEX1D_ARRAY_UAV Texture1DArray;
        D3D12_TEX2D_UAV Texture2D;
        D3D12_TEX2D_ARRAY_UAV Texture2DArray;
        D3D12_TEX3D_UAV Texture3D;
    };
} D3D12_UNORDERED_ACCESS_VIEW_DESC;
```

`ViewDimension`Поле имеет значение 0 или одно из значений перечисления [**D3D12 \_ buffer \_ UAV \_ flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) .

См. следующие перечисления и структуры:

-   [**\_Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**\_UAV буфера \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX1D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

`StructureByteStride` был добавлен в буфер Уавс, где в D3D11 это свойство ресурса. Если шаг не равен нулю, то он указывает на представление структурированного буфера, а формат должен быть задан как \_ \_ неизвестный формат DXGI.

Наконец, вызовите [**ID3D12Device:: креатеунордередакцессвиев**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).

Например,


```C++
// Create the unordered access views (UAVs) that store the results of the compute work.
CD3DX12_CPU_DESCRIPTOR_HANDLE processedCommandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), ProcessedCommandsOffset, m_cbvSrvUavDescriptorSize);
for (UINT frame = 0; frame < FrameCount; frame++)
{
    // Allocate a buffer large enough to hold all of the indirect commands
    // for a single frame as well as a UAV counter.
    commandBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(CommandBufferSizePerFrame + sizeof(UINT), D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS);
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &commandBufferDesc,
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_processedCommandBuffers[frame])));

    D3D12_UNORDERED_ACCESS_VIEW_DESC uavDesc = {};
    uavDesc.Format = DXGI_FORMAT_UNKNOWN;
    uavDesc.ViewDimension = D3D12_UAV_DIMENSION_BUFFER;
    uavDesc.Buffer.FirstElement = 0;
    uavDesc.Buffer.NumElements = TriangleCount;
    uavDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
    uavDesc.Buffer.CounterOffsetInBytes = CommandBufferSizePerFrame;
    uavDesc.Buffer.Flags = D3D12_BUFFER_UAV_FLAG_NONE;

    m_device->CreateUnorderedAccessView(            
        m_processedCommandBuffers[frame].Get(),
        m_processedCommandBuffers[frame].Get(),
        &uavDesc,
        processedCommandsHandle);

    processedCommandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
}

// Allocate a buffer that can be used to reset the UAV counters and initialize it to 0.
ThrowIfFailed(m_device->CreateCommittedResource(
    &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
    D3D12_HEAP_FLAG_NONE,
    &CD3DX12_RESOURCE_DESC::Buffer(sizeof(UINT)),
    D3D12_RESOURCE_STATE_GENERIC_READ,
    
    nullptr,
    IID_PPV_ARGS(&m_processedCommandBufferCounterReset)));

UINT8* pMappedCounterReset = nullptr;
CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
ThrowIfFailed(m_processedCommandBufferCounterReset->Map(0, &readRange, reinterpret_cast<void**>(&pMappedCounterReset)));
ZeroMemory(pMappedCounterReset, sizeof(UINT));
m_processedCommandBufferCounterReset->Unmap(0, nullptr);
```



## <a name="stream-output-view"></a>Представление потока вывода

Чтобы создать представление потока вывода, заполните структуру [**\_ \_ вывода \_ потока D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .

``` syntax
typedef struct D3D12_STREAM_OUTPUT_DESC  
    {  
    _Field_size_full_(NumEntries)  const D3D12_SO_DECLARATION_ENTRY *pSODeclaration;  
    UINT NumEntries;  
    _Field_size_full_(NumStrides)  const UINT *pBufferStrides;  
    UINT NumStrides;  
    UINT RasterizedStream;  
    }   D3D12_STREAM_OUTPUT_DESC;  
```

Затем вызовите [**ID3D12GraphicsCommandList:: сосеттаржетс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets).

## <a name="render-target-view"></a>Представление целевого объекта прорисовки

Чтобы создать представление целевого объекта прорисовки, заполните структуру [**D3D12 \_ визуализации \_ целевого \_ представления \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc) .

``` syntax
typedef struct D3D12_RENDER_TARGET_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_RTV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_RTV Buffer;
        D3D12_TEX1D_RTV Texture1D;
        D3D12_TEX1D_ARRAY_RTV Texture1DArray;
        D3D12_TEX2D_RTV Texture2D;
        D3D12_TEX2D_ARRAY_RTV Texture2DArray;
        D3D12_TEX2DMS_RTV Texture2DMS;
        D3D12_TEX2DMS_ARRAY_RTV Texture2DMSArray;
        D3D12_TEX3D_RTV Texture3D;
    };
} D3D12_RENDER_TARGET_VIEW_DESC;
```

`ViewDimension`Поле имеет значение 0 или одно значение перечисления [**\_ \_ измерения D3D12 РТВ**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_rtv_dimension) .

См. следующие перечисления и структуры:

-   [**\_Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**\_РТВ буфера \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv)
-   [**D3D12 \_ TEX1D \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX1D \_ array \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2DMS \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv)
-   [**D3D12 \_ TEX2D \_ array \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ array \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX3D \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)

Наконец, вызовите [**ID3D12Device:: креатерендертаржетвиев**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview).

Например,

```C++
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
```



## <a name="depth-stencil-view"></a>Представление трафарета глубины

Чтобы создать представление трафарета глубины, заполните структуру [**D3D12 в \_ \_ \_ представлении \_ трафарета глубины**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc) :

``` syntax
typedef struct D3D12_DEPTH_STENCIL_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_DSV_DIMENSION ViewDimension;  
    D3D12_DSV_FLAGS Flags;  
    union   
        {  
        D3D12_TEX1D_DSV Texture1D;  
        D3D12_TEX1D_ARRAY_DSV Texture1DArray;  
        D3D12_TEX2D_DSV Texture2D;  
        D3D12_TEX2D_ARRAY_DSV Texture2DArray;  
        D3D12_TEX2DMS_DSV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_DSV Texture2DMSArray;  
        }   ;  
    }   D3D12_DEPTH_STENCIL_VIEW_DESC;  
```

`ViewDimension`Поле имеет значение 0 или одно значение перечисления [**\_ \_ измерения DSV D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_dimension) . Параметры флагов см. в перечислении [**\_ \_ флагов DSV D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_flags) .

См. следующие перечисления и структуры:

-   [**\_Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**Представление \_ \_ источника данных массива D3D12 TEX1D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**Представление \_ \_ источника данных массива D3D12 TEX2D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**D3D12 \_ TEX2DMS \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv)
-   [**Представление \_ \_ источника данных массива D3D12 TEX2DMS \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)

Наконец, вызовите [**ID3D12Device:: креатедепсстенЦилвиев**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview).

Например,


```C++
// Create the depth stencil view.
{
    D3D12_DEPTH_STENCIL_VIEW_DESC depthStencilDesc = {};
    depthStencilDesc.Format = DXGI_FORMAT_D32_FLOAT;
    depthStencilDesc.ViewDimension = D3D12_DSV_DIMENSION_TEXTURE2D;
    depthStencilDesc.Flags = D3D12_DSV_FLAG_NONE;

    D3D12_CLEAR_VALUE depthOptimizedClearValue = {};
    depthOptimizedClearValue.Format = DXGI_FORMAT_D32_FLOAT;
    depthOptimizedClearValue.DepthStencil.Depth = 1.0f;
    depthOptimizedClearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Tex2D(DXGI_FORMAT_D32_FLOAT, m_width, m_height, 1, 0, 1, 0, D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL),
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &depthOptimizedClearValue,
        IID_PPV_ARGS(&m_depthStencil)
        ));

    m_device->CreateDepthStencilView(m_depthStencil.Get(), &depthStencilDesc, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Дескрипторы](descriptors.md)
</dt> <dt>

[Кучи дескрипторов](descriptor-heaps.md)
</dt> </dl>

 

 