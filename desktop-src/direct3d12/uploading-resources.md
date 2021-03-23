---
title: Отправка различных типов ресурсов
description: Показывает, как использовать один буфер для передачи данных буфера констант и данных буфера вершин в GPU, а также как правильно выделять и размещать данные в буферах.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2edca2cd9f4d3becf5036056a89f91c50f2c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103921"
---
# <a name="uploading-different-types-of-resources"></a>Отправка различных типов ресурсов

Показывает, как использовать один буфер для передачи данных буфера констант и данных буфера вершин в GPU, а также как правильно выделять и размещать данные в буферах. Использование одного буфера увеличивает гибкость использования памяти и предоставляет приложениям более строгий контроль использования памяти. Также показывает различия между моделями D3D11 и D3D12 для передачи различных типов ресурсов.

-   [Отправка различных типов ресурсов](#upload-different-types-of-resources)
    -   [Пример кода: D3D11](#code-example-d3d11)
    -   [Пример кода: D3D12](#code-example-d3d12)
-   [Константы](#constants)
-   [Ресурсы](#uploading-different-types-of-resources)
-   [Отражение размера ресурса](#resource-size-reflection)
-   [Выравнивание буфера](#buffer-alignment)
-   [Связанные темы](#related-topics)

## <a name="upload-different-types-of-resources"></a>Отправка различных типов ресурсов

В D3D12 приложения создают один буфер для размещения различных типов данных ресурсов для отправки и копируют данные ресурсов в один буфер аналогичным образом для различных данных ресурсов. Затем создаются отдельные представления для привязки этих данных ресурсов к графическому конвейеру в новой модели привязки ресурсов.

В D3D11 приложения создают отдельные буферы для различных типов данных ресурсов (Обратите внимание на отличия, `BindFlags` которые используются в приведенном ниже примере кода D3D11), явным образом привязывает каждый буфер ресурсов к графическому конвейеру и обновляет данные ресурсов с помощью различных методов, основанных на различных типах ресурсов.

Как в D3D12, так и в D3D11, приложения должны использовать только ресурсы для передачи данных, когда ЦП запишет данные один раз, и графический процессор будет считывать их один раз. Если GPU будет считывать данные несколько раз, GPU не будет считывать данные линейно, или визуализация в значительной степени ограничена графическим процессором. Лучшим вариантом может быть использование [**ID3D12GraphicsCommandList:: копитекстуререгион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) или [**ID3D12GraphicsCommandList:: копибуфферрегион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) для копирования данных буфера отправки в ресурс по умолчанию. Ресурс по умолчанию может размещаться в физической видеопамяти на дискретных графических процессорах.

### <a name="code-example-d3d11"></a>Пример кода: D3D11

``` syntax
// D3D11: Separate buffers for each resource type.

void main()
{
    // ...

    // Create a constant buffer.
    float constantBufferData[] = ...;

    D3D11_BUFFER_DESC constantBufferDesc = {0};  
    constantBufferDesc.ByteWidth = sizeof(constantBufferData);  
    constantBufferDesc.Usage = D3D11_USAGE_DYNAMIC;  
    constantBufferDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;  
    constantBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;  

    ComPtr<ID3D11Buffer> constantBuffer;
    d3dDevice->CreateBuffer(  
        &constantBufferDesc,  
        NULL,
        &constantBuffer  
        );

    // Create a vertex buffer.
    float vertexBufferData[] = ...;

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(vertexBufferData);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;

    ComPtr<ID3D11Buffer> vertexBuffer;
    d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        NULL,
        &vertexBuffer
        );

    // ...
}

void DrawFrame()
{
    // ...

    // Bind buffers to the graphics pipeline.
    d3dDeviceContext->VSSetConstantBuffers(0, 1, constantBuffer.Get());
    d3dDeviceContext->IASetVertexBuffers(0, 1, vertexBuffer.Get(), ...);

    // Update the constant buffer.
    D3D11_MAPPED_SUBRESOURCE mappedResource;  
    d3dDeviceContext->Map(
        constantBuffer.Get(),
        0, 
        D3D11_MAP_WRITE_DISCARD,
        0,
        &mappedResource
        );
    memcpy(mappedResource.pData, constantBufferData,
        sizeof(contatnBufferData));
    d3dDeviceContext->Unmap(constantBuffer.Get(), 0);  

    // Update the vertex buffer.
    d3dDeviceContext->UpdateSubresource(
        vertexBuffer.Get(),
        0,
        NULL,
        vertexBufferData,
        sizeof(vertexBufferData),
        0
    );

    // ...
}
```

### <a name="code-example-d3d12"></a>Пример кода: D3D12

``` syntax
// D3D12: One buffer to accommodate different types of resources

ComPtr<ID3D12Resource> m_spUploadBuffer;
UINT8* m_pDataBegin = nullptr;    // starting position of upload buffer
UINT8* m_pDataCur = nullptr;      // current position of upload buffer
UINT8* m_pDataEnd = nullptr;      // ending position of upload buffer

void main()
{
    //
    // Initialize an upload buffer
    //

    InitializeUploadBuffer(64 * 1024);

    // ...
}

void DrawFrame()
{
    // ...

    // Set vertices data to the upload buffer.

    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float),
            sizeof(float), 
            verticesOffset
            ));

    // Set constant data to the upload buffer.

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT, 
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model.

    D3D12_VERTEX_BUFFER_VIEW vertexBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + verticesOffset,
        sizeof(vertices), // size
        sizeof(float) * 4,  // stride
    };

    commandList->IASetVertexBuffers( 
        0,
        1,
        &vertexBufferViewDesc,
        ));

    // Create constant buffer views for the new binding model.

    D3D12_CONSTANT_BUFFER_VIEW_DESC constantBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + constantsOffset,
        sizeof(constants) // size
         };

    d3dDevice->CreateConstantBufferView(
        &constantBufferViewDesc,
        ...
        ));

    // Continue command list building and execution ...
}

//
// Create an upload buffer and keep it always mapped.
//

HRESULT InitializeUploadBuffer(SIZE_T uSize)
{
    HRESULT hr = d3dDevice->CreateCommittedResource(
         &CD3DX12_HEAP_PROPERTIES( D3D12_HEAP_TYPE_UPLOAD ),    
               D3D12_HEAP_FLAG_NONE, 
               &CD3DX12_RESOURCE_DESC::Buffer( uSize ), 
               D3D12_RESOURCE_STATE_GENERIC_READ, nullptr,  
               IID_PPV_ARGS( &m_spUploadBuffer ) );

    if (SUCCEEDED(hr))
    {
        void* pData;
        //
        // No CPU reads will be done from the resource.
        //
        CD3DX12_RANGE readRange(0, 0);
        m_spUploadBuffer->Map( 0, &readRange, &pData ); 
        m_pDataCur = m_pDataBegin = reinterpret_cast< UINT8* >( pData );
        m_pDataEnd = m_pDataBegin + uSize;
    }
    return hr;
}

//
// Sub-allocate from the buffer, with offset aligned.
//

HRESULT SuballocateFromBuffer(SIZE_T uSize, UINT uAlign)
{
    m_pDataCur = reinterpret_cast< UINT8* >(
        Align(reinterpret_cast< SIZE_T >(m_pDataCur), uAlign)
        );

    return (m_pDataCur + uSize > m_pDataEnd) ? E_INVALIDARG : S_OK;
}

//
// Place and copy data to the upload buffer.
//

HRESULT SetDataToUploadBuffer(
    const void* pData, 
    UINT bytesPerData, 
    UINT dataCount, 
    UINT alignment, 
    UINT& byteOffset
    )
{
    SIZE_T byteSize = bytesPerData * dataCount;
    HRESULT hr = SuballocateFromBuffer(byteSize, alignment);
    if (SUCCEEDED(hr))
    {
        byteOffset = UINT(m_pDataCur - m_pDataBegin);
        memcpy(m_pDataCur, pData, byteSize); 
        m_pDataCur += byteSize;
    }
    return hr;
}

//
// Align uLocation to the next multiple of uAlign.
//

UINT Align(UINT uLocation, UINT uAlign)
{
    if ( (0 == uAlign) || (uAlign & (uAlign-1)) )
    {
        ThrowException("non-pow2 alignment");
    }

    return ( (uLocation + (uAlign-1)) & ~(uAlign-1) );
}
```

Обратите внимание на использование вспомогательных [**структур \_ CD3DX12 \_ Свойства кучи**](cd3dx12-heap-properties.md) и [**CD3DX12 \_ Resource \_ DESC**](cd3dx12-resource-desc.md).

## <a name="constants"></a>Константы

Чтобы задать константы, вершины и индексы в куче передачи или Реадбакк, используйте следующие API:

-   [**ID3D12Device:: Креатеконстантбуффервиев**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**ID3D12GraphicsCommandList:: Иасетвертексбуфферс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [**ID3D12GraphicsCommandList:: Иасетиндексбуффер**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a>Ресурсы

Ресурсы — это концепция D3D, которая абстрагирует использование физической памяти GPU. Ресурсы нуждаются в виртуальном адресном пространстве GPU для доступа к физической памяти. Создание ресурсов — это бесплатный поток.

Существует три типа ресурсов, которые связаны с созданием виртуальных адресов и гибкостью в D3D12:

-   Зафиксированные ресурсы

    Выделенные ресурсы — это наиболее распространенная идея ресурсов D3D в поколениях. Создание такого ресурса выделяет диапазон виртуальных адресов, неявную кучу, достаточно большую для размещения всего ресурса, и фиксирует диапазон виртуальных адресов в физической памяти, инкапсулированной в куче. Свойства неявной кучи должны передаваться для сопоставления функциональной четности с предыдущими версиями D3D. См. [**ID3D12Device:: креатекоммиттедресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

-   Зарезервированные ресурсы

    Зарезервированные ресурсы эквивалентны D3D11 мозаичным ресурсам. При их создании выделяется только диапазон виртуальных адресов, который не сопоставлен ни с одной кучей. Приложение будет сопоставлять эти ресурсы с кучами позже. Возможности таких ресурсов в настоящее время не изменяются по сравнению с D3D11, так как они могут быть сопоставлены с кучей с гранулярностью в 64 КБ с [**упдатетилемаппингс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings). См [ **. ID3D12Device:: креатересерведресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)

-   Размещенные ресурсы

    Новые для D3D12. приложения могут создавать кучи отдельно от ресурсов. После этого приложение может располагать несколько ресурсов в одной куче. Это можно сделать без создания мозаичных или зарезервированных ресурсов, обеспечивая возможности для всех типов ресурсов, которые могут быть созданы непосредственно приложениями. Несколько ресурсов могут перекрываться, и приложение должно использовать `TiledResourceBarrier` для правильного использования физической памяти. См [ **. ID3D12Device:: креатеплацедресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)

## <a name="resource-size-reflection"></a>Отражение размера ресурса

Приложения должны использовать отражение размера ресурса, чтобы понять, сколько текстур комнаты с неизвестными макетами текстур требуется в кучах. Буферы также поддерживаются, но в основном предназначены для удобства.

Приложения должны учитывать основные несоответствия при выравнивании, чтобы обеспечить более плотную упаковку ресурсов.

Например, одноэлементный массив с однобайтовым буфером возвращает размер 64 КБ и выравнивание в 64 КБ, так как в настоящий момент буферы могут быть выровнены только 64 КБ.

Кроме того, из трех массивов элементов с двумя шаг текселя 64-разрядными текстурами и с согласованным размером в один шаг текселя 4 МБ в соответствии с порядком массива задаются разные размеры. Если текстуры с согласованием в 4 МБ находятся в середине, то полученный размер будет 12 МБ. В противном случае полученный размер равен 8 МБ. Возвращаемое выравнивание всегда будет состоять из 4 МБ, супер набора всех выравниваний в массиве ресурсов.

Сослаться на следующие API:

-   [**\_ \_ Сведения о выделении ресурсов D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [**жетресаурцеаллокатионинфо**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a>Выравнивание буфера

Ограничения выравнивания буфера не изменяются из D3D11, особенно:

-   4 МБ для многопримерных текстур.
-   64 КБ для однопримерных текстур и буферов.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Подраспределение в буферах](large-buffers.md)
</dt> </dl>

 

 




