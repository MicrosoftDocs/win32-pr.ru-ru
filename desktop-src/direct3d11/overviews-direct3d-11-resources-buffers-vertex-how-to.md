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
# <a name="how-to-create-a-vertex-buffer"></a><span data-ttu-id="5289e-104">Как создать буфер вершин</span><span class="sxs-lookup"><span data-stu-id="5289e-104">How to: Create a Vertex Buffer</span></span>

<span data-ttu-id="5289e-105">[Буферы вершин](overviews-direct3d-11-resources-buffers-intro.md) содержат данные по вершинам.</span><span class="sxs-lookup"><span data-stu-id="5289e-105">[Vertex buffers](overviews-direct3d-11-resources-buffers-intro.md) contain per vertex data.</span></span> <span data-ttu-id="5289e-106">В этом разделе показано, как инициализировать статический [буфер вершин](overviews-direct3d-11-resources-buffers-intro.md), то есть буфер вершин, который не изменяется.</span><span class="sxs-lookup"><span data-stu-id="5289e-106">This topic shows how to initialize a static [vertex buffer](overviews-direct3d-11-resources-buffers-intro.md), that is, a vertex buffer that does not change.</span></span> <span data-ttu-id="5289e-107">Справку по инициализации нестатического буфера см. в разделе ["Примечания](#remarks) ".</span><span class="sxs-lookup"><span data-stu-id="5289e-107">For help initializing a non-static buffer, see the [remarks](#remarks) section.</span></span>

<span data-ttu-id="5289e-108">**Инициализация статического буфера вершин**</span><span class="sxs-lookup"><span data-stu-id="5289e-108">**To initialize a static vertex buffer**</span></span>

1.  <span data-ttu-id="5289e-109">Определите структуру, описывающую вершину.</span><span class="sxs-lookup"><span data-stu-id="5289e-109">Define a structure that describes a vertex.</span></span> <span data-ttu-id="5289e-110">Например, если данные вершин содержат данные и цвет данных о положении, структура будет иметь один вектор, описывающий эту точку, и другую, описывающую цвет.</span><span class="sxs-lookup"><span data-stu-id="5289e-110">For example, if your vertex data contains position data and color data, your structure would have one vector that describes the position and another that describes the color.</span></span>
2.  <span data-ttu-id="5289e-111">Выделите память (с помощью malloc или New) для структуры, определенной на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="5289e-111">Allocate memory (using malloc or new) for the structure that you defined in step one.</span></span> <span data-ttu-id="5289e-112">Заполните этот буфер фактическими данными вершин, описывающими геометрию.</span><span class="sxs-lookup"><span data-stu-id="5289e-112">Fill this buffer with the actual vertex data that describes your geometry.</span></span>
3.  <span data-ttu-id="5289e-113">Создайте описание буфера, заполнив структуру [**D3D11 \_ буфера \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="5289e-113">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="5289e-114">Передайте \_ \_ флаг буфера вершин D3D11 BIND в \_ элемент **биндфлагс** и передайте размер структуры из первого шага в элемент **битевидс** .</span><span class="sxs-lookup"><span data-stu-id="5289e-114">Pass the D3D11\_BIND\_VERTEX\_BUFFER flag to the **BindFlags** member and pass the size of the structure from step one to the **ByteWidth** member.</span></span>
4.  <span data-ttu-id="5289e-115">Создайте описание данных о подресурсе, заполнив [**структуру \_ \_ данных подресурсов D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="5289e-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="5289e-116">Элемент **псисмем** структуры [**\_ \_ данных подресурса D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) должен указывать непосредственно на данные ресурса, созданные на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="5289e-116">The **pSysMem** member of the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure should point directly to the resource data created in step two.</span></span>
5.  <span data-ttu-id="5289e-117">Вызовите метод [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) при передаче структуры [**\_ буфера \_ DESC D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , [**структуры \_ \_ данных подресурса D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) и адреса указателя на интерфейс [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) для инициализации.</span><span class="sxs-lookup"><span data-stu-id="5289e-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="5289e-118">В следующем примере кода показано, как создать буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="5289e-118">The following code example demonstrates how to create a vertex buffer.</span></span> <span data-ttu-id="5289e-119">В этом примере предполагается, что **g \_ pd3dDevice** является допустимым объектом [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="5289e-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="5289e-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="5289e-120">Remarks</span></span>

<span data-ttu-id="5289e-121">Ниже приведены некоторые способы инициализации буфера вершин, который изменяется со временем.</span><span class="sxs-lookup"><span data-stu-id="5289e-121">Here are some ways to initialize a vertex buffer that changes over time.</span></span>

1.  <span data-ttu-id="5289e-122">Создайте второй буфер с [**\_ \_ промежуточным использованием D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). Заполните второй буфер с помощью [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ссылку ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)unusing; используйте [**ссылку ID3D11DeviceContext:: копиресаурце**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) для копирования из промежуточного буфера в буфер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5289e-122">Create a 2nd buffer with [**D3D11\_USAGE\_STAGING**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); fill the second buffer using [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); use [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) to copy from the staging buffer to the default buffer.</span></span>
2.  <span data-ttu-id="5289e-123">Используйте [**ссылку ID3D11DeviceContext:: упдатесубресаурце**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) для копирования данных из памяти.</span><span class="sxs-lookup"><span data-stu-id="5289e-123">Use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to copy data from memory.</span></span>
3.  <span data-ttu-id="5289e-124">Создайте буфер с [**\_ \_ динамическим использованием D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)и заполните его с помощью [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ссылку ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) unusing (с использованием флагов Discard и нуверврите соответствующим образом).</span><span class="sxs-lookup"><span data-stu-id="5289e-124">Create a buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), and fill it with [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (using the Discard and NoOverwrite flags appropriately).</span></span>

<span data-ttu-id="5289e-125">\#1 и \# 2 полезны для содержимого, которое изменяется менее одного раза на кадр.</span><span class="sxs-lookup"><span data-stu-id="5289e-125">\#1 and \#2 are useful for content that changes less than once per frame.</span></span> <span data-ttu-id="5289e-126">Как правило, считывание GPU будет выполняться быстро, а обновления ЦП будут выполняться медленнее.</span><span class="sxs-lookup"><span data-stu-id="5289e-126">In general, GPU reads will be fast and CPU updates will be slower.</span></span>

<span data-ttu-id="5289e-127">\#3 полезен для содержимого, которое изменяется более одного раза на кадр.</span><span class="sxs-lookup"><span data-stu-id="5289e-127">\#3 is useful for content that changes more than once per frame.</span></span> <span data-ttu-id="5289e-128">Как правило, чтение GPU будет выполняться медленнее, но обновления ЦП будут выполняться быстрее.</span><span class="sxs-lookup"><span data-stu-id="5289e-128">In general, GPU reads will be slower, but CPU updates will be faster.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5289e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5289e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5289e-130">Buffers</span><span class="sxs-lookup"><span data-stu-id="5289e-130">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="5289e-131">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5289e-131">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




