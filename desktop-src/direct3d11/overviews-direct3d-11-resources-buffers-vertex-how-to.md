---
title: Создание буфера вершин
description: В этом разделе показано, как инициализировать статический буфер вершин, то есть буфер вершин, который не изменяется.
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- буфер вершин, создание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e0b3d9d8f731b01e7c919105c21c8d150f864a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330792"
---
# <a name="how-to-create-a-vertex-buffer"></a>Как создать буфер вершин

[Буферы вершин](overviews-direct3d-11-resources-buffers-intro.md) содержат данные по вершинам. В этом разделе показано, как инициализировать статический [буфер вершин](overviews-direct3d-11-resources-buffers-intro.md), то есть буфер вершин, который не изменяется. Справку по инициализации нестатического буфера см. в разделе ["Примечания](#remarks) ".

**Инициализация статического буфера вершин**

1.  Определите структуру, описывающую вершину. Например, если данные вершин содержат данные и цвет данных о положении, структура будет иметь один вектор, описывающий эту точку, и другую, описывающую цвет.
2.  Выделите память (с помощью malloc или New) для структуры, определенной на шаге 1. Заполните этот буфер фактическими данными вершин, описывающими геометрию.
3.  Создайте описание буфера, заполнив структуру [**D3D11 \_ буфера \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Передайте \_ \_ флаг буфера вершин D3D11 BIND в \_ элемент **биндфлагс** и передайте размер структуры из первого шага в элемент **битевидс** .
4.  Создайте описание данных о подресурсе, заполнив [**структуру \_ \_ данных подресурсов D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) . Элемент **псисмем** структуры [**\_ \_ данных подресурса D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) должен указывать непосредственно на данные ресурса, созданные на шаге 2.
5.  Вызовите метод [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) при передаче структуры [**\_ буфера \_ DESC D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , [**структуры \_ \_ данных подресурса D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) и адреса указателя на интерфейс [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) для инициализации.

В следующем примере кода показано, как создать буфер вершин. В этом примере предполагается, что **g \_ pd3dDevice** является допустимым объектом [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .


```
ID3D11Buffer*      g_pVertexBuffer;

// Define the data-type that
// describes a vertex.
struct SimpleVertexCombined
{
    XMFLOAT3 Pos;  
    XMFLOAT3 Col;  
};

// Supply the actual vertex data.
SimpleVertexCombined verticesCombo[] =
{
    XMFLOAT3( 0.0f, 0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.0f, 0.5f ),
    XMFLOAT3( 0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.5f, 0.0f, 0.0f ),
    XMFLOAT3( -0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.5f, 0.0f ),
};

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage            = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
bufferDesc.BindFlags        = D3D11_BIND_VERTEX_BUFFER;
bufferDesc.CPUAccessFlags   = 0;
bufferDesc.MiscFlags        = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = verticesCombo;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the vertex buffer.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer );
    
```



## <a name="remarks"></a>Примечания

Ниже приведены некоторые способы инициализации буфера вершин, который изменяется со временем.

1.  Создайте второй буфер с [**\_ \_ промежуточным использованием D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). Заполните второй буфер с помощью [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ссылку ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)unusing; используйте [**ссылку ID3D11DeviceContext:: копиресаурце**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) для копирования из промежуточного буфера в буфер по умолчанию.
2.  Используйте [**ссылку ID3D11DeviceContext:: упдатесубресаурце**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) для копирования данных из памяти.
3.  Создайте буфер с [**\_ \_ динамическим использованием D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)и заполните его с помощью [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ссылку ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) unusing (с использованием флагов Discard и нуверврите соответствующим образом).

\#1 и \# 2 полезны для содержимого, которое изменяется менее одного раза на кадр. Как правило, считывание GPU будет выполняться быстро, а обновления ЦП будут выполняться медленнее.

\#3 полезен для содержимого, которое изменяется более одного раза на кадр. Как правило, чтение GPU будет выполняться медленнее, но обновления ЦП будут выполняться быстрее.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Buffers](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




