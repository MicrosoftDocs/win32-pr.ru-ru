---
title: Чтение обратно данных через буфер
description: Для считывания данных из графического процессора (например, для записи снимка экрана) используется куча реадбакк.
ms.assetid: 2F515B2C-3317-4AA8-81E1-7762ED895F77
ms.localizationpriority: high
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: 752d97d517a48a38adabc7c8fe51d11d47c1d8d3
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "104549005"
---
# <a name="read-back-data-via-a-buffer"></a>Чтение обратно данных через буфер

Для считывания данных из графического процессора (например, для записи снимка экрана) используется куча реадбакк. Этот метод связан с [отправкой данных текстуры через буфер](upload-and-readback-of-texture-data.md)с небольшими различиями.

- Чтобы считать данные обратно, создайте кучу с **D3D12_HEAP_TYPE** , для которой задано значение [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type), а не **D3D12_HEAP_TYPE_UPLOAD**.
- Ресурс в куче для чтения и обратной стороне всегда должен быть **D3D12_RESOURCE_DIMENSION_BUFFER**.
- Ограждение используется для обнаружения того, когда GPU завершает обработку кадра (после того, как он закончит запись данных в выходной буфер). Это важно, поскольку метод [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) не выполняет синхронизацию с ГРАФИЧЕСКИм процессором (Аналогичным образом, эквивалент Direct3D 11 *выполняет* синхронизацию). Вызовы **карт** Direct3D 12 ведут себя так, как если бы вы вызывали эквивалент Direct3D 11 с флагом NO_OVERWRITE.
- После подготовки данных (включая все необходимые барьеры ресурсов) вызовите [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) , чтобы сделать данные реадбакк видимыми для ЦП.

## <a name="code-example"></a>Пример кода

В приведенном ниже примере кода показан общий обзор процесса считывания данных из GPU в ЦП через буфер.

```cppwinrt

// The output buffer (created below) is on a default heap, so only the GPU can access it.

D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
D3D12_RESOURCE_DESC outputBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize, D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS) };
winrt::com_ptr<::ID3D12Resource> outputBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &defaultHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &outputBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(outputBuffer),
    outputBuffer.put_void()));

// The readback buffer (created below) is on a readback heap, so that the CPU can access it.

D3D12_HEAP_PROPERTIES readbackHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_READBACK) };
D3D12_RESOURCE_DESC readbackBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize) };
winrt::com_ptr<::ID3D12Resource> readbackBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &readbackHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &readbackBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(readbackBuffer),
    readbackBuffer.put_void()));

{
    D3D12_RESOURCE_BARRIER outputBufferResourceBarrier
    {
        CD3DX12_RESOURCE_BARRIER::Transition(
            outputBuffer.get(),
            D3D12_RESOURCE_STATE_COPY_DEST,
            D3D12_RESOURCE_STATE_COPY_SOURCE)
    };
    commandList->ResourceBarrier(1, &outputBufferResourceBarrier);
}

commandList->CopyResource(readbackBuffer.get(), outputBuffer.get());

// Code goes here to close, execute (and optionally reset) the command list, and also
// to use a fence to wait for the command queue.

// The code below assumes that the GPU wrote FLOATs to the buffer.

D3D12_RANGE readbackBufferRange{ 0, outputBufferSize };
FLOAT * pReadbackBufferData{};
winrt::check_hresult(
    readbackBuffer->Map
    (
        0,
        &readbackBufferRange,
        reinterpret_cast<void**>(&pReadbackBufferData)
    )
);

// Code goes here to access the data via pReadbackBufferData.

D3D12_RANGE emptyRange{ 0, 0 };
readbackBuffer->Unmap
(
    0,
    &emptyRange
);
```

Полную реализацию подпрограммы снимка экрана, которая считывает текстуру целевого объекта рендеринга и записывает ее на диск как файл, см. в разделе *DirectX Tools Kit for DX12* [скринграб](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp).

## <a name="related-topics"></a>Связанные темы

* [Подраспределение в пределах буфера](large-buffers.md)
