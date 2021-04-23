---
title: Использование динамических ресурсов
description: Вы создаете и используете динамические ресурсы, когда приложению требуется изменить данные в этих ресурсах. Можно создавать текстуры и буферы для динамического использования.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41e00cda7236040679c7863454e4cc18d81106b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252881"
---
# <a name="how-to-use-dynamic-resources"></a><span data-ttu-id="1b876-104">Как использовать динамические ресурсы</span><span class="sxs-lookup"><span data-stu-id="1b876-104">How to: Use dynamic resources</span></span>

<span data-ttu-id="1b876-105">**Важные API**</span><span class="sxs-lookup"><span data-stu-id="1b876-105">**Important APIs**</span></span>

-   [<span data-ttu-id="1b876-106">**Ссылку ID3D11DeviceContext:: Map**</span><span class="sxs-lookup"><span data-stu-id="1b876-106">**ID3D11DeviceContext::Map**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [<span data-ttu-id="1b876-107">**Ссылку ID3D11DeviceContext:: отмена сопоставления**</span><span class="sxs-lookup"><span data-stu-id="1b876-107">**ID3D11DeviceContext::Unmap**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [<span data-ttu-id="1b876-108">**\_Использование D3D11**</span><span class="sxs-lookup"><span data-stu-id="1b876-108">**D3D11\_USAGE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

<span data-ttu-id="1b876-109">Вы создаете и используете динамические ресурсы, когда приложению требуется изменить данные в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="1b876-109">You create and use dynamic resources when your app needs to change data in those resources.</span></span> <span data-ttu-id="1b876-110">Можно создавать текстуры и буферы для динамического использования.</span><span class="sxs-lookup"><span data-stu-id="1b876-110">You can create textures and buffers for dynamic usage.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1b876-111">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="1b876-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1b876-112">Технологии</span><span class="sxs-lookup"><span data-stu-id="1b876-112">Technologies</span></span>

-   [<span data-ttu-id="1b876-113">Как создать текстуру</span><span class="sxs-lookup"><span data-stu-id="1b876-113">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
-   [<span data-ttu-id="1b876-114">Как программно инициализировать текстуру</span><span class="sxs-lookup"><span data-stu-id="1b876-114">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [<span data-ttu-id="1b876-115">Как создать буфер константы</span><span class="sxs-lookup"><span data-stu-id="1b876-115">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a><span data-ttu-id="1b876-116">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="1b876-116">Prerequisites</span></span>

<span data-ttu-id="1b876-117">Предполагается, что вы знакомы с C++.</span><span class="sxs-lookup"><span data-stu-id="1b876-117">We assume that you are familiar with C++.</span></span> <span data-ttu-id="1b876-118">Также вы должны быть знакомы с основными принципами программирования графики.</span><span class="sxs-lookup"><span data-stu-id="1b876-118">You also need basic experience with graphics programming concepts.</span></span>

## <a name="instructions"></a><span data-ttu-id="1b876-119">Инструкции</span><span class="sxs-lookup"><span data-stu-id="1b876-119">Instructions</span></span>

### <a name="step-1-specify-dynamic-usage"></a><span data-ttu-id="1b876-120">Шаг 1. Указание динамического использования</span><span class="sxs-lookup"><span data-stu-id="1b876-120">Step 1: Specify dynamic usage</span></span>

<span data-ttu-id="1b876-121">Если вы хотите, чтобы приложение могло вносить изменения в ресурсы, необходимо указать эти ресурсы как динамические и доступные для записи при их создании.</span><span class="sxs-lookup"><span data-stu-id="1b876-121">If you want your app to be able to make changes to resources, you must specify those resources as dynamic and writable when you create them.</span></span>

<span data-ttu-id="1b876-122">**Указание динамического использования**</span><span class="sxs-lookup"><span data-stu-id="1b876-122">**To specify dynamic usage**</span></span>

1.  <span data-ttu-id="1b876-123">Укажите динамическое использование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b876-123">Specify the resource usage as dynamic.</span></span> <span data-ttu-id="1b876-124">Например, укажите [**\_ \_ динамическое значение D3D11 Usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) в элементе **Usage** в [**\_ буфере D3D11 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) для вершины или буфера констант и укажите **\_ \_ динамическое значение использования D3D11** в элементе **Usage** [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) для двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="1b876-124">For example, specify the [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) value in the **Usage** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) for a vertex or constant buffer and specify the **D3D11\_USAGE\_DYNAMIC** value in the **Usage** member of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) for a 2D texture.</span></span>
2.  <span data-ttu-id="1b876-125">Укажите ресурс как доступный для записи.</span><span class="sxs-lookup"><span data-stu-id="1b876-125">Specify the resource as writable.</span></span> <span data-ttu-id="1b876-126">Например, укажите значение [**D3D11 \_ ЦП \_ доступ \_ для записи**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) в **кпуакцессфлагс** члене [**D3D11 \_ буфера \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) или [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span><span class="sxs-lookup"><span data-stu-id="1b876-126">For example, specify the [**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) value in the **CPUAccessFlags** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) or [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span></span>
3.  <span data-ttu-id="1b876-127">Передайте описание ресурса в функцию создания.</span><span class="sxs-lookup"><span data-stu-id="1b876-127">Pass the resource description to the creation function.</span></span> <span data-ttu-id="1b876-128">Например, передайте адрес [**D3D11 \_ буфера \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) в [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) и передайте адрес [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) в [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span><span class="sxs-lookup"><span data-stu-id="1b876-128">For example, pass the address of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) to [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) and pass the address of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) to [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span></span>

<span data-ttu-id="1b876-129">Ниже приведен пример создания динамического буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="1b876-129">Here is an example of creating a dynamic vertex buffer:</span></span>


```C++
    // Create a vertex buffer for a triangle.

    float2 triangleVertices[] =
    {
        float2(-0.5f, -0.5f),
        float2(0.0f, 0.5f),
        float2(0.5f, -0.5f),
    };

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(float2)* ARRAYSIZE(triangleVertices);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;
    vertexBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
    vertexBufferDesc.MiscFlags = 0;
    vertexBufferDesc.StructureByteStride = 0;

    D3D11_SUBRESOURCE_DATA vertexBufferData;
    vertexBufferData.pSysMem = triangleVertices;
    vertexBufferData.SysMemPitch = 0;
    vertexBufferData.SysMemSlicePitch = 0;

    DX::ThrowIfFailed(
        m_d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        &vertexBufferData,
        &vertexBuffer2
        )
        );

```



### <a name="step-2-change-a-dynamic-resource"></a><span data-ttu-id="1b876-130">Шаг 2. изменение динамического ресурса</span><span class="sxs-lookup"><span data-stu-id="1b876-130">Step 2: Change a dynamic resource</span></span>

<span data-ttu-id="1b876-131">Если вы указали ресурс как динамический и доступный для записи, то позднее можно внести изменения в этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="1b876-131">If you specified a resource as dynamic and writable when you created it, you can later make changes to that resource.</span></span>

<span data-ttu-id="1b876-132">**Изменение данных в динамическом ресурсе**</span><span class="sxs-lookup"><span data-stu-id="1b876-132">**To change data in a dynamic resource**</span></span>

1.  <span data-ttu-id="1b876-133">Настройте новые данные для ресурса.</span><span class="sxs-lookup"><span data-stu-id="1b876-133">Set up the new data for the resource.</span></span> <span data-ttu-id="1b876-134">Объявите переменную [**D3D11 \_ сопоставленного типа \_ подресурса**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) и инициализируйте ее нулем.</span><span class="sxs-lookup"><span data-stu-id="1b876-134">Declare a [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) type variable and initialize it to zero.</span></span> <span data-ttu-id="1b876-135">Эта переменная будет использоваться для изменения ресурса.</span><span class="sxs-lookup"><span data-stu-id="1b876-135">You'll use this variable to change the resource.</span></span>
2.  <span data-ttu-id="1b876-136">Отключите доступ графического процессора к данным, которые необходимо изменить, и получите указатель на память, содержащую данные.</span><span class="sxs-lookup"><span data-stu-id="1b876-136">Disable graphics processing unit (GPU) access to the data that you want to change and get a pointer to the memory that contains the data.</span></span> <span data-ttu-id="1b876-137">Чтобы получить этот указатель, передайте при вызове [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)параметр *маптипе* [**Write D3D11, \_ \_ отменяющий запись \_ Map**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) .</span><span class="sxs-lookup"><span data-stu-id="1b876-137">To get this pointer, pass [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) to the *MapType* parameter when you call [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span> <span data-ttu-id="1b876-138">Установите этот указатель на адрес [**D3D11 \_ сопоставленной переменной \_ подресурса**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) из предыдущего шага.</span><span class="sxs-lookup"><span data-stu-id="1b876-138">Set this pointer to the address of the [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) variable from the previous step.</span></span>
3.  <span data-ttu-id="1b876-139">Запишите новые данные в память.</span><span class="sxs-lookup"><span data-stu-id="1b876-139">Write the new data to the memory.</span></span>
4.  <span data-ttu-id="1b876-140">Вызовите метод [**ссылку ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) uncall, чтобы снова включить доступ GPU к данным после завершения записи новых данных.</span><span class="sxs-lookup"><span data-stu-id="1b876-140">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) to reenable GPU access to the data when you're finished writing the new data.</span></span>

<span data-ttu-id="1b876-141">Ниже приведен пример изменения динамического буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="1b876-141">Here is an example of changing a dynamic vertex buffer:</span></span>


```C++
// This might get called as the result of a click event to double the size of the triangle.
void TriangleRenderer::MapDoubleVertices()
{
    D3D11_MAPPED_SUBRESOURCE mappedResource;
    ZeroMemory(&mappedResource, sizeof(D3D11_MAPPED_SUBRESOURCE));
    float2 vertices[] =
    {
        float2(-1.0f, -1.0f),
        float2(0.0f, 1.0f),
        float2(1.0f, -1.0f),
    };
    //  Disable GPU access to the vertex buffer data.
    auto m_d3dContext = m_deviceResources->GetD3DDeviceContext();
    m_d3dContext->Map(vertexBuffer2.Get(), 0, D3D11_MAP_WRITE_DISCARD, 0, &mappedResource);
    //  Update the vertex buffer here.
    memcpy(mappedResource.pData, vertices, sizeof(vertices));
    //  Reenable GPU access to the vertex buffer data.
    m_d3dContext->Unmap(vertexBuffer2.Get(), 0);
}
```



## <a name="remarks"></a><span data-ttu-id="1b876-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="1b876-142">Remarks</span></span>

### <a name="using-dynamic-textures"></a><span data-ttu-id="1b876-143">Использование динамических текстур</span><span class="sxs-lookup"><span data-stu-id="1b876-143">Using dynamic textures</span></span>

<span data-ttu-id="1b876-144">Рекомендуется создавать только одну динамическую текстуру для каждого формата и, возможно, для каждого размера.</span><span class="sxs-lookup"><span data-stu-id="1b876-144">We recommend that you create only one dynamic texture per format and possibly per size.</span></span> <span data-ttu-id="1b876-145">Не рекомендуется создавать динамические MIP-карты, Кубы и тома из-за дополнительных затрат на сопоставление каждого уровня.</span><span class="sxs-lookup"><span data-stu-id="1b876-145">We don't recommend creating dynamic mipmaps, cubes, and volumes because of the additional overhead in mapping every level.</span></span> <span data-ttu-id="1b876-146">Для MIP-карты можно указать, что [**D3D11 \_ будет \_ записывать \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) только на верхнем уровне.</span><span class="sxs-lookup"><span data-stu-id="1b876-146">For mipmaps, you can specify [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) only on the top level.</span></span> <span data-ttu-id="1b876-147">Все уровни отбрасываются путем сопоставления только верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="1b876-147">All levels are discarded by mapping just the top level.</span></span> <span data-ttu-id="1b876-148">Это поведение одинаково для томов и кубов.</span><span class="sxs-lookup"><span data-stu-id="1b876-148">This behavior is the same for volumes and cubes.</span></span> <span data-ttu-id="1b876-149">Для кубов сопоставление верхнего уровня и лицевой стороны 0 сопоставляется.</span><span class="sxs-lookup"><span data-stu-id="1b876-149">For cubes, the top level and face 0 are mapped.</span></span>

### <a name="using-dynamic-buffers"></a><span data-ttu-id="1b876-150">Использование динамических буферов</span><span class="sxs-lookup"><span data-stu-id="1b876-150">Using dynamic buffers</span></span>

<span data-ttu-id="1b876-151">При вызове [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) в статическом буфере вершин, пока GPU использует буфер, существенно снижается производительность.</span><span class="sxs-lookup"><span data-stu-id="1b876-151">When you call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) on a static vertex buffer while the GPU is using the buffer, you get a significant performance penalty.</span></span> <span data-ttu-id="1b876-152">В этом случае **Map** должен подождать, пока GPU не закончит чтение данных вершин или индексов из буфера, прежде чем **Map** может вернуться к вызывающему приложению, что приводит к значительной задержке.</span><span class="sxs-lookup"><span data-stu-id="1b876-152">In this situation, **Map** must wait until the GPU is finished reading vertex or index data from the buffer before **Map** can return to the calling app, which causes a significant delay.</span></span> <span data-ttu-id="1b876-153">Вызов **Map** и последующее отображение из статического буфера несколько раз в кадре также предотвращает буферизацию команд GPU, поскольку перед возвратом указателя на карту необходимо закончить выполнение команд.</span><span class="sxs-lookup"><span data-stu-id="1b876-153">Calling **Map** and then rendering from a static buffer several times per frame also prevents the GPU from buffering rendering commands because it must finish commands before returning the map pointer.</span></span> <span data-ttu-id="1b876-154">Без буферизованных команд GPU остается неактивным до тех пор, пока приложение не завершит заполнение буфера вершин или буфера индексов и выдаст команду подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="1b876-154">Without buffered commands, the GPU remains idle until after the app is finished filling the vertex buffer or index buffer and issues a rendering command.</span></span>

<span data-ttu-id="1b876-155">В идеале данные вершин или индексов никогда не изменяются, но это не всегда возможно.</span><span class="sxs-lookup"><span data-stu-id="1b876-155">Ideally the vertex or index data would never change, but this is not always possible.</span></span> <span data-ttu-id="1b876-156">Существует множество ситуаций, в которых приложению необходимо изменить данные вершины или индекса для каждого кадра, возможно даже несколько раз в кадре.</span><span class="sxs-lookup"><span data-stu-id="1b876-156">There are many situations where the app needs to change vertex or index data every frame, perhaps even multiple times per frame.</span></span> <span data-ttu-id="1b876-157">В таких ситуациях рекомендуется создавать буфер вершин или индексов с [**\_ \_ динамическим использованием D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span><span class="sxs-lookup"><span data-stu-id="1b876-157">For these situations, we recommend that you create the vertex or index buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span> <span data-ttu-id="1b876-158">Этот флаг использования приводит к оптимизации среды выполнения для часто выполняемых операций с картой.</span><span class="sxs-lookup"><span data-stu-id="1b876-158">This usage flag causes the runtime to optimize for frequent map operations.</span></span> <span data-ttu-id="1b876-159">**D3D11 \_ \_Динамическое использование** полезно только в том случае, когда буфер сопоставляется часто. Если данные должны оставаться постоянными, поместите их в статический буфер вершин или индекс.</span><span class="sxs-lookup"><span data-stu-id="1b876-159">**D3D11\_USAGE\_DYNAMIC** is only useful when the buffer is mapped frequently; if data is to remain constant, place that data in a static vertex or index buffer.</span></span>

<span data-ttu-id="1b876-160">Чтобы получить улучшение производительности при использовании динамических буферов вершин, приложение должно вызвать [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) с соответствующими значениями [**D3D11 \_ Map**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) .</span><span class="sxs-lookup"><span data-stu-id="1b876-160">To receive a performance improvement when you use dynamic vertex buffers, your app must call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) with the appropriate [**D3D11\_MAP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) values.</span></span> <span data-ttu-id="1b876-161">[**D3D11 \_ \_ \_ Отмена записи на карту**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) означает, что приложению не нужно сохранять в буфере старые данные вершин или индексов.</span><span class="sxs-lookup"><span data-stu-id="1b876-161">[**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app doesn't need to keep the old vertex or index data in the buffer.</span></span> <span data-ttu-id="1b876-162">Если графический процессор все еще использует буфер при вызове **Map** с **D3D11ной \_ \_ записью \_ отказа**, среда выполнения возвращает указатель на новый регион памяти вместо старых данных буфера.</span><span class="sxs-lookup"><span data-stu-id="1b876-162">If the GPU is still using the buffer when you call **Map** with **D3D11\_MAP\_WRITE\_DISCARD**, the runtime returns a pointer to a new region of memory instead of the old buffer data.</span></span> <span data-ttu-id="1b876-163">Это позволяет GPU продолжать использовать старые данные, пока приложение помещает данные в новый буфер.</span><span class="sxs-lookup"><span data-stu-id="1b876-163">This allows the GPU to continue using the old data while the app places data in the new buffer.</span></span> <span data-ttu-id="1b876-164">В приложении не требуется дополнительное управление памятью; Старый буфер повторно используется или уничтожается автоматически после завершения работы графического процессора.</span><span class="sxs-lookup"><span data-stu-id="1b876-164">No additional memory management is required in the app; the old buffer is reused or destroyed automatically when the GPU is finished with it.</span></span>

> [!Note]  
> <span data-ttu-id="1b876-165">При сопоставлении буфера с [**D3D11ной \_ \_ записью \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)на отброшенную карту среда выполнения всегда удаляет весь буфер.</span><span class="sxs-lookup"><span data-stu-id="1b876-165">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), the runtime always discards the entire buffer.</span></span> <span data-ttu-id="1b876-166">Невозможно сохранить сведения в несопоставленных областях буфера, указав ненулевое смещение или поле с ограниченным размером.</span><span class="sxs-lookup"><span data-stu-id="1b876-166">You can't preserve info in unmapped areas of the buffer by specifying a nonzero offset or limited size field.</span></span>

 

<span data-ttu-id="1b876-167">Бывают случаи, когда объем данных, которые приложение должно хранить на карте, невелик, например добавление четырех вершин для отрисовки спрайта.</span><span class="sxs-lookup"><span data-stu-id="1b876-167">There are cases where the amount of data the app needs to store per map is small, such as adding four vertices to render a sprite.</span></span> <span data-ttu-id="1b876-168">[**D3D11 \_ \_Запись Map \_ без \_ перезаписи**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) указывает, что приложение не будет перезаписывать данные, уже используемые в динамическом буфере.</span><span class="sxs-lookup"><span data-stu-id="1b876-168">[**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app will not overwrite data already in use in the dynamic buffer.</span></span> <span data-ttu-id="1b876-169">Вызов [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) вернет указатель на старые данные, что позволит приложению добавлять новые данные в неиспользуемые области вершин или буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="1b876-169">The [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) call will return a pointer to the old data, which will allow the app to add new data in unused regions of the vertex or index buffer.</span></span> <span data-ttu-id="1b876-170">Приложение не должно изменять вершины или индексы, используемые в операции рисования, так как они по-прежнему используются графическим процессором.</span><span class="sxs-lookup"><span data-stu-id="1b876-170">The app must not modify vertices or indices that are used in a draw operation as they might still be in use by the GPU.</span></span> <span data-ttu-id="1b876-171">Рекомендуется, чтобы приложение использовало [**D3D11 \_ Map \_ Write \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) , после того как динамический буфер полон для получения нового региона памяти, который удаляет старую вершину или данные индекса после завершения GPU.</span><span class="sxs-lookup"><span data-stu-id="1b876-171">We recommend that the app then use [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) after the dynamic buffer is full to receive a new region of memory, which discards the old vertex or index data after the GPU is finished.</span></span>

<span data-ttu-id="1b876-172">Механизм асинхронных запросов полезен для определения того, используются ли в GPU вершины.</span><span class="sxs-lookup"><span data-stu-id="1b876-172">The asynchronous query mechanism is useful to determine if vertices are still in use by the GPU.</span></span> <span data-ttu-id="1b876-173">Выдайте запрос на [**\_ \_ событие типа D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) после последнего вызова Draw, использующего вершины.</span><span class="sxs-lookup"><span data-stu-id="1b876-173">Issue a query of type [**D3D11\_QUERY\_EVENT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) after the last draw call that uses the vertices.</span></span> <span data-ttu-id="1b876-174">Вершины больше не используются, если [**ссылку ID3D11DeviceContext:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1b876-174">The vertices are no longer in use when [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) returns S\_OK.</span></span> <span data-ttu-id="1b876-175">При сопоставлении буфера с [**D3D11 \_ \_ записи \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) или без значений Map всегда гарантируется, что вершины будут правильно синхронизированы с графическим процессором.</span><span class="sxs-lookup"><span data-stu-id="1b876-175">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) or no map values, you are always guaranteed that the vertices are synchronized properly with the GPU.</span></span> <span data-ttu-id="1b876-176">Но при сопоставлении без значений сопоставлений вам будет присвоено снижение производительности, описанное выше.</span><span class="sxs-lookup"><span data-stu-id="1b876-176">But, when you map without map values, you will incur the performance penalty described earlier.</span></span>

> [!Note]  
> <span data-ttu-id="1b876-177">Среда выполнения Direct3D 11,1, которая доступна начиная с Windows 8, позволяет сопоставлять динамические буферы констант и представления ресурсов шейдеров (СРВС) динамических буферов с [**D3D11 \_ Map \_ \_ без \_ перезаписи**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span><span class="sxs-lookup"><span data-stu-id="1b876-177">The Direct3D 11.1 runtime, which is available starting with Windows 8, enables mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with [**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span></span> <span data-ttu-id="1b876-178">Среда выполнения Direct3D 11 и более ранних версий не ограничивает-overwrite частично-Update сопоставление с буферами вершин или индексов.</span><span class="sxs-lookup"><span data-stu-id="1b876-178">The Direct3D 11 and earlier runtimes limited no-overwrite partial-update mapping to vertex or index buffers.</span></span> <span data-ttu-id="1b876-179">Чтобы определить, поддерживает ли устройство Direct3D эти функции, вызовите [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) с [**\_ функцией D3D11 \_ D3D11 \_ Options**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span><span class="sxs-lookup"><span data-stu-id="1b876-179">To determine if a Direct3D device supports these features, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span></span> <span data-ttu-id="1b876-180">**Чеккфеатуресуппорт** заполняет элементы [**D3D11 \_ \_ данных функций \_ D3D11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) в структуре параметров с помощью функций устройства.</span><span class="sxs-lookup"><span data-stu-id="1b876-180">**CheckFeatureSupport** fills members of a [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) structure with the device's features.</span></span> <span data-ttu-id="1b876-181">Ниже приведены соответствующие элементы **мапнувервритеондинамикконстантбуффер** и **мапнувервритеондинамикбуфферсрв**.</span><span class="sxs-lookup"><span data-stu-id="1b876-181">The relevant members here are **MapNoOverwriteOnDynamicConstantBuffer** and **MapNoOverwriteOnDynamicBufferSRV**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1b876-182">См. также</span><span class="sxs-lookup"><span data-stu-id="1b876-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b876-183">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1b876-183">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




