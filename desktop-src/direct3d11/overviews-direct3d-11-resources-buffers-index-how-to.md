---
title: Создание буфера индекса
description: В этом разделе показано, как инициализировать буфер индексов при подготовке к подготовке к просмотру.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- буфер индексов, создание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d474114e5908a42a112dddd550e24c13e5e1d3bf2cec523d47dfe1d617ac0bf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119504"
---
# <a name="how-to-create-an-index-buffer"></a>Как создать буфер индексов

[Буферы индексов](overviews-direct3d-11-resources-buffers-intro.md) содержат данные индекса. В этом разделе показано, как инициализировать [буфер индексов](overviews-direct3d-11-resources-buffers-intro.md) при подготовке к подготовке к просмотру.

**Инициализация буфера индекса**

1.  Создайте буфер, содержащий сведения об индексе.
2.  Создайте описание буфера, заполнив структуру [**D3D11 \_ буфера \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Передайте \_ флаг D3D11 привязки \_ индекса в \_ элемент **биндфлагс** и передайте размер буфера в байтах элементу **битевидс** .
3.  Создайте описание данных о подресурсе, заполнив [**структуру \_ \_ данных подресурсов D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) . Элемент **псисмем** должен указывать непосредственно на данные индекса, созданные на шаге 1.
4.  Вызовите метод [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) при передаче структуры [**\_ буфера \_ DESC D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , [**структуры \_ \_ данных подресурса D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) и адреса указателя на интерфейс [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) для инициализации.

В следующем примере кода показано, как создать буфер индекса. В этом примере предполагается, что


```
g_pd3dDevice
```



является допустимым объектом [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) , который


```
g_pd3dContext
```



является допустимым объектом [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .


```
ID3D11Buffer *g_pIndexBuffer = NULL;

// Create indices.
unsigned int indices[] = { 0, 1, 2 };

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage           = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
bufferDesc.BindFlags       = D3D11_BIND_INDEX_BUFFER;
bufferDesc.CPUAccessFlags  = 0;
bufferDesc.MiscFlags       = 0;

// Define the resource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = indices;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer with the device.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
if( FAILED( hr ) )
    return hr;

// Set the buffer.
g_pd3dContext->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
    
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Buffers](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




