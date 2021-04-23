---
title: Динамическое индексирование с помощью HLSL 5.1
description: В образце D3D12DynamicIndexing показаны некоторые новые функции HLSL, доступные в модели шейдеров 5,1, особенно динамическое индексирование и неограниченные массивы, для отображения одной и той же сетки несколько раз, каждый раз выполнив визуализацию с динамически выбранным материалом. Благодаря динамическому индексированию шейдеры теперь могут индексироваться в массив, не зная значение индекса во время компиляции. При сочетании с неограниченными массивами это позволяет добавить еще один уровень косвенного обращения и гибкость для авторов шейдеров и конвейеров изображений.
ms.assetid: 9821AEDF-E83D-4034-863A-2B820D9B7455
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e41892e7deff23c8d11f8be1c38dac3fcba1de9
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548967"
---
# <a name="dynamic-indexing-using-hlsl-51"></a><span data-ttu-id="7ede2-105">Динамическое индексирование с помощью HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="7ede2-105">Dynamic Indexing using HLSL 5.1</span></span>

<span data-ttu-id="7ede2-106">В образце **D3D12DynamicIndexing** показаны некоторые новые функции HLSL, доступные в модели шейдеров 5,1, особенно динамическое индексирование и неограниченные массивы, для отображения одной и той же сетки несколько раз, каждый раз выполнив визуализацию с динамически выбранным материалом.</span><span class="sxs-lookup"><span data-stu-id="7ede2-106">The **D3D12DynamicIndexing** sample demonstrates some of the new HLSL features available in Shader Model 5.1 - particularly dynamic indexing and unbounded arrays - to render the same mesh multiple times, each time rendering it with a dynamically selected material.</span></span> <span data-ttu-id="7ede2-107">Благодаря динамическому индексированию шейдеры теперь могут индексироваться в массив, не зная значение индекса во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="7ede2-107">With dynamic indexing, shaders can now index into an array without knowing the value of the index at compile time.</span></span> <span data-ttu-id="7ede2-108">При сочетании с неограниченными массивами это позволяет добавить еще один уровень косвенного обращения и гибкость для авторов шейдеров и конвейеров изображений.</span><span class="sxs-lookup"><span data-stu-id="7ede2-108">When combined with unbounded arrays, this adds another level of indirection and flexibility for shader authors and art pipelines.</span></span>

-   [<span data-ttu-id="7ede2-109">Настройка шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="7ede2-109">Set up the pixel shader</span></span>](#set-up-the-pixel-shader)
-   [<span data-ttu-id="7ede2-110">Настройка корневой подписи</span><span class="sxs-lookup"><span data-stu-id="7ede2-110">Set up the root signature</span></span>](#set-up-the-root-signature)
-   [<span data-ttu-id="7ede2-111">Создание текстур</span><span class="sxs-lookup"><span data-stu-id="7ede2-111">Create the textures</span></span>](#create-the-textures)
-   [<span data-ttu-id="7ede2-112">Отправка данных текстуры</span><span class="sxs-lookup"><span data-stu-id="7ede2-112">Upload the texture data</span></span>](#upload-the-texture-data)
-   [<span data-ttu-id="7ede2-113">Загрузка текстуры диффузии</span><span class="sxs-lookup"><span data-stu-id="7ede2-113">Load the diffuse texture</span></span>](#load-the-diffuse-texture)
-   [<span data-ttu-id="7ede2-114">Создание образца</span><span class="sxs-lookup"><span data-stu-id="7ede2-114">Create a sampler</span></span>](#create-a-sampler)
-   [<span data-ttu-id="7ede2-115">Динамическое изменение индекса корневого параметра</span><span class="sxs-lookup"><span data-stu-id="7ede2-115">Dynamically change the root parameter index</span></span>](#dynamically-change-the-root-parameter-index)
-   [<span data-ttu-id="7ede2-116">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="7ede2-116">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="7ede2-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7ede2-117">Related topics</span></span>](#related-topics)

## <a name="set-up-the-pixel-shader"></a><span data-ttu-id="7ede2-118">Настройка шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="7ede2-118">Set up the pixel shader</span></span>

<span data-ttu-id="7ede2-119">Давайте сначала рассмотрим сам шейдер, для которого в этом примере используется шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="7ede2-119">Let's first look at the shader itself, which for this sample is a pixel shader.</span></span>

``` syntax
Texture2D        g_txDiffuse : register(t0);
Texture2D        g_txMats[]  : register(t1);
SamplerState     g_sampler   : register(s0);

struct PSSceneIn
{
    float4 pos : SV_Position;
    float2 tex : TEXCOORD0;
};

struct MaterialConstants
{
    uint matIndex;  // Dynamically set index for looking up from g_txMats[].
};
ConstantBuffer<MaterialConstants> materialConstants : register(b0, space0);

float4 PSSceneMain(PSSceneIn input) : SV_Target
{
    float3 diffuse = g_txDiffuse.Sample(g_sampler, input.tex).rgb;
    float3 mat = g_txMats[materialConstants.matIndex].Sample(g_sampler, input.tex).rgb;
    return float4(diffuse * mat, 1.0f);
}
```

<span data-ttu-id="7ede2-120">Функция неограниченного массива показана `g_txMats[]` массивом, так как не указывает размер массива.</span><span class="sxs-lookup"><span data-stu-id="7ede2-120">The unbounded array feature is illustrated by the `g_txMats[]` array as it does not specify an array size.</span></span> <span data-ttu-id="7ede2-121">Динамическое индексирование используется для индексации в `g_txMats[]` с `matIndex` , которое определено как корневая константа.</span><span class="sxs-lookup"><span data-stu-id="7ede2-121">Dynamic indexing is used to index into `g_txMats[]` with `matIndex`, which is defined as a root constant.</span></span> <span data-ttu-id="7ede2-122">Шейдер не имеет сведений о размере, массиве или значении индекса во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="7ede2-122">The shader has no knowledge of the size or the array or the value of the index at compile-time.</span></span> <span data-ttu-id="7ede2-123">Оба атрибута определены в корневой подписи объекта состояния конвейера, используемого с шейдером.</span><span class="sxs-lookup"><span data-stu-id="7ede2-123">Both attributes are defined in the root signature of the pipeline state object used with the shader.</span></span>

<span data-ttu-id="7ede2-124">Чтобы воспользоваться преимуществами функций динамической индексации в HLSL, необходимо скомпилировать шейдер с SM 5,1.</span><span class="sxs-lookup"><span data-stu-id="7ede2-124">To take advantage of the dynamic indexing features in HLSL requires that the shader be compiled with SM 5.1.</span></span> <span data-ttu-id="7ede2-125">Кроме того, для использования неограниченных массивов также должен использоваться флаг **\_ неограниченных \_ \_ таблиц дескрипторов/Enable** .</span><span class="sxs-lookup"><span data-stu-id="7ede2-125">Additionally, to make use of unbounded arrays, the **/enable\_unbounded\_descriptor\_tables** flag must also be used.</span></span> <span data-ttu-id="7ede2-126">Для компиляции этого шейдера с помощью [средства компилятора Effect](/windows/desktop/direct3dtools/fxc) (FXC) используются следующие параметры командной строки:</span><span class="sxs-lookup"><span data-stu-id="7ede2-126">The following command line options are used to compile this shader with the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC):</span></span>

``` syntax
fxc /Zi /E"PSSceneMain" /Od /Fo"dynamic_indexing_pixel.cso" /ps"_5_1" /nologo /enable_unbounded_descriptor_tables
```

## <a name="set-up-the-root-signature"></a><span data-ttu-id="7ede2-127">Настройка корневой подписи</span><span class="sxs-lookup"><span data-stu-id="7ede2-127">Set up the root signature</span></span>

<span data-ttu-id="7ede2-128">Теперь рассмотрим определение корневой сигнатуры, в частности, определение размера неограниченного массива и связывание корневой константы с `matIndex` .</span><span class="sxs-lookup"><span data-stu-id="7ede2-128">Now, let's look at the root signature definition, particularly, how we define the size of the unbounded array and link a root constant to `matIndex`.</span></span> <span data-ttu-id="7ede2-129">Для шейдера пикселей мы определим три вещи: таблицу дескрипторов для СРВС (наш Texture2Ds), таблицу дескрипторов для проб и единственную корневую константу.</span><span class="sxs-lookup"><span data-stu-id="7ede2-129">For the pixel shader, we define three things: a descriptor table for SRVs (our Texture2Ds), a descriptor table for Samplers and a single root constant.</span></span> <span data-ttu-id="7ede2-130">Таблица дескрипторов для нашего СРВС содержит `CityMaterialCount + 1` записи.</span><span class="sxs-lookup"><span data-stu-id="7ede2-130">The descriptor table for our SRVs contains `CityMaterialCount + 1` entries.</span></span> <span data-ttu-id="7ede2-131">`CityMaterialCount` Константа, определяющая длину `g_txMats[]` и значение + 1 для `g_txDiffuse` .</span><span class="sxs-lookup"><span data-stu-id="7ede2-131">`CityMaterialCount` is a constant that defines the length of `g_txMats[]` and the + 1 is for `g_txDiffuse`.</span></span> <span data-ttu-id="7ede2-132">Таблица дескрипторов для наших пробов содержит только одну запись, и мы определяем 1 32-разрядное корневое значение root с помощью **инитасконстантс**(...). в методе **лоадассетс** .</span><span class="sxs-lookup"><span data-stu-id="7ede2-132">The descriptor table for our Samplers contains only one entry and we only define one 32-bit root constant value via **InitAsConstants**(…)., in the **LoadAssets** method.</span></span>

``` syntax
 // Create the root signature.
    {
        CD3DX12_DESCRIPTOR_RANGE ranges[3];
        ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1 + CityMaterialCount, 0);  // Diffuse texture + array of materials.
        ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER, 1, 0);
        ranges[2].Init(D3D12_DESCRIPTOR_RANGE_TYPE_CBV, 1, 0);

        CD3DX12_ROOT_PARAMETER rootParameters[4];
        rootParameters[0].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[1].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[2].InitAsDescriptorTable(1, &ranges[2], D3D12_SHADER_VISIBILITY_VERTEX);
        rootParameters[3].InitAsConstants(1, 0, 0, D3D12_SHADER_VISIBILITY_PIXEL);

        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(_countof(rootParameters), rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }
```



| <span data-ttu-id="7ede2-133">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="7ede2-133">Call flow</span></span>                                                             | <span data-ttu-id="7ede2-134">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ede2-134">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="7ede2-135">**\_Диапазон дескрипторов CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="7ede2-135">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="7ede2-136">**\_Тип диапазона дескрипторов D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ede2-136">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="7ede2-137">**\_Корневой \_ параметр CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="7ede2-137">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="7ede2-138">**\_Видимость шейдера \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="7ede2-138">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="7ede2-139">**\_DESC корневой \_ подписи CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="7ede2-139">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="7ede2-140">**\_ \_ Флаги корневой подписи D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7ede2-140">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="7ede2-141">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7ede2-141">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="7ede2-142">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="7ede2-142">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="7ede2-143">**\_Версия корневой \_ СИГНАТУРы D3D \_**</span><span class="sxs-lookup"><span data-stu-id="7ede2-143">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="7ede2-144">**креатерутсигнатуре**</span><span class="sxs-lookup"><span data-stu-id="7ede2-144">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-textures"></a><span data-ttu-id="7ede2-145">Создание текстур</span><span class="sxs-lookup"><span data-stu-id="7ede2-145">Create the textures</span></span>

<span data-ttu-id="7ede2-146">Содержимое `g_txMats[]` представляют собой созданные процедурой текстуры, созданные в **лоадассетс**.</span><span class="sxs-lookup"><span data-stu-id="7ede2-146">The contents of `g_txMats[]` are procedurally generated textures created in **LoadAssets**.</span></span> <span data-ttu-id="7ede2-147">Каждый город, отображаемый в сцене, использует одну и ту же текстуру диффузии, но каждая из них также имеет собственную процедуру, сформированную процедурой.</span><span class="sxs-lookup"><span data-stu-id="7ede2-147">Each city rendered in the scene shares the same diffuse texture but each also has its own procedurally generated texture.</span></span> <span data-ttu-id="7ede2-148">Массив текстур охватывает спектр «Радуга», что позволяет легко визуализировать метод индексирования.</span><span class="sxs-lookup"><span data-stu-id="7ede2-148">The array of textures span the rainbow spectrum to easily visualize the indexing technique.</span></span>

``` syntax
 // Create the textures and sampler.
    {
        // Procedurally generate an array of textures to use as city materials.
        {
            // All of these materials use the same texture desc.
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = 1;
            textureDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            textureDesc.Width = CityMaterialTextureWidth;
            textureDesc.Height = CityMaterialTextureHeight;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            // The textures evenly span the color rainbow so that each city gets
            // a different material.
            float materialGradStep = (1.0f / static_cast<float>(CityMaterialCount));

            // Generate texture data.
            vector<vector<unsigned char>> cityTextureData;
            cityTextureData.resize(CityMaterialCount);
            for (int i = 0; i < CityMaterialCount; ++i)
            {
                CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &heapProps,
                    D3D12_HEAP_FLAG_NONE,
                    &textureDesc,
                    D3D12_RESOURCE_STATE_COPY_DEST,
                    nullptr,
                    IID_PPV_ARGS(&m_cityMaterialTextures[i])));

                // Fill the texture.
                float t = i * materialGradStep;
                cityTextureData[i].resize(CityMaterialTextureWidth * CityMaterialTextureHeight * CityMaterialTextureChannelCount);
                for (int x = 0; x < CityMaterialTextureWidth; ++x)
                {
                    for (int y = 0; y < CityMaterialTextureHeight; ++y)
                    {
                        // Compute the appropriate index into the buffer based on the x/y coordinates.
                        int pixelIndex = (y * CityMaterialTextureChannelCount * CityMaterialTextureWidth) + (x * CityMaterialTextureChannelCount);

                        // Determine this row's position along the rainbow gradient.
                        float tPrime = t + ((static_cast<float>(y) / static_cast<float>(CityMaterialTextureHeight)) * materialGradStep);

                        // Compute the RGB value for this position along the rainbow
                        // and pack the pixel value.
                        XMVECTOR hsl = XMVectorSet(tPrime, 0.5f, 0.5f, 1.0f);
                        XMVECTOR rgb = XMColorHSLToRGB(hsl);
                        cityTextureData[i][pixelIndex + 0] = static_cast<unsigned char>((255 * XMVectorGetX(rgb)));
                        cityTextureData[i][pixelIndex + 1] = static_cast<unsigned char>((255 * XMVectorGetY(rgb)));
                        cityTextureData[i][pixelIndex + 2] = static_cast<unsigned char>((255 * XMVectorGetZ(rgb)));
                        cityTextureData[i][pixelIndex + 3] = 255;
                    }
                }
            }
        }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7ede2-149">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="7ede2-149">Call flow</span></span></th>
<th><span data-ttu-id="7ede2-150">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ede2-150">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ede2-151"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-151"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-152"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-152"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="7ede2-153">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-153">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span><br /><span data-ttu-id="7ede2-154">
<a href=""></a>[<strong>D3D12_RESOURCE_DIMENSION</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_resource_dimension)</span><span class="sxs-lookup"><span data-stu-id="7ede2-154">
<a href=""></a>[<strong>D3D12_RESOURCE_DIMENSION</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ede2-155"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>креатекоммиттедресаурце</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-155"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-156"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-156"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="7ede2-157">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-157">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="7ede2-158">
<a href=""></a>[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="7ede2-158">
<a href=""></a>[<strong>D3D12_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)</span></span><br /><span data-ttu-id="7ede2-159">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-159">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="7ede2-160">
<a href=""></a>[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="7ede2-160">
<a href=""></a>[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ede2-161"><a href="/windows/desktop/dxmath/xmvector-data-type"><strong>ксмвектор</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-161"><a href="/windows/desktop/dxmath/xmvector-data-type"><strong>XMVECTOR</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-162"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorset"><strong>ксмвекторсет</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-162"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorset"><strong>XMVectorSet</strong></a></span></span><br /><span data-ttu-id="7ede2-163">
<a href=""></a>[<strong>Ксмколорхслторгб</strong>] (/Виндовс/десктоп/АПИ/директксмас/НФ-директксмас-ксмколорхслторгб)</span><span class="sxs-lookup"><span data-stu-id="7ede2-163">
<a href=""></a>[<strong>XMColorHSLToRGB</strong>](/windows/desktop/api/directxmath/nf-directxmath-xmcolorhsltorgb)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="upload-the-texture-data"></a><span data-ttu-id="7ede2-164">Отправка данных текстуры</span><span class="sxs-lookup"><span data-stu-id="7ede2-164">Upload the texture data</span></span>

<span data-ttu-id="7ede2-165">Данные текстуры передаются в графический процессор через кучу для отправки, а СРВС создаются для каждого и хранятся в куче-дескрипторе SRV.</span><span class="sxs-lookup"><span data-stu-id="7ede2-165">Texture data is uploaded to the GPU via an upload heap and SRVs are created for each and stored in an SRV descriptor heap.</span></span>

``` syntax
         // Upload texture data to the default heap resources.
            {
                const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
                const UINT64 uploadBufferStep = GetRequiredIntermediateSize(m_cityMaterialTextures[0].Get(), 0, subresourceCount); // All of our textures are the same size in this case.
                const UINT64 uploadBufferSize = uploadBufferStep * CityMaterialCount;
                CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
                auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &uploadHeap,
                    D3D12_HEAP_FLAG_NONE,
                    &uploadDesc,
                    D3D12_RESOURCE_STATE_GENERIC_READ,
                    nullptr,
                    IID_PPV_ARGS(&materialsUploadHeap)));

                for (int i = 0; i < CityMaterialCount; ++i)
                {
                    // Copy data to the intermediate upload heap and then schedule 
                    // a copy from the upload heap to the appropriate texture.
                    D3D12_SUBRESOURCE_DATA textureData = {};
                    textureData.pData = &cityTextureData[i][0];
                    textureData.RowPitch = static_cast<LONG_PTR>((CityMaterialTextureChannelCount * textureDesc.Width));
                    textureData.SlicePitch = textureData.RowPitch * textureDesc.Height;

                    UpdateSubresources(m_commandList.Get(), m_cityMaterialTextures[i].Get(), materialsUploadHeap.Get(), i * uploadBufferStep, 0, subresourceCount, &textureData);
                    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityMaterialTextures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
                    m_commandList->ResourceBarrier(1, &barrier);
                }
            }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7ede2-166">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="7ede2-166">Call flow</span></span></th>
<th><span data-ttu-id="7ede2-167">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ede2-167">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ede2-168"><a href="getrequiredintermediatesize.md"><strong>жетрекуирединтермедиатесизе</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-168"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7ede2-169"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>креатекоммиттедресаурце</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-169"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-170"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-170"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="7ede2-171">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-171">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="7ede2-172">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-172">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="7ede2-173">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-173">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="7ede2-174">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-174">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ede2-175"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-175"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7ede2-176"><a href="updatesubresources1.md"><strong>UpdateSubresources</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-176"><a href="updatesubresources1.md"><strong>UpdateSubresources</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7ede2-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ресаурцебарриер</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-178"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-178"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="7ede2-179">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-179">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="load-the-diffuse-texture"></a><span data-ttu-id="7ede2-180">Загрузка текстуры диффузии</span><span class="sxs-lookup"><span data-stu-id="7ede2-180">Load the diffuse texture</span></span>

<span data-ttu-id="7ede2-181">Рассеянная текстура, g \_ `txDiffuse` , передается аналогичным образом, а также получает собственную SRV, но данные текстуры уже определены в оккЦити. bin.</span><span class="sxs-lookup"><span data-stu-id="7ede2-181">The diffuse texture, g\_`txDiffuse`, is uploaded in a similar manner and also gets its own SRV, but the texture data is already defined in occcity.bin.</span></span>

``` syntax
// Load the occcity diffuse texture with baked-in ambient lighting.
        // This texture will be blended with a texture from the materials
        // array in the pixel shader.
        {
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = SampleAssets::Textures[0].MipLevels;
            textureDesc.Format = SampleAssets::Textures[0].Format;
            textureDesc.Width = SampleAssets::Textures[0].Width;
            textureDesc.Height = SampleAssets::Textures[0].Height;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &heapProps,
                D3D12_HEAP_FLAG_NONE,
                &textureDesc,
                D3D12_RESOURCE_STATE_COPY_DEST,
                nullptr,
                IID_PPV_ARGS(&m_cityDiffuseTexture)));

            const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
            const UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_cityDiffuseTexture.Get(), 0, subresourceCount);
            CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
            auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &uploadHeap,
                D3D12_HEAP_FLAG_NONE,
                &uploadDesc,
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&textureUploadHeap)));

            // Copy data to the intermediate upload heap and then schedule 
            // a copy from the upload heap to the diffuse texture.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pMeshData + SampleAssets::Textures[0].Data[0].Offset;
            textureData.RowPitch = SampleAssets::Textures[0].Data[0].Pitch;
            textureData.SlicePitch = SampleAssets::Textures[0].Data[0].Size;

            UpdateSubresources(m_commandList.Get(), m_cityDiffuseTexture.Get(), textureUploadHeap.Get(), 0, 0, subresourceCount, &textureData);
            auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityDiffuseTexture.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
            m_commandList->ResourceBarrier(1, &barrier);
        }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7ede2-182">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="7ede2-182">Call flow</span></span></th>
<th><span data-ttu-id="7ede2-183">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ede2-183">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ede2-184"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-184"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-185"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-185"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span><br /><span data-ttu-id="7ede2-186">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension"><strong>D3D12_RESOURCE_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-186">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension"><strong>D3D12_RESOURCE_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ede2-187"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>креатекоммиттедресаурце</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-187"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-188"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-188"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="7ede2-189">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-189">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="7ede2-190">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-190">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="7ede2-191">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-191">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="7ede2-192">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-192">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ede2-193"><a href="getrequiredintermediatesize.md"><strong>жетрекуирединтермедиатесизе</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-193"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7ede2-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>креатекоммиттедресаурце</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-195"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-195"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="7ede2-196">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-196">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="7ede2-197">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-197">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="7ede2-198">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-198">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="7ede2-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ede2-200"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-200"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7ede2-201"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ресаурцебарриер</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-201"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-202"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-202"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="7ede2-203">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-203">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="create-a-sampler"></a><span data-ttu-id="7ede2-204">Создание образца</span><span class="sxs-lookup"><span data-stu-id="7ede2-204">Create a sampler</span></span>

<span data-ttu-id="7ede2-205">Наконец, для **лоадассетс** создается одна пробная выборке из текстуры диффузии или из массива текстур.</span><span class="sxs-lookup"><span data-stu-id="7ede2-205">Finally for **LoadAssets**, a single sampler is created to sample from either the diffuse texture or the texture array.</span></span>

``` syntax
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

        // Create SRV for the city's diffuse texture.
        CD3DX12_CPU_DESCRIPTOR_HANDLE srvHandle(m_cbvSrvHeap->GetCPUDescriptorHandleForHeapStart(), 0, m_cbvSrvDescriptorSize);
        D3D12_SHADER_RESOURCE_VIEW_DESC diffuseSrvDesc = {};
        diffuseSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        diffuseSrvDesc.Format = SampleAssets::Textures->Format;
        diffuseSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        diffuseSrvDesc.Texture2D.MipLevels = 1;
        m_device->CreateShaderResourceView(m_cityDiffuseTexture.Get(), &diffuseSrvDesc, srvHandle);
        srvHandle.Offset(m_cbvSrvDescriptorSize);

        // Create SRVs for each city material.
        for (int i = 0; i < CityMaterialCount; ++i)
        {
            D3D12_SHADER_RESOURCE_VIEW_DESC materialSrvDesc = {};
            materialSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
            materialSrvDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            materialSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
            materialSrvDesc.Texture2D.MipLevels = 1;
            m_device->CreateShaderResourceView(m_cityMaterialTextures[i].Get(), &materialSrvDesc, srvHandle);

            srvHandle.Offset(m_cbvSrvDescriptorSize);
        }   
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7ede2-206">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="7ede2-206">Call flow</span></span></th>
<th><span data-ttu-id="7ede2-207">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ede2-207">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ede2-208"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc"><strong>D3D12_SAMPLER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-208"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc"><strong>D3D12_SAMPLER_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-209"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter"><strong>D3D12_FILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-209"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter"><strong>D3D12_FILTER</strong></a></span></span><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode"></a><br />
<span data-ttu-id="7ede2-210">D3D12_FLOAT32_MAX (<a href="constants.md"><strong>константы</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="7ede2-210">D3D12_FLOAT32_MAX (<a href="constants.md"><strong>Constants</strong></a>)</span></span><br /><span data-ttu-id="7ede2-211">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func"><strong>D3D12_COMPARISON_FUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-211">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func"><strong>D3D12_COMPARISON_FUNC</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ede2-212"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler"><strong>креатесамплер</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-212"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler"><strong>CreateSampler</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7ede2-213"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-213"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="7ede2-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>жеткпудескрипторхандлефорхеапстарт</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ede2-215"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-215"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-216"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="7ede2-216"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="7ede2-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ede2-218"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>креатешадерресаурцевиев</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-218"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7ede2-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="7ede2-220"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="7ede2-220"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="7ede2-221">
<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-221">
<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="7ede2-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ede2-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>креатешадерресаурцевиев</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ede2-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="dynamically-change-the-root-parameter-index"></a><span data-ttu-id="7ede2-224">Динамическое изменение индекса корневого параметра</span><span class="sxs-lookup"><span data-stu-id="7ede2-224">Dynamically change the root parameter index</span></span>

<span data-ttu-id="7ede2-225">Если бы нам пришлось визуализировать сцену, все города будут выглядеть одинаково, так как мы не установили значение корневой константы `matIndex` .</span><span class="sxs-lookup"><span data-stu-id="7ede2-225">If we were to render the scene now, all of the cities would appear the same, because we have not set the value of our root constant, `matIndex`.</span></span> <span data-ttu-id="7ede2-226">Каждый построитель текстуры получит индекс в 0 – ом слоте `g_txMats` , а сцена будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7ede2-226">Each pixel shader would index into the 0th slot of `g_txMats` and the scene would look like this:</span></span>

![Все города выглядят одинаковым цветом](images/dynamicindexing-image1.png)

<span data-ttu-id="7ede2-228">Значение корневой константы задается в **фрамересаурце::P опулатекоммандлистс**.</span><span class="sxs-lookup"><span data-stu-id="7ede2-228">The value of the root constant is set in **FrameResource::PopulateCommandLists**.</span></span> <span data-ttu-id="7ede2-229">В **цикле** двойной точности, где для каждого города записана команда рисования, мы записываем вызов [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants) , указывающий наш индекс корневого параметра в отношении корневой сигнатуры, в данном случае 3 — значение динамического индекса и смещение — в данном случае 0.</span><span class="sxs-lookup"><span data-stu-id="7ede2-229">In the double **for** loop where a draw command is recorded for each city, we record a call to [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants) specifying our root parameter index in regards to the root signature – in this case 3 – the value of the dynamic index and an offset – in this case 0.</span></span> <span data-ttu-id="7ede2-230">Так как длина `g_txMats` равна количеству отображаемых городов, значение индекса постепенно устанавливается для каждого города.</span><span class="sxs-lookup"><span data-stu-id="7ede2-230">Since the length of `g_txMats` is equal to the number of cities we render, the value of the index is incrementally set for each city.</span></span>

``` syntax
 for (UINT i = 0; i < m_cityRowCount; i++)
    {
        for (UINT j = 0; j < m_cityColumnCount; j++)
        {
            pCommandList->SetPipelineState(pPso);

            // Set the city's root constant for dynamically indexing into the material array.
            pCommandList->SetGraphicsRoot32BitConstant(3, (i * m_cityColumnCount) + j, 0);

            // Set this city's CBV table and move to the next descriptor.
            pCommandList->SetGraphicsRootDescriptorTable(2, cbvSrvHandle);
            cbvSrvHandle.Offset(cbvSrvDescriptorSize);

            pCommandList->DrawIndexedInstanced(numIndices, 1, 0, 0, 0);
        }
    }
```



| <span data-ttu-id="7ede2-231">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="7ede2-231">Call flow</span></span>                                                                                          | <span data-ttu-id="7ede2-232">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ede2-232">Parameters</span></span> |
|----------------------------------------------------------------------------------------------------|------------|
| [<span data-ttu-id="7ede2-233">**сетпипелинестате**</span><span class="sxs-lookup"><span data-stu-id="7ede2-233">**SetPipelineState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)                             |            |
| [<span data-ttu-id="7ede2-234">**SetGraphicsRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="7ede2-234">**SetGraphicsRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)     |            |
| [<span data-ttu-id="7ede2-235">**сетграфиксрутдескриптортабле**</span><span class="sxs-lookup"><span data-stu-id="7ede2-235">**SetGraphicsRootDescriptorTable**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) |            |
| [<span data-ttu-id="7ede2-236">**дравиндексединстанцед**</span><span class="sxs-lookup"><span data-stu-id="7ede2-236">**DrawIndexedInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)                     |            |

## <a name="run-the-sample"></a><span data-ttu-id="7ede2-237">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="7ede2-237">Run the sample</span></span>

<span data-ttu-id="7ede2-238">Теперь, когда мы подготавливаем сцену, каждый город будет иметь отличное значение для `matIndex` и, таким образом, будет искать другую текстуру, чтобы `g_txMats[]` сделать сцену выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7ede2-238">Now when we render the scene, each city will have a different value for `matIndex` and will thus look up a different texture from `g_txMats[]` making the scene look like this:</span></span>

![Все города отображаются в разных цветах](images/dynamicindexing-image2.png)

## <a name="related-topics"></a><span data-ttu-id="7ede2-240">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7ede2-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ede2-241">Пошаговые инструкции по коду D3D12</span><span class="sxs-lookup"><span data-stu-id="7ede2-241">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="7ede2-242">Effect — средство компилятора</span><span class="sxs-lookup"><span data-stu-id="7ede2-242">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[<span data-ttu-id="7ede2-243">Функции HLSL Shader Model 5,1 для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7ede2-243">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="7ede2-244">Привязка ресурсов в HLSL</span><span class="sxs-lookup"><span data-stu-id="7ede2-244">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="7ede2-245">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="7ede2-245">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="7ede2-246">Указание корневых подписей в HLSL</span><span class="sxs-lookup"><span data-stu-id="7ede2-246">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>
