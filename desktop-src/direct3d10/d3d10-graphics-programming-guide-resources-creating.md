---
description: Создание буферов требует определения данных, которые будут храниться в буфере, предоставления данных инициализации и настройки соответствующих флагов использования и привязки. Сведения о создании текстур см. в разделе Создание ресурсов текстуры (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Создание ресурсов буфера (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807535"
---
# <a name="creating-buffer-resources-direct3d-10"></a><span data-ttu-id="289c7-104">Создание ресурсов буфера (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="289c7-104">Creating Buffer Resources (Direct3D 10)</span></span>

<span data-ttu-id="289c7-105">Создание буферов требует определения данных, которые будут храниться в буфере, предоставления данных инициализации и настройки соответствующих флагов использования и привязки.</span><span class="sxs-lookup"><span data-stu-id="289c7-105">Creating buffers requires defining the data that the buffer will store, providing initialization data, and setting up appropriate usage and binding flags.</span></span> <span data-ttu-id="289c7-106">Сведения о создании текстур см. в разделе [Создание ресурсов текстуры (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span><span class="sxs-lookup"><span data-stu-id="289c7-106">To create textures, see [Creating Texture Resources (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>

-   [<span data-ttu-id="289c7-107">Создание буфера вершин</span><span class="sxs-lookup"><span data-stu-id="289c7-107">Create a Vertex Buffer</span></span>](#create-a-vertex-buffer)
    -   [<span data-ttu-id="289c7-108">Создание описания буфера</span><span class="sxs-lookup"><span data-stu-id="289c7-108">Create a Buffer Description</span></span>](#create-a-buffer-description)
    -   [<span data-ttu-id="289c7-109">Создание данных инициализации для буфера</span><span class="sxs-lookup"><span data-stu-id="289c7-109">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
    -   [<span data-ttu-id="289c7-110">Создание буфера</span><span class="sxs-lookup"><span data-stu-id="289c7-110">Create the Buffer</span></span>](#create-the-buffer)
-   [<span data-ttu-id="289c7-111">Создание буфера индекса</span><span class="sxs-lookup"><span data-stu-id="289c7-111">Create an Index Buffer</span></span>](#create-an-index-buffer)
-   [<span data-ttu-id="289c7-112">Создание буфера констант</span><span class="sxs-lookup"><span data-stu-id="289c7-112">Create a Constant Buffer</span></span>](#create-a-constant-buffer)
-   [<span data-ttu-id="289c7-113">См. также</span><span class="sxs-lookup"><span data-stu-id="289c7-113">Related topics</span></span>](#related-topics)

## <a name="create-a-vertex-buffer"></a><span data-ttu-id="289c7-114">Создание буфера вершин</span><span class="sxs-lookup"><span data-stu-id="289c7-114">Create a Vertex Buffer</span></span>

<span data-ttu-id="289c7-115">Ниже приведены шаги по созданию [буфера вершин](d3d10-graphics-programming-guide-resources-types.md) .</span><span class="sxs-lookup"><span data-stu-id="289c7-115">The steps to creating a [vertex buffer](d3d10-graphics-programming-guide-resources-types.md) are as follows.</span></span>

-   [<span data-ttu-id="289c7-116">Создание описания буфера</span><span class="sxs-lookup"><span data-stu-id="289c7-116">Create a Buffer Description</span></span>](#create-a-buffer-description)
-   [<span data-ttu-id="289c7-117">Создание данных инициализации для буфера</span><span class="sxs-lookup"><span data-stu-id="289c7-117">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
-   [<span data-ttu-id="289c7-118">Создание буфера</span><span class="sxs-lookup"><span data-stu-id="289c7-118">Create the Buffer</span></span>](#create-the-buffer)

### <a name="create-a-buffer-description"></a><span data-ttu-id="289c7-119">Создание описания буфера</span><span class="sxs-lookup"><span data-stu-id="289c7-119">Create a Buffer Description</span></span>

<span data-ttu-id="289c7-120">При создании буфера вершин описание буфера (см. [**D3D10 \_ buffer \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) используется для определения того, как данные организованы в буфере, как конвейер может получить доступ к буферу и как будет использоваться буфер.</span><span class="sxs-lookup"><span data-stu-id="289c7-120">When creating a vertex buffer, a buffer description (see [**D3D10\_BUFFER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) is used to define how data is organized within the buffer, how the pipeline can access the buffer, and how the buffer will be used.</span></span>

<span data-ttu-id="289c7-121">В следующем примере показано, как создать описание буфера для одного треугольника с вершинами, содержащими значения позиций и цветов.</span><span class="sxs-lookup"><span data-stu-id="289c7-121">The following example demonstrates how to create a buffer description for a single triangle with vertices that contain position and color values.</span></span>


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



<span data-ttu-id="289c7-122">В этом примере описание буфера инициализируется почти всеми параметрами по умолчанию для [**использования**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**доступа ЦП**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) и [**прочих флагов**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span><span class="sxs-lookup"><span data-stu-id="289c7-122">In this example, the buffer description is initialized with almost all default settings for [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**CPU access**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) and [**miscellaneous flags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span></span> <span data-ttu-id="289c7-123">Другие параметры предназначены для [**флага привязки**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) , который определяет ресурс как буфер вершин и размер буфера.</span><span class="sxs-lookup"><span data-stu-id="289c7-123">The other settings are for the [**bind flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) which identifies the resource as a vertex buffer only, and the size of the buffer.</span></span>

<span data-ttu-id="289c7-124">Флаги использования и доступа к ЦП важны для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="289c7-124">The usage and CPU access flags are important for performance.</span></span> <span data-ttu-id="289c7-125">Эти два флага вместе определяют частоту доступа к ресурсу, тип памяти, в которую может быть загружен ресурс, и то, какой процессор должен получить доступ к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="289c7-125">These two flags together determine how often a resource gets accessed, what type of memory the resource could be loaded into, and what processor needs to access the resource.</span></span> <span data-ttu-id="289c7-126">Использование по умолчанию этот ресурс не будет обновляться очень часто.</span><span class="sxs-lookup"><span data-stu-id="289c7-126">Default usage this resource will not be updated very often.</span></span> <span data-ttu-id="289c7-127">Установка значения "доступ ЦП" равным 0 означает, что ЦП не должен считывать или записывать ресурс.</span><span class="sxs-lookup"><span data-stu-id="289c7-127">Setting CPU access to 0 means that the CPU will not need to either read or write the resource.</span></span> <span data-ttu-id="289c7-128">В сочетании это означает, что среда выполнения может загрузить ресурс в наиболее производительную память для GPU, так как ресурс не требует доступа к ЦП.</span><span class="sxs-lookup"><span data-stu-id="289c7-128">Taken in combination, this means that the runtime can load the resource into the highest performing memory for the GPU since the resource does not require CPU access.</span></span>

<span data-ttu-id="289c7-129">Как и ожидалось, существует компромисс между оптимальной производительностью и любым уровнем доступности любого из процессоров.</span><span class="sxs-lookup"><span data-stu-id="289c7-129">As expected, there is a tradeoff between best performance and any-time accessibility by either processor.</span></span> <span data-ttu-id="289c7-130">Например, использование по умолчанию без доступа к ЦП означает, что ресурс можно сделать доступным только для GPU.</span><span class="sxs-lookup"><span data-stu-id="289c7-130">For example, the default usage with no CPU access means that the resource can be made available to the GPU exclusively.</span></span> <span data-ttu-id="289c7-131">Это может включать загрузку ресурса в память, не доступную напрямую ЦП.</span><span class="sxs-lookup"><span data-stu-id="289c7-131">This could include loading the resource into memory not directly accessible by the CPU.</span></span> <span data-ttu-id="289c7-132">Ресурс можно изменить только с помощью [**упдатесубресаурце**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span><span class="sxs-lookup"><span data-stu-id="289c7-132">The resource could only be modified with [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span></span>

### <a name="create-the-initialization-data-for-the-buffer"></a><span data-ttu-id="289c7-133">Создание данных инициализации для буфера</span><span class="sxs-lookup"><span data-stu-id="289c7-133">Create the Initialization Data for the Buffer</span></span>

<span data-ttu-id="289c7-134">Буфер — это просто коллекция элементов, которая располагается в виде массива 1D.</span><span class="sxs-lookup"><span data-stu-id="289c7-134">A buffer is just a collection of elements and is laid out as a 1D array.</span></span> <span data-ttu-id="289c7-135">В результате одновременное прорезание системной памяти и шаг среза системной памяти одинаковы. Размер объявления данных вершин.</span><span class="sxs-lookup"><span data-stu-id="289c7-135">As a result, the system memory pitch and system memory slice pitch are both the same; the size of the vertex data declaration.</span></span> <span data-ttu-id="289c7-136">Приложение может предоставлять данные инициализации при создании буфера с помощью [**описания подресурса**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), которое содержит указатель на фактические данные ресурса и содержит сведения о размере и структуре этих данных.</span><span class="sxs-lookup"><span data-stu-id="289c7-136">An application can provide initialization data when a buffer is created using a [**subresource description**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), which contains a pointer to the actual resource data and contains information about the size and layout of that data.</span></span>

<span data-ttu-id="289c7-137">Любой буфер, созданный с неизменяемым использованием (см. раздел [**D3D10 \_ Usage \_ unmutable**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)), должен быть инициализирован во время создания.</span><span class="sxs-lookup"><span data-stu-id="289c7-137">Any buffer created with immutable usage (see [**D3D10\_USAGE\_IMMUTABLE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) must be initialized at creation time.</span></span> <span data-ttu-id="289c7-138">Буферы, использующие любой из других флагов использования, могут быть обновлены после инициализации с помощью [**копиресаурце**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**кописубресаурцерегион**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)и [**упдатесубресаурце**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)или доступа к его базовой памяти с помощью метода [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) .</span><span class="sxs-lookup"><span data-stu-id="289c7-138">Buffers that use any of the other usage flags can be updated after initialization using [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion), and [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), or by accessing its underlying memory using the [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) method.</span></span>

### <a name="create-the-buffer"></a><span data-ttu-id="289c7-139">Создание буфера</span><span class="sxs-lookup"><span data-stu-id="289c7-139">Create the Buffer</span></span>

<span data-ttu-id="289c7-140">Используя описание буфера и данные инициализации (необязательно), вызовите [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) , чтобы создать буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="289c7-140">Using the buffer description and the initialization data (which is optional) call [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) to create a vertex buffer.</span></span> <span data-ttu-id="289c7-141">В следующем фрагменте кода показано, как создать буфер вершин из массива данных вершин, объявленных приложением.</span><span class="sxs-lookup"><span data-stu-id="289c7-141">The following code snippet demonstrates how to create a vertex buffer from an array of vertex data declared by the application.</span></span>


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a><span data-ttu-id="289c7-142">Создание буфера индекса</span><span class="sxs-lookup"><span data-stu-id="289c7-142">Create an Index Buffer</span></span>

<span data-ttu-id="289c7-143">Создание буфера индекса очень похоже на создание буфера вершин; с двумя различиями.</span><span class="sxs-lookup"><span data-stu-id="289c7-143">Creating an index buffer is very similar to creating a vertex buffer; with two differences.</span></span> <span data-ttu-id="289c7-144">Буфер индексов содержит только 16-разрядные или 32-разрядные данные (вместо широкого диапазона форматов, доступных для буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="289c7-144">An index buffer contains only 16-bit or 32-bit data (instead of the wide range of formats available to a vertex buffer.</span></span> <span data-ttu-id="289c7-145">Буфер индексов также требует наличия флага привязки index-buffer.</span><span class="sxs-lookup"><span data-stu-id="289c7-145">An index buffer also requires an index-buffer bind flag.</span></span>

<span data-ttu-id="289c7-146">В следующем примере показано, как создать буфер индекса из массива данных индекса.</span><span class="sxs-lookup"><span data-stu-id="289c7-146">The following example demonstrates how to create an index buffer from an array of index data.</span></span>


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a><span data-ttu-id="289c7-147">Создание буфера констант</span><span class="sxs-lookup"><span data-stu-id="289c7-147">Create a Constant Buffer</span></span>

<span data-ttu-id="289c7-148">В Direct3D 10 появился буфер констант.</span><span class="sxs-lookup"><span data-stu-id="289c7-148">Direct3D 10 introduces a constant buffer.</span></span> <span data-ttu-id="289c7-149">Буфер константы или буфер констант шейдера — это буфер, содержащий константы шейдера.</span><span class="sxs-lookup"><span data-stu-id="289c7-149">A constant buffer, or shader constant buffer, is a buffer that contains shader constants.</span></span> <span data-ttu-id="289c7-150">Ниже приведен пример создания буфера констант, взятого из [примера HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="289c7-150">Here is an example of creating a constant buffer, taken from the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



<span data-ttu-id="289c7-151">Обратите внимание, что при использовании интерфейса [**интерфейса ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) процесс создания, привязки и передачи постоянного буфера обрабатывается экземпляром **интерфейса ID3D10Effect** .</span><span class="sxs-lookup"><span data-stu-id="289c7-151">Note that when using the [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) interface the process of creating, binding and comitting a constant buffer is handled by the **ID3D10Effect Interface** instance.</span></span> <span data-ttu-id="289c7-152">В этом случае можно только получить переменную из воздействия с помощью одного из методов несцесари, таких как [**жетвариаблебинаме**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) , и обновить переменную с помощью одного из методов SetVariable, таких как [**сетматрикс**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span><span class="sxs-lookup"><span data-stu-id="289c7-152">In that case it is only nescesary to get the variable from the effect with one of the GetVariable methods such as [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) and update the variable with one of the SetVariable methods such as [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span></span> <span data-ttu-id="289c7-153">Пример использования **интерфейса ID3D10Effect** для управления буфером констант см. в [руководстве 7. Сопоставление текстур и буферы констант](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="289c7-153">For an example of using **ID3D10Effect Interface** to manage a constant buffer see [Tutorial 7: Texture Mapping and Constant Buffers](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="289c7-154">См. также</span><span class="sxs-lookup"><span data-stu-id="289c7-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="289c7-155">Ресурсы (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="289c7-155">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



