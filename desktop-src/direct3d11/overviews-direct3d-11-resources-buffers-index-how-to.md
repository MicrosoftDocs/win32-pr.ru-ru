---
title: Создание буфера индекса
description: В этом разделе показано, как инициализировать буфер индексов при подготовке к подготовке к просмотру.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- буфер индексов, создание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c4c99639748876a5f5fd84e546aaf299885c76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258733"
---
# <a name="how-to-create-an-index-buffer"></a><span data-ttu-id="bac84-104">Как создать буфер индексов</span><span class="sxs-lookup"><span data-stu-id="bac84-104">How to: Create an Index Buffer</span></span>

<span data-ttu-id="bac84-105">[Буферы индексов](overviews-direct3d-11-resources-buffers-intro.md) содержат данные индекса.</span><span class="sxs-lookup"><span data-stu-id="bac84-105">[Index buffers](overviews-direct3d-11-resources-buffers-intro.md) contain index data.</span></span> <span data-ttu-id="bac84-106">В этом разделе показано, как инициализировать [буфер индексов](overviews-direct3d-11-resources-buffers-intro.md) при подготовке к подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="bac84-106">This topic shows how to initialize an [index buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="bac84-107">**Инициализация буфера индекса**</span><span class="sxs-lookup"><span data-stu-id="bac84-107">**To initialize an index buffer**</span></span>

1.  <span data-ttu-id="bac84-108">Создайте буфер, содержащий сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="bac84-108">Create a buffer that contains your index information.</span></span>
2.  <span data-ttu-id="bac84-109">Создайте описание буфера, заполнив структуру [**D3D11 \_ буфера \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="bac84-109">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="bac84-110">Передайте \_ флаг D3D11 привязки \_ индекса в \_ элемент **биндфлагс** и передайте размер буфера в байтах элементу **битевидс** .</span><span class="sxs-lookup"><span data-stu-id="bac84-110">Pass the D3D11\_BIND\_INDEX\_BUFFER flag to the **BindFlags** member and pass the size of the buffer in bytes to the **ByteWidth** member.</span></span>
3.  <span data-ttu-id="bac84-111">Создайте описание данных о подресурсе, заполнив [**структуру \_ \_ данных подресурсов D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="bac84-111">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="bac84-112">Элемент **псисмем** должен указывать непосредственно на данные индекса, созданные на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="bac84-112">The **pSysMem** member should point directly to the index data created in step one.</span></span>
4.  <span data-ttu-id="bac84-113">Вызовите метод [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) при передаче структуры [**\_ буфера \_ DESC D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , [**структуры \_ \_ данных подресурса D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) и адреса указателя на интерфейс [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) для инициализации.</span><span class="sxs-lookup"><span data-stu-id="bac84-113">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="bac84-114">В следующем примере кода показано, как создать буфер индекса.</span><span class="sxs-lookup"><span data-stu-id="bac84-114">The following code example demonstrates how to create an index buffer.</span></span> <span data-ttu-id="bac84-115">В этом примере предполагается, что</span><span class="sxs-lookup"><span data-stu-id="bac84-115">This example assumes that</span></span>


```
g_pd3dDevice
```



<span data-ttu-id="bac84-116">является допустимым объектом [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) , который</span><span class="sxs-lookup"><span data-stu-id="bac84-116">is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that</span></span>


```
g_pd3dContext
```



<span data-ttu-id="bac84-117">является допустимым объектом [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="bac84-117">is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="bac84-118">См. также</span><span class="sxs-lookup"><span data-stu-id="bac84-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bac84-119">Buffers</span><span class="sxs-lookup"><span data-stu-id="bac84-119">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="bac84-120">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="bac84-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




